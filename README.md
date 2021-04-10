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

This project is based off the work of other creators including Seafox_c (https://create.arduino.cc/projecthub/florenmichael/cheap-portable-cocktail-maker-barbot-wit-app-4f9079) and Ted Kinsman (https://makezine.com/projects/build-cocktail-drinkbot/). With the push of a Staples Easy Button, an Arduino Uno is coded to pour pre-determined amounts of liquid using 2 pumps, resulting in a freshly made Tequila Sunrise. Each pump and bottle has a corresponding LED with a unique colour. When no liquid is being poured, the LEDS will flicker in a linear, strobing pattern. When liquid is being poured, the LED corresponding to the pump/bottle that is in use will turn off, allowing the user to easily see which liquid is being poured.

# Install Instructions

## List of Components 
  - Arduino Uno
  - Generic Breadboard
  - CPU
  - 12V water pumps (3)
  - 560K Ohm Resisotrs (3)
  - Jumper Wires 
  - Male/Female Jumper wires 
  - Elegoo Relay Module 8 Channel 5V 
  - Silicone hose (width dependent on pumps and length dependent on build)
  - Wood to build frame 
  - Funnel 
  - Push button  

## Frame Build

2 - 4 by 1 inch boards were cut at a lenght of 2 feet. Another 4 by 1 inch board was attached perpendicularly to the first 2 boards using screws. This created the base of the stand. 
2- 6 by 1 inch boards were cut at a length of 22inches and vertically attached to either side of the base using screws. 
A 22inch board was placed on the vertical boards to create the top of the frame. Another 22inch board was cut and screwed to the back of the vertical boards, creating the backing. On this backing 3 holes were drilled for the pump wires and 3 holes were drilled for the LEDs. 
A small board was attached in front of the pumps and 3 holes were drilled for the silicone hoses to run through. A funnel was mounted to the bottom of the small board to collect the liquid from all of the houses and pour it into 1 cup. 

These dimensions could easily be modified depending on the needs of the project or preference. 

*See picture below for our original blue print* 

*See pictures of completed build for visual overview*

<img width="500" alt="Screen Shot 2021-04-09 at 7 17 40 PM" src="https://user-images.githubusercontent.com/79594183/114253689-6714d880-9968-11eb-8f1f-929302c36e30.png">


## Power Supply for Pumps
### Powering Pumps using CPU

This project uses a CPU power supply to provide the pumps (via the Elegoo) with 12V DC. 
In order to power the pumps (via the Elegoo) and to ground the pumps, wires from the CPU P1 were hijacked: 
  - One of the black wires from P1 was cut and used to ground all pumps straight to the CPU.    
  - The green wire (PSU on) and ibe if the yellow wires (+12 V) were both used to provide power to the pumps via the Elegoo.

*See image below for the wires extracted from P1*

<img width="500" alt="Screen Shot 2021-04-09 at 10 31 00 AM" src="https://user-images.githubusercontent.com/79594183/114212184-c2ba7400-991e-11eb-8bda-e9ba688b2f73.png">


## Elegoo  
### Wiring the pumps to the elegoo and CPU

The yellow and green wires were directly connected to first relay of the Elegoo, via the third pin. Furthermore,relay 2 and 3 were powered by carrying the postive voltage via jumper wires. 

The pumps receive positive voltage via the middle (second) pin on each relay. 

*See picture below for clarification.*

<img width="500" alt="Screen Shot 2021-04-09 at 10 10 16 AM" src="https://user-images.githubusercontent.com/79594183/114209447-ddd7b480-991b-11eb-9508-23713e8b8035.png">


### Wiring the elegoo to the arduino 

Digitl pins 2-9 on the Arduino Uno were directly connected to Elegoo as follows: 
  - Pin 2 - IN1 
  - Pin 3 - IN2
  - Pin 4 - IN3
  - Pin 5 - IN4
  - Pin 6 - IN5
  - Pin 7 - IN6
  - Pin 8 - IN7
  - Pin 9 - IN8
  - GND - GND 
  - Positve rail of bread board - VCC

*See image below for overview*

<img width="500" alt="Screen Shot 2021-04-09 at 10 13 49 AM" src="https://user-images.githubusercontent.com/79594183/114209994-7ec66f80-991c-11eb-8eb7-bbd2be6141ac.png">


## LED's
### Connecting the LEDS to the Arduino Uno

The LED's were wired by "wrapping" a wire to the negative leg and another to the positive leg (these wires differed in lenght depdning on how far they would be placed from the Arduino Uno). The wires were then attached to a jumper wire to ease connectivity with the breadboard and Arduino Uno. 
All LED's received Ground from the bread board, via 560KOhm resistors, to ensure the LED's did not receive too much power. 3 560KOhm resistors were used for LED2 as it was brighter than the rest and we wished to dull its brightness.  
LED1 was connected to the Arduino Uno via pin11. 
LED2 was connected to the Arduino Uno via pin13. 
LED3 was connected to the Arduino Uno via pin10. 

*See image below for overview*


<img width="500" alt="Screen Shot 2021-04-09 at 10 28 55 AM" src="https://user-images.githubusercontent.com/79594183/114211987-8a1a9a80-991e-11eb-9bbf-f9ef08f54d63.png">


## Button
### Hijacking the Easy button 

The Easy button was taken apart by removing the 4 screws on the bottom and removing the "easy" cover.  2 wires were soldered, one to GND and one to PWM1. A hole was drilled through the "easy" cover of the button in order for our newly attached wires to have an exit point. 
  
*See image below*

No other modifications were made as we wanted the speaker to continue saying "That was Easy" for our project.

<img width="500" alt="Screen Shot 2021-04-09 at 10 33 41 AM" src="https://user-images.githubusercontent.com/79594183/114212429-1036e100-991f-11eb-813e-8edacf29bb37.png">

** Sadly we were unable to hijack the easy button and a regular push button was wired into the bread board instead **

### Connecting button to the Arduino Uno 

The Ground of the easy button was connected to the Ground on the bread board. 
WM1 was connected to Pin12 on the Arduino Uno

*See image below for overview*

<img width="500" alt="Screen Shot 2021-04-09 at 10 34 13 AM" src="https://user-images.githubusercontent.com/79594183/114212494-2349b100-991f-11eb-890c-cc8263cccb7e.png">


## Add all components to Frame
Once everything has been wired all components were added to the frame. 

*See picture below for fully compleyted hardware*

<img width="500" alt="Screen Shot 2021-04-09 at 10 42 36 AM" src="https://user-images.githubusercontent.com/79594183/114213538-504a9380-9920-11eb-8957-9c3a4e78e432.png">

<img width="500" alt="Screen Shot 2021-04-09 at 10 44 52 AM" src="https://user-images.githubusercontent.com/79594183/114213747-9f90c400-9920-11eb-8c1a-5f8d6ef043b1.png">

## Schematic

(make an overall schematic)


## Now its Time to Code!

Please refer to Code File for our fully functioning code. 

<img width="500" alt="Screen Shot 2021-04-09 at 7 55 12 PM" src="https://user-images.githubusercontent.com/79594183/114254602-95e17d80-996d-11eb-8741-188f0f58e514.png">

<img width="650" alt="Screen Shot 2021-04-09 at 7 56 10 PM" src="https://user-images.githubusercontent.com/79594183/114254612-a8f44d80-996d-11eb-8e19-8ed132c97973.png">

<img width="829" alt="Screen Shot 2021-04-09 at 7 56 33 PM" src="https://user-images.githubusercontent.com/79594183/114254619-b14c8880-996d-11eb-9a48-ed603c0ccc2e.png">

<img width="767" alt="Screen Shot 2021-04-09 at 7 56 50 PM" src="https://user-images.githubusercontent.com/79594183/114254626-bc071d80-996d-11eb-9039-1092b3cdf3ef.png">


# Usage Section 

With the push of a button a drink is easily made, and an LED will indicate which pump is currently dispensing liquid. 
Simply insert the silicone hoses into your choice of mix and Get-Your-Drink-On. 

In order for the build to work as desired simply follow the above instructions and copy-paste our code into your Arduino code, then you are set to go! 

*click on the linke below for a video of our project!* 

https://user-images.githubusercontent.com/79594183/114253867-70eb0b80-9969-11eb-97e5-9b551813fb7d.mp4



# Planned Features
There are a number of improvements that can be made to this project. First, additional pumps and LEDs can easily be added to allow for a larger variety of cocktail options. Due to limited time, we were only able to use 2 pumps, but plan to add a third in the future. Additionally, Bluetooth capabilities could be added to the build to allow for drinks to be ‘ordered’ from mobile device. For instructions on how to incorporate this, review Seafox_c’s project (https://create.arduino.cc/projecthub/florenmichael/cheap-portable-cocktail-maker-barbot-wit-app-4f9079). We had planned to incorporate Bluetooth as a ‘reach milestone’, but experienced a few setbacks that prevented this.

# Bugs List 
We ran into a number of issues while working on this project. A major setback we experienced was finding a power source to run the pumps that was relatively simple to connect and cheap. Since we were both beginners, we had a lot of difficulty understanding what would work as a power supply. Thankfully, our professor, Dr. Tomesh, was able to provide us with guidance and a CPU. 
Another issue we encountered was with wiring the LEDs. The other projects we looked at connected a resistor directly onto one leg of each LED. As such, we trusted this processed and soldered a 560 ohm resistor onto the negative leg of each LED. However, we found that the LEDs would not light up with the resistors attached in this way. As a solution, we cut off the soldered resistors and placed new ones directly onto the Arduino breadboard and chose instead to strip about 1 cm of wire (positive and negative) and wind it around each leg of the LED. 
Additionally, we had trouble coding the Easy Button so that it would communicate with the Arduino Uno. After a meeting with Dr. Tomesh it was decided that the easy button was not an optimal option for this project and a standard push button was wired into the bread board.  
The final issue we encountered was that one of our pumps did not work when we took it out of the box due to a manufacturers defect. As such, this project only used 2 pumps instead of the anticipated 3 pumps. This problem was easily resolved by contacting Amazon and sending the pump back. Unfortunately, there was not enough time to receive another pump before the project was due, but we have ordered another and will insert it in the future. Furthermore, the pumps that did work were not able to pull the liquid up and into the pump (the force of gravity seems to be stronger than the force of the pump). In order to get the liquid to the pumps they needed to be primed (liquid had to be sucked into the pump). Once liquid had entered the pump, they were able to continue pumping the liquid. This is why in our usage video the hoses must be held, as the liquid has been primed into the pump ahead of time. 



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
This project would not have been possible if not for the continued patience and guidance of our professor, Dr. Tomesh. Not only did he meet with us multiple times to help us wire and troubleshoot, but was he kind enough to supply us with a CPU free of charge. We also would like to thank Randy Pomedli for helping us build the frame and solder wires. He also provided much needed encouragement in times of struggle. 

