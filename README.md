# LAMP Deck

Lightweight multisite manager for LAMP servers.

**LAMP Deck** installs and manages a complete LAMP environment with a simple dashboard and CLI helpers for fast website deployment.

Focused on simplicity, reproducibility and low resource usage.

<p align="center">
  <img src="https://raw.githubusercontent.com/albarreto/lampdeck-v2/main/screenshots/frontpage-2.5.4.webp" width="900">
</p>


## Stack

- Apache2 (event MPM)
- PHP 8 (FPM)
- MariaDB
- Redis
- phpMyAdmin


## Features

### Core

- One-command installation
- Multisite structure in `/var/www`
- Automatic website listing
- Lightweight dashboard
- Minimal resource usage
- Predictable directory structure
- Modular architecture for app installers


### Site management

- Fast creation of HTML websites
- Automatic CMS installation
  - WordPress
  - Joomla
- Automatic database creation for supported apps
- Optional site description via `.siteinfo`
- Automatic detection of site type:
  - Regular PHP/HTML
  - WordPress
  - Joomla
- Direct admin links in dashboard
  - WP-Admin
  - Joomla Administrator
- Optional domain association
- Optional SSL via Let's Encrypt
- Safe validation of site names
- Prevents overwrite of existing sites


### CLI helpers

Examples:

```bash
sudo lampdeck install html acme-docs "Technical documentation portal" &&
sudo lampdeck install php acme-corporate "Institutional website for ACME Corporation"
sudo lampdeck install wordpress blog "Company blog"
sudo lampdeck install joomla portal "Company portal"
sudo lampdeck install wordpress acme-blog "Official company blog"
sudo lampdeck install joomla acme-portal "Customer self-service portal"
sudo lampdeck install dokuwiki wiki "Internal documentation wiki"
sudo lampdeck install mediawiki wiki-portal "Enterprise knowledge base"

sudo lampdeck create-domain site1.com site1
sudo lampdeck activate-ssl site1.com
```


### Installation

Download installer package:

``` bash
wget https://github.com/albarreto/lampdeck-v2/raw/main/latest/install_lampdeck.tar.gz

tar -xzf install_lampdeck.tar.gz

cd install_lampdeck_<versao>

chmod +x install_lampdeck.sh

sudo ./install_lampdeck.sh

Note--ignore-install: Skips all package verification and installation steps.
```

Access dashboard:

https://SERVER-IP/


## Suitable for:

-   development environments
-   small VPS servers
-   multisite hosting
-   internal tools
-   lab environments
-   self-hosted services

