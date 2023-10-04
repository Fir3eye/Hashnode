---
title: "Project - 2. Deploy Java Application On Kubernetes"
datePublished: Wed Oct 04 2023 15:11:47 GMT+0000 (Coordinated Universal Time)
cuid: clnbvztt3000m09lagblj2xts
slug: project-2-deploy-java-application-on-kubernetes
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696429365785/fc8c4f60-6a3d-4712-bc00-f01341e12ce7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696432233454/59e8aee7-fa7b-4bb9-8b6e-a75c2d3e1ecd.png
tags: docker, github, kubernetes, devops, cicd-cjy1vtdk2005kjjs17n8couc3

---

# **Deploy Java Application On Kubernetes**

### **Pre-requisite:-**

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
    

### Command

```bash
# Docker Install 
sudo apt install docker.io
# Install Kubernetes and minikube
https://hashnode.com/post/cln6siq7v000009jjex70enqi
# Clone the code and push to own repo github 
sudo git clone https://github.com/Fir3eye/docker-java-kubernetes-project.git
# How to Push code follow these step 
sudo git remote -v  # check the repo url 
# Set the own repo url
sudo git remote set-url origin <our_repo_URL>
#check the url is set 
sudo git remote -v 
# send code to staging Area
sudo git add .
# Send to local repo 
sudo git commit -m "first commit"
# Now ready to push the repo on own central repo 
sudo git push -u origin  main # check our branch and specify instead of main 
#username: abc
#password: token generate from github 
```

### Build the image

```bash
# Build the image from Dockerfile
docker build -t fir3eye/myimg:latest .
# Check images
docker images
# Run the container
docker run -t -p 8000:8000 myimg
# Check container is runnig or not 
docker ps 
# if port is busy so check 
netstat -lntp
# kill the port if busy 
kill -9 pid
```

### Push image on DockerHub

```bash
# First Login the Docker account
docker login # give access
# push the images
docker push docker_account_name/image_name # docker push fir3eye/myimg:latest
# Go and check our docker repo
```

### Kubernetes Command

```bash
# check the pods
kubectl get pods
# Apply the our deployment file
kubectl apply -f deployment.yml
# check the deployment
kubectl get deployment
# Check service
kubectl get svc
# After deployment check the ip 
minikube service <service_name>
# You would not be access from the internet, 
# For accessing from the internet , you will have to do port-forwarding
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