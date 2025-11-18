## Ubuntu Version Names
Ubuntu uses version names for number, so that it is easier to remember.

- Ubuntu 24.04 - noble
- Ubuntu 22.04 - jammy
- Ubuntu 20.04 - focal

It is similar to android naming convention for versions.

> We need to use correct version, because previous versions may not have certian libraries, based on which software are run. Like in qgis installation error happened.

## Difference between Latest Release or Long Term Release
Long Term Release is a software which has undergone significant amount of testing and majority of bugs are resolved, company will provide support for it for long term. Where as Latest release has advanced features, but it may have bugs which are not noticed, it will undergo frequent changes to overcome these bugs. after a period of 1 or 2 years it becomes Long term Release.

For work purposes it is better to select LTR version, as it less prone to bugs and behaves as what is expected out of it.

## Ubuntu Application Installation
In Ubuntu, a program or a software can be installed from various stores, such as APT (Advanced Packaging Tool), Flatpak (Flathub - GUI), Snap Store. Program can also be downloaded in portable format as AppImage format.

### APT
APT stands for Advanced Packaging Tool, programs can be installed with command. 

```bash
# update store repository list
sudo apt update 

# install programs
sudo apt install vlc libreoffice code
```

#### PPA
PPA stands for Personal Package Archive. It is like a third party application store. As a developer, my program takes certain time to get verified by APT maintainers, to push latest update to my users, i create a third party store, individual can get this store list as well and install their latest version.

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

