# MarketPeak E-Commerce Deployment

## Project Overview
E-commerce platform deployment using Git, Linux, and AWS EC2 for the online marketplace "MarketPeak".

## Technologies Used
- Git (Version Control)
- HTML/CSS (Frontend)
- Apache (Web Server)
- AWS EC2 (Cloud Deployment)

## Deployment Steps

### 1. Git Setup
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOURUSERNAME/MarketPeak_Ecommerce.git
git push -u origin main
```

### 2. AWS EC2 Configuration
- Launched Amazon Linux 2023 AMI (t2.micro)
- Security Groups: HTTP (80) + SSH (22)
- Connected via SSH:
  ```bash
  ssh -i key.pem ec2-user@IP
  ```

### 3. Web Server Installation
```bash
sudo yum update -y
sudo yum install httpd git -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 4. File Transfer
```bash
git clone https://github.com/YOURUSERNAME/MarketPeak_Ecommerce.git
sudo cp -r MarketPeak_Ecommerce/* /var/www/html/
sudo systemctl restart httpd
```

## Screenshots
![Homepage](documentation/screenshots/01-homepage.png)
![Products Page](documentation/screenshots/02-products.png)
![AWS Deployment](documentation/screenshots/03-aws-deployment.png)

## Access
Live URL: http://107.22.146.74

## Troubleshooting
- 403 Forbidden Error: Ensure files are in `/var/www/html` with proper permissions
- Git Push Issues: Verify PAT (Personal Access Token) is configured
