# Introduction

It really just started with a trip to Disneyland. I was really just disappointed with the cheap plastic lightsabers they had available. I had hoped to pick something more display-worthy, or at least in the “toys for grownups” category, but did not find anything. So when I got home, I went and ordered an FX “black series” Luke lightsaber, which looks quite nice, but the sound, light and interactivity was still pretty disappointing.

At this point I started to think about how I would make a lightsaber. I had already done things with neopixels before, so that was kind of a no-brainer for making a better blade, but I really wanted to do was to make the sound react fluidly to motion.

At this point I joined a bunch of forums and came across the NEC and Plecter boards, but there didn’t seem to be a way to alter how they produced sounds, so I picked up a teensy and a PJRC prop shield and started building from there.

The Teensy 3.2 + PJRC prop + SD card reader + voltage booster + FETs I ended up with, was fairly large. Luckily, the Graflex lightsabers are also fairly large, so I purchased a Graflex 2.1 and barely managed to squeeze everything in there.

Around this time, I got kind of stuck with how to synthesize all the sounds a lightsaber makes, so I decided to imple- ment support for Plecter and NEC sound fonts to get the saber I built make some sounds. There are some amazing sound fonts out there, but even so, the interactivity I craved was still missing.

Since I didn’t really have a good idea for how to make that interactivity happen, I took on a different challenge instead: Make it smaller. For the TeensySaber V2, I decided to try to make my own circuit board. That meant integrating some components from the prop shield, the sd card reader, the voltage booster and the FETs into a single board. To make things interesting, I bought a Korbanth OWK, which has an inner diameter of 7/8 inches, and my goal was to fit everything in there. It took a while to do, but the result was the TeensySaber V2 board. The V2 fits really great inside an OWK, without cutting into the inner chassis parts, and was generally a great success, but the sound quality wasn’t as good as I wanted it to be, so eventually I designed he TeensySaber V3, which is mostly the same as the V2, but uses a digital 3W amplifier.

As I was working on the TeensySaber V3, this guy Thexter showed up on a couple of forums, with some great videos showing off an algorithm for better swing sounds. Since this was what I wanted all along, I couldn’t wait until he provided a description of his algorithm so that I could implement it. Lucky for me, he didn’t mind describing his algorithm, so I imple- mented it. My implementation never really sounded as good as his videos though, but that’s probably because I’m not really a font designer. Later, Thexter came back with an improved version, which is what we now call “SmoothSwing V2”.

With SmoothSwing V3, TeensySaber V3 was getting some attention from people, but a lot of people still thought it was too big, since it’s made out of two boards sandwiched together. The sandwiching also creates extra work for installers and extra complications for hobbyists, so it was time to try to put everything together into one board.

At first, I was thinking of using the same components that make up a Teensy to make the all-in-one board, but it turned out to be complicated and expensive. Instead I found another board called a “Butterfly”, which had nearly identical capabilities and an already functional arduino plugin. Even better, the Butterfly was 100% open source (the teensy is only *mostly* open source).

I spent most of the Christmas vacation last year designing the Proffieboard, and it took another couple of months of testing to get a working prototype, but it’s been a lot of fun.

Fredrik Hubinette