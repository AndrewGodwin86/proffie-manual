#### TeensySaber {docsify-ignore}
# Wiring Diagrams {docsify-ignore}

## Board Pinout
![TeensySaber Board Pinout](../_media/teensy-board-pinout.png)

**Battery +** – 2.6 to 4.5 volt input, drives everything except the LEDs  
**Battery -** – negative pad for LEDs, needs to be at same level as GND when both are connected  
**GND** – ground for electronics except LEDs. Note that GND is also available on short edge of the teensy (See the teensy pinout for details)  
**Speaker +/-** – hooks up to speaker
**Activation / Aux / Aux2 button** – hook up to closing buttons, or potentially touch buttons  
**Blade ID / Neopixel Data 1** – normally used to measure the blade ID restor, and if it’s a neopixel blade, feed out neopixel data  
**LED 1, 2, 3** – hooks up to negative side of LED (positive side of LED hooks up directly to battery.) These pads can handle
up to 30 volts  
**LED 4, 5, 6** – like LED1/2/3, but requires FETs to be placed on the bottom of the board to function. Voltage is limited by
selection of FETs  
**Power 1, Power 2, Power 3** – these control the FETs which drive LED 1, 2, 3  
**AUX LED 1, 2, 3** – these are hooked up to pads on the bottom which can be populated with FETs and used to drive additional LEDs. If the bottom FETs are not populated, these pins are free and can be used for any purpose  
**RX3, TX3** – these pins are used for wiring a bluetooth module for wireless control or additional Neopixel Data out  
**SDA, SCL** – these pins are used to wire OLED display  
**+3.3V 250mA max** – generated by the Teensy for powering OLED display or Bluetooth module  
**micro USB port** – micro USB port used only for firmware upload and can be used for sound files upload to SD card.  
THIS PORT ISN’T USED FOR CHARGING THE BATTERY!