# AWS-Ec2-Web-App

📌 Project Overview
-
This project shows how to create and manage a web application server using Amazon EC2.
An EC2 instance is launched, configured with a web server, and used to host a simple web application.

🛠 Tools & Services Used
-
Amazon EC2
Amazon VPC
Security Group
Key Pair
Linux (Amazon Linux / Ubuntu)
Apache Web Server
⚙️ Instance Details

Instance Name: web-app
-
Instance Type: t3.micro (Free Tier)
Region: us-east-1
Availability Zone: us-east-1d

🧱 Architecture
-
EC2 instance is launched inside a VPC
Security group allows SSH (22) and HTTP (80)
Linux OS is installed on EC2
Apache web server is installed
Web application is deployed

🔄 Step-by-Step Implementation
-
Step 1: Launch EC2 Instance
Login to AWS Console
Select EC2 service
Launch instance with Amazon Linux
Choose t3.micro instance type

Step 2: Configure Security Group
-
Allow SSH (22) from my IP
Allow HTTP (80) from anywhere

Step 3: Connect to EC2
-
ssh -i key.pem ec2-user@<public-ip>

Step 4: Install Web Server
-
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

Step 5: Deploy Application
-
cd /var/www/html
vi index.html

<h1>AWS EC2 Web Application</h1>
<p>Deployed successfully</p>

Step 6: Access Application
-
http://<public-ip>














Application is accessed using public IP
