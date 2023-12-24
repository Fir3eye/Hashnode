---
title: "2. Deploy a Website Use EC2 and ECR using GitHub Actions"
datePublished: Sun Dec 24 2023 12:00:07 GMT+0000 (Coordinated Universal Time)
cuid: clqjftcpt000208jqhdmabm2h
slug: 2-deploy-a-website-use-ec2-and-ecr-using-github-actions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703419619168/fcaa7c71-ea23-4780-ae8a-a87901879c35.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1703419642816/a1da8e91-f522-4ec3-869a-f7ecb06276a0.png
tags: ec2, github, github-actions-1, aws-ecr

---

## Pre-Requisites

1. GitHub Account
    
    1. Create Repository
        
    2. Set Secret and Variable
        
    3. Code
        
    4. Action
        
2. AWS Account
    
    1. EC2 Instance
        
    2. ECR (Elastic Container Registry)
        
    3. IAM Access Key
        

---

### Create Repository

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246665575/2c90c2f7-ee32-4e4b-ab5d-728384da6903.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246674255/3c364ff4-f37c-42f9-b5a7-e2c08a9cd76b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246688741/236abf52-7a76-43f9-ab1c-e5a3aafc835c.png align="center")

### Clone The Code

```bash
git clone https://github.com/Fir3eye/fir3-Portfolio.git
```

### Click on Action Button and click setup a workflow yourself

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247095504/b64b5c88-a82d-46f2-a654-86399a9f7bad.png align="center")

1. Openend workspace Like This
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247251301/c780b80d-5d9e-4aa6-9e8d-788310a679cf.png align="center")
    
2. Paste the Code
    
    <div data-node-type="callout">
    <div data-node-type="callout-emoji">💡</div>
    <div data-node-type="callout-text">Note:- Change the aws region and ECR registry Name with your own.</div>
    </div>
    
    ```bash
    name: Deploy to AWS
    on:
      push:
        branches:
          - "main"
    env:
      AWS_REGION: ap-south-1
      AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY }}
      AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
      PRIVATE_SSH_KEY: ${{ secrets.AWS_SSH_KEY }}
      SERVER_PUBLIC_IP: ${{ secrets.AWS_PUBLIC_KEY }}
    
    jobs:
      deploy:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout
            uses: actions/checkout@v3
          - name: Login to AWS ECR
            id: login-ecr
            uses: aws-actions/amazon-ecr-login@v1
          - name: Build, push docker image
            env:
              REGISTRY: ${{ steps.login-ecr.outputs.registry }}
              REPOSITORY: aws-deploy
              IMAGE_TAG: ${{ github.sha }}
            run: |-
              docker build -t $REGISTRY/$REPOSITORY:$IMAGE_TAG .
              docker push $REGISTRY/$REPOSITORY:$IMAGE_TAG
          - name: Deploy docker image to EC2
            env:
              REGISTRY: ${{ steps.login-ecr.outputs.registry }}
              REPOSITORY: aws-deploy
              IMAGE_TAG: ${{ github.sha }}
              AWS_DEFAULT_REGION: ap-south-1
            uses: appleboy/ssh-action@master
            with:
              host: ${{ env.SERVER_PUBLIC_IP }}
              username: ubuntu
              key: ${{ env.PRIVATE_SSH_KEY }}
              envs: PRIVATE_SSH_KEY,REGISTRY,REPOSITORY,IMAGE_TAG,AWS_ACCESS_KEY_ID,AWS_SECRET_ACCESS_KEY,AWS_DEFAULT_REGION,AWS_REGION
              script: |-
                sudo apt update
                sudo apt install docker.io -y
                sudo apt install awscli -y
                sudo $(aws ecr get-login --no-include-email --region ap-south-1);
                sudo docker stop myappcontainer || true
                sudo docker rm myappcontainer || true
                sudo docker pull $REGISTRY/$REPOSITORY:$IMAGE_TAG
                sudo docker run -d --name myappcontainer -p 8090:80 $REGISTRY/$REPOSITORY:$IMAGE_TAG
    ```
    

