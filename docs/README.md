This site is very much both under construction and an experiment.

## adfadfa


### adfad

## adfadf

Test:

First Run

## The First Boot

Put the micro sd card into your Pi and power it up (the upper switch on your JellyBOX with a Raspbery logo).

The first boot may take up to 8 minutes, even though it often finishes in less than 4 minutes.

The RPi will restart once or twice. Eventually, you will see a string of numbers in place of the usual "JellyBOX is ready" message on the LCD controller. This is the IP address of your OctoPrint.

## Load Your OctoPrint in a Web Browser

**Mac:** open a web browser and go to [http://octopi.local](<http://octopi.local>). Alternatively, for example if you have multiple OctoPrints or for troubleshooting purposes, you can put the IP address from the LCD into browser (e.g.,`http://192.168.0.107:80`).

**Windows PC:** open a web browser (modern browsers like Chrome or Firefox are recommended) and enter the IP address you see on the LCD screen, e.g.,`http://192.168.0.107:80`.

Here's a guide on [Windows: HowTo access your OctoPrint Via octopi.local](Windows - HowTo access your OctoPrint Via octopi.local) (nice address instead of the IP address. You can do that now, or later.

## The First Run Setup Wizard

Once you get to your OctoPi (be it via octopi.local or the IP address), you will are greated with a convenient _Setup Wizard_. It is highly recommended you read the Wizard carefully: it contains information important to your privacy and security.
![2019-05-26_00-46-07.png](/Users/filipgoc/Documents/OneDrive/imade3d-onedrive/GITHUB/GitLab/imade3d-docs/assets/2019-05-26_00-46-07.png)
### Admin Password
The first thing to set up is the Access Control.
- _Recommended Action:_ Pick a secure `password`. This is the admin account.
- Use [https://xkpasswd.net/s/](https://xkpasswd.net/s/) if you need a secure password that is easy to remember. (Inspired by the famous [https://xkcd.com/936/](https://xkcd.com/936/)))
![2019-05-26_00-46-53.png](/Users/filipgoc/Documents/OneDrive/imade3d-onedrive/GITHUB/GitLab/imade3d-docs/assets/2019-05-26_00-46-53.png)
### Anonymous Tracking
This is an open source project, and the information really helps. You can fine-tune what gets collected in the Settings and you can review how the anonymous data is treated in detail here. Long story short: OctoPrint is honest and unlike your phone and browser does not cross boundaries it shouldn't.
- _Recommended Action:_ Enable.