# uberspace-wp-install
Shell script to roll out WordPress dev environments for new customer projects on Uberspace.de - Serverversion 7

## WP-Install
wp-install creates a subdirectory with the needed naming convention for uberspace within the webroot. A seperate database for this installation is created. WP-CLI downloads, configures and installs the latest WordPress version. As uberspace does not offer domain hosting the IPv4 and IPv6 entries have to done on the nameserver (I use Namecheap). Having a wildcard for subs of course omits this step and the installation is instantly available. Addtional modifications for language, plugins and themes are done via WP-CLI, as far as creating a childtheme and modifying it so that it can be updatet with Git-Updater.

## Cleanup
once the development is finalized and the live site is shipped, cleanup will exactly do this: get rid of all files and the datebase and remove the entries at uberspace domain management. The shortname that is chose during the installation process has to be submitted as parameter

## uberspace-wp-install
Shell Script um auf Uberspace7 auf die Schnelle ein neues Kundenentwicklungsprojekt mit WordPress auszurollen

## ToDo
+ optional parameters for shortname and title, alternatively the interactive entry for these
+ complete interactive mode to ask for all variable (with default settings)
+ read config-file with parameters

## Changelog

1.4 more wp-cli magic, including the download from a github repo, change of language settings, creation of childtheme and tweaking via commandline to make it git-updater compatible. More comments

1.3 buxfixes and comments

1.3 Bugfixes und Kommentare

1.2 second admin - revoked

1.1 automatic retrieval of db-passwort from .my.cnf and passing it to the respective variable - no password stored within the script

1.0 Initial release