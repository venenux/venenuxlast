# venenuxlast - live build of current debian VenenuX
-------

That's VenenuX live-build environment, using Linux\Debian as a base system.

## Introduction and Downloads

It is a ready-to-use Debian operating system that includes powered packages from VenenuX
for remote management, hacking tools and development, also some critical component to assist users.


** All this is not necessary, download it ready to use from our website
web: http://vegnuli.sourceforge.net/** Where it says "VenenuX OS"!

[![Download VeGNUli ISO](https://a.fsdn.com/con/app/sf-download-button)](https://sourceforge.net/projects/vegnuli/files/VenenuX-1.0/)

## Quick guide to this repository

Running what is in this repository **will create a disk or ISO with an operating system,
ready to use, YES, READY TO USE, DOES NOT REQUIRE TO INSTALL but can be installed**, 
file produced can be "recorded on a blank CD/DVD" or "can be recorded on a USBdrive" and used on the PC,
without deleting your installed operating system, but with the option to replace it if you want.

#### directory structure

live build creates a structure with which you can alter the result of the live cd, here shown, 
below the specific documentation of this and how to make your own iso:

```
├── README.md              <--------- this file
└── config
    ├── archives           <--------- xxxx.list.yyyy sources.list for debian package download and install
    ├── hooks              <--------- script that will run wehen the live iso boots or the disk install
    ├── includes.binary    <--------- those files will be put into the ISO file directly
    ├── includes.chroot
    │   ├── etc
    │   │   ├── live       <--------- live user setups scripts
    │   │   └── skel       <--------- skeleton /home directory that will setup live user
    ├── includes.installer <--------- installer preseed.cfg file and logo/theme update for the graphical installer
    ├── package-lists      <--------- list of package names to be included and install on live or disk
    └── packages.chroot    <--------- manually put packages that doe snto have a repository
```

#### Quick documentation live build:

1. Install apt-cacher-ng:
    apt-get install apt-cacher-ng

2. Install live-build suite:
    apt-get install live-build

3. Customize configs if neccessary.

4. Start building!
    lb config
    lb build


