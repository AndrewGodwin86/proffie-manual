#### ProffieBoard {docsify-ignore}
# Firmware Upload and Update {docsify-ignore}

## Software installation and setup

To upload firmware to ProffieBoard Arduino IDE program is required. Follow these steps to install it to your PC:

1. Install latest Arduino IDE software (don’t use BETA).
Installing as Windows app also is not recommended, because it will be installed in a specific protected folder that won’t allow you to install any additional software/plugin in it. If ProffieBoard won’t show up in COM port, use
Arduino IDE 1.8.6 version.

2. Install the Proffieboard Arduino Plugin and Zadig software. Follow installation instructions.
3. Select Proffieboard-STM32L433 in Tools -> Board USB Type – Serial
CPU Speed – 80 MHz
Optimize – Smallest Code
DOSFS – SDCARD (SPI)
Port – COM(the number your PC assigned) (Butterfly-L433CC)  

## Uploading firmware
1. Download the ProffieBoard firmware and SD card content. Unzip lightsaber-1.286.zip to your Documents directory or to Desktop, but not to Arduino program folder or anywhere in Programs directory where all programs are installed. You will see a lightsaber folder and files inside it. Don’t move any of these files to any other location outside the lightsaber folder and don’t reorganize them! Unzip ProffieOS_SD_Card.zip to the folder where you keep lightsaber-1.286 folder. Copy all files from ProffieOS_SD_Card folder to your SD card.

2. Unhide file extensions in File Explorer settings to see .h ending of config files. Don’t add “.h” to the config file name!
Go to config folder and create you own config.h file (see page 42 for how-to).
Double-click the lightsaber.ino file.

3. Add the name of your config.h file as shown and Save this lightsaber.ino file. Make sure the other config files are commented out, there should be only one CONFIG_FILE without //. You can have multiple config files
in lightsaber>config folder and just define the one you need in lightsaber.ino file and upload it again to ProffieBoard.

4. Connect battery to ProffieBoard and hook up to your PC with a data transfer micro-USB-to-USB cable.
Press arrow button, it will compile and upload firmware to the board. Wait for red text progress bars to stop at 100%, ProffieBoard will play boot sound if speaker is connected.  
Now you can unplug the USB cable. Done!  
If it gives an error instead, this means your config.h file has issues, #define CONFIG_FILE name has mistakes, config.h file is out of config folder, your PC user name is non-latin...
