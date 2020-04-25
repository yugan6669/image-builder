#Project Title

Packer installation and set up 
--------------------------------------
yum install git -y && yum install wget -y && yum install unzip &&
wget https://releases.hashicorp.com/packer/1.5.5/packer_1.5.5_linux_amd64.zip && 
unzip packer_1.5.5_linux_amd64.zip && mv packer /bin && rm -rf ./packer*

git clone 

vi variables.json
{
    "aws_access_key": "",
    "aws_secret_key": "",
    "region": "us-east-1"
  }

packer validate -var-file=variables.json builders.json
packer build -var-file=variables.json builders.json

