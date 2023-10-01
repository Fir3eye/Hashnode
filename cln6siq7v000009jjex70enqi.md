---
title: "Minikube and Kubectl Setup on Ubuntu"
seoTitle: "Install Minikube and Kubectl on Ubuntu"
datePublished: Sun Oct 01 2023 01:35:39 GMT+0000 (Coordinated Universal Time)
cuid: cln6siq7v000009jjex70enqi
slug: minikube-and-kubectl-setup-on-ubuntu
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696125185470/0a01e197-2293-4787-8929-e0bfa67a1884.png
tags: kubernetes, devops, kubectl, minikube

---

## 🚀Install Minikube

```bash
# install Docker
sudo apt install docker.io
# Download minikube
wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
# Give Permissions
chmod 755 minikube
mv minikube /usr/local/bin/minikube
# Set the usergrp
sudo usermod -aG docker $USER && newgrp docker
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Note:- Dont use Root User before starting minikube</div>
</div>

```bash
# Note:- Dont use Root User
minikube start
```

## 🚀Install Kubectl

```bash
# Download first Kubectl by link
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
# Give Permission
chmod +x kubectl
# Move on to global Environment
mv kubectl /usr/local/bin/kubectl
# check status
minikube status

# Have Fun :-)
# Do more Practice
```