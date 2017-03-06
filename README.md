# ESP8266 basic board

![Imgur](http://i.imgur.com/WBkdxMS.jpg)


##What?

This is the schematic for a simple perfboard to upload code to ESP8266 (https://en.wikipedia.org/wiki/ESP8266) using an Arduino, and to create bidirectional communication between the ESP8266 and the Arduino board (using SoftwareSerial library)


##Why?

When I started learning about the ESP8266, I discovered that it needs to be programmed separately, and I used this link to build the basic circuit on a breadboard: https://diyhacking.com/esp8266-tutorial/ (in my case STEP 1: Connect the Hardware to Your ESP8266 => 3. Using Arduino Uno to Flash the Code to ESP8266)

so since I may be using the ESP8266 in different projects, I thought to build a more elegant board than the messy breadboard with all its wires!

##How?

After building and soldering the perfboard, and if you want to program the ESP8266 through an Arduino (instead of a USB to TTL converter), then simply follow these steps (inspired from this link: https://diyhacking.com/esp8266-tutorial/)  
  
**1-** upload an Arduino sketch that contains an empty setup() and loop() [Make sure Rx/Tx pins are not connected to the ESP8266 yet, and select the correct Arduino board from Arduino IDE]

```
void setup() {

}

void loop() {

}
```


**2-** Install the ESP8266 platform and select "Generic ESP8266 Module" from the board submenu (check this tutorial for instructions: https://diyhacking.com/esp8266-gpio/)


**3-** connect Arduino Rx to the perfboard Rx, and Arduino Tx to the perfboard Tx


**4-** connect Arduino GND, 5V to the perfboard GND, 5V


**5-** upload your code using the arduino IDE, and while uploading the code make sure you keep pressing the 'flash' button on the perfboard, then press the Reset button (while you keep pressing the flash button), then release the reset, then release the flash button, check these pictures for more info:

![Imgur](http://i.imgur.com/fcD3jmm.jpg)
**Step1:** press the Flash button


![Imgur](http://i.imgur.com/mUS5aSI.jpg)
**Step 2:** press the Reset button (while pressing the Flash button)

![Imgur](http://i.imgur.com/dsa1NvB.jpg)
**Step 3:** release the Reset button

![Imgur](http://i.imgur.com/EAZxvT4.jpg)
**Step 4:** release the Flash button

These are some pictures for the perfboard, I have also uploaded to this repo the fritzing file and the stickers file in order to label the pins and the buttons.

**Note:** you can download the fritzing part for the ESP8266 here: https://github.com/ydonnelly/ESP8266_fritzing (I am currently using the ESP8266-01)


![Imgur](http://i.imgur.com/EzOE0YH.jpg)

![Imgur](http://i.imgur.com/bbCfLV4.png)

![Imgur](http://i.imgur.com/yRZQpte.jpg)


