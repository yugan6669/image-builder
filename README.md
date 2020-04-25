Project Title
================
Packer is used to build Amazon Machine images


installation and set up 
===================================
$yum install git -y && yum install wget -y && yum install unzip 

$wget https://releases.hashicorp.com/packer/1.5.5/packer_1.5.5_linux_amd64.zip

$unzip packer_1.5.5_linux_amd64.zip && mv packer /bin/ && rm -rf ./packer*


Execution Flow
===========================

step 1: clone repo

$git clone https://github.com/krishnamaram2/Image_Builder.git


step 2: enter src directory

$cd Image_Builder/src


step 3: enter access key and secret key

vi variables.json

{

    "aws_access_key": "",
    
    "aws_secret_key": "",
    
    "region": "us-east-1"
    
  }


Step 4: validate syntax

packer validate -var-file=variables.json builders.json


Step 5: Build custome AMI

packer build -var-file=variables.json builders.json

