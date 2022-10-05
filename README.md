# Internet of Things
By Raekwon Gerold

## Table of Contents 🗂

1. 🏮 [Philips Hue](https://github.com/Falicer/IoT/edit/main/README.md#philips-hue-assignment)

# Philips Hue Assignment
Before doing this you gotta do a few steps first:

### Install the Adafruit Library
<details open>

1. Open the library manager of your Arduino IDE
2. Look up "Adafruit IO Arduino"
3. Install it/ "Install All"

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

# Markup quicksheet
<details closed>
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
