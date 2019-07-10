# JellyBOX Marlin Firmware

!> Remote live Z adjustment does NOT work with the current latest JellyBOX Firmware. Upgrade to our beta firmware `jb-3.0-dev6` to fix this issue and gain many new superpowers.

?> The good news is, you **upgrade your firmware using OctoPrint**, remotely and with little effort!

[>> Link to the Release Notes](https://github.com/IMADE3D/Marlin/releases/tag/jb-3.0-dev6)

## How to Upgrade JellyBOX Firmware using OctoPrint

!> This process will reset your settings. Note down anything you may want to restore later like E steps/mm or Z probe offset.

### Copy the Upgrade URL

First, scroll down to the [firmware upgrade links](#firmware-upgrade-links), locate your JellyBOX variant, and copy the whole Upgrade Link URL.

![upgrade_1.copy.jpg](/assets/upgrade_1.copy.jpg)

### Head over to OctoPrint.

Go to Setting, and then scroll down in the left sidebar to find **Firmware Updater**.
**Don't yet hit** the Flash button, but instead go press the **Settings button (2)**.

![upgrade_2enter.jpg](/assets/upgrade_2enter.jpg)


### Verify Post-Flash Settings

Click on the `Pre-Flash and Post-Flash Settings`, and then verify that `Post-flash gcode` is enabled and has `M502` and `M500` at the end. Save.

?> This code will perform the Factory Reset, which truly needs to be done. Too much is new in this firmware.

![upgrade_2.verify.jpg](/assets/upgrade_2.verify.jpg)

### Paste and Flash from URL

Back in the Firmware Updater, it's time to (1) paste the Upgrade URL you copied in the first step. (2) Wait until this button becomes darker blue (the file needs to load) and click `Flash from URL.`

![upgrade_3paste.jpg](/assets/upgrade_3paste.jpg)

Wait.

![upgrade_4.flash.jpg](/assets/upgrade_4.flash.jpg)

### After wait comes success!

You can restore any settings you noted down, kick back, and go back to printing and exploring NEW FEATURES of your new firmware.

![upgrade_5.success.jpg](/assets/upgrade_5.success.jpg)

## Firmware Upgrade Links

These are designed to be used with the Firmware Updater in OctoPrint, but you can also download the file and flash the firmware using Cura, Hex Uploader, or XLoader. Do what makes you happy.


| JellyBOX Model and Variant                  | jb-3.0-dev6 Firmware Upgrade Link                                                                                                  |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| jellybox 2 cold_bed                               | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_2_cold_bed.hex`                               |
| jellybox 2 heated_bed                             | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_2_heated_bed.hex`                             |
| jellybox original cold_bed one_fan green_probe    | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_cold_bed_one_fan_green_probe.hex`    |
| jellybox original cold_bed one_fan yellow_probe   | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_cold_bed_one_fan_yellow_probe.hex`   |
| jellybox original cold_bed two_fans               | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_cold_bed_two_fans.hex`               |
| jellybox original heated_bed one_fan green_probe  | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_heated_bed_one_fan_green_probe.hex`  |
| jellybox original heated_bed one_fan yellow_probe | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_heated_bed_one_fan_yellow_probe.hex` |
| jellybox original heated_bed two_fans             | `https://github.com/IMADE3D/Marlin/releases/download/jb-3.0-dev6/jbm-3.0-dev6-jellybox_original_heated_bed_two_fans.hex`             |

<span></span>