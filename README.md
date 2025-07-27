# 🚀 WordPress Deployment with Ansible + NGINX

This project automates the deployment of a fully functional **WordPress website** using **Ansible**, served by **NGINX**, and backed by **MySQL** — without relying on Docker or prebuilt images.

> 🛠️ Perfect for DevOps learners, junior sysadmins, or engineers looking to get hands-on with raw infrastructure automation.

---

## 📦 What This Project Does

This repo uses Ansible to configure a full **LEMP stack** (Linux, NGINX, MySQL, PHP) and install the **latest version of WordPress** on a fresh Ubuntu server.

💡 **What’s automated:**
- ✔️ Installing and configuring NGINX as the web server
- ✔️ Setting up MySQL with a user and database for WordPress
- ✔️ Downloading and configuring WordPress
- ✔️ Templating the `wp-config.php` file via Jinja2
- ✔️ Ensuring correct file and folder permissions

---

## 🛠️ Tech Stack

- 🧠 **Ansible** – Automation and provisioning
- 🌐 **NGINX** – Web server for serving WordPress
- 🐬 **MySQL** – Relational database for WordPress content
- 🐘 **PHP** – Required by WordPress
- 🐧 **Ubuntu 20.04+** – Target operating system
- 🔧 **Git** – For version control and collaboration

---

## 📁 Project Structure

```bash
📁 wordpress-ansible/
├── configure_wordpress.yaml       # Main Ansible playbook
├── templates/
│   └── wp-config.php.j2           # Jinja2 template for WordPress config
├── project-vars                   # (Ignored) File containing custom variables
├── ansible-cfg                    # Ansible configuration
└── README.md                      # You’re reading it!
````

---

## 🧩 Required Setup: `project-vars` File

Before running the playbook, **you must create a file named `project-vars`** in the project root directory. This file holds the credentials and database details needed to configure WordPress.

📄 **Sample `project-vars` file:**

```yaml
# project-vars

wordpress_user: your_db_username
wordpress_password: your_db_password
wordpress_db_name: your_db_name
wordpress_db_host: your_db_host  # e.g., localhost or 127.0.0.1
```

> ⚠️ **Important:** This file contains sensitive data and is already excluded from Git via `.gitignore`.
> Do **NOT** commit this file to your repository!

✅ **Example:**

```yaml
wordpress_user: admin
wordpress_password: strongpass123
wordpress_db_name: wordpress
wordpress_db_host: localhost
```

---

## 🚀 How to Deploy

1. 🖥️ **Clone the Repository**

   ```bash
   git clone https://github.com/OmarGamalAlden/wordpress-ansible-deployment.git
   cd wordpress-ansible-deployment
   ```

2. 🧩 **Create `project-vars` File**
   See the section above and configure your custom variables.

3. 📦 **Run the Playbook**

   ```bash
   ansible-playbook configure_wordpress.yaml -e "@project-vars"
   ```

4. 🌐 **Access Your WordPress Site**
   Open your browser and navigate to your server's IP (e.g., `http://your_server_ip`) to complete the WordPress setup.

---

## 🙈 Security Best Practices

* The `project-vars` file is **not committed** to version control.
* Always use **strong passwords** and **change default settings** after installation.
* Consider securing your server with **firewalls** and **SSL** once setup is complete.

---

## 🌟 Contributions

Contributions, issues, and feature requests are welcome! Feel free to fork and submit a PR if you’ve got improvements or ideas.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 💬 Questions?

Open an issue or ping me on [LinkedIn](https://linkedin.com/in/omargamalalden) if you have questions or need help setting things up.