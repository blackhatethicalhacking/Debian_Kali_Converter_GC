# Debian_Kali_Converter_GC

![alt text](https://pbs.twimg.com/profile_images/1384538705797554177/o0BURm0O_400x400.png)

**Convert Debian 10 to Kali Linux on Google Cloud or Any Debian**

**After you create an account on Google Cloud, and create your VPS using Debian 10, follow the below guide to convert your Debian to Kali Linux Latest Version:**

# Convert Debian to Kali:

**Step 1:**

`apt-get update -y && apt-get full-upgrade -y && apt-get dist-upgrade -y && apt autoremove -y && apt autoclean`

**Step 2:**

`apt-get install wget gnupg dirmngr`

**Step 3:**

`wget -q -O - https://archive.kali.org/archive-key.asc | gpg --import`

**Step 4:**

`echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" >> /etc/apt/sources.list`
`gpg -a --export ED444FF07D8D0BF6 | sudo apt-key add -`

**Step 5:**

`apt-get update -y && apt-get full-upgrade -y && apt-get dist-upgrade -y && apt autoremove -y && apt autoclean`

**Step 6:**

`apt-get install kali-linux-default or core, everything and for the biggest image large`


**Script to update:**

`touch kali_update.sh`

`echo "apt-get update -y && apt-get full-upgrade -y && apt-get dist-upgrade -y && apt autoremove -y && apt autoclean" > kali_update.sh`

`chmod +x kali_update.sh`

**Enable Root Login SSH:**

/etc/ssh/sshd_config

PermitRootLogin yes
PasswordAuthentication yes

**Some Tools:**

**Install PIP**

`apt install python3-pip`

**Install Figlet / lolcat / Motd Change**

`apt-get install figlet`

`pip install lolcat`

`apt-get install neofetch`

Figlet /etc/motd

**Enable Remote GUI:**

Install Gui:

**First Create a Firewall Rule for Port 5900 and 5901 in Google Cloud on 0.0.0.0/0**

`apt-get install xfce4 xfce4-goodies -y`

Configure:

`nano ~/.vnc/xstartup`

Put:

#!/bin/bash
xrdb $HOME/.Xresources
startxfce4 &

`chmod +x ~/.vnc/xstartup`


First Try with tightvncserver 

`apt-get install tightvncserver`

Then try with X11vnc if you need.


`apt-get install x11vnc novnc net-tools`

Set PW:
`x11vnc -storepasswd`

Check:
`ps wwwaux | grep auth`

**Connect with RealVNC**

**For Full Episode check it our on our Twitch Channel: twitch.tv/bheh1337**

**Black Hat Ethical Hacking All Rights Reserved 2021 - blackhatethicalhacking.com**
