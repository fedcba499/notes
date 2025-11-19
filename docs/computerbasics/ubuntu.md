## Linux
Linux is a kernal (similar to engine of car), it helps to interact with hardware of computer.

## Debian
Debian is a complete Operating System, with package manager (apt, apt-get, dpkg), command line tools, GUI (GNOME) etc.

## dpkg
dpkg stands for Debian Package, it is low level package manager. It does not install dependency

## apt
apt stands for Advaced Packaging tool, it is high level package manager. It uses dpkg underneath and adds dependency libraries also. apt is new version of apt-get. apt include apt-get and other features.

## Ubuntu
Ubuntu is Operating System based on Debain OS with additional functionality. Ubuntu uses version names for number, so that it is easier to remember.

- Ubuntu 24.04 - noble
- Ubuntu 22.04 - jammy
- Ubuntu 20.04 - focal

It is similar to android naming convention for versions.

> We need to use correct version, because previous versions may not have certian libraries, based on which software are run. Like in qgis installation error happened.

## Difference between Latest Release or Long Term Release
Long Term Release is a software which has undergone significant amount of testing and majority of bugs are resolved, company will provide support for it for long term. Where as Latest release has advanced features, but it may have bugs which are not noticed, it will undergo frequent changes to overcome these bugs. after a period of 1 or 2 years it becomes Long term Release.

For work purposes it is better to select LTR version, as it less prone to bugs and behaves as what is expected out of it.

## Ubuntu Application Installation
In Ubuntu, a program or a software can be installed from various stores, such as APT (Advanced Packaging Tool), Flatpak (Flathub - GUI), Snap Store. Program can also be downloaded in portable format as AppImage format. apt uses shared library like pip in python, but it may result in conflicting version of library used by other applications. flathub, snap and appimage uses sandbox like venv, they have their own library set (recommanded method). flatpak is recommended it is community driven, where as snap is controlled by ubuntu. similar to playstore and f droid anology.

### APT
APT stands for Advanced Packaging Tool, programs can be installed with command. APT grants superuser user access to entire system. It is recommended to intsall trusted packages only. 

```bash
# update store repository list
sudo apt update 

# install programs
sudo apt install vlc libreoffice code
```

#### PPA
PPA stands for Personal Package Archive. It is like a third party application store. As a developer, my program takes certain time to get verified by APT maintainers, to push latest update to my users, i create a third party store, individual can get this store list as well and install their latest version.

PPA is a repository hosted on launchpad.net (maintained by ubuntu). PPA are used in ubuntu and ubuntu based os.


```bash
sudo add-apt-repository ppa:<PPA_info>
```

By using PPA, we can install application which are not in apt store. we can add additional application list other than apt store.

> It is similar to F Droid, certain apps which are not in Play store (requires paying fees to add apps), can be found in F Droid (No Payment fee).

Using PPA developers can add application instead of send application to apt for validation.

If a application exists in apt list as well as ppa list, higher version, wins and it gets installed.

```bash
# To install particular version via apt
sudo apt install kicad=7.0.0-1ubuntu

```

APT can install .deb packages.

```bash
sudo apt install ./package.deb
```

Packages from repositories

| Repository | Remarks | Examples |
| --- | --- | --- |
| main | opensource and ubuntu maintained | bash, apt, python3, firefox, LibreOffice, GNOME desktop |
| universe | opensource and community maintain | kicad, vlc, gimp, arduino, freecad, inkscape |
| multiverse | closed source | rar, steam, ttf-mscorefonts-installer |
| restricted | closed source but maintained by ubuntu | intel firmware, wifi drivers, nvidia drivers |
| PPA | Third Party | Kicad, Qgis, VS Code |

## Thumb Rule 

```
APT           -   Command line tools
AppImage      -   if AppImage available on official website
Snap          -   GUI maintained by ubuntu
Flatpak       -   GUI maintained by community
```

## APT command list

### Syntax
```bash
apt command
apt [options] command
apt [options] command
apt [options] command pkg1
apt [options] command pkg1 pkg2
```

```bash
# Download Package information from all sources (including added third party PPA)
sudo apt update

# Upgrade all packages currently installed on the system
sudo apt upgrade

# List of packages that can be upgraded on the system
apt list --upgradable

# Install package
sudo apt install pkgname

# Delete or remove package (configuration files stays)
sudo apt remove pkgname

# Delete or remove package and configuration files
sudo apt purge pkgname

# Removes automatically installed dependency packages that are no longer needed by any installed package
apt autoremove

# Search packages (in name or description)
apt search pkgname

# List packages
apt list pkgname
apt list --installed
apt list --installed | grep pkgname

# List package dependency
apt depends pkgname

# Information about package
apt show pkgname
```

## cmd line tools vs GUI tools
Command Line Tools are better than GUI tools. Taking example of yt-dlp (command line tool for downloading youtube video), where requirement is to download youtube video. using yt-dlp we just need to pass link as an argument, it does every thing with default settings and download video

```bash
yt-dlp https://www.youtube.com/watch?v=example
```

It helps developer to focus on code which is essential to download, rather than wasting time on creating GUI, which is time consuming as well as he need to cater for various os. command line tools are universal can easily run on any OS, and can focus on its tasks.

Ex - yt-dlp, ffmpeg, git etc.






