---
title: "1. Deploy Website using GitHub Actions"
datePublished: Fri Dec 22 2023 12:56:25 GMT+0000 (Coordinated Universal Time)
cuid: clqgmy1de000708jo4hsx9asr
slug: 1-deploy-website-using-github-actions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703431298347/1bcdfd7b-04e2-41de-9fb6-f482569b6061.png
tags: aws, github, git, devops, s3-bucket

---

## Pre-Requisites

1. GitHub Account
    
    1. Create Repository
        
    2. Code
        
    3. Action
        
    4. Set Secret Token
        
2. AWS Account
    
    1. IAM Access Key
        
    2. S3 Bucket
        
        1. Define Policy
            

---

### Create Repository

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246665575/2c90c2f7-ee32-4e4b-ab5d-728384da6903.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246674255/3c364ff4-f37c-42f9-b5a7-e2c08a9cd76b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246688741/236abf52-7a76-43f9-ab1c-e5a3aafc835c.png align="center")

### Clone The Code

```bash
git clone https://github.com/Fir3eye/fir3-Portfolio.git
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703246790149/58813100-de9a-4edf-8dfe-6e7472b7bc7d.png align="center")

### Click on Action Button and click setup a workflow yourself

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247095504/b64b5c88-a82d-46f2-a654-86399a9f7bad.png align="center")

1. Openend Like This
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247251301/c780b80d-5d9e-4aa6-9e8d-788310a679cf.png align="center")
    
2. Paste the Code
    
    ```bash
    name: Portfolio Deployment
    
    on:
      push:
        branches:
        - main
    
    jobs:
      build-and-deploy:
        runs-on: ubuntu-latest
        steps:
        - name: Checkout
          uses: actions/checkout@v1
    
        - name: Configure AWS Credentials
          uses: aws-actions/configure-aws-credentials@v1
          with:
            aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
            aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
            aws-region: us-east-1
    
        - name: Deploy static site to S3 bucket
          run: aws s3 sync . s3://your-bucket-name --delete
    ```
    

---

### Create S3 Bucket

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247433758/55e2d54f-c7f6-48a8-90b5-4a8e9c4b4d13.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247650249/5fa89813-ff4a-4cd0-8d83-73e26a2d5bb7.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247665093/32731832-358f-4224-9647-60d09eb4e8c1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703247678294/0a9bebfb-18b5-45a4-93a2-93e867a629f1.png align="center")

### Ceate Access Key

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248066539/04ca9d69-852e-46f0-8342-ef9243909b05.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248085455/36351390-e5bb-4a27-902b-f53e635f9b3f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248102989/3cfef4ab-c40f-4e1c-abf5-4d70f2a76a45.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248155357/2df9129c-a756-4987-a002-e15a8ebe51db.png align="center")

### Add Secret Token in GitHub Account

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248242744/815550c0-2b2b-47fa-811e-34ccd8c84f7a.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248365245/6bfa5fd5-2c32-4448-9d41-b5cab7ff9198.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248392945/3a5a2b6d-fbd2-418a-88ce-419b43ba424f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248410955/5315f73c-031a-40e6-a780-e61225255c28.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248425663/20757ddf-0210-4d2d-b41a-9bd87c973539.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248444406/e542c7e0-e7a0-4df7-b996-5ff407f2d1e5.png align="center")

### Click on GitHub Actions

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248565844/003f86f3-efab-4372-b6ee-b81f439f5706.png align="center")

### Show code in S3 Bucket

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248679974/690ce933-1dfb-4e17-8b8f-8d2e73c99bf7.png align="center")

### Enable Static Website

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248951980/5ec4b17c-c29b-4770-97e8-a37ddbe6177f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248973352/91e9ff54-92db-4456-8e0e-1f95714f4795.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248982150/cfb7ab5f-541e-4fd5-972d-1241ffbdd2e9.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703248992532/1821f2c0-2b17-4286-825d-45a38d66f23e.png align="center")

### Create Policy

copy this code and change the bucket name

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703249234332/3f7eb5e3-0d14-4d53-960e-a3a970e01541.png align="center")

```bash
{
    "Version": "2012-10-17",
    "Id": "Policy1703243664849",
    "Statement": [
        {
            "Sid": "Stmt1703243663411",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::fir3-portfolio/*"
        }
    ]
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703249111855/bce92608-15d3-4d06-991d-7db9c32e8c75.png align="center")

Go and copy link

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703249355676/8216cca9-a0b7-4b28-a093-c74b4332ae4f.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1703249360630/4047bc7c-bf08-4b46-89dc-c2732eb78183.png align="center")

copy link on brower :-) keep learning