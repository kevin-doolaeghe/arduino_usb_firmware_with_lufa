# LUFA Library - Arduino USB Firmware

## Atmega 16u2 firmware upload

1. Install package `dfu-programmer`

```
sudo apt-get install dfu-programmer
```

2. Reset the Atmega 16u2 to enter programming mode by shorting RESET and GND pins (pins 5 and 6).

3. Program the Arduino board

```
sudo dfu-programmer at90usb82 erase
sudo dfu-programmer at90usb82 flash UNO-dfu_and_usbserial_combined.hex --suppress-bootloader-mem
sudo dfu-programmer at90usb82 reset
```
