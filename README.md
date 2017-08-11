## About linux-journey
### This is a repo to help me get back on my feet after a major format of my pc.

## Network Manager
NetworkManager is a program for providing detection and configuration for systems to automatically connect to network. NetworkManager's functionality can be useful for both wireless and wired networks. For wireless networks, NetworkManager prefers known wireless networks and has the ability to switch to the most reliable network. NetworkManager-aware applications can switch from online and offline mode. http://projects.gnome.org/NetworkManager/

### Installation
NetworkManager can be installed with the package networkmanager.While network-manager-applet works in Xfce, in order to see notifications, including error messages, nm-applet needs an implementation of the FreeDesktop.org Desktop notifications. In the xfce panel settings the applet is named "Notification Area" which might be misleading to some users especially in different translation. To enable notifications install xfce4-notifyd.

### Starting

sudo systemctl enable NetworkManager.service
sudo systemctl start NetworkManager.service

## Bible Time

BibleTime is a completely free Bible study program, built for Linux, Windows, FreeBSD and Mac OS X. 
BibleTime contains over 200 free Bible texts, commentaries, dictionaries and books, provided by the Crosswire 
Bible Society via the SWORD programming library. BibleTime is written in C++ and uses the Qt GUI toolkit. http://bibletime.info/

### Installation

sudo pacman -S bibletime

Note: Its very heavy on memory, includes additional commentaries and bibles + languages
