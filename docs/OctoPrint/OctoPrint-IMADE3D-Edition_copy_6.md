# OctoPrint IMADE3D Edition

## About

- **[OctoPrint](http://octoprint.org)** is a snappy and open source web interface for 3D printers created & maintained by Gina Häußge (@foosel). **[OctoPi](https://github.com/guysoft/OctoPi)** is an easy to use OctoPrint image for RaspberryPi computers created and maintained by Guy Sheffer (@guysoft).
- IMADE3D provides an OctoPi image conveniently pre- configured and optimized for JellyBOXes, but we are not maintaintainers or developers of either OctoPrint or OctoPi.
    - OctoPrint homepage: [octoprint.org](https://octoprint.org/)
    - OctoPi homepage: [github.com/guysoft/OctoPi](https://github.com/guysoft/OctoPi)

## Help?!

- For general issues, [please refer to the official OctoPrint FAQ](https://community.octoprint.org/c/support/faq).
- For connectivity issues please contact our support or post on our friendly [forum.imade3d.com](http://forum.imade3d.com).
- Bug reports belong on github: [github.com/foosel/OctoPrint/issues](https://github.com/foosel/OctoPrint/issues)

## Set Up

### **Hardware**

*(This section is underdeveloped, but enough to serve as a reminder for power users.)*

- **MicroSD card**, 4GB or more, ideally **class 10 or higher** (as in speed. A 16GB or 32GB class 10 card is probably the best value as of 2019. According to [Jeff Geerling's SD card testing](https://www.jeffgeerling.com/blogs/jeff-geerling/raspberry-pi-microsd-card), *Samsung 32GB EVO Plus* card will get you the best performance.)
- **Raspberry Pi 3B+**. Raspberry Pi 2 works, but it's just slower all around, and especially networking-wise. Pi 3B also works, but... just get the 3B+. It's better.
- 12V → 5V step down convertor and a secondary power switch.
- USB cable type B (the cable that came with your JellyBOX)

### **Software: Prepare the SD Card**

Warning: do NOT load the SD card into your Pi right after burning. You first need to set your admin password, and that can only be done once - on the first boot. 

1. Download the latest OctoPi IMADE3D Edition image for your Raspberry Pi from [http://imade3d.com/resources/OctoPi-IE](http://imade3d.com/resources/OctoPi-IE).
You don't have to unzip the file, but if you do, you'll see there's a single `.img` file inside.

2. Download and install **Balena Etcher** from [https://etcher.io](https://etcher.io/)

3. Burn the image onto your SD card with Etcher.

### **Software:  Configuration**

1. Re-insert the SD card into your computer if it got ejected and you should see a 'boot' SD card partition.
(Etcher by default ejects the card after the burn, that's why you have to re-insert the card.)
2. **Option One: Connect the Raspberry Pi to your network with a LAN cable.** If that's an option, it's always preferable. It's easier, faster, and more robust than WiFi. Especially in school environment, LAN is preferable. 
3. **Option Two: Set up the WiFi network.** 
    - Find `octopi-wpa-supplicant.txt` file and open it with a plain text editor (Visual Studio Code, Atom, Sublime Text, Notepad ++).
    - *Do NOT use TextEdit (Mac) or MS Word, Notepad, WordPad (PC)... none of that. These editors are known to mangle the file, making the configuration fail.*
    - Find this block of code

            ## WPA/WPA2 secured
            #network={
            #  ssid="put SSID here"
            #  psk="put password here"
            #}

    - Delete the last four  `# symbols` and put it your own WiFi network name (aka SSID) and password key (aka psk). For example:

            ## WPA/WPA2 secured
            network={
              ssid="Winternet is coming"
              psk="the-North-remembers"
            }

4. **Change the Raspberry Pi admin password!**
    - Find `octopi-password.txt` file and open it with a text editor (Visual Studio Code, Atom, Sublime Text, Notepad ++). Replace the default `raspberry` password with **your own secure password**.

        ![](Untitled-ab9ce31d-a5c1-4769-b9c8-c14e7aeb4fec.png)

        ![](Untitled-397e11d4-8b1b-4f2c-8d87-6f245be14bf5.png)

    - We recommend [https://xkpasswd.net/s/](https://xkpasswd.net/s/) if you need a secure password that is easy to remember. (Inspired by the famous [https://xkcd.com/936/](https://xkcd.com/936/))
    - Keep this password safe. It gives anyone complete control over the Raspberry Pi and a person with malicious intent could cause real damage (even fire).

## First Boot

1. **Put the micro sd card into your Pi and power it up** (the upper switch on your JellyBOX). The first boot may take up to 5 minutes. 
2. *Mac:* open a web browser and go to [http://octopi.local](http://octopi.local). Follow the first time set up Wizard.
3. *Windows PC:*  open a web browser and **go to [http://octopi.local](http://octopi.local). If even after five full minutes you refresh the page (!) and see nothing, then read on. 
    - Install [Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US). Then the [octopi.local](http://octopi.local) address should work (if the Octoprint works). You may need to restart the Pi and/or the PC.
    - What's going on here?

        Windows doesn’t have so called `Zeroconf (<-Bonjour)`, which is what makes the nice `[octopi.local](http://octopi.local)` address tick, but a few popular applications including Skype, Apple’s iTunes and Adobe Photoshop CS3 or later use it, so it was worth a shot just trying it.

        Here, by installing  [Bonjour Print Services for Windows](https://support.apple.com/kb/DL999?locale=en_US), we are making sure Bonjour is available. 

        It's still possible to access the Octoprint without Bonjour, but this is the easiest way and we feel it's way worth the hassle. 

    - **Alternatively**, you can figure out what the IP address of the Raspberry Pi is and then type it into the url box instead of [octopi.local](http://octopi.local).We recommend the open source [Angry IP Scanner.](https://angryip.org/)

4. Eventually, you should arrive at the Welcome Screen Wizard. Go through to set up the essentials - especially the Access Control administrator user name and password. 

## Quick Start Guide

*This section is under development. In the meantime, here's some external resources:*

[Setting up OctoPrint on the Raspberry Pi](https://pimylifeup.com/raspberry-pi-octoprint/)

- Skip to the Getting Started with OctoPrint section
- This one is images + text kind of guide on basic set up and usage

[Guides](https://community.octoprint.org/c/support/guides)

- It's the Guides section on the official OctoPrint forum!

[3D Printing - Octoprint Series - YouTube](https://www.youtube.com/playlist?list=PLGc0ilxmLZs8UwoQMdpOkYF4gZMMu_Qro)

- This one is lengthy. Most of the things you'll not need, but you'll also learn a lot of potentially useful things.

## Advanced

Octoprint has a thriving plugin ecosystem that can do anything from modifying the UI to flashing slicing stl files. 

You can browse plugins at [https://plugins.octoprint.org/plugins/](https://plugins.octoprint.org/plugins/) and install them through 

### Additional JellyBOX Cura for OctoPrint Profiles

OctoPi IE comes with Cura 15 (legacy) slicer, and with one simple coarse PLA profile. 

Here are more profiles you can use: 

Warning: these are not the same profiles as Cura 3 uses.

[IMADE3D/Slicing-Profiles](https://github.com/IMADE3D/Slicing-Profiles/tree/master/Old%20Cura%2015%20-%20Legacy)

### These plugins come pre-installed:

**BetterHeaterTimeout**

- Turns off the heaters after a period of inactivity. For those of us who forget printers heated up.

**GcodeEditor**

- Edit uploaded gcode. Useful for gcode preview and for occasional temperature hacking
- [https://plugins.octoprint.org/plugins/gcodebar/](https://plugins.octoprint.org/plugins/gcodebar/)

**TerminalCommands**

- Allows adding custom gcode macros

**Autoscroll**

- Improves the terminal UX

**Autoselect**

- Less clicking

**FirmwareUpdater**

- Flash Marlin firmware wirelessly

**FullScreen**

- Double click the camera to fullscreen

**SimpleEmergencyStop**

- Adds an emergency stop button to the navbar. Use in emergency.

**Tempsgraph**

- Supercharges the temperature graph. Zoom in, out... and export to csv(!)

**ipOnConnect**

- Shows the ip address of your JellyBOX when connected to OctoPrint

### These plugins may also be your cup of tea:

**Full-featured Slicer**

- If you actually want to use Cura on your Pi, you should really install the Slicer UI.
- This plugin will likely become pre-installed in the next Octopi IE release.
- [https://plugins.octoprint.org/plugins/slicer/](https://plugins.octoprint.org/plugins/slicer/)

**TouchUI**

- Useful when you are accessing OctoPrint via a mobile device or touchscreen.

**Gcodebar**

- Send gcode from the home tab. Yay.

**Octolapse**

- Seriously awesome and involved timelapses

**AstroPrint**

- Access Astroprint cloud files

**GitFiles**

- Print files from your repo!

**NavbarTemp**

- Always display temperature on the navbar

**Yamlpatcher**

- Only if you're a developer. Useless otherwise.
- [https://github.com/OctoPrint/OctoPrint-Yamlpatcher#patch-format](https://github.com/OctoPrint/OctoPrint-Yamlpatcher#patch-format)

**RequestSpinner**

- A bit of UX
- This plugin will likely become pre-installed in the next Octopi IE release.

**Filemanager**

- Manage those files

**UserWhitelist**

- If you're in an organization, this simple plugin helps  keeping track of who is running prints