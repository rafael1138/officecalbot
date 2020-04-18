# Dad is on a Call - Arduino Esp32-01s + Telegram

![Dad is on a Call - ESP-01s + Telegram](C:\Users\Rafael\AppData\Local\Microsoft\Windows\INetCache\IE\5ACB99J6\HVI9Z1j[1].jpg)

### i.General:

This is a pretty nice project.

The original idea came from Steve Forde, who He a status sign to let his family know when he is in a work call.

![](https://i.imgur.com/3D8hOCW.png)

<center>https://twitter.com/cairn4/status/1245539977993355265</center>

### ii. **Specs & Parts**:

He worked with a ESP8266, my version works with a ESP-01s and this is the prototype version:

![](https://i.imgur.com/9ucytie.png)

![Dad is on a Call - ESP-01s + Telegram](C:\Users\Rafael\AppData\Local\Microsoft\Windows\INetCache\IE\5ACB99J6\HVI9Z1j[1].jpg)

##### ESP-01S Connections:

Vcc --> 3.3v. (Do not use 5v!!!!!!)
Gnd --> Ground.
CHPD --> Vcc.
GP0 --> 10k Resistor --> Vcc & GP0 --> 220 Resistor --> Led --> Ground.
GP2 --> 220 Resistor --> Led --> Ground.

##### Ardino IDE Libraries & Bot Setup:

So, this project uses a library that allows the ESP32-01s receive commands from Telegram:
Universal Telegram Bot: https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot

1. You need to install the library Telegram Bot Library in the Arduino IDE.
2. Downgrade your Json installation in the Arduino IDE Library (See  notes in code). This is because the Telegram Bot Library doesnt works  with any 6.x version. (Select v5.13.5).
3. Go to Telegram and add BotFather (https://telegram.me/botfather).
4. Create your bot using the command "/newbot3.2".
   It will ask you new bot name.
   It will  ask for a username that ends with "bot".
   It will show you your unique  Token. (This need to be paste it in the code).
   Save all this info.

##### The required parts are:

1 ESP32-01S. (or similar)
2 Leds
3 Resistors (2x220ohms - 1x10k ohms)
1 Breadboard.
Jumper cables.
Power supply (3.3v)

### iii. ***The CODE***:

The code is based on "Control an LED strip using Inline Keyboard on Telegram" by Brian Lough.

You can find my modiicated code here: https://github.com/rafael1138/officecalbot

***Note: You need to know how to setup and upload the code to the esp-01s. There is a lot of tutorials about this.

### iv. ***Operation***:

Turn on your ESP32-01s and go to Telegram and type in your bot:

/start (This is for the first time connection)

/options --> You should see the available options:

![](https://i.imgur.com/NCSaWh2.gif)



Now you are ready to go. the commands are:

On = Turn on pin (led) GP02.
Off = Turn off pin (led) GP02.
BT = Turn on pin (led) GP0.
BTOFF = Turn of pin (led) GP0.
ALLOFF = Turn of both pins (Leds).
10/20/30mins = Turn on pin (led) GP02 during that time.

[![YouTube: Demo Video](https://i.ytimg.com/vi/o5JdhVkOapg/hqdefault.jpg?sqp=-oaymwEZCPYBEIoBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLBDYC2pocfPmyNmxmEl7GLVOxtuRg)](https://www.youtube.com/watch?v=o5JdhVkOapg "Demo Esp32-01s + Telegram")

With all leds off this is the consumption:

<img src="https://i.imgur.com/3UGhCR6.jpg" style="zoom: 7%;" />

With all leds on:

<img src="https://i.imgur.com/9f7lBsJ.jpg" style="zoom:7%;" />



After this, you should put it in a frame like Steve Forde did.

I still have a doubt, if I want this in a frame and I want it standalone, how I give juice to it?

This need 3.3v so if I'm going to use a battery (lipo/lion), I'll need a  usb/charger-protection module but with a step down function. Do you have any recommendation?

I really hope you like this and helps you in  your WFH period.

if you have any question let me know.

Thanks!!!
