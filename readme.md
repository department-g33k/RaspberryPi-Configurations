# RaspberryPi ScreenlyOSE Configuration
#### Use at your own risk.  I know almost nothing about Linux, and have written this to share the few shards of knowledge I have collected.
1.  Use Etcher to write image to microSD card
2.  Copy network.ini into /boot/ on microSD card
3.  Copy xinitrc into /home/pi/.xinitrc (note: add the leading '.' to the file name when copying)
4.  Boot Raspberry Pi - From local console, use Ctrl+Alt+F1 to get to console
    - sudo apt-get update
    - export DISPLAY=:0 (needed to enable xset, apparently)
    - sudo raspi-config
      - Expand filesystem
	  - Interfaces > Enable ssh
      - Interfaces > Enable vnc
	   - Advanced > Disable Overscan
      - reboot to finish Filesystem expansion
5.  Once Screenly displays, visit [ip]:8080 to configure.  From Screenly UI:
    - Turn off splash screen
