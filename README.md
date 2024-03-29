# US-Visa-Approval 
[![Deploy Application Docker Image to EC2 instance](https://github.com/akshats1/US-Visa-Approval/actions/workflows/aws.yaml/badge.svg)](https://github.com/akshats1/US-Visa-Approval/actions/workflows/aws.yaml)

## How to Run
```bash
conda create -n visa python=3.8 -y
```
```bash
conda activate visa
```
```bash
pip install -r requirements.txt
```

```bash
python app.py

```
## Dataset Used US-Visa
[https://www.kaggle.com/datasets/moro23/easyvisa-dataset?resource=download]

## WorkFlow
1. Constant
2. config_entity
3. artifact_entity
4. component
5. pipeline
6. app.py

## Export the environment variable
```bash
export MONGODB_URL="mongodb+srv://<username>:<password>...."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
```


# AWS-CICD-Deployment-with-Github-Actions
## 1. Login to AWS console.
## 2. Create IAM user for deployment
#with specific access
```bash
1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


# Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2


#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

## 3. Create ECR repo to store/save docker image
```bash
- Save the URI: 136566696263.dkr.ecr.us-east-1.amazonaws.com/mlproject
```
## 4. Create EC2 machine (Ubuntu)
## 5. Open EC2 and Install docker in EC2 Machine:

#optinal
```bash
sudo apt-get update -y

sudo apt-get upgrade
```

#required
```bash
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

## 6. Configure EC2 as self-hosted runner:
```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```
## 7. Setup github secrets:
```bash
 - AWS_ACCESS_KEY_ID
 - AWS_SECRET_ACCESS_KEY
 - AWS_DEFAULT_REGION
 - ECR_REPO
```



