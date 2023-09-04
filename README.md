# Raspberry Pi 4 EEPROM format

The Raspberry Pi 4 series use an EEPROM to store the second stage
bootloader. While firmware blobs are hosted on
[GitHub](https://github.com/raspberrypi/rpi-eeprom/blob/master/firmware/stable/recovery.bin),
the format is undocumented (as far as I can see).

I have written an imHex pattern file that can
be used to extract content from an EEPROM dump such as
those included on the [Raspberry Pi EEPROM archive](https://github.com/raspberrypi/rpi-eeprom/blob/master/firmware/stable/recovery.bin).

Combined with the [decompression tool](https://git.venev.name/hristo/rpi-eeprom-compress)
we can extract the proprietary bootloader and its configuration.

![EEPROM parsed with the imHex pattern](./pi4-eeprom-screenshot.png)

## Links

- [Broadcom BCM2711 System on a Chip](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/computers/processors/bcm2711.adoc)
- [First Stage Bootloader Documentation](https://www.raspberrypi.com/documentation/computers/raspberry-pi.html#first-stage-bootloader)
- [DataSheet for the BCM2711](https://datasheets.raspberrypi.com/bcm2711/bcm2711-peripherals.pdf)
- [ARM Cortex-A72](https://en.wikipedia.org/wiki/ARM_Cortex-A72)
- [Custom decompression tool](https://git.venev.name/hristo/rpi-eeprom-compress)
