# How to install a GSI (and root) your Galaxy A21s
## Requirments:
- a Galaxy A21s
- a computer (preferably running Windows)
- an USB cable
- common sense

Note: This guide is tested on the SM-A217F, but it may work on other A21s varients. **If you brick your phone, I take no responsibility, but I can help you unbrick it.**

## Enabling Developer Options
To access Developer Options, go to About Device or sometimes it's called About Phone.

![About phone](https://images.samsung.com/is/image/samsung/assets/uk/support/how-do-i-turn-on-the-developer-options-menu-on-my-samsung-galaxy-device/2-uk-turn-on-developer-options.png?$ORIGIN_PNG$)

Now, press Software Information.

![Software Information](https://images.samsung.com/is/image/samsung/assets/uk/support/how-do-i-turn-on-the-developer-options-menu-on-my-samsung-galaxy-device/3-uk-turn-on-developer-options.png?$ORIGIN_PNG$)

After you opened the menu, press Build Number, 7 times. It may ask you for a PIN or whatever your security is, but simply give it to the system.

![Build number](https://images.samsung.com/is/image/samsung/assets/uk/support/how-do-i-turn-on-the-developer-options-menu-on-my-samsung-galaxy-device/4-uk-turn-on-developer-options.png?$ORIGIN_PNG$)

Now you should have Developer Options.

### Enabling OEM unlocking

Now, go to Developer Options, and enable OEM unlocking. Now your phone is able to unlock the bootloader.

![Unlocking Bootloader](https://images.tenorshare.com/topics/unlock-android/oem-unlocking.jpg?w=287&h=510)

# Unlocking the bootloader

To unlock the bootloader, restart your phone, and hold the **Volume Up**+**Volume Down** keys until the phone boots into the Unlock Bootloader screen. **Reminder: This will wipe all data so be careful and backup all data!!**

[<img src="https://i.redd.it/041b0t6unoua1.png" width="250"/>](https://i.redd.it/041b0t6unoua1.png)

Now this screen should appear:

[<img src="https://i.ibb.co/V2GZh7v/device-lock.jpg" width="350"/>](https://i.ibb.co/V2GZh7v/device-lock.jpg)

### Remember that this will wipe all data!!!
Now press Volume Up and you're done.
**Congratulations you unlocked your bootloader!** Time for the next step.

# Patching image with Magisk

**Note: Use Magisk version 26.3 to patch image, if not it will bootloop.**

First you need to find your CSC code, I recommend [this article](https://www.cocosenor.com/articles/android/how-to-check-your-samsung-phone-model-or-csc-region-code.html) to find it out. After finding out your CSC code (e.x SEE). 
Now, I personally use SamFW to download the firmware since it is the fastest, but you can use other websites. Heres the firmware download for the [A217F](https://samfw.com/firmware/SM-A217F). Now download the firmware using your CSC code. After is it done, turn on your phone and set it up. Download Magisk 26.3 from the offical Magisk github right [here](https://github.com/topjohnwu/Magisk/releases/tag/v26.3) and install the APK file. Now extract the zip file, and copy the file that starts with AP to your phones Internal Storage. Once it is done, open Magisk, and press Install where it says App, press the
