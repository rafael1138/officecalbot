# Dad's on a Call - Arduino Esp01 + Telegram

​              ![img](https://www.redditstatic.com/desktop2x/img/renderTimingPixel.png)            

[![Post image](https://preview.redd.it/b93ib487p4t41.jpg?width=1810&format=pjpg&auto=webp&s=61a39e5904a99d2ce587fb24663aa016ffd1c5a3)](https://preview.redd.it/b93ib487p4t41.jpg?width=1810&format=pjpg&auto=webp&s=61a39e5904a99d2ce587fb24663aa016ffd1c5a3)

Breadboard Setup



i. ***GENERAL:***

This is a pretty nice project.

The original idea came from Steve Forde:

https://twitter.com/cairn4/status/1245539977993355265



He created a status board to let his family know when he is in a work call.



ii. ***SPECS & Parts***:

He worked with a ESP8266, my version works with a ESP-01s and this is the prototype version:



[![Post image](https://preview.redd.it/gzcrewrsh4t41.png?width=562&format=png&auto=webp&s=11244f498c30ab97e8c11ab1f486da53d3757088)](https://preview.redd.it/gzcrewrsh4t41.png?width=562&format=png&auto=webp&s=11244f498c30ab97e8c11ab1f486da53d3757088)

ESP-01S Connections. Remember VCC = 3.3v

So, this project uses a library that allows the ESP-01s receives commands from Telegram:Universal Telegram Bot: https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot

The Parts are:

1 ESP-01s.2 Leds.3 Resistors (2 * 220ohms - 1 * 10k ohms)1 Breadboard.A lot of jumpers.

iii. ***The CODE***:

The code is based on "Control an LED strip using Inline Keyboard on Telegram" by Brian Lough.

You can find it here: https://github.com/rafael1138/officecalbot

***Note: You need to know how to setup and upload the code to the esp-01s. There is a lot of tutorials about his.



iv. ***Instructions for Telegram Bot:***

I'm going to give you a really tiny & fast explanation but you can follow this an will works pretty nice: https://steemit.com/utopian-io/@drencolha/making-a-telegram-chat-bot-with-the-telegrambot-arduino-library-and-esp8266-wifi-module-tutorial



1. You need to install the library Telegram Bot Library in the Arduino IDE :



[![Post image](https://preview.redd.it/pr6gp76jm4t41.png?width=640&format=png&auto=webp&s=c3f77d979e2ec0b693ac1cd2b7373d4a0d7d4ce3)](https://preview.redd.it/pr6gp76jm4t41.png?width=640&format=png&auto=webp&s=c3f77d979e2ec0b693ac1cd2b7373d4a0d7d4ce3)

Use the zip file from the above link.

\2. You need to Downgrade your Json installation in the Arduino IDE (See  notes in code). This is because the Telegram Bot Library doesnt works  with any 6.x version.

\3. Go to telegram and add BotFather (https://telegram.me/botfather) and:

3.1 Create your bot: /newbot3.2 It will ask you new bot name.3.3 It will  ask for a username that ends with "bot"3.4 It will show you your unique  Token. (This need to be paste it in the code)

Save all this info.

v. ***Operation***:

Turn on your ESP-01s and go to Telegram and type in your bot:

/start --> after you get the answer type --> /options

You should see something like this:



[![Post image](https://preview.redd.it/qejowjh3p4t41.jpg?width=701&format=pjpg&auto=webp&s=f6a68e2c97daf4421d40da321c5f96e2d1650095)](https://preview.redd.it/qejowjh3p4t41.jpg?width=701&format=pjpg&auto=webp&s=f6a68e2c97daf4421d40da321c5f96e2d1650095)

This is the Menu with available commands.



Demo. (Sorry for the bad quality)



[![Post image](https://preview.redd.it/aixief6ir4t41.jpg?width=960&format=pjpg&auto=webp&s=8019784e79d0b6ac5fa995fe2ad10cf0866174e3)](https://preview.redd.it/aixief6ir4t41.jpg?width=960&format=pjpg&auto=webp&s=8019784e79d0b6ac5fa995fe2ad10cf0866174e3)

3.3v - 73 mA for the 2 leds.

After this, you should put it in a frame like Steve Forde did.

I still have a doubt, if I want this in a frame and I want it standalone, how I give juice to it?

This need 3.3v so if I'm going to use a battery (lipo/lion), I'll need a  usb/charger-protection module but with a step down function. Do you have any recommendation?

I really hope you like this and helps you in  your WFH period.

if you have any question let me know.

Thanks!!!