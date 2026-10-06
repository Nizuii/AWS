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

Once the `Create VPC` button is clicked, the VPC will be created successfully. The next step is to create subnets. In this demonstration, four subnets will be created: two public subnets across two Availability Zones and two private subnets across two Availability Zones.

To begin, select Subnets from the left-hand navigation panel, then click Create subnet. Next, select the appropriate VPC from the VPC ID dropdown menu. Under Subnet settings, name the subnet public-subnet-1, set the Availability Zone to ap-south-1a, and specify the IPv4 subnet CIDR block as 10.0.1.0/24.

<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/07034d94-df36-4b46-8831-2ecc84da70f1" />

<img width="1920" height="1013" alt="image" src="https://github.com/user-attachments/assets/b0fcd66c-34af-4351-8b9f-b3e3bc749295" />

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/190e5497-904e-413b-abb9-3ebb40a6af53" />

Following the same procedure used to create public-subnet-1, the next step is to create public-subnet-2. The only differences will be the Availability Zone, which will be set to ap-south-1b, and the CIDR notation, which will be 10.0.2.0/24.

Similarly, two private subnets will now be created: private-subnet-1 with the Availability Zone ap-south-1a and CIDR notation 10.0.3.0/24, followed by private-subnet-2 with the Availability Zone ap-south-1b and CIDR notation 10.0.4.0/24.

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/e5260b58-1a96-4de4-be84-fd6fdb4215be" />

<img width="1920" height="1011" alt="image" src="https://github.com/user-attachments/assets/f68c35a0-4de9-4be2-86c5-8553de445d83" />

<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/60c80c33-c5bc-437c-bba8-2b7212b97f31" />

The next task is to set up the routing tables. To do this, select Route Tables from the left-hand navigation panel, then click the Create route table button.

First, a route table will be created for the public subnets already provisioned. Name this route table public-rt, select LunarLabs-VPC as the associated VPC, and click Create route table to complete the process. Following the same procedure, create a second route table for the private subnets, with the only difference being the name, which will be private-rt.

<img width="1920" height="1011" alt="image" src="https://github.com/user-attachments/assets/f47e3d4b-b7ba-4d5e-8938-b7088b4683e9" />

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/636bd03b-b44a-4bbf-859e-180b005da229" />

<img width="1920" height="1013" alt="image" src="https://github.com/user-attachments/assets/10d0045a-efa4-43c8-a0c6-64ed32f11fbd" />

The next step is to create an internet gateway. Click the Create internet gateway button, then provide a name for the gateway. In this example, it will be named lunar-labs-IGW. Once the name is entered, click Create internet gateway to complete the process.

<img width="1920" height="1009" alt="image" src="https://github.com/user-attachments/assets/4d0f4295-6337-4cb8-9a4a-66f42730bdb6" />

<img width="1920" height="1007" alt="image" src="https://github.com/user-attachments/assets/5224337a-0f9c-4daa-acf1-02bf8f16f553" />

Next, the public-rt route table needs to be configured and associated with the newly created internet gateway. To do this, click Edit routes, then add a new route with the destination 0.0.0.0/0 and the target set to Internet Gateway, specifying the IGW created earlier. Once configured, click Save changes to complete the process.

<img width="1920" height="1012" alt="image" src="https://github.com/user-attachments/assets/c32623f2-82fa-4893-9bd1-93495ed91cdf" />

<img width="1920" height="1011" alt="image" src="https://github.com/user-attachments/assets/ad33e969-c103-402d-9260-352a512d62aa" />
