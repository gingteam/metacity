## What is this?
This is a patch of `metacity` so it can work well on `xfce4` (Especially version 4.16)

## Necessary packages of dependencies:

```bash
sudo apt-get install autoconf-archive automake autopoint build-essential gettext gsettings-desktop-schemas-dev libcanberra-gtk3-dev libglib2.0-dev libgtk-3-dev libgtop2-dev libice-dev libpango1.0-dev libsm-dev libstartup-notification0-dev libtool libvulkan-dev libx11-dev libxcomposite-dev libxcursor-dev libxdamage-dev libxext-dev libxfixes-dev libxinerama-dev libxpresent-dev libxrandr-dev libxrender-dev libxres-dev libxt-dev yelp-tools zenity
```

## How to install:

```bash
./autogen.sh --prefix /usr
make
sudo make install
```
## To uninstall:

```bash
sudo make uninstall
```

## How to use Metacity replace Xfwm4?

```bash
xfconf-query -c xfce4-session -p /sessions/Failsafe/Client0_Command -n -a -t string -s "metacity"
rm -rf .cache/sessions
reboot
```
