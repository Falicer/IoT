# Internet of Things
By Raekwon Gerold

## Table of Contents 🗂

1. 🏮 [Philips Hue](https://github.com/Falicer/IoT/edit/main/README.md#philips-hue-assignment)
2. 🍘 [Telegram Ledstrip](https://github.com/Falicer/IoT/edit/main/README.md#telegram-ledstrip)

# Philips Hue Assignment
<details open>
Before doing this you gotta do a few steps first:

### Requirements
- Arduino
- Arduino IDE
- Ledstrip

### Make sure your board LED strip is attached to your Arduino correctly
<details open>

1. Make sure that the GND cable is connected to the GND pin
2. Make sure that the Data/Pixel cable is connected to the D5 pin
3. Make sure that the +5V cable is connected to the 3v3 Pin
4. When done it should look this.
<img src="https://i.postimg.cc/Jn7j8nmY/image.png" width="375px" alt="Arduino connected with LED">

</details>

### Install the Adafruit Library
<details open>

1. Open the library manager of your Arduino IDE
2. Look up "Adafruit IO Arduino"
3. Install it "Install All"

This should go succesfull
</details>

### Make an Adafruit IO Account
<details open>

1. Go to [Adafruit IO Registration](https://accounts.adafruit.com/users/sign_up) and make a free account
2. Go back to [Adafruit IO](https://io.adafruit.com/)
3. Click on the yellow key in the menu
4. Copy your key and username

If you feel lost, calmly go back through the steps
</details>

### Adafruit IO Feed and Colorpicker creation
In adafruit
<details open>

1. Dashboards > New Dashboard 
2. Name it Colorpicker, put in the description that you want
3. Once made click on it
4. Make a new block by clicking on the corkwheel and clicking "Create new Block"
5. Click the color picker, it should be a blue circle once hovering over it it should say "Color picker"
6. Create the feed name "color"
7. Create block
8. Select the feed you just made and click "Next step"
9. Choose a color through the color picker
10. Create it (you might need to choose a color again, idk why they did this but don't ask me)

This should hopefully go smoothly
</details>

### Editing code
<details open>

1. In Arduino: File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
2. In the tab ‘config.h’: paste your Adafruit IO Key and username
3. In the tab ‘config.h’: input your wifi network and password
    - 🚨 The NodeMCU does not work on 5Ghz WiFi 🚨
    - Preferably use the hotspot on your phone, this barely uses any data (less than 0.1mb an hour)
4. In the Tab adafruit_14_Neopixel.ino
    - Edit: #define PIXEL_PIN 5 to #define PIXEL_PIN D5
    
This should hopefully go well.
</details>

### Uploading Code
<details open>

1. Upload the code
2. Turn on the "serial monitor"
3. Open the serial monitor at the bottom of your IDE
4. Put the monitor on "115200 Baud"
5. If everything works well it should say that your monitor is connected
    - If it's not working:
        - Check if your board is connected to your device, if not connect/plug it.
        - Check if your board is connected properly.
        - Check if your libraries are installed correctly.
6. Go back to [Adafruit IO](https://io.adafruit.com/) and change the color in your color picker, you will see feedback in the serial monitor
7. If the led light is connected and you can edit the colors through the Adafruit IO color picker....

🥳 CONGRATULATIONS YOU MADE YOUR OWN PHILIPS(Signify) HUE!! 🥳
For maybe a few bucks? Adafruit also works on mobile! 😁👍
</details>

### Sources
 - [The Adafruit IO Quickguide made by the teachers](https://docs.google.com/document/d/14jhaxaJUhuu0p6_u_oNj8_50Y6PAmtrvcePtKc0HDGs/edit?usp=sharing)

</details>

</details>

# Telegram Ledstrip
<details open>

##  First Try

<details open>

### Installing the libraries
- Open the libraries tab and download the following:
    - Install UniversalTelegramBot by Brian Lough
    - Install ArduinoJson by Benoit Blanchon

### Installing Telegram and creating a bot
- Open Telegram and make a Telegram account
- Search for the BotFather
<img src="https://i.gyazo.com/57bd44fa2332bf159b12591aa5bb36ed.png" width="375px" alt="The BotFather">

- Follow the setup for a new bot
<img src="https://i.gyazo.com/f0a67450174155640180bc3bd18a7853.png" alt="BotFather Conversation">

- Keep the bot name, username and bot token
- Copy this code into Arduino:
```
#include <ESP8266WiFi.h>
#include <WiFiClientSecure.h>
#include <TelegramBot.h>

#define LED 15
#define DATA_PIN D5

const char* ssid = "wifi_username";
const char* password = "wifi_password";

const char BotToken[] = "bot_token";

WiFiClientSecure net_ssl;
TelegramBot bot (BotToken, net_ssl);

void setup()
{
  Serial.begin(115200);
  while (!Serial) {} //Start running when the serial is open
  delay(3000);
  Serial.print("Connecting WiFi.");
  Serial.println(ssid);
  while (WiFi.begin(ssid, password) != WL_CONNECTED)
  {
    Serial.print(".");
    delay(500);
  }
  Serial.println("");
  Serial.println("WiFi connected");
  bot.begin();
  pinMode(LED, OUTPUT);
}
void loop() 
{  
  message m = bot.getUpdates(); // Read new messages  
  if (m.text.equals("on")) 
  {  
    digitalWrite(LED, 1);   
    bot.sendMessage(m.chat_id, "LED is ON");
  }  
  else if (m.text.equals("off")) 
  {  
    digitalWrite(LED, 0);   
    bot.sendMessage(m.chat_id, "LED is OFF");  
  } 
}
```
- Fill in wifi_username/wifi_pass and bot_token
- Make sure your Arduino is connected 
<img src="https://i.gyazo.com/8a400f8599551d8f3acc9e89acbe50b6.jpg" alt="connected Arduino">

- Verify the code
<img src="https://i.gyazo.com/90506e511d885f17daf4e0e9fd57cd91.png" alt="Exit Status 1">

- Get Error Code: Exit Status 1
- Google the error code
<img src="https://i.gyazo.com/4ccfffb5a383ea985f536ca196d73038.png" alt="Fall into Despair">

- Cry your heart out
- Try messing with the code trying to see an issue
- Do not succeed
- Cry again

</details>

## Second Try
<details open>



</details>

</details>

# Markup quicksheet
```
coding area
```

 - testing
    - testing
    
1. Testing
    - Testing

<details open>
Details area
</details>

[url usage atm with in document linking](https://github.com/Falicer/IoT/edit/main/README.md#internet-of-things)

| another test | test| 
| --- | --- |
| testing | Testing |
</details>
