<div align="center">
<img src="https://files.catbox.moe/x7b0e2.png" height="128" width="128" style="border-radius:25%">
   <h1> Semaphorin 
      <br/> 64-Bit Downgrade, Dualboot & Jailbreak Utility
   </h1>
</div>

<h4 align="center"> Uses seprmvr64 by mineek<h4>
<h6 align="center"> Supports* iOS 7.0.4-12.1.2 as well as A7-A10 devices </h6>

# IF YOUR DEVICE SUPPORTS [LEGACY-IOS-KIT](https://github.com/LukeZGD/Legacy-iOS-Kit), YOU SHOULD REALLY USE THAT OVER THIS.

# Chart of device compatibility

| iOS                    | A7 SoC  | A8/A8X SoC | A9/A9X SoC | A10 SoC | A10X SoC | A11 SoC |
|------------------------|---------|------------|------------|---------|----------|---------|
| 7.0.4                  | &#9745; | &#9744;    | &#9744;    | &#9744; | &#9744;  | &#9744; |
| 7.0.6                  | &#9745; | &#9744;    | &#9744;    | &#9744; | &#9744;  | &#9744; |
| 7.1.2                  | &#9745; | &#9744;    | &#9744;    | &#9744; | &#9744;  | &#9744; |
| 8.0b4                  | &#9745; | &#9744;    | &#9744;    | &#9744; | &#9744;  | &#9744; |
| 9.3.2                  | &#9745; | &#9745;    | &#9744;    | &#9744; | &#9744;  | &#9744; |
| 10.3.3                 | &#9745; | &#9745;    | &#9745;    | &#9745; | &#9744;  | &#9744; |
| 11.1                   | &#9745; | &#9745;    | &#9745;    | &#9745; | &#9744;  | &#9744; |
| 12.1.2                 | &#9745; | &#9745;    | &#9745;    | &#9745; | &#9744;  | &#9744; |


# Chart of feature compatibility

| iOS         | App Store | Home button  | Volume keys | Cydia     | Tweaks  | Respring | Cellular | Sideloadly | iTunes |
|-------------|-----------|--------------|-------------|-----------|---------|----------|----------|------------|--------|
| 7.0.4**     | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9744;  | &#9745;  | &#9745;    | &#9745;|
| 7.0.6**     | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9744;  | &#9745;  | &#9745;    | &#9745;|
| 7.1.2**     | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9745;  | &#9745;  | &#9745;    | &#9745;|
| 8.0b4**     | &#9744;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9745;  | &#9745;  | &#9745;    | &#9745;|
| 9.3.2**     | &#9744;   | &#9745;      | &#9745;     | &#9745;   | &#9744; | &#9745;  | &#9745;  | &#9744;    | &#9744;|
| 10.3.3      | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9745;  | &#9745;  | &#9744;    | &#9744;|
| 11.1        | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9745;  | &#9745;  | &#9744;    | &#9744;|
| 12.1.2      | &#9745;   | &#9745;      | &#9745;     | &#9745;   | &#9745; | &#9745;  | &#9745;  | &#9744;    | &#9744;|

** These versions can only be tether booted with semaphorin, dualboot is only supported when downgrading to iOS 10.3.3 or later. You will lose all your data on your device if you downgrade to any of these versions, please keep that in mind before using this tool.

## How do I use this?

This script deletes everything on your phone, including the main OS if you are not downgrading to iOS 10.3.3 or later. Make sure to backup all of your data before using this script as **anything on the device prior to running this script will be UNRECOVERABLE afterwards**. Use this script at your own risk. We are not responsible for any damages caused by you using this script.

To use this app, you need to downgrade to a supported version, and have a supported device.

`xcode-select install` to install `git` on macos

`git clone https://github.com/y08wilm/Semaphorin && cd Semaphorin`

Connect device in DFU mode

`sudo ./semaphorin.sh <the version you are downgrading to> --restore`

For example you may write `sudo ./semaphorin.sh 11.1 --restore`

The script has to backup important files from your current iOS version before you can downgrade.

When the script asks `[*] Please enter the iOS version that is currently installed on your device.`, type your current iOS version and then hit the Enter key to continue.

It should then begin the process of downgrading your device. Please follow the on screen instructions. This might take a while. Your device will reboot multiple times.

If you downgraded to iOS 10 or later, please use the jailbreak app on your home screen to begin jailbreaking your device.

## Subsequent runs after downgrade is finished

Connect device in DFU mode

`sudo ./semaphorin.sh <the version you downgraded to previously> --boot`

For example, if you downgraded to iOS 11.1, you would run `sudo ./semaphorin.sh 11.1 --boot`.

