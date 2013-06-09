---
layout: post
title: (B)lazing Safe Kernels
tagline: for stock Samsung JB 4.1.2
category: GT-I9100g
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

XDA Thread: [Link](http://forum.xda-developers.com/showthread.php?t=2293576)

<center>
<h1>Downloads</h1>
<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">XXLSR<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722749">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722746">TWRP version</a></li>
  </ul>
</div>

<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">DDLS3<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722753">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722742">TWRP version</a></li>
  </ul>
</div>

<div class="btn-group">
  <button class="btn btn-warning dropdown-toggle" data-toggle="dropdown">DXLS8<span class="caret"></span></button>
  <ul class="dropdown-menu">
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722751">CWM6 version</a></li>
    <li><a href="http://www.androidfilehost.com/?fid=22964708692722744">TWRP version</a></li>
  </ul>
</div>
</center>
<br />
<br />

Yippie! After I managed to create a true dual boot kernel, now I am finally able to unpack the ramdisk from a zImage to modify it (add custom recovery to it etc.) and repack it back! So there you have it \[B]lazing Safe Stock Kernels (or B Safe Stock Kernels for short)!

##Features:
- Pure stock kernel! (yup, straight from Samsung, only the ramdisk is modified and nothing else)
- Can be flashed through stock recovery
- CWM 6.0.3.1 or TWRP 2.5
- Both recoveries modified to support preload partition
- Init.d support
- Custom bootanimation support
- Custom boot sound support

##FAQ:
1. What do you mean by a "safe" kernel?
<br />
-Since I only modified the ramdisk of the kernel, the kernel part is left intact, so it's all Samsung's settings! And Samsung should know best about the device (they made the phone anyway...or not? )! So things just work out of the box (exFAT support, SOD free (maybe? Lol) etc etc)...

2. How do you set custom bootanimation?
<br />
-Just place a bootanimtion.zip in /system/media
-To restore original bootanimation, just delete the bootanimtion.zip in /system/media

3. How do you set custom boot sounds?
<br />
-Just place PowerOn.ogg in /system/media
-To mute, create an empty file named "mute" in /system/media
-To unmute, create an empty file named "unmute" in /system/media
-To restore original boot sound, create an empty file named "ori_sound" in /system/media

4. Why is there a weird kernel version in Settings->About device?
<br />
-In custom kernels, the kernels are compiled with the verison name coded into it (e.g. -blazing-v10) and the second line shows who compiled it (e.g. ryuinferno @ Acer-Aspire-v3-571G)...since the kernel is pure stock, the version and compiler's name is set by Samsung...

5. I would like to have the kernel of the xxx firmware repacked, what should I do?
<br />
-Well, just tell me the Android verison and firmware version and upload the zImage here...I will do my magic then...just that simple...

6. I wanz OC, UV, everything else in custom kernalz in tis kernalz!!!!!
<br />
-It is just a stock kernel (yes, straight from Samsung, I just modified the ramdisk), so do not be silly and request stuff like OC, UV, fast charge etc etc which is impossible...

##Instructions:
Flash via stock or custom recovery:
1. Choose your recovery type: CWM6 or TWRP.
2. Download the corresponding zip package.
3. Place in sdcard (external sdcard for those running stock recovery)
4. Flash the zip.
5. Reboot.

<center><a href="https://github.com/Ryuinferno/galaxys2_kernel_repack/tree/i9100g" class="btn btn-primary btn-large">View Method in Github</a></center>
