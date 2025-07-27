# 🚀 WordPress Deployment with Ansible + NGINX

This project automates the deployment of a fully functional **WordPress website** using **Ansible**, served by **NGINX**, and backed by **MySQL**.

> 🛠️ Ideal for DevOps learners, sysadmins, and engineers seeking automated LAMP/LEMP deployment.

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

## 📦 Tech Stack

- ✅ Ansible (Provisioning & Automation)
- ✅ NGINX (Web Server)
- ✅ MySQL (Database)
- ✅ PHP (for WordPress)
- ✅ Ubuntu (tested on 20.04+)
- ✅ Git (version control)

---

## 📁 Project Structure

```bash
📁 wordpress-ansible/
├── configure_wordpress.yaml         # Main playbook
├── templates/
│   └── wp-config.php.j2            # Dynamic config template
├── project-vars                   # Variables file
├── ansible-cfg                   # Main Ansible Configuration file
└── README.md