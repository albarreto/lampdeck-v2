# Changelog

## Version 2.12.2 - 2026-06-11
- Restore: removed duplicated database import
- Fixed backup/restore issues
- Fixed recover issues
- Fixed frontpage authentication
- Installer: added colorized output

## Version 2.12.1 - 2026-06-08
- Installer: added backup and restore commands to the post-install command summary
- Restore: fixed extraction of website files from current backup format
- Restore: added validation for missing files directory and SQL dump

## Version 2.12.0 - 2026-06-06
- Added Kanboard installer
- Added phpMyFaq installer
- Frontpage: added favicon support
- Added backup/restore command for websites and databases
- Added backup-all/restore-all command for full server website backup and restore

## Version 2.11.0 - 2026-06-02
- Added LAMP Deck Mail Relay using Postfix as a local SMTP relay for installed apps
- Nextcloud: disabled default example files for new users
- Nextcloud: enabled APCu and Redis memory caching
- Nextcloud: enabled Redis transactional file locking
- Nextcloud: added SVG preview support through ImageMagick and librsvg
- Frontpage: added operating system information to Host card
- Frontpage: improved statistics layout to better accommodate long hostnames/FQDNs
- Alpine: fixed installer failure
- Alpine: added PHP Calendar extension required by Dolibarr
- Improved cached package validation
- Fixed subsite URLs without trailing slash
- Security: added HSTS header to HTTPS virtual hosts
- Performance: increased PHP OPcache memory and interned strings buffer for enterprise applications
- Added frontpage authentication management commands (auth-enable / auth-disable)

## Version 2.9.2 - 2026-05-29
- Nextcloud: fixed installation on Debian
- Moodle: added automatic cron configuration for scheduled tasks
- Moodle: installer now automatically downloads and configures Portuguese (Brazil), Spanish, French, and German language packs

## Version 2.9.0 - 2026-05-22
- Added Moodle installer
- Nextcloud installation is now blocked on unsupported PHP versions
- Nextcloud: added default admin username ([admin]) to installer prompt
- Nextcloud: added admin password to final installation summary
- Nextcloud: fixed install in ubuntu jammy
- Installers now display both public hostname/FQDN and direct server IP access URLs after website creation

## Version 2.8.0 - 2026-05-18
- Added EspoCRM installer
- Added Nextcloud installer
- New command: recover (recreate missing Apache alias for a website)
- New command: recover-all (recreate missing Apache aliases for all websites)
- Fixed reinstall/upgrade preserving existing website aliases and configurations
- Added bzip2 support for .tar.bz2 application packages
- Added support for apps using custom webroot (APP_WEBROOT)
- Improved compatibility with modern PHP applications using /public structure
- Improved PHP defaults for enterprise applications (max_input_time)
- Added persistent global config (/etc/lampdeck/config.sh)

## Version 2.7.1 - 2026-05-13
- Fixed bash autocompletion support for Alpine Linux
- Improved Alpine shell compatibility

## Version 2.7.0 - 2026-05-12
- Added Alpine Linux support (bash is required: apk add bash)
- Fixed Alpine frontpage showing Apache system directories
- Improved Alpine Linux service compatibility
- Renamed Apache section to Web Server

## Version 2.6.3 - 2026-05-10
- Improved Alpine Linux support
- Fixed HTTPS domain handling on Alpine
- Improved Apache virtual host compatibility across distributions
- Fixed frontpage and subsite coexistence
- Improved subpath website access compatibility
- Fixed domain vhost precedence overriding websites with frontpage default virtual hosts
- Removed unnecessary 000-lampdeck Apache vhosts during domain creation
- Improved Apache VirtualHost behavior for domain-based access on Alpine Linux
- Fixed PHP-FPM startup issues after reboot on Debian, Ubuntu and Alpine
- Improved PHP version detection across all supported distributions
- Improved Linux distribution detection using PRETTY_NAME
- Fixed Alpine Linux compatibility with OpenRC environments
- Fixed Apache/PHP-FPM socket handling on Alpine Linux

## Version 2.6.0 - 2026-05-08
- Added automatic web user detection (multi-distro support)
- Removed hardcoded www-data user
- Improved compatibility with Alpine Linux
- Tools tab moved to other position
- Fixed regression introduced in 2.5.11 causing PHP-FPM socket issues after reboot

