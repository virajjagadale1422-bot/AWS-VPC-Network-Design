# AWS Custom VPC Network Design and Nginx Deployment

## Project Overview

This project demonstrates the design and implementation of a custom AWS Virtual Private Cloud (VPC) with public and private subnets. The project includes network configuration, routing, internet connectivity, security group management, and deployment of an Nginx web server on an Ubuntu EC2 instance.

The objective was to gain hands-on experience with AWS networking services, Linux server administration, and web server deployment.

---

## Architecture Diagram

AWS-VPC-Network-Design
│
├── README.md
├── architecture-diagram.png
│
└── screenshots
    ├── vpc-dashboard.png
    ├── subnets.png
    ├── internet-gateway.png
    ├── route-table.png
    ├── security-group.png
    ├── ec2-instance.png
    ├── ping-google.png
    ├── nginx-status.png
    └── nginx-homepage.png

### Architecture Components

* Custom VPC (10.0.0.0/16)
* Public Subnet (10.0.1.0/24)
* Private Subnet (10.0.2.0/24)
* Internet Gateway (my-IGW)
* Route Tables
* Security Groups
* Ubuntu EC2 Instance
* Nginx Web Server

---

## AWS Services Used

* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Tables
* Security Groups
* Ubuntu Linux
* Nginx Web Server

---

## Network Configuration

### VPC

| Resource   | Configuration  |
| ---------- | -------------- |
| VPC Name   | my-network-vpc |
| CIDR Block | 10.0.0.0/16    |

### Subnets

| Subnet         | CIDR Block  | Purpose                              |
| -------------- | ----------- | ------------------------------------ |
| Public Subnet  | 10.0.1.0/24 | Web Server                           |
| Private Subnet | 10.0.2.0/24 | Future Database / Internal Resources |

### Route Table

| Destination | Target           |
| ----------- | ---------------- |
| 10.0.0.0/16 | Local            |
| 0.0.0.0/0   | Internet Gateway |

### Security Group Rules

| Protocol | Port | Source    |
| -------- | ---- | --------- |
| SSH      | 22   | 0.0.0.0/0 |
| HTTP     | 80   | 0.0.0.0/0 |

---

## Implementation Steps

### Step 1

Created a custom VPC with CIDR block 10.0.0.0/16.

### Step 2

Created Public and Private Subnets.

### Step 3

Created and attached an Internet Gateway to the VPC.

### Step 4

Configured Route Tables and associated the Public Subnet.

### Step 5

Created Security Groups for SSH and HTTP access.

### Step 6

Launched an Ubuntu EC2 instance inside the Public Subnet.

### Step 7

Verified internet connectivity using:

```bash
ping google.com
```

### Step 8

Installed Nginx Web Server:

```bash
sudo apt update
sudo apt install nginx -y
```

### Step 9

Verified Nginx service status:

```bash
sudo systemctl status nginx
```

### Step 10

Accessed the Nginx welcome page using the EC2 Public IP.

---

## Screenshots

VPC Dashboard
Subnets
Internet Gateway
Route Table
Security Group
EC2 Instance
Ping Google
Nginx Status
Nginx Homepage

---

## Skills Demonstrated

### AWS

* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Tables
* Security Groups

### Networking

* TCP/IP Networking
* CIDR Blocks
* Public and Private Subnets
* Routing Concepts
* Internet Connectivity

### Linux

* Ubuntu Administration
* SSH Access
* Package Management
* Service Management

### Web Server Administration

* Nginx Installation
* HTTP Configuration
* Web Server Verification

---

## Project Outcome

Successfully designed and deployed a secure AWS networking environment with public and private subnets. Configured routing, internet access, security controls, and deployed an Nginx web server on an Ubuntu EC2 instance. Verified network connectivity and web server accessibility through a public IP address.

---

## Description

**Custom VPC Network Design and Nginx Deployment | AWS**

* Designed and configured a custom AWS VPC with public and private subnets using CIDR-based addressing.
* Implemented Internet Gateway and Route Tables to provide internet connectivity.
* Configured Security Groups for secure SSH and HTTP access.
* Deployed an Ubuntu EC2 instance and installed an Nginx web server.
* Verified routing, DNS resolution, and internet connectivity through Linux networking tools.
