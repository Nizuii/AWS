# How to build a VPC?

This documentation outlines the process for building a VPC from scratch. For this demonstration, the Mumbai region will be used. To begin, we will create a new VPC. The first step is to sign in to an AWS account; in this example, a free tier AWS account is being used. Once signed in, navigate to the VPC section within AWS services. To access it, simply search for "VPC" in the search bar at the top, as illustrated below.w.

<img width="1920" height="1011" alt="image" src="https://github.com/user-attachments/assets/5b6defce-2eaa-4103-a175-2cc024b01f9a" />

<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/f810697c-300c-47f6-ba8f-a0eeae3a351a" />

The next step is to create the VPC. To do so, select `Your VPCs` from the left-hand navigation panel, then click the orange `Create VPC button`. Be sure to choose the `VPC only` option rather than VPC and more, as all settings will be configured manually.

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/13d8156a-76fb-4331-9061-110676b76a6f" />

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/a91d3bca-3fe9-4e5a-ae4e-b9d8841b3c13" />

The next step is to assign a name to the VPC. In this example, the VPC will be named LunarLabs-VPC, and the IPv4 CIDR block will be specified as 10.0.0.0/16. A /16 CIDR block provides 65,534 usable host IP addresses. All remaining settings should be left at their default values, as shown in the image.

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/658e05ad-9285-4d6b-a5f2-7696d4bbf83b" />

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/91ec96aa-5111-4c1f-b5dc-8cff3e7ef89d" />

After that click on the Create VPC button and our VPC will be created successfully. Our next step is to create subnets. Here i will be create 4 subnets. 2 public subnets in 2 AZ's and 2 private subnets in 2 AZ's. First click on the Subnets in the left navigation panel. Then click on create subnet. After that we need to select our VPC from the VPC ID drop down bar. In the subnet settings below I am naming my subnet as public-subnet-1. And the availability zone is ap-south-1a, and IPv4 subnet CIDR block as 10.0.0.0/24

<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/07034d94-df36-4b46-8831-2ecc84da70f1" />

Once the `Create VPC` button is clicked, the VPC will be created successfully. The next step is to create subnets. In this demonstration, four subnets will be created: two public subnets across two Availability Zones and two private subnets across two Availability Zones.

To begin, select Subnets from the left-hand navigation panel, then click Create subnet. Next, select the appropriate VPC from the VPC ID dropdown menu. Under Subnet settings, name the subnet public-subnet-1, set the Availability Zone to ap-south-1a, and specify the IPv4 subnet CIDR block as 10.0.0.0/24.
