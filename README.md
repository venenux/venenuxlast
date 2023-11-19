# venenuxlast - live build of current debian VenenuX
-------

That's VenenuX live-build environment, using Linux\Debian as a base system.

## Introduction and Downloads

It is a source code repository for a ready-to-use Debian operating system that includes powered packages from VenenuX
for remote management, hacking tools and development, also some critical component to assist users.

[![Download VeGNUli ISO](https://a.fsdn.com/con/app/sf-download-button)](https://sourceforge.net/projects/vegnuli/files/VenenuX-1.0/)

## Quick guide to this repository

Running what is in this repository **will create a disk or ISO with an operating system,
ready to use, YES, READY TO USE, DOES NOT REQUIRE TO INSTALL but can be installed**, 
file produced can be "recorded on a blank CD/DVD" or "can be recorded on a USBdrive" and used on the PC,
without deleting your installed operating system, but with the option to replace it if you want.

#### how to use this repository

1. You must clone this repository `mkdir $HOME/Devel && git clone https://codeberg.org/venenux/venenuxlast`
2. You then must install required software `apt-get install live-build`
3. Get into the files and customize as you wish
4. Start building your new VenenuX ISO `cd $HOME/Devel/venenuxlast && lb clean && lb build`

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

#### Requirements

* Debootstrap to deploy a debian base root or a Debian OS installed
* networking, recommended fast one
* Live-build and git packages installed
* almost 30 gigs of space available
* almost a dual core machine
* almost 4 gigs of RAM

