

# Frequently Asked Questions #

This page should contain answer for most questions asked by non developers, subjects too many times asked in XDA thread.

## In which wave models badadroids work? Is xxx model supported / going to be supported? ##
May 2013: just S8500 (Wave I) and S8530 (Wave II), similar hardware/software (Qualcomm)

Others wave models (
S5250 Wave 525,
S5330 Wave 533,
S5380 Wave Y,
S5750 Wave 575
S7230 Wave 723,
S7250 Wave M,
S8600 Wave III ) have very different hardware (Broadcomm), different bootloader ... maybe they need a whole new port project.

Some related XDA threads  [723](http://forum.xda-developers.com/showthread.php?t=1144809), [525](http://forum.xda-developers.com/showthread.php?t=1253913), [525 FOTA bootloader ](http://forum.xda-developers.com/showthread.php?t=2240466). The most serious attempt for other wave models is done (january 2013) for S8600 by oleg\_k, first developer of badadroid: [Android port for S8600 XDA thread](http://forum.xda-developers.com/showthread.php?t=2116846)

## Does xxx work or not ? ##
Hardware: look at ProjectStatus.

Google play: look in this FAQ

### Do Microphone and audio work in calls? ###
Yes! (september 2013)

XDA related posts:

http://forum.xda-developers.com/showthread.php?p=44886529

http://forum.xda-developers.com/showthread.php?p=45682082

### Are data (GPRS, 3G...) connection  working? ###
Yes! (october 2013)

XDA related post:

http://forum.xda-developers.com/showpost.php?p=46684373&postcount=947

### Does GPS work? ###
No.

XDA related post:

http://forum.xda-developers.com/showpost.php?p=46684373&postcount=947


## How do I install badadroid? ##
Look for "FIRST INSTALLATION" in http://forum.xda-developers.com/showthread.php?t=1851818

## How do I report a bug / take logs / save logcat ? ##
Look for "BUG REPORTS" in http://forum.xda-developers.com/showthread.php?t=1851818

There is another similar way, using adb shell
Run from command line (windows, linux) "adb logcat -b system -b radio -b events -b main  > logcat.log", and you will have logcat.log file in your local file system in your computer.

Tips to run "adb":
  * you have to install android SDK, which includes adb utility.
  * you have to enabe in your wave checkbox at Settings > Developer options > Android debugging
  * of course, you have to have your wave plugged to your PC , if not, you receive message "error: device not found"

## How do I install Google Play? ##
Start CWM Recovery and install http://goo.im/gapps/gapps-jb-20121011-signed.zip
(It has to be this version for Cyanogenmod 10.1, check "Use this table to figure out which package you need!" table in http://goo.im/gapps)

Google Apps (Gapps) is not included by default in this ROM by licencing reasons.

## Why message "Unfortunately, Android keyboard (AOSP) has stopped" ? ##
Wrong gapss version.

## Badadroid is stuck in animation with rotating circle where Cyanogenmod is written in ##
It happens if you don't comply with installation requirements. Enter Bada Settings->General->Memory and make sure you have at least:
  * 370MB of free "System" memory
  * 150MB of free "User" memory
  * 400MB of free "Applications" memory

Sometimes it seems installation requierements are ok, but the system partition is corrupted somehow
Solution: make a clean installation of bada: full flash

Related XDA posts:

http://forum.xda-developers.com/showthread.php?p=39859136#post39859136

http://forum.xda-developers.com/showpost.php?p=49510498&postcount=71

## Badadroid is going to work with xxx custom Bada firmware ? ##
Yes, you just have to flash the right bootfiles and FOTA, and comply with Bada Badadroid requirements (see above)

## Do Volk204's official kernel and ROM support other custom ROMs and kernels? ##
No.

Related XDA posts:

http://forum.xda-developers.com/showpost.php?p=47208240&postcount=1369

## Do Volk204's official kernel and ROM support "bigmem / 320 MB " kernel? ##
No.

First, total RAM ammount in Wave I and II is 384 MB.

Bigmem / 320 MB kernel needs a modified kernel without some features (camera, tv out, video playback...), somehow optimized for high resource demanding games.
Some developpers have done such kernel / ROM, but not commpliant with GPL license, and threads are closed in XDA.

Related XDA posts:

http://forum.xda-developers.com/showpost.php?p=48202541&postcount=104

http://forum.xda-developers.com/showpost.php?p=48212213&postcount=111

http://forum.xda-developers.com/showthread.php?p=46855920#post46855920


## How do I make badadroid use external SD as main storage / install apps in external SD Card? ##
Install swap\_SD.zip or look for persist.sys.vold.switchexternal flag setting solution.

Related XDA posts: http://forum.xda-developers.com/showthread.php?t=1851818&page=107

Note: CM 10.1

Partitions are already swapped in this ROM.
No need to flash Swap SD.zip anymore

http://forum.xda-developers.com/showpost.php?p=44881813&postcount=171

## How do I change phone ID ? ##
Some apps do not work if model is GT-S8500 or GT-S8530; look for GT-I9000.zip file in threads http://forum.xda-developers.com/showthread.php?t=1851818&highlight=nvram&page=58