---
title: "Project - 3. DevSecOps | Real Time Complete CI/CD Project"
datePublished: Tue Nov 28 2023 09:16:13 GMT+0000 (Coordinated Universal Time)
cuid: clpi4iezt000009jvbolre08s
slug: project-3-devsecops-real-time-complete-cicd-project
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700840465266/d023d124-9f70-420d-94c2-f851b1f4e0ea.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1701162947831/776e79d4-9012-4032-ab0d-470e967cbe23.png
tags: docker, aws, github, jenkins, devsecops, sonarqube-installation

---

---

## 📢🎡**Pre-requisites**

1. EC2 Instance t2.large 30gb
    
2. Docker and Docker Hub
    
3. Jenkins Setup
    
4. Trivy for file scan
    
5. SonarQube
    

## **🎢Working Steps🎢**

1. **Create an Ubuntu t2.large Instance**
    
2. **Install Docker, Jenkins, and Trivy Create a Sonarqube container using Docker.**
    
3. **Install Plugins like JDK, Sonarqube Scanner, Maven, and OWASP Dependency Check.**
    
4. **Create a Pipeline Project in  Jenkins Using a Declarative Pipeline**
    
5. **Build and Push on Docker Hub**
    
6. **Deploy on Docker**
    
7. **Access the Real World Application**
    
8. **Terminate the AWS EC2 Instance**
    

---

## **Step-1. Create an Ubuntu t2.large Instance**

Go to the AWS account and launch the ec2 t2.micro instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700840896124/4668975b-a0cb-4f56-92e8-7c2a02e47c7f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700840960318/6944e2f3-10d8-450e-a50a-5e886b4cefd0.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700841005473/d3920bae-919a-495c-ab2a-e2f2ee493272.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700841044572/d5db68b1-bb4c-4279-b9b3-9d6362eda2d5.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700841059287/cccf621e-ad75-4e43-bf62-56b1c07dc73d.png align="center")

---

## **Step-2. Install Docker, Jenkins, and Trivy Create a Sonarqube container using Docker**

> A. **<mark>Install Docker</mark>**

```bash
vi docker.sh
```

```bash
sudo apt-get update
sudo apt-get install docker.io -y
sudo usermod -aG docker $USER
newgrp docker
sudo chmod 777 /var/run/docker.sock
docker ps
```

Save -&gt; Press &lt;<mark>ESC</mark> + <mark>:</mark> + <mark>wq</mark> + <mark>Enter</mark>\&gt;

Give Permission

```bash
chmod 700 docker.sh
```

Run

```bash
./docker.sh
```

Run in Background Mode

```bash
sudo systemctl enable docker
```

---

> B. <mark>Jenkins Setup</mark>

```bash
vi jenkins.sh
```

```bash
#!/bin/bash
sudo apt update -y
sudo touch /etc/apt/keyrings/adoptium.asc
sudo wget -O /etc/apt/keyrings/adoptium.asc https://packages.adoptium.net/artifactory/api/gpg/key/public
echo "deb [signed-by=/etc/apt/keyrings/adoptium.asc] https://packages.adoptium.net/artifactory/deb $(awk -F= '/^VERSION_CODENAME/{print$2}' /etc/os-release) main" | sudo tee /etc/apt/sources.list.d/adoptium.list
sudo apt update -y
sudo apt install temurin-17-jdk -y
/usr/bin/java --version
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
	                  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
	                              /etc/apt/sources.list.d/jenkins.list > /dev/null
```

Save -&gt; Press &lt;<mark>ESC</mark> + <mark>:</mark> + <mark>wq</mark> + <mark>Enter</mark>\&gt;

```bash
sudo apt-get update -y
sudo apt-get install jenkins -y
sudo systemctl start jenkins
sudo systemctl status jenkins
```

Define Port <mark>8080</mark> in the Security Group

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843306803/1b33bfdd-eb7e-4d8b-b947-bdf8cd25249d.png align="center")

Paste &lt;<mark>IP:8080</mark>\&gt; on the browser

Get Password

