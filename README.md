# Commands to create ci cd automation tool  using jeanken in aws EC2-instance

## 1st step
Create a ec2 instance and then configer it using your own securtiy group or firewall acoding to your requirement.</br>

## 2nd step
On the location where Key Pair is saved, open terminal and type the following command.</br>
> cd ~/my-aws-key-pairs</br>
  chmod 400 my-ec2-key-pair.pem</br>
  ssh -i my-ec2-key-pair.pem ec2-user@EC2-INSTANCE-PUBLIC-IP-ADDRESS</br>

## 3rd step
Ensure that your software packages are up to date.</br> 
> sudo yum update –y

## 4th step
Add the Jenkins repo.</br>
> sudo wget -O /etc/yum.repos.d/jenkins.repo \https://pkg.jenkins.io/redhat-stable/jenkins.repo

## 5th step
Import a key file from Jenkins-CI.</br>
> sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
> sudo yum upgrade

## 6th step
Install Java></br> 
> sudo amazon-linux-extras install java-openjdk11 -y

## 7th step
Install Jenkins.</br> 
> sudo yum install jenkins -y

## next step
Enable the Jenkins service to start.</br> 
> sudo systemctl enable jenkins

## next step
Start Jenkins as a service.</br> 
> sudo systemctl start jenkins

## next step
Use the following command to display this password.</br> 
> sudo cat /var/lib/jenkins/secrets/initialAdminPassword

## next step
After recive user password you can run 'ec2-user@EC2-INSTANCE-PUBLIC-IP-ADDRESS:8080' in your browser. after you create a user you can create a new ci cd pipeline accoding to your requirement using different stages.
