## Notes from https://youtu.be/yIGxtHi9Ilw

Serial cable - don't connect VCC. Rx/Tx/Gnd only.

Boot android with console cable.

Hit enter to enter uboot:
* save uboot environment
  * `printenv`

Reboot and don't hit enter to let android boot:
* Insert fat32 stick into usb1
* partitions in `/dev/block`
* usb sticks in `/storage/external_storage/sdaX`
* backup boot data system recovery
  * `dd if=/dev/block/data | gzip -c9 > $USB/data.img.gz`


To shut up the kernel on the console:
* `dmesg -D` `--console-off disable printing messages to console`
* `dmesg -E` `--console-on  enable printing messages to console`

## Notes from openelec forum

http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq?p=510814#post510814

> If the toothpick method is not working because of a hosed NAND, the fix is simple:
> 
> If you power up the system with a SD card inserted, the box looks for kernel.img
> If you power up the system with a SD card inserted AND you have toothpick inserted, the box looks for recovery.img
> 
> Since the toothpick is not working for you, on the SD card, rename "recovery.img" to "kernel.img" and restart the box.
>
> It will flash your box.
>
> WARNING: It will flash every time it boots unless you remove that SD card with kernel.img. If the flash writes the image (you watch the green robot for about 5 minutes) and reboots the box, pull out the card as soon as the box goes black otherwise it will restore/write the image over and over and over again.....

http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq/page195

Notes from libreelec forum

https://forum.libreelec.tv/thread-200.html

## Interesting links

* [Unbrick](http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/s805/others-ab/523003-mxq-ott-s805-box-bricked-red-led-constantly-on)
* [u-boot env](http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq?p=551919#post551919)
* [boot sdcard w/ stock bootloader](http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq?p=552379#post552379)
* [backup partitions while running openelec](http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq?p=556310#post556310)
* [LHS = HD18Q, RHS = MXQ](http://s20.postimg.org/k7r0o5ji4/IMG_20160123_Remotes.jpg)
