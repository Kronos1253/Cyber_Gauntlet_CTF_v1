## **Cyber Gauntlet CTF**

Beginner-friendly Capture the Flag.

### **Overview**
Cyber Gauntlet CTF is an immersive cybersecurity challenge designed to test and refine your hacking skills. The environment consists of:
- **Attacker Machine** – A Kali Linux workstation for penetration testing.
- **Vulnerable Victim Machine** – A Linux system with security weaknesses.
- **CTFd Platform** – A scoring system to submit captured flags.

This setup is built using **Docker Compose**, ensuring a portable and easily deployable CTF environment.

---

### **Current Setup**
✅ **Kali Attacker Machine**
- Uses the `kalilinux/kali-rolling` Docker image.
- Interactive terminal access for conducting attacks.

✅ **Ubuntu Victim Machine**
- Currently uses `ubuntu:latest`.
- Future iterations will introduce pre-configured vulnerabilities.

✅ **CTFd Scoring Platform**
- Hosted using the `ctfd/ctfd` image.
- Accessible at **http://localhost:8000**.
- Tracks challenges and submissions.

All components communicate over a dedicated **Docker network**.

---

### **Task List**
1️⃣ **Set up the Attacker Machine** (Kali Linux)
2️⃣ **Deploy the Victim Machine** (Ubuntu-based target)
3️⃣ **Host CTFd for Scoring and Flag Submission**

---

### **Future Enhancements**
🚀 **Pre-configured vulnerable machine** for realistic attack scenarios.  
📂 **Persistent storage** to track player progress.  
🛠️ **Automated flag generation** within victim machines.  

---

### **Getting Started**
#### **Prerequisites**

https://docs.docker.com/get-started/get-docker/
https://docs.docker.com/compose/install/

🔹 Docker & Docker Compose installed.

#### **Deployment**
Run the following command to deploy the environment:
```sh
docker-compose up -d
```

#### **Accessing the Components**
🔹 **Kali Attacker Machine:**
```sh
docker exec -it attacker /bin/bash
```
🔹 **Ubuntu Victim Machine:**
```sh
docker exec -it victim /bin/bash
```
🔹 **CTFd (Scoring Platform):**  
Open [http://localhost:8000](http://localhost:8000) in your browser.

---

### **Are You Ready to Conquer the Gauntlet?**
Join us for an electrifying CTF experience where only the most skilled will prevail! 🚀
