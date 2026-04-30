# Changelog

## Version 2.5.7 - 2026-05-02
- Support for Ubuntu 26.04 LTS (Resolute)
- Ubuntu Jammy installer: switched to native PHP 8.1 (removed PPA).
- Ubuntu Noble installer: switched to native PHP 8.3 (removed PPA).

## Version 2.5.6 - 2026-04-30
- Fixed runtime version check on frontpage
- Refactored frontpage PHP helpers into dedicated libraries

## Version 2.5.5 - 2026-04-27
- Added Grav CMS installer
- Added MediaWiki installer and new Wiki examples in Instructions section
- Fixed clean overwrite during install (lib/apps/pkg/assets)
- Fixed Ubuntu Noble SSL cert path issue
- Centralized version in common.sh

## Version 2.5.4 - 2026-04-21
- Added option for installer/upgrade: # install_lampdeck.sh --ignore-install
- Added Dokuwiki installer
- Added MediaWiki installer
- Added enable/disable commands to temporarily hide sites without deleting them

## Version 2.5.3 - 2026-04-18
- Fixed install from scratch

## Version 2.5.2 - 2026-04-18
- added app categories

## Version 2.5.1 - 2026-04-17
- Fixed bookworm packages

## Version 2.5.0 - 2026-04-17
- Removed create-website command (replaced for "lampdesk install html/php ...")

## Version 2.4.2 - 2026-04-17
- Fixed site type detection in "lampdeck sites"

## Version 2.4.1 - 2026-04-17
- Standardized app installers using shared app-common.sh
- Unified structure for apps with and without database
- Simplified creation of new app scripts (minimal variables required)
- Unified extraction process using /tmp/app-<slug>-XXXXXX
- Added daily cache to avoid re-downloading packages on the same day
- Improved rollback when installation is cancelled or fails
- Fixed site folder removal when database overwrite is declined
- Fixed Joomla installation path after extraction
- Fixed loading of shared functions from app-common
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
- Support for Ubuntu 20.04 LTS (Jammy)
- Support for Ubuntu 24.04 LTS (Noble)
- Support for Alpine 3.x

## Version 2.0.0 - 2026-04-11
- Initial release
