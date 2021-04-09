# Get-Your-Drink-On
This is the final project for CS207 through the University of Regina. We will be creating the software and hardware for an Arduino Uno powered drink bot. This bot will be able to deliver pre-set amounts of "liquid" into a preplaced glass via the push of a button. Cheers! 


# Tables of Contents
1. Features List 
2. Install Instructions
3. Usage Section 
4. Planned Features
5. Bugs List 
6. Licenses 
7. Credits 
8. Thanks

# Features List 
Do you enjoy having leisurely beverages but hate mixing such drinks?! So do we. We created this project in the hopes that our leisure time would no longer be dampened by the hassle of making drinks and by arguments about whose turn it was to mix the next round of beverages. Another issued solved by this project is the fatal inaccuracy of liquid measuring, specifically alcohol measuring that tends to occur as the number of beverages consumed increases. This project allows for argument-free drinks that will remain accurately measured throughout the night, ensuring fun and ‘responsible’ social visits. Plus, you’ll get to impress guests with the awesome hardware and software skills required to make a drink robot. Now, get your drink on! 

This project is based off the work of other creators including Seafox_c ((https://create.arduino.cc/projecthub/florenmichael/cheap-portable-cocktail-maker-barbot-wit-app-4f9079) and Ted Kinsman (https://makezine.com/projects/build-cocktail-drinkbot/). With the push of a Staples Easy Button, an Arduino Uno is coded to pour pre-determined amounts of liquid using 2 pumps, resulting in a freshly made Tequila Sunrise. Each pump and bottle has a corresponding LED with a unique colour. When no liquid is being poured, the LEDS will flicker in a linear, strobing pattern. When liquid is being poured, the LED corresponding to the pump/bottle that is in use will turn off, allowing the user to easily see which liquid is being poured.

# Install Instructions

## Frame Build

Insert Pic 



## Power Supply for Pumps
### Powering Pumps using CPU

This project uses a CPU power supply to provide the pumps (via the Elegoo) with 12V DC. 
In order to power the pumps (via the Elegoo) and to ground the pumps, wires from the CPU P1 were hijacked: 
  - One of the black wires from P1 was cut and used to ground all pumps straight to the CPU.    
  - The green wire (PSU on) and ibe if the yellow wires (+12 V) were both used to provide power to the pumps via the Elegoo.
See image below for the wires extracted from P1

<img width="500" alt="Screen Shot 2021-04-09 at 10 31 00 AM" src="https://user-images.githubusercontent.com/79594183/114212184-c2ba7400-991e-11eb-8bda-e9ba688b2f73.png">



<img width="500" alt="Screen Shot 2021-04-09 at 10 31 20 AM" src="https://user-images.githubusercontent.com/79594183/114212219-ccdc7280-991e-11eb-824b-35198ef8b28d.png">


## Elegoo  
### Wiring the pumps to the elegoo and CPU

<img width="500" alt="Screen Shot 2021-04-09 at 10 10 16 AM" src="https://user-images.githubusercontent.com/79594183/114209447-ddd7b480-991b-11eb-9508-23713e8b8035.png">


Wiring the elegoo to the arduino 

<img width="500" alt="Screen Shot 2021-04-09 at 10 13 49 AM" src="https://user-images.githubusercontent.com/79594183/114209994-7ec66f80-991c-11eb-8eb7-bbd2be6141ac.png">


## LED's
### Connecting the LEDS to the Arduino Uno

<img width="500" alt="Screen Shot 2021-04-09 at 10 28 55 AM" src="https://user-images.githubusercontent.com/79594183/114211987-8a1a9a80-991e-11eb-9bbf-f9ef08f54d63.png">


## Button
### Hijacking the Easy button 

<img width="500" alt="Screen Shot 2021-04-09 at 10 33 41 AM" src="https://user-images.githubusercontent.com/79594183/114212429-1036e100-991f-11eb-813e-8edacf29bb37.png">


### Connecting button to the Arduino Uno 

<img width="500" alt="Screen Shot 2021-04-09 at 10 34 13 AM" src="https://user-images.githubusercontent.com/79594183/114212494-2349b100-991f-11eb-890c-cc8263cccb7e.png">



## Add all components to Frame
Once everything has been wired you can add all components to the frame 

<img width="500" alt="Screen Shot 2021-04-09 at 10 42 36 AM" src="https://user-images.githubusercontent.com/79594183/114213538-504a9380-9920-11eb-8957-9c3a4e78e432.png">

<img width="500" alt="Screen Shot 2021-04-09 at 10 44 52 AM" src="https://user-images.githubusercontent.com/79594183/114213747-9f90c400-9920-11eb-8c1a-5f8d6ef043b1.png">


## Now its Time to Code!
(insert code maybe or guide user to check out the code in the code folder we made?) 


# Usage Section 

# Planned Features
There are a number of improvements that can be made to this project. First, additional pumps and LEDs can easily be added to allow for a larger variety of cocktail options. Due to limited time, we were only able to use 2 pumps, but plan to add a third in the future. Additionally, Bluetooth capabilities could be added to the build to allow for drinks to be ‘ordered’ from mobile device. For instructions on how to incorporate this, review Seafox_c’s project ((https://create.arduino.cc/projecthub/florenmichael/cheap-portable-cocktail-maker-barbot-wit-app-4f9079). We had planned to incorporate Bluetooth as a ‘reach milestone’, but experienced a few setbacks that prevented this.

# Bugs List 
We ran into a number of issues while working on this project. A major setback we experienced was finding a power source to run the pumps that was relatively simple to connect and cheap. Since we were both beginners, we had a lot of difficulty understanding what would work as a power supply. Thankfully, our professor, Dr. Tomesh, was able to provide us with guidance and a CPU. 
Another issue we encountered was with wiring the LEDs. The other projects we looked at connected a resistor directly onto one leg of each LED. As such, we trusted this processed and soldered a 560 ohm resistor onto the negative leg of each LED. However, we found that the LEDs would not light up with the resistors attached in this way. As a solution, we cut off the soldered resistors and placed new ones directly onto the Arduino breadboard and chose instead to strip about 1 cm of wire (positive and negative) and wind it around each leg of the LED. 
Additionally, we had trouble coding the Easy Button so that it would communicate with the motors. However, a meeting with Dr. Tomesh solved this project as he provided some additional guidance. 
The final issue we encountered was that one of our pumps did not work when we took it out of the box due to a manufacturers defect. As such, this project only used 2 pumps instead of the anticipated 3 pumps. This problem was easily resolved by contacting Amazon and sending the pump back. Unfortunately, there was not enough time to receive another pump before the project was due, but we have ordered another and will insert it in the future.

# Licenses 
(Stolen directly from Tori’s GitHub)

This is free and unencumbered software released into the public domain.
Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.
In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
For more information, please refer to https://unlicense.org

# Credits 
Seafox_c’s project served to guide us on how to connect the elegoo to the Arduino and the pumps to the elegoo. This project also explains how Bluetooth capabilities could be incorporated:
https://create.arduino.cc/projecthub/florenmichael/cheap-portable-cocktail-maker-barbot-wit-app-4f9079

Ted Kinsman’s project helped us to write the code for making the LEDs strobe and for coding the Easy button:
https://makezine.com/projects/build-cocktail-drinkbot/

In order to wire the CPU to the elegoo, the following resource was used: 
https://www.instructables.com/A-Makers-Guide-to-ATX-Power-Supplies/

In order to hack the Easy Button, the following resource was used:
http://buildinprogress.media.mit.edu/projects/3109/steps

The following GitHub repository was also reviewed as an additional general resource: 
https://github.com/toriyuzik/DrinkBotProject2017

# Thanks 
This project would not have been possible if not for the continued patience and guidance of our professor, Dr. Tomesh. Not only did he meet with us multiple times to help us wire and troubleshoot, but was he kind enough to supply us with a CPU free of charge. We also would like to thank Randy Pomedli for helping us build the frame and solder wires. He also provided needed encouragement when we were struggling.

