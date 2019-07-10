# The First Boot

Put the micro sd card with OctoPi IMADE3D Edition installed into your Pi and power it up (the upper switch on your JellyBOX with a Raspbery logo).

![pi-sd.png](/assets/pi-sd.jpg)
<div style="font-size:60%; font-style:italic;">image courtesy: https://projects.raspberrypi.org</div>

The first boot may take up to 8 minutes, even though it often finishes in less than 4 minutes.

The RPi will restart once or twice. Eventually, you will see a string of numbers in place of the usual "JellyBOX is ready" message on the LCD controller. This is the IP address of your OctoPrint.

## Access Your OctoPrint Through a Web Browser

**Mac:** open a web browser and go to [http://octopi.local](http://octopi.local). Alternatively, for example if you have multiple OctoPrints or for troubleshooting purposes, you can put the IP address from the LCD into browser (e.g.,`http://192.168.0.107:80`).

**Windows PC:** open a web browser (modern browsers like Chrome or Firefox are recommended) and enter the IP address you see on the LCD screen, e.g.,`http://192.168.0.107:80`.

You can also set up a nicer URL that you can bookmark and remember, `octopi.local`, but it is a bit more work. Here's the on [HowTo access your OctoPrint Via octopi.local on Windows](#how-to-set-up-octopilocal-pretty-url-on-windows) (nice address instead of the IP address. You can do it now, or at any point in the future, including never.

## The Setup Wizard

Once you get to your OctoPi (be it via octopi.local or the IP address), you will are greated with a convenient _Setup Wizard_. It is highly recommended you read the Wizard carefully: it contains information important to your privacy and security.

![2019-05-26_00-46-07.png](/assets/2019-05-26_00-46-07.jpg)

### Admin Password

> **Recommended Action:** Pick a secure `password`. This is the admin account.

The first thing to set up is the Access Control.

Use [https://xkpasswd.net/s/](https://xkpasswd.net/s/) if you need a secure password that is easy to remember. (Inspired by the famous [https://xkcd.com/936/](https://xkcd.com/936/)))

![2019-05-26_00-46-53.png](/assets/2019-05-26_00-46-53.jpg)

### Anonymous Tracking

> **Recommended Action:** Enable.

This is an open source project, and the information really helps. You can fine-tune what gets collected in the Settings and you can review how the anonymous data is treated in detail here. Long story short: OctoPrint is honest and unlike your phone and browser does not cross boundaries it shouldn't.

![tracking.png](/assets/tracking.png)

### Connectivity Check

> **Recommended Action:** Enable.

This prevents your OctoPrint from wasting time and energy.

If the `Test` fails, try to use another Host IP, as some providers (Comcast looking at you) block the `8.8.8.8` Google DNS server address. Try `1.1.1.1`, or `4.2.2.2` server (Level 3 DNS) which should fix the issue. If it still does not work, try another DNS server or any other public IP.

![2019-05-26_00-49-14.png](/assets/2019-05-26_00-49-14.jpg)

### Plugin Blacklist

> **Recommended Action:** Enable.

Contrary to the intense name, this is not a list of bad plugins; rather just a list of plugins that are not compatible with your software.

![2019-05-26_00-49-35.png](/assets/2019-05-26_00-49-35.jpg)

### Done + Safety Warning + More Info

> **Recommended Action:** Donate if you can.

Read. Maybe it's too early for you now, but once and if you find the software useful, remember it's open source and it could never exist without the support of regular folk.

![2019-05-26_00-49-44.png](/assets/2019-05-26_00-49-44.jpg)

---

## How to Set up "octopi.local" Pretty URL on Windows

**TL;DR** Try it. If it does not work, install [Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US) and try again.

There are two ways to access your OctoPrint; two addresses. One is `http://octopi.local`, and the other one is the IP address of your Raspberry Pi (e.g.,`http://192.168.0.107:80`).

The IP address will always work, but it can change (depending on your network setup). This makes it both hard to remember and hard to bookmark. Still, it's a good method if you are in a pinch or if you are traveling and connecting to foreign networks.

The octopi.local relies a system called Zeroconf (also known as Bonjour or Avahi), which is not installed on Windows by default. A few popular applications including Skype, Apple’s iTunes and Adobe Photoshop CS3 or later use it, so it still is worth a shot just trying it.

1. Open a web browser and go to [http://octopi.local](http://octopi.local).
2. Give it a good wait. If it doesn't work:
3. Install [Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US). Then the [octopi.local](http://octopi.local) address should work. You may need to restart the Pi and/or the PC.

<span></span>