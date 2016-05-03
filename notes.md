## Notes from https://youtu.be/yIGxtHi9Ilw

Serial cable - don't connect VCC. Rx/Tx/Gnd only.

Boot android with console cable.
* Insert fat32 stick into usb1
* partitions in `/dev/block`
* usb sticks in `/storage/external_storage/sdaX`
* backup boot data system recovery
  * `dd if=/dev/block/data | gzip -c9 > $USB/data.img.gz`

To shut up the kernel on the console:
* `dmesg -D` `--console-off disable printing messages to console`
* `dmesg -E` `--console-on  enable printing messages to console`

## Forum

http://freaktab.com/forum/tv-player-support/amlogic-based-tv-players/23766-rom-unofficial-openelec-for-mk808b-and-mxq

Up to page 43.
