# MarketPeak E-Commerce Deployment

## Project Overview
MarketPeak is an e-commerce platform featuring product listings, a shopping cart, and user authentication.  
This project involves setting up version control with Git, developing in a Linux environment, and deploying on AWS EC2.  
The goal is to demonstrate a complete DevOps workflow from local development to cloud deployment.

---

## Project Evidence Screenshots
All project screenshots will be stored in the **/screenshots** folder in the root of this repository.  
Example Markdown for adding a screenshot in your README:
```markdown
![Description of screenshot](screenshots/screenshot-name.png)
```

---

## Phase 1 – Sync & Review (Completed ✅)
**Tasks Performed:**
- Cloned existing GitHub repository to local machine.
- Verified website template files exist (`index.html`, `about.html`, `contact.html`, product pages, CSS/JS assets).
- Confirmed repository was initialized with Git.
- Checked remote linking to GitHub (`origin`).
- No uncommitted changes at the start.

**Evidence:**
- ![Project directory structure](screenshots/phase1-directory-structure.png)
- ![Git status clean working tree](screenshots/phase1-git-status.png)
- ![Remote repository link](screenshots/phase1-remote-link.png)

---

## Phase 2 – Git Version Control Setup (Completed ✅)
**Tasks Performed:**
- Configured global Git username and email.
- Verified presence of `main` and `development` branches.
- Pushed both branches to GitHub to ensure remote synchronization.

**Evidence:**
- ![Git config output](screenshots/phase2-git-config.png)
- ![Branch list and switching](screenshots/phase2-branch-list.png)
- ![Git push success for branches](screenshots/phase2-git-push.png)

---

## Phase 3 – Linux Development Environment (Upcoming)
**Planned Tasks:**
- Switch to `development` branch for new updates.
- Implement additional features or content updates.
- Merge changes from `development` into `main`.
## Phase 3 – Linux Development Environment

### 3.1 Create Development Branch
```bash
git checkout -b development

## Phase 3 — AWS Deployment

This phase covers setting up an Amazon EC2 instance, installing a web server, transferring files, and making the site publicly accessible.

---

### 3.1 EC2 Instance Setup
1. **Login to AWS Management Console**
2. **Launch EC2 Instance**
   - AMI: Amazon Linux 2023
   - Instance type: t2.micro (Free Tier)
   - Key pair: `your-key.pem` (Download & keep safe)
   - Security Group: Allow HTTP (port 80) and SSH (port 22)
3. **Connect to EC2 using SSH**
   ```bash
   ssh -i your-key.pem ec2-user@107.22.146.74

## Phase 3 – AWS Deployment Execution Plan

### Step 1 – Launch EC2 Instance
1. Log in to AWS Management Console.
2. Go to **EC2 → Launch Instance**:
   - **Name:** MarketPeak-EC2
   - **AMI:** Amazon Linux 2023 (Free Tier eligible)
   - **Instance type:** `t2.micro`
   - **Key pair:** Create or use existing (e.g., `Tribeca1.pem`)
   - **Security Group:** Allow **SSH (22)** and **HTTP (80)**
3. Launch the instance and copy the **Public IPv4 address**.

📸 **Screenshot:** `screenshots/phase3-ec2-instance.png`

---

### Step 2 – Connect to EC2
From local machine:
```bash
ssh -i Tribeca1.pem ec2-user@<EC2-Public-IP>

---

## Phase 4 – AWS Deployment (Upcoming)
**Planned Tasks:**
- Launch Amazon EC2 instance (Amazon Linux 2023 AMI).
- Transfer website files to EC2 instance via SCP/SFTP.
- Install Apache HTTP server (`httpd`).
- Configure server to serve website.
- Access site in browser via EC2 public IP.

---

## Phase 5 – CI/CD Workflow (Upcoming)
**Planned Tasks:**
- Use Git branching for updates.
- Push changes to GitHub and pull updates on EC2 server.
- Automate deployment steps where possible.

---

## Phase 6 – Documentation & Submission (Upcoming)
**Planned Tasks:**
- Complete README.md with final documentation, screenshots, and troubleshooting notes.
- Share GitHub repository link for project submission.