---

### Create EC2 instance

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Note:- Choose Region and Create your own Infra</div>
</div>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414617454/e3b601c9-fdcc-432e-8da3-4e0d6250106b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414622170/5e86089f-f79c-4bb9-bd2b-e03e80264375.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414630296/ee376051-0fd4-4d23-bfcd-4576b60d3998.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414653902/eecb8fbe-59de-4e1c-98d1-be386498bf94.png align="center")

---

### Create ECR

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414664224/561ff767-4dbd-4088-9ea4-fa3449ff716a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414749957/3cf68a2f-fe54-4915-9cc3-f22c18ee0309.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414754478/5aea42f7-0d35-463f-9b77-208c050423d1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414761237/b0a72a4f-70fc-486a-b39e-4dcca4e5cf0f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414769237/83116e80-84dc-4acf-8135-1e8f9ab256fb.png align="center")

> There is no images right now

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414778939/86220b5b-a846-4201-b73f-f776d9114d73.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414833783/075bfee5-6960-4a3f-8b68-46c72d577499.png align="center")

---

### Create Access Key

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248066539/04ca9d69-852e-46f0-8342-ef9243909b05.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248085455/36351390-e5bb-4a27-902b-f53e635f9b3f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248102989/3cfef4ab-c40f-4e1c-abf5-4d70f2a76a45.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248155357/2df9129c-a756-4987-a002-e15a8ebe51db.png align="center")

---

### Add Secret Token in GitHub Account

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248242744/815550c0-2b2b-47fa-811e-34ccd8c84f7a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248365245/6bfa5fd5-2c32-4448-9d41-b5cab7ff9198.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248392945/3a5a2b6d-fbd2-418a-88ce-419b43ba424f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248410955/5315f73c-031a-40e6-a780-e61225255c28.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248425663/20757ddf-0210-4d2d-b41a-9bd87c973539.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248444406/e542c7e0-e7a0-4df7-b996-5ff407f2d1e5.png align="center")

> Your instance private key "key.pem"

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414937859/75d16651-31f2-4461-8bc0-6c3d4894cd6c.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414982282/a3646104-8a41-46a5-88d4-5c65dc01babd.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703414999988/329db99a-bf89-4ca3-baca-44976f67708e.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415011220/87458a69-0857-443f-b29b-6d578f47b3d9.png align="center")

---

### Click on GitHub Actions

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415039179/3d3b39e7-05d4-4572-9229-164030c66f88.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415104529/606882fa-fa93-4013-9aa6-b981cb7e9a84.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415111457/f6ef22ed-6071-40c2-a4ab-86d767508976.png align="center")

---

### Edit Inbound Rule

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Note:- Specify that port which one is define on main.yaml file</div>
</div>

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415479085/d96eb6ac-1b42-4d59-a392-5285c61dd937.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415486223/1f133885-b565-45d8-816e-a927286e25a2.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415126224/bb4d3421-3955-4848-b3f0-090a587bb016.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415509658/8c223852-2006-4531-8d02-61fd3cfabf02.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415522507/c6aecf6f-45f4-4c89-91fc-80ab923acfa2.png align="center")

---

### Show Image on ECR

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415646659/bdf3edb2-bfc1-44f5-9c76-f4c86e81d2d1.png align="center")

---

### Access The Website

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415685039/378d49ac-7224-4ae9-9a38-47133f283e7b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415693550/acff4536-26e3-4baa-bc1b-a8b9f11c790b.png align="center")

---

### Terminate Instance

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415708507/ad59abad-4ae9-463d-8bcf-ccd8936b181e.png align="center")

---

### Delete ECR

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415724344/47140332-395b-411b-b966-188a88b0b5fc.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415753864/11aa0fc7-e2ae-4ba2-b553-68e164d7b9f8.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703415766472/181a8988-4501-4365-9307-2eae45a6952a.png align="center")

copy link on brower :-) keep learning