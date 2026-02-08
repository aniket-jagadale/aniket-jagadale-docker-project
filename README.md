## 📌 Project Overview

This project demonstrates a **basic AWS & DevOps deployment** using a simple **frontend and backend application**, containerized with **Docker** and deployed on **AWS EC2**.
The application connects successfully to a database and follows cost-optimized cloud practices.

As per assignment instructions, this submission is supported using
![](/img/architecture%20diagram.png)

---

## 1️⃣ Application

* Developed a **simple frontend and backend application**
* Used **one database** (MySQL / MongoDB)
* Backend successfully **connects to the database**
* Application data is stored and retrieved properly

📸 *Screenshots included to show database connection and app working*

---

## 2️⃣ Docker

* Created **Dockerfile(s)** for the application
* Application runs inside **Docker containers**
* Required ports are **exposed**
* Containers are configured to **auto-start on system reboot**
![](/img/image.png)
---

## 3️⃣ AWS EC2 Deployment

* Launched **EC2 instance** using cost-optimized type:

  * `t2.micro` / `t3.micro`
* Installed **Docker** on EC2
* Ran application containers on EC2 instance
---
![](/img/ec2.png)
## 4️⃣ Application Access

The application is accessible using:

* ✅ **EC2 Public IP** / **Elastic IP**
* (Optional) Route 53 domain not used

![](/img/application-acces.png)
---

## 5️⃣ Load Balancer & Auto Scaling

* Configured **Application Load Balancer (ALB)**
![](/img/loadbalancer.png)
* Created **Target Group**
![](/img/targetgroup.png)
* Attached **Auto Scaling Group (ASG)**
![](/img/ASG.png)
* Auto scaling configured based on **CPU utilization**
![](/img/cpuAS.png)


---

## 6️⃣ Cost Optimization

* Used **free-tier eligible EC2 instances**
* Minimal system resources allocated
* Auto Scaling ensures **no over-provisioning**
* Only required AWS services were enabled

---

## 7️⃣ Troubleshooting (Explanation)

### 🔹 App Not Accessible

* Checked EC2 security group inbound rules
* Verified application container is running
* Confirmed correct IP and port access

### 🔹 Container Running but Port Not Reachable

* Verified Docker port mapping
* Checked exposed ports in Dockerfile
* Ensured EC2 firewall allows traffic

### 🔹 ALB Health Check Failures

* Verified correct health check path
* Confirmed application listens on correct port
* Checked target group status

## ✅ Final Status

* Application successfully deployed
* Database connection working
* Dockerized setup completed
* ALB and Auto Scaling configured
* Cost-optimized AWS deployment achieved

---

