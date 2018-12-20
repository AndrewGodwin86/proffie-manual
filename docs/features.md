# Specs and Features

## ProffieBoard Specific

- Dimensions: 17.9 x 34.6 x 5.7mm (with micro USB port and micro SD card) 
- Single pcb board design

## TeensySaber v3 Specific
- Dimensions: 18 x 39.5 x 9mm (with micro USB port and micro SD card)
- 2-pcb boards stack design

## Common
- 100% Open-Source, you may add any feature you like (GPLv3)
- Power supply: 2.6-4.5 Volts, up to 10A per LED output 1-6; single Li-Ion 3.6-3.7V (low 2.6V, full 4.2V) battery recommended - Speaker: 4 ohm or 8 ohm, 2W (with lower volume) or 3-5W (recommended)
- Unlimited amount of sound banks/fonts, supports regular (Plecter, NEC) and “Smoothswing” sound fonts
- Sound FX (WAV sound files): boot, blaster blocking, lockup, hum, swing, clash, drag, font, force, ingnition, retraction
- Light FX: blade flickering, pulsing, flash on clash, drag, stab, blaster blocking, lockup and other
- Music tracks (WAV sound files) playback in idle mode and saber sound effects background
- Micro SD card: 4-16Gb Class 4-10 by SanDisk brand recommended
- Support for remote control via bluetooth (with external bluetooth module addon)
- Speedy 32-bit processor for advanced features like sound filters, synthesizing and mp3 playback
- 3 Watts sound amplifier, 16-bit digital output (12-bit for TeensySaber V1 and V2)
- Sample rate is 44kHz (default), 22kHz and 11kHz are supported and upsampled to 44kHz automatically
- Gapless playback, with 2.5ms cross-fade when you interrupt one sample to go to another
- Polyphonic playback, currently configured for up to 5 simultaneous samples
- “Smoothswing” algorithm support (a new more natural swing motion sounds playback)
- PL9823 (RGB), WS2812B (GRB), SK6812 (GRB, WWA) Neopixel support
- 1/2/3/4-color LED stars (Tri-Cree and Quad (also RGBA) LED modules)
- Segmented (6 segments + Flash string) classic string blades support
- Multi-blade support for dual and crossguard setups
- Blade LED type, Presets and Blade Styles selection by different values of a resistor (Blade ID functions)
- Crystal chamber support
- Power-level indicator with neopixel blade
- OLED PLI and FONT, animations display
- MTP support (drag-n-drop files from windows through USB connection)
- POV (persistance of vision) mode support
- Accent LEDs support (also implemented as additional “blades”)
- Spoken error and low battery messages
- Easy and free firmware updates by user