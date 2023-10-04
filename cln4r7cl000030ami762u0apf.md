---
title: "Project-1. CI/CD Pipeline Using Jenkins and Docker"
datePublished: Fri Sep 29 2023 15:23:16 GMT+0000 (Coordinated Universal Time)
cuid: cln4r7cl000030ami762u0apf
slug: project-1-cicd-pipeline-using-jenkins-and-docker
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696000840148/1a50053c-c7b4-4ce2-8cc0-a1b81caf639d.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696000963300/461c059c-614b-4b4e-ab21-bfa8329ad287.png
tags: docker, github, jenkins, docker-images, ec2-instance

---

## **📢🎡Project - Creating CI/CD pipeline for web app**

### 🚩**Prerequisite-:** Git, GitHub, Docker, Docker Hub, Jenkins,

### 🚀**Description:-**

Implemented CI/CD pipelines for a web app using Docker containers, Jenkins automation, and AWS services to streamline code deployment, ensuring efficiency, scalability, and reliability.

<details data-node-type="hn-details-summary"><summary>Working</summary><div data-type="detailsContent">🎖️🚩First of all, clone the code from the centralized platform (GitHub) and build images, then run the container to verify whether the code is running.🎖️🚩Now configure to Jenkins with GitHub and if there is any update on the GitHub repo Jenkins will automate the trigger by using Webhook to build the code and deploy.</div></details>

---

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Brief</div>
</div>

**🎢Working Step🎢**

> Step-1. Create EC2 Instance
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696003591121/4cd0f91a-e6b8-4231-bd6a-89232ea4a341.png align="center")
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696003706789/8c33de7a-3a4d-4e7e-8ba6-03ea25abf5c4.png align="center")
> 
> ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696003827347/2d333ea9-9a3d-4b15-a647-5adfbeb40dd2.png align="center")

> Step-2. Setup and Install Jenkins

```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

> Step-3. Clone the code from the GitHub Repository

```bash
git clone https://github.com/Fir3eye/Node-todo-project.git
```

> *Step-4.* Build code and Test Locally

```bash
sudo apt install docker.io
# After installing docker build code
docker build -t myimg .
docker run -d -p 8000:8000 myimg
# check images
docker images
# check container are running or not
docker ps -a
# stop container
docker stop <container_id>
# Delete Container
docker rm <container_id>
# Delete Images
docker rmi <container_id>
```

> Step-5. Add inbound and outbound rules on EC2 Instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696003995428/1fdeb7fa-4f80-4c3e-9399-ede81557d82c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696004007919/eed2dd79-1622-4861-99fc-8a751044ea78.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696004017057/fd2bf85a-32a9-4739-a4a3-9608df4623fd.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1696004028257/3430cd30-c3ca-4841-b91b-b11640ebc2dc.png align="center")

> Step-6. Integrate Jenkins with GitHub

> Step-7. Create a Job on Jenkins

> Step-8. Build and Test