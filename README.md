# VPC  (Virtual Private Cloud )
A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from 
other virtual networks in the AWS Cloud. You can launch your AWS resources, such as Amazon EC2 instances, into your 
VPC.

![image](https://github.com/user-attachments/assets/68942c35-be00-4be2-8234-d282f5941caf)
## create VPC 

for creating a VPC , flow the following steps:
go to AWS Console ,then click Services ,then go to Networking & Content Delivery , click on VPC , click on Your VPCs.
after these steps on click on VPC.
![image](https://github.com/user-attachments/assets/983c59a7-2d99-4d28-97ef-772893999bd4)

## CREATE SUBNETS
for VPC , we will create four subnets. 
![WhatsApp Image 2024-11-04 at 22 50 17_7eab8d70](https://github.com/user-attachments/assets/91a9e402-0c7a-4f55-8787-9b7f2de6f59d)

## Create Internet gateway and attach to VPC 
Internet Gateways. An internet gateway is a horizontally scaled, redundant, and highly available VPC component 
that allows communication between instances in your VPC and the internet. It therefore imposes no availability risks or 
bandwidth constraints on your network traffic.

create a gateway then attach it to your VPC ,
FOR, attaching your IGW 
actions->attach to VPC
![image](https://github.com/user-attachments/assets/ec4aff80-b48e-4888-8ead-50ed1bbdae7b)

## Create Virtual Private Gateway and Attach to VPC 
It can be a physical or software appliance. The anchor on the AWS side of the VPN connection is called a virtual 
private gateway. The following diagram shows your network, the customer gateway, the VPN connection that goes to 
the virtual private gateway, and the VPC.
create a VPGW-> actions -> attach to VPC
![image](https://github.com/user-attachments/assets/3e798236-3618-499c-b48a-386d2ed0cb5f)