## Version 2.5.11 - 2026-05-04
- Added "Supported Apps" tab with application list and descriptions
- Simplified Instructions tab
- Unified PHP-FPM socket
- Cleaned old PHP-FPM services and Apache configs automatically
- Standardized PHP packages
- All vhosts use version-independent socket
- Fixed incorrect PHP version detection
- Fixed Apache version output (now displays only the version number)
- Fixed PHP-FPM service detection in frontpage
- Fixed PHP version display on Ubuntu Jammy (removed distro suffix)
- Fixed PHP version detection in CLI (now matches active PHP-FPM)
- Fixed underline on update badge link in frontpage
- Support for Ubuntu 26.04 LTS (Resolute) - beta
- Ubuntu Jammy installer: switched to native PHP 8.1 (removed PPA).
- Ubuntu Noble installer: switched to native PHP 8.3 (removed PPA).

## Version 2.5.6 - 2026-04-30
- Added Dolibarr ERP/CRM installer
- Added Grav CMS installer
- Added MediaWiki installer and new Wiki examples in Instructions section
- Added option for installer/upgrade: # install_lampdeck.sh --ignore-install
- Added Dokuwiki installer
- Added enable/disable commands to temporarily hide sites without deleting them
- Refactored frontpage PHP helpers into dedicated libraries
- added app categories
- Fixed runtime version check on frontpage
- Fixed clean overwrite during install (lib/apps/pkg/assets)
- Fixed Ubuntu Noble SSL cert path issue
- Fixed clean overwrite during install (lib/apps/pkg/assets)
- Fixed Ubuntu Noble SSL cert path issue
- Fixed install from scratch
- Fixed bookworm packages

## Version 2.5.0 - 2026-04-17
- Removed create-website command (replaced for "lampdesk install html/php ...")

## Version 2.4.2 - 2026-04-17
- Standardized app installers using shared app-common.sh
- Unified structure for apps with and without database
- Simplified creation of new app scripts (minimal variables required)
- Unified extraction process using /tmp/app-<slug>-XXXXXX
- Added daily cache to avoid re-downloading packages on the same day
- Improved rollback when installation is cancelled or fails
- Fixed site folder removal when database overwrite is declined
- Fixed Joomla installation path after extraction
- Fixed loading of shared functions from app-common
- Fixed site type detection in "lampdeck sites"
- Renamed frontpage tab from HTML to HTML/PHP
- Updated frontpage new version alert text

## Version 2.4.0 - 2026-04-16
- Frontpage filter by app type (HTML, WordPress, Joomla)
- Improved error message for unsupported apps
- Added confirmation prompt before replacing an existing database
- Existing database is only dropped after user confirmation
- Site folder is now removed if installation is cancelled during database overwrite

## Version 2.3.2 - 2026-04-16
- Dashboard notification when a newer version of LAMP Deck is available.

## Version 2.3.1 - 2026-04-16
- Fixed MariaDB root password prompt bug
- New optional `-d <domain>` flag in `lampdeck install` to create the domain during app installation.

## Version 2.3.0 - 2026-04-15
- Added Joomla installer
- Shared DB validation library for apps
- Improved validation rules for site names
- Admin link support (WordPress, Joomla)
- Improved create-website layout
- Consistent typography in site info cards

## Version 2.2.1 - 2026-04-14
- Simplified changelog
- Shared validation and DB logic across apps
- Prevent unnecessary DB password prompt when site exists

## Version 2.2.0 - 2026-04-14
- Modular app architecture
- WordPress installer moved to apps/wordpress.sh
- New command: lampdeck install wordpress
- Improved frontpage app detection using .app-type markers
- Improved install flow validation
- Cached WordPress download reused when available

## Version 2.1.5 - 2026-04-14
- Frontpage is always preserved when accessing the server by IP
- Domains no longer override the main frontpage
- Improved multisite behavior
- Prevents modification when website folder already exists
- More reliable domain creation
- Improved default website template (light layout)
- Version command now shows Apache, PHP, MariaDB and Redis versions
- Fixed phpMyAdmin installation in upgrades
- Fixed logo size in frontpage
- Fixed PHP 8.4 installation for Ubuntu releases

## Version 2.1.0 - 2026-04-12
- Added support for Ubuntu LTS releases (22.04 Jammy, 24.04 Noble)

## Version 2.0.0 - 2026-04-11
- Initial release
