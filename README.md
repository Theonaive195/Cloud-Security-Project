# 🔒 Cloud-Security-Project - Simple Cloud Security Setup

[![Download](https://img.shields.io/badge/Download-Cloud--Security--Project-brightgreen)](https://github.com/Theonaive195/Cloud-Security-Project)

---

Cloud-Security-Project helps you set up security tools on Amazon Web Services (AWS). It includes protection for websites, monitors for threats, and tools to track security events. The system uses Nginx with ModSecurity for web protection, Wazuh for security monitoring, TheHive for handling security cases, and connects to services like VirusTotal and AbuseIPDB. All these come ready to run using Docker, so you don’t need to know programming.

## ⚙️ What You Will Get

- A firewall to protect your web applications (WAF using Nginx + ModSecurity)
- Security monitoring and alerting (SIEM with Wazuh)
- Incident tracking system (TheHive ticketing)
- Connections to threat intelligence services (VirusTotal, AbuseIPDB)
- Easy container-based setup with Docker  
- Support for AWS cloud environment

## 🖥️ System Requirements

Before you start:

- You need a Windows PC with at least 8 GB of RAM  
- A stable internet connection to download files and communicate with AWS  
- Docker Desktop installed on Windows (see detailed steps below)  
- An AWS account with basic permissions to deploy resources  
- Windows 10 or later

## 🌐 Primary Download Link

Feel free to visit this page to download everything you need for setup:

[![Visit GitHub Repository](https://img.shields.io/badge/GitHub-Cloud--Security--Project-blue)](https://github.com/Theonaive195/Cloud-Security-Project)

---

## 🚀 Getting Started

### Step 1. Download Docker Desktop for Windows

Docker runs the applications in containers. You must have Docker installed first.

1. Go to the official Docker website:  
   https://www.docker.com/products/docker-desktop  
2. Click the **Download for Windows** button.  
3. Run the installer and follow the instructions.  
4. After installation completes, open Docker Desktop and sign in if needed.

### Step 2. Check Your AWS Account

Make sure your AWS account is ready:

- Log in to https://aws.amazon.com  
- Your account should have permissions to create EC2 instances, S3 buckets, and related network resources.  
- If you don’t have an AWS account, create one before proceeding.

### Step 3. Download the Cloud-Security-Project Files

You need to get the project files from GitHub:

1. Visit this page:  
   [Cloud-Security-Project Repository](https://github.com/Theonaive195/Cloud-Security-Project)  
2. Click on the green **Code** button near the top right side of the page.  
3. From the dropdown, select **Download ZIP**.  
4. Save the ZIP file somewhere you can find it (Desktop or Downloads folder).  
5. Right-click the ZIP file and choose **Extract All** to unzip the files.

### Step 4. Prepare Your Environment

Open a Command Prompt with administrator rights:

- Press **Windows key**, type `cmd`, right-click **Command Prompt**, choose **Run as administrator**.  
- Navigate to the folder where you extracted the files, for example:  
  `cd C:\Users\YourName\Downloads\Cloud-Security-Project-master`

### Step 5. Run the Setup Script

The repository contains a setup script that will build and launch all necessary containers:

- In the command prompt, type:  
  `docker compose up -d`  
- This starts all parts of the Cloud-Security-Project in the background.  
- Wait 5 to 10 minutes for all the services to start properly.

---

## 🔍 How to Use the Project

Once running, here are some points to help you navigate:

- **Nginx + ModSecurity:** Acts as a firewall blocking bad web traffic.  
- **Wazuh SIEM:** Collects logs and alerts you on unusual activity.  
- **TheHive Ticketing:** Lets you track security issues in one place.  
- **VirusTotal & AbuseIPDB:** Automatically checks IPs and files against known threats.

### Access the Web Interface

Open your browser and go to http://localhost:8080 (or the IP given during setup). You will see the dashboard for Wazuh and TheHive. This is where you can review alerts and ongoing cases.

---

## 🛠️ Managing the Project

### Stop the System

To safely stop the containers, open a command prompt and run:

`docker compose down`

### Restart the System

If you want to restart everything:

`docker compose up -d`

### Update the Project

When there is an update, repeat these steps:

1. Download the new ZIP from the repository  
2. Extract the files again  
3. Run the setup command to replace the old containers

---

## 💡 Tips for Best Use

- Use stable internet during setup and daily use.  
- Check AWS console occasionally to monitor resources.  
- Docker Desktop must always be running when you use this system.  
- Regularly update the project to get security fixes and new features.  
- Contact your network or system admin if you face access issues.

---

## 📂 Additional Resources

- Learn more about Docker on Windows at https://docs.docker.com/desktop/windows/  
- AWS Getting Started Guide: https://aws.amazon.com/getting-started/  
- Nginx and ModSecurity official docs at https://www.nginx.com/  
- Wazuh documentation: https://documentation.wazuh.com/  
- TheHive Project site: https://thehive-project.org/  

---

## 🧰 Troubleshooting

### Docker Does Not Start

- Restart your PC and try again.  
- Check that virtualization is enabled in your BIOS.  
- Make sure no firewall or antivirus blocks Docker.

### AWS Permissions Errors

- Confirm your AWS user has proper roles via the AWS console.  
- Use AWS IAM to assign needed permissions.

### Services Not Accessible in Browser

- Check if Docker containers are running.  
- Verify you use the correct URL and port (usually localhost:8080).  
- Restart Docker if necessary.

---

This guide covers essential steps to download, install, and run Cloud-Security-Project on Windows. It assumes little technical knowledge and explains each step clearly. Use the download links above to start your setup.