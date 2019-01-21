# Troubleshooting {docsify-ignore}

## How to solve most common issues
### TeensySaber board or Proffieboard is not recognized by computer (nothing under Port selection in Arduino IDE)...
Make sure a charged 3.7V battery is connected to the board, micro-USB cable is a data transfer cable, all plugins and drivers are installed – check again pages 21 for TeensySaber or 40 for Proffieboard. Try a different USB port on your computer.

### Proffieboard is recognized by computer always only as “STM32 BOOTLOADER” (nothing under Port selection in Arduino IDE)...
If Zadig driver is installed properly but Proffieboard is still recognized by PC always as “STM32 BOOTLOADER” instead of “Proffieboard” and only after pressing RESET button while holding BOOT button – open Arduino IDE, make sure you use latest ProffieOS and Proffieboard plugin version, without selecting the Port under Tools tab click the Verify code button and after it’s finished click the Upload button. 
Firmware must now update on Proffieboard and it will be recognized correctly next time you plug it into USB port.

### Sketch (code) compile error in Arduino IDE...
Check your #define CONFIG_FILE “config/..._config.h” line in opened lightsaber.ino file if it’s written correctly with config/ in it.

### Sketch (code) compile error in Arduino IDE...
Check if the ..._config.h file you defined in the lightsaber.ino sketch file is same name as in the lightsaber-”firmware version”/lightsaber/ config folder and is located in this folder.

### Sketch (code) compile error in Arduino IDE...
Check your settings under Tools tab in Arduino IDE program. Check again pages 21 for TeensySaber or 40 for Proffieboard. 

### Sketch (code) compile error in Arduino IDE...
Check if your ..._config.h file is correct: Blade Styles; Presets; const unsigned int maxLedsPerStrip = 144; if BladeConfig blades[] = is correct... 

### Sketch (code) compile error in Arduino IDE...
If nothing helps, install Arduino IDE version 1.86 and try to compile and upload the firmware again.

### Sound doesn’t play...
Remove SD card and insert again, check speaker wiring. Make sure all sound files on SD card are correctly named (8 characters max long). Re-format SD card in FAT32, load sound files and try again, try another SD card.

### Board says “LOW POWER”...
Charge the battery.

### Serial Monitor shows info sent by the board but your commands don’t work...
In the bottom right corner of Serial Monitor window make sure the Line Ending drop down is set to New Line.

### Sound is weird and distorted...
Check your SD card speed (see page 44). Check speaker wiring, try another good speaker.

## For more help, please check these links:

[ProffieOS/ProffieBoard/TeensySaber wiki](https://github.com/profezzorn/ProffieOS/wiki) on GitHub  
[Ask your question on The Rebel Armory forums](http://therebelarmory.com/board/97/profezzorns-lab)  
[Ask your question on FX-sabers forums](https://www.fx-sabers.com/forum/index.php?board=185.0)  
[Ask your question in Facebook group](https://www.facebook.com/groups/288564715213016/)  