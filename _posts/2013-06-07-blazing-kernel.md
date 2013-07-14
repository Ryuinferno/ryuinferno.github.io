---
layout: post
title: Blazing Kernel
tagline: for JB 4.1.2 & 4.2.2
category: GT-I9100G
tags: [kernel, i9100g]
---
{% include JB/setup %}

<!-- Navbar-->
<div class="navbar navbar-inverse navbar-fixed-top">
  <div class="navbar-inner">
     <div class="container">
        <button type="button" class="btn btn-navbar" data-toggle="collapse" data-target=".nav-collapse">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
           <span class="icon-bar"></span>
        </button>
        <a class="brand" href="/index.html">Blazing Hot Android Development</a>
          <div class="nav-collapse collapse">
            <ul class="nav">
              <li class="">
                <a href="/categories.html">Categories</a>
              </li>
              <li class="">
                <a href="/tags.html">Tags</a>
              </li>
              <li class="">
                <a href="/about.html">About</a>
              </li>
            </ul>
          </div>
     </div>
  </div>
</div>

XDA Thread: [Link](http://forum.xda-developers.com/showthread.php?t=2275275)

<center>
<h1>Downloads</h1>
<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">Download Dual Boot Files<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="https://play.google.com/store/apps/details?id=jackpal.androidterm">Terminal Emulator (Play Store link)</a></li>
    <li><a href="http://jackpal.github.com/Android-Terminal-Emulator/downloads/Term.apk">Terminal Emulator (Direct APK link)</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22979706399754465">DualBoot_BL_v3.apk</a></li>
  </ul>
</div>

<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">Download v11<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=13858085825318748717">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=23017610006234460">TWRP version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=13858085825318748567">PHILZ version</a></li>
  </ul>
</div>

<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">Download v10<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=22964708692721679">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22964708692721680">TWRP version</a></li>
  </ul>
</div>

<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">Download v9<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=22946563261203745">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22946563261203746">TWRP version</a></li>
  </ul>
</div>
</center>
<br />
<br />

Ho yeah!!! I finally made it! A kernel similar to Siyah kernel! You can use this on AOSP 4.2.2 ROMs or stock Sammy 4.1.2 ROMs, it will work in both! Plus, using a similar dual booting method like what [fuss132](https://github.com/fuss132) did, you can now dual boot stock+stock, AOSP+AOSP or stock+AOSP!

##Features
####AOSP & Stock Features:
- Can be flashed directly using stock recovery!
- **Supports DUAL BOOTING**
- Compiled using CM source
- Compiled using Linaro toolchain 4.7.3
- Linux kernel version 3.0.60
- 2 versions of recovery available (different zImage): TWRP and CWM!
- Default scheduler is cfq
- Default governor is interactive
- MMC_CAP_ERASE already disabled by Samsung -> no more brick bug
- Supports CIFS
- USB fast charge (use an app called "Fast Charge" to toggle)
- Custom voltage settings (use "Voltage Control" to set)
- Frandom support!
- Patched /dev/random
- More RAM (original=769 MB, Blazing Kernel=774MB)
- Additional governors: HYPER, Scary, wheatley, abyssplug, minmax, lulzactive, lazy, pegasusq, lagfree, smartassV2
- Addtional I/O schedulers: vr, sio, row
- swap support
- zRAM support
- exFAT module support
- Dynamic Fsync
- Dynamic Dirty Page Writeback
- Battery Life eXtender (BLX)
- Miscellaneous tweaks

####Stock only features:
- Custom bootanimation (just place bootanimtion.zip in /system/media; to restore original bootanimation, just delete the bootanimtion.zip in /system/media) \[AOSP already has this]
- Custom boot sound (just place PowerOn.ogg in /system/media; to mute, create an empty file named "mute" in /system/media; to unmute, create an empty file named "unmute" in /system/media ; to restore original boot sound, create an empty file named "ori_sound" in /system/media)
- Init.d scripts support (Place scripts in /system/etc/init.d or /data/etc/init.d) \[AOSP already has this]

##Bugs
####AOSP:
- Cannot control vibration intensity

####Stock:
- Cannot control touchkey light duration or turn on/off

##Requirements
- Running a stock 4.1.2 Samsung ROM or stock 4.1.2 based ROM
- Running a AOSP 4.2.2 ROM
- **At least 3 GB in internal storage if you want to dual boot**

##ROMs Supported
Basically ALL ROMs!
- stock Samsung ROMs \[4.1.2]
- stock based ROMs \[4.1.2]
- MIUI \[4.1.2]
- CM 10.1 \[4.2.2]
- CM 10.1 based ROMs \[4.2.2]
- AOKP \[4.2.2]
- AOKP based \[4.2.2]
- AOSP based \[4.2.2]

##Instructions
Flash via stock or custom recovery (Safest and easiest method):
1. Choose your recovery type: CWM6 or TWRP.
2. Download the corresponding zip package.
3. Place in sdcard (external sdcard for those running stock recovery)
4. Flash the zip.
5. Reboot. It may take a little while as the kernel has lots of things to configure.

##Changelog
	v11:
	- Updated to Linux kernel 3.0.75
	- BLX
	- Dynamic Fsync
	- Dynamic Dirty Page Writeback
	- Dyanmic mutex spin management
	- CRC32 algorithm
	- Updated voltage control
	- Latest sync with CM for better compatibility
	- Fixed MTP not working in stock for certain people
	- Philz recovery now available!
	- Compiled using Linaro 4.7.4 toolchain 

	v10:
	- Updated to Linux kernel 3.0.60 (this is a real update, applied patches step by step instead of skiping those in between 
	(there's one kernel that skipped most of the patches and went to 3.0.75 straight away lol, reverted the 3.0.76 and applied 3.0.77, and claims that it is on 3.0.77 now...lol...and I tried to advice him, but always ignored...:silly:))
	- Fixed random reboots in recovery 
	- Removed interactiveX governor (main cause of the reboots)
	- zRAM support (for fun...lol)
	- swap support (for fun...lol)
	- exFAT module support (sdcards can be formatted in exFAT format now)
	- Compiled using Linaro 4.7.3 toolchain 
  
	v9:
	- Initial dual base kernel commit
	- Bring forward all features from v8
	- Dual boot support

##Dual Booting
This feature requires extra attention, so please read carefully!

1. Decide which ROM you want to place as secondary ROM. The most suitable ROM would be the one that has less updates and stable. Keep in mind that currently all secondary ROMs will start off clean, means ALL DATA WILL BE CLEARED, and /data is 1GB in size.
<br />
<br />
*Now, decide between step 2 or 3:*
2. If you decide to keep using the current ROM you are running as primary ROM, please make a FULL BACKUP now and skip to step 4.
3. If you decide to use the current ROM as secondary and do not mind about data loss, please flash the latest kernel zip package now and skip to step 5.
4. Since you decide to use another ROM as secondary ROM, AFTER making a backup, flash the other ROM. Then, flash the latest kernel zip package and proceed to step 5.
5. Now, reboot the phone and install the control app & Terminal Emulator. You will see this:
![Alt image](http://i.imgur.com/gEcGCAF.png)
6. Hit the Deploy Files button, then the Dual Boot Setup button and wait for the process to finish.
7. The default ROM now is your phone ROM (primary ROM). To boot into SD ROM (secondary ROM) or from SD ROM to phone ROM, hit the Switch ROM button. (Will show current ROM in the future)
8. You can now reboot by hitting the Reboot button. If you want to restore your primary ROM, you can do it now. But remember to flash the kernel zip package again OR if you want to use another ROM as primary, flash that ROM and kernel zip.
9. Booting time may take longer as you are dual booting and dalvik-cache is building up.
10. Repeat all the steps above every time you wanna change new ROMs (means new zip packages).

**NOTE: MTP, USB mass storage or ADB and GPS does not work on secondary ROM**

<center><a href="https://github.com/Ryuinferno/GT-I9100G-Blazing_Kernel" class="btn btn-primary btn-large">View Sources in Github</a></center>
