# Advanced Topics

## OctoPrint Plugins

Octoprint has a thriving plugin ecosystem and people make plugins for anything from modifying the UI to controlling smart plugs.

You can browse for plugins at [https://plugins.octoprint.org/plugins/](https://plugins.octoprint.org/plugins/) and them install them through the integrated Plugin Manager.

(Scroll down to see the list of pre-installed plugins.)

### Plugins Pre-Installed in the OctoPi IMADE3 EDITION:

<details>
<summary>Pre-Installed Plugins</summary>

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

**RequestSpinner**
- A bit of UX
- This plugin will likely become pre-installed in the next Octopi IE release.

**Filemanager**
- Manage those files

**Full-featured Slicer**
- If you actually want to use Cura on your Pi, you should really install the Slicer UI.
- This plugin will likely become pre-installed in the next Octopi IE release.
- [https://plugins.octoprint.org/plugins/slicer/](https://plugins.octoprint.org/plugins/slicer/)

**Autoselect Plugin**
- Automatically selects the gcode file that's just been uploaded to be printed (if there is no print job active.) Not only it saves clicks, but prevents you from printing an old file by mistake.

**PortLister**
- Improves the UX of automatically re-connecting to the machine

**RequestSpinner**
- A little graphical element that let's you when OctoPrint is taking long to do something, but it's still working.

**Tab Order**
 - Allows for customization of the order and the looks of the tabs. Fancy icons here we go.

**EEPROM Marlin Editor**
- Enables you to view, edit and save JellyBOX settings in the persisten `EEPROM` memory. Things like Z probe offset, bed leveling mesh, or E-steps/mm.

</details>

### These plugins may also be your cup of tea:

> This list is NOT exhaustive. Just to get you started.

<details>
<summary>More Plugins We Like</summary>

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

**UserWhitelist**
- If you're in an organization, this simple plugin helps  keeping track of who is running prints

**Navbar Temperature Plugin**
- A neat plugin that always shows you the current/ target temperatures as well as the RPi core temp. One of the first plugins Filip installs; even though it does make the UI cluttered.
- ![navbar.png](assets/navbar.png)

**M117PopUp**
- A neat little plugin that shows the message otherwise only seen on the LCD. It does _not_ work for M0 messages though :-(

</details>

### How To Install Additional Plugins

There's a nice plugin manager in the settings. Use it :-)

![2019-05-26_00-50-33.png](/assets/2019-05-26_00-50-33.jpg)

![2019-05-26_00-51-12.png](/assets/2019-05-26_00-51-12.png)
