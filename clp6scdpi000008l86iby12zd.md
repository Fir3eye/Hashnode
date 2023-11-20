---
title: "Project - 1. Push Docker Image to Docker Hub using Jenkins Pipeline"
datePublished: Mon Nov 20 2023 10:50:08 GMT+0000 (Coordinated Universal Time)
cuid: clp6scdpi000008l86iby12zd
slug: project-1-push-docker-image-to-docker-hub-using-jenkins-pipeline
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700473669159/33a375e1-9c5e-4083-8c77-68f3bec69c51.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700477323702/4386fd1e-2e25-4f49-b969-3eb223ad37d1.png
tags: ec2, docker, aws, jenkins, dockerhub

---

## **Pre-requisites**

1. EC2 Instance t2.micro
    
2. Install Docker
    
3. Docker Hub Account
    
4. Install Jenkins
    
5. Install the Plugin and Set the Credentials
    
6. Create a job
    

## **Working Steps:-**

### **Step-1. Launch (Ubuntu) Ec2 instance t2.micro**

> A. Go to AWS Console and Click on search box and type Ec2

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474289610/0ee5bc75-1627-408d-b891-2b8efe27e881.png align="center")

> B. Click on Launch Instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474369084/df5cb5fb-8d69-47d9-a387-0d1b2baead95.png align="center")

> C. Type the Instance Name and Choose the Ubuntu Machine

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474523358/de091d70-4abf-48a3-b31f-1515253a49f8.png align="center")

> D . Create Key

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474637780/7f3a09cd-3c29-457a-ab32-5af265261212.png align="center")

> E. Check (HTTP, HTTPS) box and click launch instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474722484/58def706-c28d-49cd-8ff6-b2f5a3827c4c.png align="center")

> F. Copy Public Ip and Access your Instance

```bash
ssh ubuntu@IP -i "key_name"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474784188/beeac3fa-a2e1-4636-ac43-c0feed37505e.png align="center")

## Step-2. Install Docker

```bash
sudo apt install docker.io
```

## Step-3. Create a Docker Hub Account

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475227339/8ce35d64-9078-46b8-b5b8-e00acc3d18f6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475249565/f28196c4-8757-4217-8fce-e41993bd0adc.png align="center")

## Step-4. Install Jenkins

```bash
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.8" 2023-07-18
OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)
```

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

> Access Jenkins on browser

```bash
# your instance IP and port 8080
241.15.54.55:8080
```

## Step-5. Install the plugins and set the Credentials

> A. Go to Manage Jenkins and Click on Plugins

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475856864/54781c90-202f-4f19-880a-c918cefee0aa.png align="center")

> B. Choose required Plugins

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475881038/fcb74c4e-5382-4ca9-aff8-5e7d1a0f079e.png align="center")

> C. Successfully Installed

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475899003/aa429a78-f21a-4705-a2f2-becf4fab7e5e.png align="center")

> D. Set Credentials

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476337371/197c7e26-fae9-462a-ba4e-2341d161974e.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476352625/56718182-9f26-48c4-8cbe-4158ad148cf1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476362491/ccf3a3c1-49aa-4961-ae78-238e96daed50.png align="center")

## Step-6. Create a Job

> A.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476798745/371c9d8a-b987-4974-b7d9-d1ac1abf9ad7.png align="center")

> sd

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476822023/efe7615f-8ac1-4af6-8aca-ef3eae30b083.png align="center")

> C. Write pipeline Code and paste the pipeline box

```bash
pipeline{
    agent any
    
    environment {
        APP_NAME = "complete-pro"
        RELEASE = "latest"
        DOCKER_USER = "fir3eye"
        DOCKER_PASS = 'dockerhub'
        IMAGE_NAME = "${DOCKER_USER}" + "/" + "${APP_NAME}"
        IMAGE_TAG = "${RELEASE}-${BUILD_NUMBER}"

    }
    stages{
        stage("Cleanup Workspace"){
            steps {
                cleanWs()
            }
        }
        stage("Checkout from SCM"){
            steps {
                git branch: 'master', credentialsId: 'github', url: 'https://github.com/shazforiot/nodeapp_test.git'
            }

        }
        stage("Build & Push Docker Image") {
            steps {
                script {
                    docker.withRegistry('',DOCKER_PASS) {
                        docker_image = docker.build "${IMAGE_NAME}"
                    }

                    docker.withRegistry('',DOCKER_PASS) {
                        docker_image.push("${IMAGE_TAG}")
                        docker_image.push('latest')
                    }
                }
            }

        }
    }
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476846349/6049433b-b22f-4349-a02d-6ef86d50d079.png align="center")

> D. Click on the Build Button

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476878844/be2ab31b-46c0-4900-96eb-508a27670fd4.png align="center")

> E. See the Result

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476899959/1543266a-7e82-4af6-a2a3-959c0ead07ea.png align="center")