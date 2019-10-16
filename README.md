# fa19-team-001-ami
Pre-Requisite:
Install Packer

Copy Aws credentials to ami-var-lacal.json

Build AMI using packer
packer build -var-file=./ami-vars-local.json centOS-ami.json

Launch EC2 instance from local machine and aws console 
ssh -i /home/arjun/.ssh/ centos@ec2-54-234-151-24.compute-1.amazonaws.com

Copy web-app to centos ec2 instance
scp -i /home/arjun/.ssh/ /home/arjun/Documents/devnew/ccwebapp/webapp.zip centos@ec2-54-234-151-24.compute-1.amazonaws.com:.

Setup Mysql 

Run NPM start to start web app in webapp folder