```bash
cat /var/lib/jenkins/secrets/initialAdminPassword
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842590037/1af2b109-7bcf-4cab-8369-01783dbea17b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842302150/2d0ae853-cea9-4b3c-8195-1f080cf56c30.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842637145/ead69786-672e-464e-a04a-1d33523eec3b.png align="center")

![Why You Should Stop Relying on Jenkins Plugins](https://assets-global.website-files.com/5f10ed4c0ebf7221fb5661a5/62978bfd039b1556703992e5_Jenkins%20Installation.png align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842656274/8509528f-91fd-4925-bc0a-e92cec87e161.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842668556/10bee89a-4cfd-4c49-9c55-963207a843ef.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842683004/a154b980-80f8-4772-a83a-776bd6ddfcc2.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842697133/2b2466be-88fc-4d79-a3a0-dea2f379073f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842704248/8ca5c639-f91c-4d66-95c5-50966eb9a423.png align="center")

Change with your own password like user- <mark>admin</mark>, pass - <mark>admin123</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842718568/8c4b44d9-c5ca-408c-ad9a-151528819967.png align="center")

Username - <mark>admin</mark>

Pass- <mark>admin123</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700842724492/1482a20a-84c7-4e1c-8282-d60bd247a0b7.png align="center")

---

> C. **Create a <mark>Sonarqube</mark> container using <mark>Docker</mark>**

```bash
docker run -d --name sonar -p 9000:9000 sonarqube:lts-community
```

Define Port in the Security Group <mark>9000</mark>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843258950/416cc262-95d5-4859-b123-169713140add.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843267232/a6eeccdf-ee75-481f-bb0a-7637e4695339.png align="center")

Paste &lt;<mark>IP:8080</mark>\&gt; on the browser

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843769472/d48e3b7b-a0dd-4334-8978-f8f4fdf37afb.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843775203/eee82734-f6e3-49fa-95e1-9e10177611fd.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700843784786/b365b1bc-7435-4aa1-a92d-0fe530424636.png align="center")

---

> D. Install Trivy

```bash
vi trivy.sh
```

Paste the code

```bash
sudo apt-get install wget apt-transport-https gnupg lsb-release -y
wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null
echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list
```

Save -&gt; Press &lt;<mark>ESC</mark> + <mark>:</mark> + <mark>wq</mark> + <mark>Enter</mark>\&gt;

```bash
sudo apt-get update
sudo apt-get install trivy
```

---

## **Step-3. Install Plugins like JDK, Sonarqube Scanner, Maven, OWASP Dependency Check**

> **A. <mark>Install Below Plugins</mark>**

* Eclipse Temurin Installer \*(Install without Restart)
    
* SonarQube Scanner
    
* OWASP Dependency-Check
    
* Docker
    

> Eclipse Temurin Installer \*(Install without Restart)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700844676869/d38ba83c-4428-4b66-a27d-05c5111ff615.png align="center")

> SonarQube Scanner

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700844706075/c0d4dc85-b9fe-4ff2-89c4-90cc02db7bba.png align="center")

> OWASP Dependency-Check

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700844732381/850af54c-4b1f-418c-b720-420f578f85f4.png align="center")

> Docker

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845082879/bd89d8f0-4cb0-4d14-9536-740ad2274f2f.png align="center")

---

> B. **<mark>Tools Configuration</mark>**

Go to Manage Jenkins and Click on tools section

* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845129100/a4332beb-b0fe-406f-91c1-f53478eb3bf6.png align="center")
    
    <mark>Sonarqube</mark> ---&gt; install automatically ---&gt; version latest
    
* <mark>Maven3</mark> ---&gt; Install automatically ---&gt; Version ---&gt; 3.6.0
    
* <mark>DP-Check</mark> ---&gt; install from GitHub ---&gt; version 6.5.1
    
* <mark>Docker</mark> ---&gt; install from [docker.com](http://docker.com) ---&gt; version latest
    
* <mark>jdk17</mark> ---&gt; install automatically  ----&gt; Version ---&gt; 11.0.20.8
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845156368/18dad8a6-0366-44b3-bc10-eec0882c6512.png align="center")

<mark>Sonarqube</mark> ---&gt; install automatically ---&gt; version latest

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845172771/5f66fb09-d32d-4cc0-85f7-e4e2d2d718ca.png align="center")

<mark>DP-Check</mark> ---&gt; install from GitHub ---&gt; version 6.5.1

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845192054/a4848159-d801-4ad8-b1a6-8078ed7e4e25.png align="center")

<mark>Docker</mark> ---&gt; install from [docker.com](http://docker.com) ---&gt; version latest

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700845209756/72843e32-3f31-461b-9301-15772fe9ad17.png align="center")

---

> C. **SonarQube Integrate with jenkins**

**<mark>Credentials</mark>**

**Sonarqube** ---&gt; Administration ---&gt; user ---&gt; create a token  squ\_1f347027a4c6599763466d3d3e859c4d98967162

Got to ---&gt; manage jenkins ----&gt; security ----&gt; Credentials ----&gt; add credentials ----&gt; secret text ---&gt; Id &gt; Sonar-token

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700848698797/a42462ae-db18-4a0b-aa62-9ce23173c573.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700848742488/95ce4384-1c4a-4e90-846c-cdd282f4ea96.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700848758133/76965499-7b6a-42ef-9d0e-045d820e1eaf.png align="center")

**<mark>System</mark>**

Integrate sonarqube ---&gt; sonarqube installation ---&gt;name-sonar-server---&gt; server-url -&gt;IP:9000 ---&gt; apply and save

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700848944452/0323396b-ead8-4df8-9dea-823ea2cefeef.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700849012319/6704e906-b25e-4ed6-9ec5-70f7dff0d146.png align="center")

**Jenkins Integrate with Sonarqube**

Go to administration ---&gt; configuration ---&gt; webhook

Name&gt; jenkins----&gt; url &gt; [http://IP:8080/sonarqube-webhook/](http://IP:8080/sonarqube-webhook/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700849037058/4696870c-0b9d-46af-821a-db5304589867.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700849117367/9fec9b08-e1e7-4be0-b8ae-b92522cfcbca.png align="center")

> ALL are set :-)

Now Next....

---

## **Step-4. Create a Pipeline Project in  Jenkins Using a Declarative Pipeline**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700849332189/b25bb923-1bea-4db8-83d8-251f5e613f69.png align="center")

> **<mark>Pipeline</mark>**

```bash
pipeline {
    agent any 
    tools {
        jdk 'jdk11'
        maven 'maven3'
    }
    environment {
        APP_NAME = "image_name"
        RELEASE = "latest"
        DOCKER_USER = "fir3eye"
        DOCKER_PASS = 'dockerhub'
        IMAGE_NAME = "${DOCKER_USER}" + "/" + "${APP_NAME}"
        IMAGE_TAG = "${RELEASE}-${BUILD_NUMBER}" 
    }
    stages{
        stage("Clean WorkSpace"){
            steps {
                cleanWs()
            }
        }
        stage("Checkout SCM"){
            steps {
                git 'https://github.com/Fir3eye/pr_03_amazon-eks-jenkins-terraform.git'
            }
        }
        stage("Maven Compile"){
            steps {
                sh 'mvn clean compile'
            }
        }
        stage("SonarQube Analysis"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh 'mvn sonar:sonar'
                    }
                }
            }
        }
        stage ('Build War file') {
            steps {
                sh 'mvn clean install package'
            }
        }  
    }
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700849422311/975f22ff-9a95-4d49-9a62-29578afb0940.png align="center")

