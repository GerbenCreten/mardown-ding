# Cheat sheets and checklists

## Basiscommando's

| Taak                                                   | Commando                         |
| :----------------------------------------------------- | :------------------------------- |
| Bekijk IP-adressen van alle netwerkadapters            | `ip a`                           |
| Bekijk de status van een service                       | `systemctl status SERVICE`       |
| Start een service                                      | `sudo systemctl start SERVICE`   |
| Stop een service                                       | `sudo systemctl stop SERVICE`    |
| Herstart een service                                   | `sudo systemctl restart SERVICE` |
| Update de package repositories (Ubuntu & Debian based) | `sudo apt update`                |
| Installeer een package (Ubuntu & Debian based)         | `sudo apt install PACKAGE`       |

## Git workflow

Simpele git workflow voor projecten met een enkele branch en zonder contributors.

| Task                                                               | Command                   |
| :----------------------------------------------------------------- | :------------------------ |
| Status van het huidige project                                     | `git status`              |
| Selecteer te committen bestanden                                   | `git add FILE...`         |
| Commit alle wijzigingen naar de lokale repository                  | `git commit -m 'MESSAGE'` |
| Push lokale wijzigingen naar de remote repository                  | `git push`                |
| Haal alle wijzigingen van de remote repository binnen in de lokale | `git pull`                |

## Checklist netwerkconfiguratie

1. Is het IP-adres correct? `ip a`
2. Is de router/default gateway correct? `ip r -n`
3. Is een DNS-server ingesteld? `cat /etc/resolv.conf`

# Basic Ubuntu Commands Cheat Sheet

Here are some basic Ubuntu commands that can be used in the terminal:

## Navigation Commands

- `cd`: change directory
- `ls`: list files and directories
- `pwd`: print working directory

## File Commands

- `touch`: create a new empty file
- `mkdir`: create a new directory
- `cp`: copy files or directories
- `mv`: move or rename files or directories
- `rm`: remove files or directories
- `nano`: edit a file using the nano editor

## System Commands

- `sudo`: execute a command as the superuser
- `apt-get`: manage software packages on Ubuntu
- `choco`: manage software packages on Windows via Chocolatey package manager
- `systemctl`: manage system services
- `reboot`: restart the system
- `shutdown`: shut down the system

## Network Commands

- `ping`: test connectivity to a network host
- `ifconfig`: display network interface configuration
- `ip`: show / manipulate routing, network devices, and tunnels

## User Management Commands

- `adduser`: add a new user account
- `passwd`: set or change user password
- `su`: switch to another user account

### Explanation of `apt-get` Command

`apt-get` is a package management tool used in Ubuntu to install, remove, and manage software packages. It is a command-line tool that allows you to easily install and update software packages from Ubuntu's repositories.

Here are some common commands that you can use with `apt-get`:

- `apt-get update`: updates the package lists for upgrades and new installations
- `apt-get upgrade`: upgrades all installed packages to their latest versions
- `apt-get install package_name`: installs a new package
- `apt-get remove package_name`: removes a package
- `apt-get autoremove`: removes any packages that were installed as dependencies but are no longer needed
- `apt-cache search keyword`: searches for a package that matches the specified keyword

### Explanation of `choco` Command

`choco` is a package management tool used in Windows to install, upgrade, and uninstall software packages from the Chocolatey repository. It allows you to easily install and update software packages using the command line.

Here are some common commands that you can use with `choco`:

- `choco search package_name`: searches for a package in the Chocolatey repository
- `choco install package_name`: installs a new package
- `choco upgrade package_name`: upgrades an installed package to its latest version
- `choco uninstall package_name`: uninstalls a package
- `choco list --local-only`: lists all installed packages

## Windows

- Schakelt de controle op digitale gehandtekende scripts uit voor de huidige PowerShell sessie, en maakt alle scripts uitvoerbaar: `Set-ExecutionPolicyBypass-ScopeProcess`

## De apt package manager

- Een lijst tonen van de software die nu geïnstalleerd is via apt: `apt list --installed`

- Alle packages die nu geïnstalleerd zijn bijwerken tot de laatste versie: `sudo apt-get update && sudo apt-get upgrade`

- Via de console een package opzoeken: `apt-cache search <package_name>`

- Een geïnstalleerde applicatie verwijderen: `sudo apt-get remove <package_name>`

## De Chocolatey package manager

- Een lijst tonen van de software die nu geïnstalleerd is via Chocolatey: `choco list --local-only`

- Alle packages die nu geïnstalleerd zijn bijwerken tot de laatste versie: `choco upgrade all`

- Via de console een package opzoeken: `choco search <package_name>`

- Een geïnstalleerde applicatie verwijderen: `choco uninstall <package_name>`

## Virtual machine

- check de verbinding: `ping <IP-adres>`

- programma installeren: `sudo apt install <package>`

- status van een server checken: `systemctl status <package>`

- programma herstarten: `sudo systemctl restart <package>`

- console van een programma openen: `sudo <package>`

- open mysql met mysql -u root -p (wachtw: "letmein")

- ss -tlnp open ports checken

## sql linux

Om de MySQL server te laten luisteren op alle beschikbare netwerk interfaces (inclusief 0.0.0.0), moet u het MySQL configuratie bestand aanpassen. Hier zijn de stappen om dat te doen:

- Open het MySQL-configuratiebestand. Op Linux-systemen bevindt het bestand zich in /etc/mysql/mysql.conf.d/mysqld.cnf. Open het met cd /etc/mysql/mysql.conf.d/ en dan sudo nano mysqld.cnf.

- Zoek naar de bind-address in de sectie [mysqld] verander de waarde in 0.0.0.0. Als het niet aanwezig is, kun je het toevoegen aan de [mysqld] sectie.

- Sla de wijzigingen in het configuratiebestand op en sluit af.

- Herstart de MySQL server. Op Linux-systemen kunt u dit doen met het commando sudo service mysql restart.
