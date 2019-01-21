#### ProffieBoard {docsify-ignore}

# Changing Sound Board Parameters {docsify-ignore}

## config.h file structure, editing
All sound files (sound fonts, music tracks) are stored on the micro SD card. Add required sound fonts folders (Plecter, NEC and Smoothswing fonts are supported, no need to change WAV files names, just copy and paste) to SD card root directory as it’s done in the default ProffieOS_SD_Card content folder and music tracks to the tracks folder.

Make sure to name all music tracks and sound fonts folders with latin characters and only up to 8 characters long, without using any special characters (like ?,.|\}{[/- etc.).
Make sure you have a config.ini file in each sound font folder, if there is none - copy one from some default TeensySaber/ProffieBoard sound font and paste into newly added sound font folder. It has only one parameter that you can modify - humstart. It helps to match hum sound start with blade ignition, 1000 usually works fine.

![ProffieBoard Soundfont Config](../_media/proffie-soundfont-configini.png)




All blade effects, LED configuration, volume level, clash sensitivity etc. are changed in the config.h file located in lightsaber>config folder. To do that open any _config.h file in the “lightsaber>config” folder directory in any Text Editor (Notepad - to see code correctly in Notepad, Cut-and-Paste it to WordPad, then Cut-and-Paste it back to Notepad, Save), Ctrl+A (select all text) and Delete it, then Copy-and-Paste (Ctrl+C, Ctrl+V) your wiring diagram config code into empty _config.h file and Save it under new name. Follow the instructions on page 39 to upload it to the board.


## Blade styles
ProffieBoard and TeensySaber use Blade Styles for the main saber blade and any other accent leds to define all light effects (color changing, flashes, flickering, delays, ignition/retraction timing etc...).

Use [Blade Style Editor](https://fredrik.hubbe.net/lightsaber/style_editor.html) to create and adjust Blade Styles. **Megtooth Sith Sabers** did a great [video tutorial](https://youtu.be/2H4XMSKajCI) where he shows and explains how to use Blade Style Editor. Also you can grab some pre-made Blade Styles or share yours [here on TRA forums](http://therebelarmory.com/thread/9273/teensysaber-blade-style-sharing-thread).

A Blade Style example of simple **flickering Green** blade with **Spark on start**, **Clash**, **Blaster**, **Lockup** and **Drag**, **Ignition/Retraction** effects:

```c
StylePtr<InOutHelper<SimpleClash<Lockup<Blast<OnSpark<AudioFlicker<Rgb<0,255,0>,Rgb<50,100,0>>,Rgb<255,255,0>,150>,Rgb<255,50,0>>,AudioFlicker<Rgb<100,255,0>,Rgb<255,0,150>>>,Rgb<255,100,150>,40>,200,300,Black>>
```
– this is how the Blade Style code looks pasted in the config.h file Preset (it sits inside a StylePtr<...> container)


```c
InOutHelper<SimpleClash<Lockup<Blast<OnSpark<AudioFlicker<Rgb<0,255,0>,Rgb<50,100,0>>,Rgb<255,255,0>,150>,Rgb<255,50,0>>,AudioFlicker<Rgb<100,255,0>,Rgb<255,0,150>>>,Rgb<255,100,150>,40>,200,300,Black>
```
– this is how the Blade Style code looks when editing it inside a Blade Style Editor


Each Blade Style is made of a variety of Effects, each added effect goes instead of a base color in the previous effect:


InOutHelper<base color,200,300,Black> – base color can be defined by words (WHITE, RED, GREEN, PURPLE etc..) or by Rgb<0-255,0-255,0-255> values for more custom shades; 200 is extension length in milliseconds; 300 is retraction length in milliseconds; Black is color when retracted (also can be any other color)

SimpleClash<base color,clash color,40> – clash effect; 40 is clash duration in milliseconds

Lockup<base color,lockup color> – lockup effect

Blast<base color,blast color> – blaster effect

OnSpark<base color,spark color,150> – spark on ignition effect; 150 is spark duration in milliseconds

AudioFlicker<”A” color,”B” color> – flickering effect (blade flickers to the actual saber hum sound); the more difference between “A” and “B” colors - the more abrupt is flickering

Rgb<255,50,0> – actual color in RGB format (0 is no light; 255 is the maximum brightness value for Red, Green or Blue channel)