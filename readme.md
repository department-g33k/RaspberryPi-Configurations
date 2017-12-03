# RaspberryPi ScreenlyOSE Configuration
#### Use at your own risk.  I know almost nothing about Linux, and have written this to share the few shards of knowledge I have collected.
1.  Use Etcher to write image to microSD card
2.  Copy network.ini into /boot/ on microSD card
3.  Boot Raspberry Pi - From local console, use Ctrl+Alt+F1 to get to console
    - sudo apt-get update
    - export DISPLAY=:0 (needed to enable xset, apparently)
    - sudo raspi-config
      - Expand filesystem
	  - Interfaces > Enable ssh
      - Interfaces > Enable vnc
	   - Advanced > Disable Overscan
      - reboot to finish Filesystem expansion
4.  Copy setterm into /etc/init.d/
          - chmod +x /etc/init.d/setterm #to make it executable
          - update-rc.d setterm defaults # to create the /etc/rcX.d symlinks
5.  Once Screenly displays, visit [ip]:8080 to configure.  From Screenly UI:
    - Turn off splash screen
