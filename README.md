# LAMP Deck

Provision and manage multiple web applications in seconds — no Docker required.
Supports PHP apps, CMS platforms like WordPress, Joomla, DokuWiki and more.

**LAMP Deck** is a lightweight multisite manager for LAMP environments with a simple CLI and a built-in dashboard.

Perfect for developers who want fast setup, low overhead and zero complexity.

<p align="center">
  <img src="https://raw.githubusercontent.com/albarreto/lampdeck-v2/main/screenshots/frontpage.webp" width="900">
</p>



## 🚀 Quick start

```bash
sudo lampdeck install wordpress blog "Corporate website"
sudo lampdeck create-domain blog.local blog
sudo lampdeck activate-ssl blog.local
```

Access:

```
https://SERVER-IP/blog/
```



## 🧠 Why LAMP Deck?

- No containers
- No complex configuration
- No orchestration overhead
- Fully reproducible environments
- Built-in dashboard for site management

👉 Ideal alternative when Docker is overkill.



## ⚙️ What it installs

- Apache 2.4 (event MPM)
- PHP-FPM 8.x
- MariaDB
- Redis
- phpMyAdmin
- Certbot (Let's Encrypt)



## 🐧 Supported Operating Systems

- Alpine Linux v3
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 22.04 LTS (Jammy)
- Ubuntu 24.04 LTS (Noble)
- Ubuntu 26.04 LTS (Resolute)



## 📦 Features

### Core

- One-command environment setup
- Multisite structure (`/var/www`)
- Lightweight web dashboard
- Predictable and clean architecture
- Modular app installer system
- Responsive web dashboard (mobile and tablet friendly)


### Website management

- Instantly create HTML and PHP websites
- Deploy any of the following applications with a single command:

| Category              | Application | Description                     | Database |
|-----------------------|-------------|---------------------------------|----------|
| Static / Dev          | HTML        | Static websites                 | ❌       |
| Static / Dev          | PHP         | Custom PHP applications         | -        |
| CMS                   | WordPress   | Blogging and CMS platform       | ✅       |
| CMS                   | Joomla      | Enterprise CMS                  | ✅       |
| CMS                   | Grav        | Flat-file CMS                   | ❌       |
| Wiki / Documentation  | DokuWiki    | Lightweight wiki                | ❌       |
| Wiki / Documentation  | MediaWiki   | Wikipedia-style wiki            | ✅       |
| Business              | Dolibarr    | ERP / CRM system                | ✅       |
| Business              | EspoCRM     | ERP / CRM system                | ✅       |
| Files / Collaboration | Nextcloud   | Self-hosted file sync and collaboration platform | ✅       |

> More applications coming soon...


### CLI examples

```bash
lampdeck install html docs "Documentation portal"
lampdeck install php api "Internal API"
lampdeck install wordpress blog "Company blog"
lampdeck install joomla portal "Customer portal"
lampdeck install dokuwiki wiki "Internal wiki"
lampdeck install mediawiki wiki "Another wiki"
lampdeck install dolibarr my-crm "Enterprise CRM"

lampdeck create-domain blog.local blog
lampdeck activate-ssl blog.local
lampdeck disable dokuwiki

```



## 🧩 When to use

- Local development
- Small VPS hosting
- Internal tools
- Multisite environments
- Self-hosted applications
- Lab environments



## ⚖️ Comparison

| Feature           | Docker | Manual LAMP | LAMP Deck |
|------------------|--------|------------|----------|
| Setup time       | Medium | High       | Low      |
| Complexity       | High   | Medium     | Low      |
| UI dashboard     | ❌     | ❌         | ✅       |
| Multisite ready  | ⚠️     | Manual     | ✅       |



## 📥 Installation

```bash
wget https://github.com/albarreto/lampdeck-v2/raw/main/latest/install_lampdeck.tar.gz
tar -xzf install_lampdeck.tar.gz
cd install_lampdeck_<version>
chmod +x install_lampdeck.sh
sudo ./install_lampdeck.sh
```

Optional:

```bash
--ignore-install  # Skip package installation checks
```



## 🌐 Access

```
https://SERVER-IP/
```



## 🎯 Target audience

- PHP developers
- WordPress developers
- Sysadmins
- Homelab enthusiasts
- Anyone managing multiple sites on a single server

