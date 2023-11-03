venenux
-------

That's VenenuX live-build environment, using Linux\Debian as a base system with some tweaks
for better high performance and close to VenenuX hints

Building
--------


1. Install apt-cacher-ng:
    apt-get install apt-cacher-ng

2. Install live-build suite:
    apt-get install live-build

3. Customize configs if neccessary.

4. Start building!
    lb config
    lb build


Known issues
-----------

dpkg fails on tint2 package when installing user lists - restart the building and it should work.


Included software
==

Debian (duh!)

Check out config/package-lists for full list of packages installed during the building process.

