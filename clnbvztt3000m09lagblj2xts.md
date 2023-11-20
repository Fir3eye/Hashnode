---
title: "Project - 3. Deploy Java Application On Kubernetes"
datePublished: Wed Oct 04 2023 15:11:47 GMT+0000 (Coordinated Universal Time)
cuid: clnbvztt3000m09lagblj2xts
slug: project-2-deploy-java-application-on-kubernetes
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696429365785/fc8c4f60-6a3d-4712-bc00-f01341e12ce7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696432233454/59e8aee7-fa7b-4bb9-8b6e-a75c2d3e1ecd.png
tags: docker, github, kubernetes, devops, cicd-cjy1vtdk2005kjjs17n8couc3

---

### 📢🎡**Pre-requisite:-**

* Java application
    
* Docker installed
    
* Kubernetes cluster
    
* Basic knowledge of Maven, docker, and Kubernetes
    

### **Integration with Kubernetes**

* Commit code on GitHub
    
* Pull code from GitHub on the local repository
    
* Install maven before building a docker image run command - maven clean install
    
* Build a Docker image and push the image to the Docker Registry
    
* Pull the image from the Docker registry and Deploy to the Kubernetes Cluster
    

### Step -1. **<mark>Update</mark>** the machine

```bash
sudo apt update
```

### Step -2. Install **<mark>Docker</mark>**

```bash
sudo apt install docker.io
```

### Step -3. Install **<mark>Maven</mark>**

```bash
sudo apt install maven
mvn --version
# Setup Environment Variable
export MAVEN_HOME=/usr/share/maven
# Verify
echo $MAVEN_HOME
```

### Step -4. **<mark>Clone</mark>** the code from **<mark>Github</mark>**

```bash
git clone https://github.com/Fir3eye/docker-java-kubernetes-project.git
```

### Step -5. Build the image

<details data-node-type="hn-details-summary"><summary>There are three micro-service</summary><div data-type="detailsContent">&lt; shopfront &gt;, &lt; productcatal &gt;, &lt; stockmanager &gt;</div></details>

> Build the first image **<mark>&lt; shopfront &gt;</mark>**
> 
> Note:- Instead of fir3eye you give our username of dockerhub.

```bash
# Before building the image run this command
mvn clean install
docker build -t fir3eye/shopfront:latest .
```

> Build the second image **<mark>&lt; productcatal &gt;</mark>**

```bash
# Before building the image run this command
mvn clean install
docker build -t fir3eye/productcatal:latest .
```

> Build the Third microservice **<mark>&lt; stockmanager &gt;</mark>**

```bash
# Before building the image run this command
mvn clean install
docker build -t fir3eye/stockmanager:latest .
```

> Check the images

```bash
sudo docker images
```

### Step -6. **<mark>Push</mark>** the images on **<mark>DockerHub</mark>**

> first you need login to Docker hub using the below command

```bash
# Login Docker on your Terminal
sudo docker login
```

> Give the username of password of the docker account, if the password is not working, one solution create a token and give it instead of the password.
> 
> After successful login

```bash
# Push the Image on docker hub
docker push fir3eye/shopfront:latest
docker push fir3eye/productcatal:latest 
docker push fir3eye/stockmanager:latest
```

> Logout Docker

```bash
docker logout
```

### Step -7. Setup <mark>Minikube</mark> and **<mark>Kubectl</mark>**

> Install Minikube

```bash
sudo wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo cp minikube-linux-amd64 /usr/local/bin/minikube
sudo chmod 755 /usr/local/bin/minikube
```

> Install kubectl

```bash
sudo curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

sudo chmod +x kubectl
sudo mv kubectl /usr/local/bin/Kubectl
sudo minikube start --driver=docker
sudo usermod -aG docker $USER && newgrp docker
Minikube status
```

### Step -8. App Deploy on **<mark>Kubernetes</mark>**

```bash
kubectl apply -f shopfront-service.yaml
kubectl apply -f productcatal-service.yaml
kubectl apply -f stockmanager-service.yaml
```

> Check the Pods, deployments, services

```bash
kubectl get pods
kubectl get deployment
kubectl get svc
```

> Get the Service URL

```bash
kubectl get service
```

> Copy the URL

```bash
minikube service <service_name>
```

> Port Forward

```bash
# You would not have access from the internet, 
# For accessing from the internet, you will have to do port-forwarding
kubectl port-forward svc/myservice 8000:8000 --address 0.0.0.0 &
# now you can access the web from the internet copy ip and use our port
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">How to generate a token</div>
</div>

> Login to GitHub Account
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431110755/4a013688-04bf-486b-8168-662deaac4c51.png align="center")
> 
> Got to ---&gt; Settings
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431120814/6da3bda7-1d5c-4565-92b3-e715a74c8a33.png align="center")
> 
> Go to bottom -----&gt; Developer Settings
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696430889937/9edc9698-c416-4768-8388-cc5c3ef7c731.png align="center")
> 
> Click on Personal Access Token
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431009336/d23fa55d-d422-4bff-b5ed-5158277114a3.png align="center")
> 
> Click on Token Classic
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431023898/8752b16e-4073-4d39-ad35-5f6e6a268eb9.png align="center")
> 
> Click Generate Token
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431034886/bb5aa826-9c7c-4961-95eb-bc3831e68e98.png align="center")
> 
> Generate new Token \*(Classic)
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431049002/8fbcbadd-0e1d-4b8e-ac18-13524416e692.png align="center")
> 
> Give Access
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431058588/39d08b69-eba5-4e10-b4c3-ad588ba0ff9e.png align="center")
> 
> Your own key name and give access to own way
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431076426/28f9fa2d-6221-46f0-b9fa-1c76bb7bfb35.png align="center")
> 
> Click to Generate Token Have Fun :-)
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696431092102/69b5470f-e7a5-4039-b794-24f464e14444.png align="center")