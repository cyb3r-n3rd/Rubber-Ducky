# Rubber-Ducky
Rubber Ducky the Bad USB

Project Name: USB Rubber Ducky
About the Project: By emulating a USB keyboard, this device can be used to remote control a computer, automate tasks or execute software to gain full access. All in the matter of seconds!
This is all possible because keyboards are trusted devices, you plug it in and can start typing right away!
A human might not type very fast, but an automated device like this presses of hundreds of keys per second.
This open source project aims to provide a user-friendly tool to learn about such keystroke injection attacks.
You can simply plug it in, connect to its Wi-Fi network and manage all scripts from within the web interface. You don't need to install an app; you don't need to log in, and you don't need to compile or flash anything. Your scripts are saved on the device itself, so you don't need a micro SD card either.
 
                    



HARDWARE: 
                              
This tool requires following hardware:
An Atmega32u4 development board (for example: Arduino Leonardo or Pro Micro)
An ESP8266 or ESP8285 development board (for example NodeMCU or Wemos d1 mini)
[Optional] A single Neopixel (WS2812b) or Dotstar (APA102) LED
 
Development Boards:
Arduino Leonardo
Arduino Micro
AT Tiny 85
 
Flash Software: Before Flashing Some Preparation needs to be Done.
Preparations:
Download and install the Arduino IDE.
Start the Arduino IDE, go to File > Preferences.
At Additional Board Manager ULRs enter https://raw.githubusercontent.com/spacehuhn/hardware/master/wifiduck/package_wifiduck_index.json. You can add multiple URLs, separating them with commas.
Go to Tools > Board > Board Manager, search for wifi duck and install WiFi Duck AVR Boards and WiFi Duck ESP8266 Boards.
Download and extract this repository or git clone it.


 
 
Ducky Script: 
Basics: Keys are separated by a single space.
Everything written in a single line gets pressed and released at the same time.
To write text, use the STRING function.
 
 
 
Example
Explanation
WINDOWS  r
Type the Windows key and then the r key
WINDOWS r
Press the Windows key and the r key simultaneously
STRING WINDOWS r
Write WINDOWS r

Functions:
Command
Example
Description
REM
REM Hello World!
                        Comment
DEFAULT DELAY or DEFAULT_DELAY
DEFAULTDELAY 200
Time in ms between every command
DELAY
DELAY 1000
                     Delay in ms
STRING
STRING Hello World!
        Types the following string
REPEAT or REPLAY
REPEAT 3
Repeats the last command n times
LOCALE
LOCALE DE
Sets the keyboard layout. Available: DE, ES, GB, US, DK, RU, FR
KEYCODE
KEYCODE 0x02 0x04
Types a specific key code (modifier, key1[, ..., key6]) in decimal or hexadecimal
LED
LED 40 20 10
Changes the color of the LED in decimal RGB values (0-255)




Examples:
REM Hello World for Windows PCs
DEFAULTDELAY 200
GUI r
STRING notepad
ENTER
STRING Hello World!
 
References: 
For Ducky Script: https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads
Original Manufacturer: https://hak5.org/products/usb-rubber-ducky-deluxe
Tutorial For AT Tiny: https://www.youtube.com/watch?v=wPET-fizkQY
