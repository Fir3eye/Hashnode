---
title: "Project-2. Created CI/CD pipelines of Web App using Docker Jenkins AWS."
datePublished: Tue Nov 21 2023 07:55:32 GMT+0000 (Coordinated Universal Time)
cuid: clp81jp81000q09jmhvmc6ik8
slug: project-2-created-cicd-pipelines-of-web-app-using-docker-jenkins-aws
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700552847967/7cc8ebf3-2e7c-4e70-b196-65fd51111fe1.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700553280762/1b9dea5d-a689-4f23-9ba1-f7346864c4ac.png
tags: docker, aws, github, git, jenkins

---

## 📢🎡**Pre-requisites**

1. **<mark>EC2</mark> Instance t2.micro**
    
2. **Install <mark>Docker</mark>**
    
3. **<mark>Docker Hub</mark> Account**
    
4. **<mark>Jenkins</mark>**
    

## **🎢Working Steps🎢**

1. **Launch Ec2 Instance t2.micro**
    
2. **Install Docker**
    
3. **Run Code in Live Server EC2**
    
4. **Create DockerHub Account**
    
5. **Deploy the app on AWS EC2 using Docker**
    
6. **Install Jenkins**
    
7. **Install the plugins and set the Credentials**
    
8. **Create Freestyle Job**
    
9. **Create CI/CD Pipeline Using Jenkins and Deploy the app on AWS**
    
10. **Result**
    

### **Step-1. Launch (Ubuntu) Ec2 instance t2.micro**

> **A. Go to AWS Console Click on the search box and type Ec2**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474289610/0ee5bc75-1627-408d-b891-2b8efe27e881.png align="center")

> **B. Click on Launch Instance**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474369084/df5cb5fb-8d69-47d9-a387-0d1b2baead95.png align="center")

> **C. Type the Instance Name and Choose the Ubuntu Machine**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474523358/de091d70-4abf-48a3-b31f-1515253a49f8.png align="center")

> **D . Create Key**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474637780/7f3a09cd-3c29-457a-ab32-5af265261212.png align="center")

> **E. Check (HTTP, HTTPS) box and click launch instance**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474722484/58def706-c28d-49cd-8ff6-b2f5a3827c4c.png align="center")

> **F. Copy the Public Ip and Access your Instance**

```bash
ssh ubuntu@IP -i "key_name"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700474784188/beeac3fa-a2e1-4636-ac43-c0feed37505e.png align="center")

---

## Step-2. Install Docker

```bash
sudo apt update
sudo apt install docker.io
sudo chmod 777 /var/run/docker.sock
sudo usermod -aG docker jenkins
```

---

## Step-3. Run Code in <mark>Live Server</mark>

```bash
sudo apt install nodejs -y
sudo apt install npm -y
sudo npm install -y
```

> **Run the application**

```bash
node index.js
```

> **Copy and paste on the browser**

```bash
your_instance_IP:3000
#note:- before pasting IP and port specify a port(3000) in our security group
```

---

## Step-4. Create a Docker Hub Account

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475227339/8ce35d64-9078-46b8-b5b8-e00acc3d18f6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475249565/f28196c4-8757-4217-8fce-e41993bd0adc.png align="center")

---

## Step-5. Deploy the app on EC2 using Docker

> **A. Clone the Code from GitHub**

```bash
git clone https://github.com/Fir3eye/pr_01_docker_push_img.git
```

> **B. Build the Docker Image**

```bash
docker build -t fir3eye/test_app .
```

> **C. Check the available images**

```bash
docker images
```

> **D. Run the application**

```bash
docker run -d -p 3000:3000 fir3eye/test_app
```

> **E. Check the container**

```bash
docker ps -a
```

---

## Step-6. Install Jenkins

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

> **Access Jenkins on the browser**

```bash
# your instance IP and port 8080
241.15.54.55:8080
```

---

## Step-7. Install the plugins and set the Credentials

> **A. Go to Manage Jenkins and Click on Plugins**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475856864/54781c90-202f-4f19-880a-c918cefee0aa.png align="center")

> **B. Choose required Plugins**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475881038/fcb74c4e-5382-4ca9-aff8-5e7d1a0f079e.png align="center")

> **C. Successfully Installed**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700475899003/aa429a78-f21a-4705-a2f2-becf4fab7e5e.png align="center")

> **D. Set Credentials**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476337371/197c7e26-fae9-462a-ba4e-2341d161974e.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476352625/56718182-9f26-48c4-8cbe-4158ad148cf1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476362491/ccf3a3c1-49aa-4961-ae78-238e96daed50.png align="center")

## Step-8. Create a freestyle Job

> **A. Click on New Item**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476798745/371c9d8a-b987-4974-b7d9-d1ac1abf9ad7.png align="center")

> **B. Type your own project name**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700550697087/70e65edd-7f24-4b3c-bb20-3cb2fd0ffc74.png align="center")

> **C. Set the repository url and type your repo branch**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700550522267/098d29f3-cd77-42e2-8a7e-a13c2af66454.png align="center")

> **D. Click execute shell and write build/run command**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700550541314/a4e41519-0f44-471d-9662-cd29c3f76b97.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700550569022/d39ad8b2-82be-4e1c-8abb-fffad550920f.png align="center")

**E. Go to Dashboard**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700550599770/94dce0e8-481e-4b4a-9bcb-fc95d3d4d9d3.png align="center")

---

## Step-9. Create CI/CD pipeline using Jenkins and Deploy the app on EC2

> **A. Create Pipeline**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700552339690/75c376eb-f3a3-48bb-93b2-68529946d3b7.png align="center")

> **B. Write pipeline Code and paste the pipeline box**

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
        stage('Deploy to container'){
            steps{
                sh 'docker run -d --name test_app -p 3000:3000 fir3eye/test_app:latest'
            }
        }

    }
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700476846349/6049433b-b22f-4349-a02d-6ef86d50d079.png align="center")

> **C. Click on the Build Button**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700552369463/b3bb4534-6a89-4f41-8b46-922bf1e2f7c5.png align="center")

> **D. See the Result**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700552159513/4b5ce3b4-c30f-4e06-86b3-d4b3a0598f16.png align="center")

## Result:-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700552468087/b7008679-0daf-44cd-9ec5-c93a1cae310c.png align="center")