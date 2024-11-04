# VPC
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

## Create route tables and attach to subnets 
Route Tables. A route table contains a set of rules, called routes that are used to determine where network 
traffic is directed. Each subnet in your VPC must be associated with a route table; the table controls the routing for the 
subnet. 
One route for Internet gateway, another for Virtual private gateway (R1-IGW and R2-VGW) 
* Route - 0.0.0.0/0 to IGW
* Route - 192.168.0.0/16 to VGW

create route tables ->then add route

  ![WhatsApp Image 2024-11-05 at 00 03 21_87b98a1c](https://github.com/user-attachments/assets/87dd1fbc-4684-47e3-9ae0-c3c2d0366890)

  
![WhatsApp Image 2024-11-05 at 00 01 09_5ad6c39d](https://github.com/user-attachments/assets/2664dd7a-d520-4a9b-8489-20098dde04f0)

Attach routing tables to subnets. R1-IGW to S3-Public and S4-Public, public network required to have internet access. 
Attach R2-VGW to S1-Private and S2-Private (No internet become a private subnets)

