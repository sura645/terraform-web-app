# 🚀 Terraform Web App Deployment on AWS

## 📌 Project Overview

This project demonstrates how to use Infrastructure as Code (IaC) with Terraform to deploy a simple web application on AWS.

An EC2 instance is provisioned, a security group is configured, and Nginx is installed automatically using user data to serve a static web page.

---

## 🧠 Architecture

Terraform → AWS → EC2 Instance → Nginx → Web Page

---

## 🛠️ Tools & Technologies Used

* Terraform (Infrastructure as Code)
* AWS (EC2, VPC, Security Groups)
* Nginx (Web Server)
* Git & GitHub (Version Control)

---

## 📁 Project Structure

```
terraform-web-app/
│
├── main.tf          # Main infrastructure configuration
├── variables.tf     # Input variables
├── outputs.tf       # Output values (Public IP)
├── terraform.tfvars # Variable values (optional)
├── .gitignore       # Ignore sensitive files
└── README.md        # Project documentation
```

---

## ⚙️ Prerequisites

Before you begin, ensure you have:

* AWS Account
* Terraform installed
* AWS CLI installed and configured
* Git installed

---

## 🔐 Configure AWS Credentials

Run the following command and provide your AWS credentials:

```
aws configure
```

---

## 🚀 Deployment Steps

### 1️⃣ Initialize Terraform

```
terraform init
```

---

### 2️⃣ Validate Configuration

```
terraform validate
```

---

### 3️⃣ Preview Changes

```
terraform plan
```

---

### 4️⃣ Apply Configuration

```
terraform apply
```

Type:

```
yes
```

---

## 🌐 Access the Application

After deployment, Terraform will output a public IP address.

Open your browser and navigate to:

```
http://<public-ip>
```

You should see:

```
🚀 Terraform Project Working!
```

---

## 🧪 Troubleshooting

### ❌ Website not loading

* Wait 1–2 minutes for Nginx to install
* Check security group allows port 80
* Verify instance is running

---

### ❌ SSH Issues

* Ensure key pair is configured
* Use correct `.pem` file permissions

---

### ❌ AMI Errors

* Use dynamic AMI lookup via Terraform data source

---

## 🧹 Cleanup (Avoid AWS Charges)

To delete all resources:

```
terraform destroy
```

Type:

```
yes
```

---

## 🔒 Security Best Practices

* Do NOT upload `.tfstate` files
* Do NOT commit `.pem` keys
* Use `.gitignore` to exclude sensitive files
* Use IAM roles instead of root credentials

---

