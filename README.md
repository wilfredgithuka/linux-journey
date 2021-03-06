# ArchLinux Journey

A repo to help me get back on my feet after a major format of my pc.

## Video
mpv is a media player based on MPlayer and MPlayer2. It supports a wide variety of video file formats, audio and video codecs, and subtitle types. mpv comes with a minimal GUI called On Screen Controller (OSC), that appears when moving the mouse.

### Installation

sudo pacman -S mpv

## Kdenlive Video Editor
Kdenlive is an acronym for KDE Non-Linear Video Editor. It is primarily aimed at the GNU/Linux platform but also works on BSD and MacOS. It is currently being ported to Windows as a GSOC project. Non-linear video editing is much more powerful than beginners’ (linear) editors, hence it requires a bit more organization before starting. However, it is not reserved to specialists and can be used for small personal projects.

### Installation

* sudo pacman -Syy
* sudo pacman -S kdenlive frei0r-plugins dvdauthor vlc cdrtools

## Sound
PulseAudio serves as a proxy to sound applications using existing kernel sound components like ALSA or OSS. Since ALSA is included in Arch Linux by default, the most common deployment scenarios include PulseAudio with ALSA.

### Installation

* sudo pacman -S pulseaduio paprefs pavucontrol
* Restart computer

## Audacity
A program that lets you manipulate digital audio waveforms

### Installation

sudo pacman -S audacity

## Network Manager
NetworkManager is a program for providing detection and configuration for systems to automatically connect to network. NetworkManager's functionality can be useful for both wireless and wired networks. For wireless networks, NetworkManager prefers known wireless networks and has the ability to switch to the most reliable network. NetworkManager-aware applications can switch from online and offline mode. http://projects.gnome.org/NetworkManager/

### Installation
NetworkManager can be installed with the package networkmanager.While network-manager-applet works in Xfce, in order to see notifications, including error messages, nm-applet needs an implementation of the FreeDesktop.org Desktop notifications. In the xfce panel settings the applet is named "Notification Area" which might be misleading to some users especially in different translation. To enable notifications install xfce4-notifyd.

### Starting

sudo systemctl enable NetworkManager.service

sudo systemctl start NetworkManager.service

### Creating a wifi Access Point
Sometimes times may need to create a wifi network from your pc wifi card. This is how its done using create_ap. A software access point is used when you want your computer to act as a Wi-Fi access point for the local network. It saves you the trouble of getting a separate wireless router.

The create_ap script combines hostapd, dnsmasq and iptables to create a Bridged/NATed Access Point (available in create_ap or create_ap-gitAUR). After downloading create_ap, run the following script:

* sudo create_ap -n wifiunterfacename ssid password

Replace with approprate details above with your device's name.

## Chromium
Chromium is an open-source graphical web browser from "The Chromium Project", based on the Blink rendering engine.

### Installation

sudo pacman -S chromium

### Notes

Its 55MB and takes 208MB when installed

## Bible Time

BibleTime is a completely free Bible study program, built for Linux, Windows, FreeBSD and Mac OS X. 
BibleTime contains over 200 free Bible texts, commentaries, dictionaries and books, provided by the Crosswire 
Bible Society via the SWORD programming library. BibleTime is written in C++ and uses the Qt GUI toolkit. http://bibletime.info/

### Installation

sudo pacman -S bibletime

Note: Its very heavy on memory, includes additional commentaries and bibles + languages

## Mods

### The I Love Candy Pacman Mod

[Pacman](https://wiki.archlinux.org/index.php/pacman ) is the official package manager for Archlinux. Sometimes its 
boring watching the Hashes which are used to show progress when Pacman is downloading/working. This kind of user interface has a new mod that shows a capital C eating 
small things during the progress.

#### Modify the Pacman config file using your favorite editor.

sudo nano /etc/pacman.conf

Go down to Misc Options and add the word ILoveCandy to the end of the list.

#### Misc options
#UseSyslog
#Color
#TotalDownload
CheckSpace
#VerbosePkgLists
ILoveCandy

Save the changes and it will take effect immediately.
