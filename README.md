# AWS-VPC-Setup

Overview

This project involves creating a custom Virtual Private Cloud (VPC) in AWS, along with configuring essential networking components such as subnets and an internet gateway. This step-by-step guide will walk you through setting up a VPC and preparing your AWS resources for secure, scalable deployments. documentation and snippets of the workflow for this project can be found in the pdf file for this repo

#Table of Contents

-Introduction to VPC
-Project Steps
-Step 1: Create a VPC
-Step 2: Create Subnets
-Step 3: Create an Internet Gateway
-Key Concepts
-Next Steps.


#Introduction to VPC

A Virtual Private Cloud (VPC) in AWS is like managing your own private city within the AWS cloud. It enables you to configure isolated environments, including neighborhoods (subnets), traffic rules (route tables), and security (NACLs, Security Groups), to keep your AWS resources secure.


Without VPCs, resources would be deployed in an unstructured, open space. VPCs give you control and ensure that your resources are secure and organized, preventing a chaotic environment like an unmanaged city without boundaries.

#Project Steps

#Step 1: Create a VPC
-Search for VPC: In the AWS Management Console, search for "VPC" and select it from the dropdown.

-Select Your VPC: In the left navigation pane, choose "Your VPCs."

-Create VPC: Click "Create VPC" and select "VPC Only."

-Name tag: Assign a name (e.g., "MyVPC").

-IPv4 CIDR block: Define the IP range (e.g., 10.0.0.0/16).

-Save and create the VPC.


#Step 2: Create Subnets

-Navigate to Subnets: On the VPC Dashboard, select "Subnets."

-Create a Subnet: Click "Create Subnet."

-Name tag: Name your subnet (e.g., "PublicSubnet1").

-VPC ID: Select the VPC you created.

-Availability Zone: Choose the first zone in your region.

-CIDR block: Define a subnet CIDR (e.g., 10.0.1.0/24).

-Enable Public IP Assignment: Select your subnet, go to "Edit Subnet Settings" and enable the auto-assign public IPv4 option.

Note: Naming a subnet "Public" doesn’t automatically make it public. You need to route it through an Internet Gateway.


#Step 3: Create an Internet Gateway

-Go to Internet Gateways: In the VPC console, select "Internet Gateways."

-Create Internet Gateway: Click "Create Internet Gateway" and assign a name.

-Attach to VPC: After creation, attach the Internet Gateway to your VPC.



#Key Concepts

-Virtual Private Cloud (VPC)

A VPC is an isolated section of the AWS cloud where you can launch AWS resources in a virtual network.


-Subnets

Subnets are subdivisions of your VPC, grouping resources with similar access rules. Public subnets connect to the internet, while private subnets are isolated.


-Internet Gateway
An Internet Gateway allows resources in your VPC to access the internet. It's a gateway between your private network and the public internet.

#Next Steps

Although we've successfully created a VPC, subnet, and attached an Internet Gateway, instances in your public subnet still need a route to the internet. In the next steps, you'll configure route tables to allow traffic to pass through your Internet Gateway.
