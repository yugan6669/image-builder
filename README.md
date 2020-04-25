#Project Title

Installation and set up
----------------------------
yum install git -y && yum install wget -y && yum install unzip &&
wget https://releases.hashicorp.com/packer/1.5.5/packer_1.5.5_linux_amd64.zip && 
unzip packer_1.5.5_linux_amd64.zip && mv packer /bin && rm -rf ./packer*
