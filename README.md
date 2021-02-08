# m5timercam_notes

m5stack Timer Camera X - OV3660 ESP32 - the missing readme

Self contained box with esp32 board, battery, USB-C port and OV3660 camera.

Out of the box only seems towork over serial (i.e no WiFi and no Bluetooth).

Poweron by pressing side (bottom) button for abou 2 seconds.
To power off, press reset (using a paperclip) in small round hole on front, top-right.

Charge over USB (presumbly over port as well.

Can flash board and see camera over USB with serial connectio (Windows only) using https://docs.m5stack.com/#/en/quick_start/timer_cam/quick_start_cameratool

NOTE with 4K display need to run in compat mode.
May need admin permissions.

Flash (or as labeled, "burner") only works if disconnected from camera.


Can flash via command line (and thu spresumbly under Linux) with regular esp tool..

    esptool.exe   --chip esp32 --port COM4: erase_flash
    esptool.exe   --chip esp32 --port COM4: --baud 1500000 write_flash -z  0x1000  firmware.bin

Firmware is in cameratool archive.

## Notes

  * https://github.com/lemariva/micropython-camera-driver doesn't look like it has driver support for this camera- https://github.com/lemariva/micropython-camera-driver/issues/15
  * https://github.com/espressif/esp32-camera
  * https://docs.m5stack.com/#/en/unit/timercam?id=tutorialampquick-start
  
