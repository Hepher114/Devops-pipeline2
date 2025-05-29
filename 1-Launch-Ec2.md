# **AWS EC2 Instance Setup Guide**

## **Step-by-Step EC2 Instance Setup**

### **Step 1: Log in to AWS Console**
- Go to [AWS Management Console](https://aws.amazon.com/console/)
- Sign in with your AWS account credentials
- Navigate to **EC2 Dashboard**

### **Step 2: Launch a New EC2 Instance**
- Click **Launch Instance**
- Enter an instance name

### **Step 3: Choose an Amazon Machine Image (AMI)**
- Select an OS
- Click **Select**

### **Step 4: Choose an Instance Type**
- Select a suitable instance type:
  - **t2.large** 
- Click **Next**

### **Step 5: Configure Instance Details**
- Keep the default **VPC & Subnet** (unless customizing networking)
- Enable **Auto-assign Public IP** (for internet access)
- Click **Next**

### **Step 6: Add Storage**
- Default storage: 30 GB
- Click **Next**

### **Step 7: Configure Security Group**
- Create a new security group or use an existing one
- Allow **SSH (port 22)** for Linux instances

### **Step 8: Generate or Select a Key Pair**
- Select **Create a new key pair**
- Choose **RSA** format and download the `.pem` file
- **Store the key securely** (You will need it to access your instance)
- Click **Launch Instance**

### **Step 9: Connect to Your EC2 Instance**
- Navigate to **EC2 Dashboard** → **Instances**
- Select the instance and click **Connect**

#### **For Linux Instances:**
- Use SSH from terminal:
  ```bash
  ssh -i /path/to/your-key.pem ec2-user@your-instance-public-ip
  ```

