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

To unlock the bootloader, restart your phone, and hold the **Volume Up**+**Volume Down** keys until the phone boots into the Unlock Bootloader screen. Hold the volume up key.  **Reminder: This will wipe all data so be careful and backup all data!!**

[<img src="https://i.redd.it/041b0t6unoua1.png" width="250"/>](https://i.redd.it/041b0t6unoua1.png)

Now this screen should appear:

[<img src="https://i.ibb.co/V2GZh7v/device-lock.jpg" width="350"/>](https://i.ibb.co/V2GZh7v/device-lock.jpg)

### Remember that this will wipe all data!!!
Now press Volume Up and you're done.
**Congratulations you unlocked your bootloader!** Time for the next step.

# Patching image with Magisk

**Note: Use Magisk version 26.3 to patch image, if not it will bootloop.**

First you need to find your CSC code, I recommend [this article](https://www.cocosenor.com/articles/android/how-to-check-your-samsung-phone-model-or-csc-region-code.html) to find it out. After finding out your CSC code (e.x SEE). 
Now, I personally use SamFW to download the firmware since it is the fastest, but you can use other websites.

Heres the firmware download for the [A217F](https://samfw.com/firmware/SM-A217F). Now download the firmware using your CSC code. After is it done, turn on your phone and set it up.

Download Magisk 26.3 from the offical Magisk github right [here](https://github.com/topjohnwu/Magisk/releases/tag/v26.3) and install the APK file. Now extract the firmware zip file, and copy the file that starts with AP to your phones Internal Storage. 

Once it is done, open Magisk, and press Install where it says "Magisk". Now press "Select and Patch file" and select your AP file. It will take a minute but your patched firmware will be done. It should be called something like "magisk_patched_26003.tar". Now copy the file (its usually in the Downloads folder in your phone) to your computer.

# Flashing the boot image

Okay, to flash the Magisk image, download [Odin](https://xdaforums.com/t/patched-odin-3-13-1.3762572/). I personally use **Odin3_v3.13.3.zip** version. Now setup your phone after you unlocked the bootloader. Make sure to connect it to the internet. After setting up the phone, shutdown the phone. Connect it to a computer and turn it on while holding the **Volume Up+ Volume Down** keys. It should boot to the download mode.

[<img src="https://i.redd.it/041b0t6unoua1.png" width="250"/>](https://i.redd.it/041b0t6unoua1.png)

Now press Volume Up.

(placeholder image here)

You should be in Download Mode. In the right top corner, check if the KG State says "Checking". If it says checking, you can install unoffical firmware. If it says "Prenormal". Connect your phone to the internet and change the date 7 days into the future. And redo this entire process if that happens. Now open Odin.

(placeholder image here for future me)

Now plug in your phone. If your phone is detected by Odin, download the Samsung USB drivers. If it still doesn't detect, do this. Close Odin. Unplug the USB. Now replug the USB cable and open Odin. It should detect. Press "AP" and select the "magisk_patched_26003.tar". Now press start. Your phone should be flashing the modified firmware. Congratulations, you rooted your phone.

# Installing TWRP recovery

Now, once the flashing is done, wait for your phone to turn on. After it turns on, setup the phone as normal and **connect it to the internet**. Now that it is done setting up. Let the phone be connected to the internet for around 15-20 minutes. After waiting, boot your phone to Download Mode (as explained above). Now download TWRP from [here](https://objects.githubusercontent.com/github-production-release-asset-2e65be/520554716/63f1822a-2cd6-4ddc-8789-2882281c8542?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20240726%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240726T125756Z&X-Amz-Expires=300&X-Amz-Signature=dc35bc29bf7638aa104f044193320bb325d84879d4b4033d173af31069cbf1c5&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=520554716&response-content-disposition=attachment%3B%20filename%3Drecovery.tar&response-content-type=application%2Foctet-stream) to get the recovery.tar file. Select it in AP. Let it flash. After its done, hold the **Volume Up + Power Button**. You should be in TWRP.

# Decrypting and formatting storage

In TWRP, go to "Settings" and press "Terminal". In terminal, write "multidisabler". This will disable encryption. After it's done, go to Wipe, Format Data, and format the data. Now reboot phone to recovery again.

# Repartitioning
