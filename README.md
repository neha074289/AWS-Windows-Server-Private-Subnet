# AWS-Windows-Server-Private-Subnet
Launching a windows server in a private subnet and accessing the same from the local machine

Youtube Video Link:
https://youtu.be/lngfRfmCIrY

This project demonstrates how to launch a **Windows Server instance in a private subnet** on AWS and access it securely from a **local machine** using a bastion host.

Steps:
Step 1: Create a VPC
- Used “VPC and more” option to create a custom VPC named `lab`.
- Configured a public subnet-10.0.0.0/24 and a private subnet-10.0.1.0/24.
- Added an Internet Gateway and NAT Gateway.

Step 2: Create Route Tables
- Public route table routes internet traffic via Internet Gateway.
- Private route table routes through the NAT Gateway.

Step 3: Create Security Groups
- Created a Public Server Security Group from my local machine.
- Created a Private Server Security Group.

Step 4: Launch instance in EC2
- Launched a Windows instance in the public subnet.

Step 5: Launch Windows Server in Private Subnet
- Launched another Windows Server 2022 instance in the private subnet.
- Assigned the private subnet and attached the private security group.

Step 6: Access via Bastion Host
- Connected to the bastion host via RDP.
- From there, used the private IP of the Windows Server to connect to it securely.

Step 7: Verification
- Verified that the server was accessible only via the bastion host and could reach the internet via the NAT Gateway.
