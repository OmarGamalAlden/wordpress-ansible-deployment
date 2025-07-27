<h1 align="center">🚀 Wordpress Deployment with Ansible 🐘</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Automation-Ansible-179287?style=for-the-badge&logo=ansible&logoColor=white"/>
  <img src="https://img.shields.io/badge/WebServer-Nginx-0db7ed?style=for-the-badge&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/Database-MariaDB-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/OS-Ubuntu-6f42c1?style=for-the-badge&logo=ubuntu"/>
</p>

---

> 🧠 *Imagine deploying WordPress with a single playbook, no manual steps, no wasted time.*  
> Welcome to infrastructure automation that works *out of the box*.

---

## 📦 What This Project Does

This repo automates the deployment of a fully working **WordPress** website using **Ansible** on a fresh Ubuntu server. No Docker, no fluff. Just raw power and YAML magic.  

💻 **What you get:**
- Nginx web server configured to serve WordPress
- MySQL with preconfigured database/user
- Latest WordPress setup
- File & folder permissions fixed
- Configuration templated through Jinja2

---

## ⚙️ Tech Stack

| Layer          | Technology   |
|----------------|--------------|
| OS             | Ubuntu 20.04 |
| Automation     | Ansible      |
| Web Server     | Nginx        |
| Database       | MySQL        |
| CMS            | WordPress    |

---

## 🛠️ Project Structure

```bash
📁 wordpress-ansible/
├── configure_wordpress.yaml         # Main playbook
├── templates/
│   └── wp-config.php.j2            # Dynamic config template
├── project-vars                   # Variables file
└── README.md