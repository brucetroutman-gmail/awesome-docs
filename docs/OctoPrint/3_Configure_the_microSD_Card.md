# Configure the microSD Card
## Insert into a Computer

Insert the microSD card into your computer and you should see a 'boot' SD card partition.

## Change the Raspberry Pi Admin Password!

 Find `octopi-password.txt` file and open it with a text editor (Visual Studio Code, Atom, Sublime Text, Notepad ++). Replace the default `raspberry` password with **your own secure password**.

![](/assets/Untitled-ab9ce31d-a5c1-4769-b9c8-c14e7aeb4fec.png)

![](/assets/Untitled-397e11d4-8b1b-4f2c-8d87-6f245be14bf5.png)

- We recommend [https://xkpasswd.net/s/](https://xkpasswd.net/s/) if you need a secure password that is easy to remember. (Inspired by the famous [https://xkcd.com/936/](https://xkcd.com/936/))
- Keep this password safe. It gives anyone complete control over the Raspberry Pi and a person with malicious intent could cause real damage (even fire).

## Configure Networking (Internet)

### Option One: Wired (LAN/ Ethernet)

?> Wired connection is always preferable if you can get it. It's easier, faster, and more robust than WiFi; especially in a school environment.

Connect the Raspberry Pi to your network with an ethernet cable. You're done :-)

### Option Two: Set up the WiFi network.

!> Do NOT use TextEdit (Mac) or MS Word, Notepad, WordPad (PC)... none of that. These editors are known to mangle the file, making the configuration fail.

Find `octopi-wpa-supplicant.txt` file and open it with a plain text editor (Visual Studio Code, Atom, Sublime Text, Notepad ++).

1. Find this block of code

       ## WPA/WPA2 secured
       #network={
       #  ssid="put SSID here"
       #  psk="put password here"
       #}

2. Put it your own WiFi network name (aka SSID) and password key (aka psk).
3. Delete the `#` symbols in front of the four affected lines. Otherwise it will _not_ work.

       ## WPA/WPA2 secured
       network={
           ssid="Winternet is coming"
           psk="the-North-remembers"
       }

### Change the Country Code

Scroll down and find this block of code, and make sure your country is the one _without_ `#` in front of it.

For example, in the USA, this is what it should look like:

    # Uncomment the country your Pi is in to activate Wifi in RaspberryPi 3 B+ and above
    # For full list see: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
    #country=GB # United Kingdom
    #country=CA # Canada
    #country=DE # Germany
    #country=FR # France
    country=US # United States
