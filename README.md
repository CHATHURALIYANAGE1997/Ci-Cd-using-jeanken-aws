# Commands to create ci cd automation tool  using jeanken in aws EC2-instance

## 1st step
Create a ec2 instance and then configer it using your own securtiy group or firewall acoding to your requirement.</br>

## 2nd step
On the location where Key Pair is saved, open terminal and type the following command.</br>
> cd ~/my-aws-key-pairs</br>
  chmod 400 my-ec2-key-pair.pem</br>
  ssh -i my-ec2-key-pair.pem ec2-user@EC2-INSTANCE-PUBLIC-IP-ADDRESS</br>