It should just boot to your requested iOS version normally.

## Requirements

macOS Catalina or later. The script only officially supports these versions.

Java 8 https://builds.openlogic.com/downloadJDK/openlogic-openjdk/8u262-b10/openlogic-openjdk-8u262-b10-mac-x64.pkg

Intel Mac. Hackintoshes with AMD CPUs will **NOT** work with this.

Stable internet connection. Please don't try using this with dial up...

At least 20GB of free space on your computer

USB Type-A port and Lightning cable. USB Type-C ports will **NOT** work with this script. If you're using a Mac that only has a USB-C port (such as 12" MacBooks, and late Intel MacBook Airs) a dongle/dock with a USB-A port should work just fine with a standard USB-A to Lightning cable.

Working iDevice: The script has to backup `apticket.der`, `sep-firmware.img4`, `Baseband`, and `keybags` from your device before you can downgrade to an older iOS version.

## Support

We now have a [Discord server](https://discord.gg/WQWDBBYJTb) where you can get help with this project.

If, for whatever reason, that invite link does not work, please contact [wilm271](https://t.me/wilm271) on Telegram.

The Discord server is strictly for Semaphorin support only. Please don't bring personal issues into our server.

## Setup.app bypass

We will not be providing any support for any method of deleting `/Applications/Setup.app` with our script.

This is only to comply with [r/jailbreak](https://www.reddit.com/r/jailbreak/) and [r/LegacyJailbreak](https://www.reddit.com/r/LegacyJailbreak/) rules and guidelines.

The script will downgrade your iOS version and jailbreak the downgraded OS very easily, but will not allow for bypassing **any** sort of Activation Lock.

We back up the `activation_records` from your main OS prior to downgrading your device, so please make sure your main OS is activated before using this tool.

## Troubleshooting

   ### Deep sleep, device won't turn on after locking it, have to reboot.
   The issue that causes deep sleep is unfortunately **unfixable**. There is, however, a workaround to this:
      
      1. Add [this repo](julioverne.github.io) to Cydia after setup
      
      2. Search for the tweak Fiona
      
      3. Install it
      
      4. Profit
      
   *Note: This does slightly affect battery life due to the way it works. You probably aren't using this script for battery life though, are you.

   ### Unsupported OS
   The script only officially works on macOS 10.15 or later due to some limitations on the developer's end. You have to install one of those versions to use the script. Please do not ask us about this.

Linux and Windows support is not planned either, do not ask about this either.

   ### Unable to connect to WiFi networks, incorrect password.
   This is caused by an issue that's *impossible* to fix. You need to connect to an open WiFi network

   You can create one using the Internet Sharing feature on macOS or [linux-wifi-hotspot](https://github.com/lakinduakash/linux-wifi-hotspot) on, you guessed it, Linux if you prefer using another computer for this. 

   Be careful when doing this since *anyone* can connect to the open network you created. We are not responsible for **any** damages caused by doing this.

   ### No apps on the Home Screen (iOS 8.0 beta 4)
   This is a weird issue with iOS 8 beta 4. The workaround is easy, however.

   After you unlock your device for the first time post setup, there will be no apps on the Home Screen. The workaround is, once you're on the Home Screen, to open the Control Center (swipe up) and press the Calculator icon. Once open, you can exit out of Calculator. This should make all icons appear.

   ### Cydia is absent (on iPads)
   iPads have uicache issues with most jailbreaking tools. To open Cydia, enter `cydia://` in Safari's address bar and press Enter.  

   ### wtfis.app is absent (on iPads)
   iPads have uicache issues with most jailbreaking tools. To open wtfis, enter `wtfis://` in Safari's address bar and press Enter.  

   ### Safari and others apps not opening (iOS 7)
   Uninstall Cydia Substrate from within Cydia, and then reboot your device using semaphorin. When the device boots back up, reinstall your tweaks, but when Cydia asks you to "restart springboard" do not hit that button! Hit the home button on your device instead, and open Safari and type `wtfis://` in Safari's address bar and press Enter. Hit "go" inside the wtfis app. This will properly respring your device. All the apps on your device should now be working properly if you follow these steps.
 
### iOS 9.3 Support

There are still some bugs left with iOS 9.3 downgrades. Due to the nature of hfs limitations on iOS 9.3-10.2.1, there is `Sandbox: hook..execve() killing %s pid %ld[UID: %d]: failure in upcall to containermanagerd for a platform app\n` errors during boot when using seprmvr64.

This is because hfs on iOS 9.3-10.2.1 requires the `/dev/disk0s1s2` partition to have a `protect` flag, otherwise sandbox complains. But the `protect` flag ensures that `/dev/disk0s1s2` is encrypted, but file system encryption is not possible because we have sep patched out. So we have to work around the issue. We patched out the sandbox eval function, but we are still getting that aforementioned error.

Most system apps can read/write to var just fine, but most if not all platformized apps cannot read/write to var and until we fix that issue we will have a lot of bugs on iOS 9.3. I made [containermanagerd64patcher](https://github.com/y08wilm/containermanagerd64patcher) which "patches" it but at the same time doesn't fix the actual issue. Most system apps crash on launch because they can not read or write to var. Oddly enough, those apps can create files just fine, just not open them.

See [here](https://files.catbox.moe/wn83g9.mp4) for a video example of why we need sandbox patches for iOS 9.

iOS 8.0 GM - 9.2.1 support will never be possible because keybags do not unlock on those versions which means nearly the entire OS is nonfunctional.

## Credits

- [PsychoTea](https://github.com/PsychoTea/) for [MeridianJB](https://github.com/PsychoTea/MeridianJB/) which we use for iOS 10.3.3 downgrades
- [coolstar](https://github.com/coolstar) for [Electra](https://www.coolstar.org/electra/) and [Chimera](https://chimera.coolstar.org/) jailbreaks which we use on iOS 11 and 12 downgrades
- [edwin170](https://github.com/edwin170) for a ton of help with fixing cell service, icloud, audio, 3d touch, gyroscope, microphone and other issues
- [johndoe123](https://twitter.com/iarchiveml) for the a7 ios 7 [downgrade guide](https://ios7.iarchive.app/downgrade/) which made this entire project possible
- [LukeZGD](https://github.com/LukeZGD/) for the updated [cydia.tar](https://github.com/LukeZGD/Legacy-iOS-Kit/raw/main/resources/jailbreak/freeze.tar) for jailbreaking older ios versions
- [TheRealClarity](https://github.com/TheRealClarity) for wtfis.app which we [repurposed](https://github.com/y08wilm/wtfis/blob/ios7/wtfis/ViewController.m#L27) to run [evasi0n7](https://ios.cfw.guide/installing-evasi0n7/) for sandbox patch on ios 7 to allow cydia substrate to not break apps
- [Nathan](https://github.com/verygenericname) for the ssh ramdisk and [iBoot64Patcher fork](https://github.com/verygenericname/iBoot64Patcher)
- [Mineek](https://github.com/mineek) for [seprmvr64](https://github.com/mineek/seprmvr64) and other patches. I want to give a very special thanks to [Mineek](https://github.com/mineek), if it werent for them this entire project would have not been possible. you are amazing and i appreciate all that you do, thank you so much
- [nyuszika7h](https://github.com/nyuszika7h) for the script to help get into DFU
- [tihmstar](https://github.com/tihmstar) for [pzb](https://github.com/tihmstar/partialZipBrowser)/original [iBoot64Patcher](https://github.com/tihmstar/iBoot64Patcher)/original [liboffsetfinder64](https://github.com/tihmstar/liboffsetfinder64)/[img4tool](https://github.com/tihmstar/img4tool)
- [Tom](https://github.com/guacaplushy) for a couple patches and bugfixes
- [xerub](https://github.com/xerub) for [img4lib](https://github.com/xerub/img4lib) and [restored_external](https://github.com/xerub/sshrd) in the ramdisk
- [Cryptic](https://github.com/Cryptiiiic) for [iBoot64Patcher](https://github.com/Cryptiiiic/iBoot64Patcher) fork, and [liboffsetfinder64](https://github.com/Cryptiiiic/liboffsetfinder64) fork
- [libimobiledevice](https://github.com/libimobiledevice) for several tools used in this project (irecovery, ideviceenterrecovery etc), and [nikias](https://github.com/nikias) for keeping it up to date
- [Nick Chan](https://github.com/asdfugil) general help with patches and iBoot payload stuff
- [Serena](https://github.com/SerenaKit) for helping with boot ramdisk.
- [planetbeing](https://github.com/planetbeing/) for dmg tool from [xpwn](https://github.com/planetbeing/xpwn)
- [exploit3dguy](https://github.com/exploit3dguy/) for [iPatcher](https://github.com/exploit3dguy/iPatcher) which is used for patching iBoot on ios 7
- [dora2-ios](https://github.com/dora2-iOS) for [iPwnder](https://iarchive.app/Download/ipwnder_macosx)
- [NyanSatan](https://github.com/NyanSatan) for [fixkeybag](https://github.com/NyanSatan/fixkeybag)