## Step -5. Build and push on Docker Hub

```bash
        stage("Build Docker Image"){
            steps{
                script {
                    docker.withRegistry('',DOCKER_PASS) {
                        //sh "docker images --format '{{.Repository}}:{{.Tag}}' | grep ${IMAGE_NAME} | grep -v ${RELEASE}-${BUILD_NUMBER} | grep -v latest | xargs -I {} docker rmi {} || true" 
                        docker_image = docker.build "${IMAGE_NAME}"
                    }
                }
            }
        }
        stage("Push Docker Image"){
            steps{
                script {
                    docker.withRegistry('',DOCKER_PASS){
                        docker_image.push("${IMAGE_TAG}")
                        docker_image.push('latest')
                    }
                }
            }
        }
```

## Step -6. Deploy on Docker

```bash
        stage ('Deploy to Container') {
            steps {
                sh 'docker run -d --name pet1 -p 8082:8080 fir3eye/image_name:latest'
            }
        }
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701163471950/0ab0d8ca-1c4d-4319-a273-8337efcb3243.png align="center")

---

## **Step -7. Access the Real World Application**

Copy server IP:8082 and paste on the browser

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701161981124/59c58892-7530-4aef-a3df-c10dba01735a.png align="center")

---

## **Step - 8. Terminate the AWS EC2 Instance**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701162053393/8012a9c2-a76f-4766-8a1a-5b904d077431.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701162034086/4757069d-8b6a-48b9-9ecb-9e356b126d5b.png align="center")