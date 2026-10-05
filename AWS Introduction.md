# What is AWS?

**AWS** or **Amazon Web Services** is a cloud computing platform that provides on-demand IT-resources such as computing power, data storage, databases, over the internet on a pay-as-you-go pricing model. The most common uses cases of AWS are web hosting (running scalable websites or web applications), data analytics (Process and analyze large volumes of business data), app development (build, test and deploy applications quickly).

## Commonly used AWS services
Amazon provides a vast amount of services. The most and commonly used AWS services are:

- **EC2 (Elastic Cloud Compute)**: AWS EC2 allows us to rent virtual computers (called instances) to un our applications. Think of it as a physical computer located in an Amazon data center that you control remotely over the internet, without the hassle of buying or maintaining physical hardware.
- **ECS (Elastic Container Service)**: ECS is an AWS service for running and managing docker containers on AWS. With ECS on EC2, ECS orchestrates your containers, but you still have EC2 infrastructure underneath. But with ECS on Fargate, AWS handles the underlying compute infrastructure, so you focus much more on the containers themselves.
- **EKS (Elastic Kubernetes Service)** EKS is an AWS service that makes it easy to run Kubernetes on AWS without needing to install, operate, and maintain your own Kubernetes control plane. Kubernetes is the industry-standard, open-source platform for automating the deployment, scaling, and management of containerized applications. EKS handles the heavy lifting of keeping that platform secure, highly available, and up to date.
- **Security Groups**: AWS Security Group is a virtual firewall for EC2 instance to control inbound and outbound traffic. They operate at the instance level (not the subnet level), meaning each virtual server can have its own unique set of firewall rules.
- **AWS S3 (Simple Storage Service)**: AWS S3 is an object storage service that offers scalability, data availability, security and performance. Think of it as an infinite digital filing cabinet in the cloud where you can store and protect any amount of data for a wide range of use cases, such as websites, mobile applications, backup and restore, and big data analytics.
