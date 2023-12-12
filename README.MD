# Requirements
* #### 16×2 I2C Liquid Crystal Display (LCD)
* #### ESP32-CAM AI-Thinker
* #### Miscellaneous
# Initialization
Install all the dependent Arduino libraries
## 1. Install ESP32 Board in Arduino IDE
* ### [Windows](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/)
* ### [Mac and Linux](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-mac-and-linux-instructions/)
## 2. Install the LiquidCrystal_I2C Library
* ### [Download](https://github.com/marcoschwartz/LiquidCrystal_I2C/archive/master.zip)
* Unzip the .zip folder and you should get LiquidCrystal_I2C-master folder
* Rename your folder from LiquidCrystal_I2C-master to LiquidCrystal_I2C
* Move the LiquidCrystal_I2C folder to your Arduino IDE installation libraries folder
* Finally, re-open your Arduino IDE
## 3. Insert your Network Credentials in `secrets.h`
* ### `SECRET_SSID` Your internet name
* ### `SECRET_PASS` Your internet password
## 4. Reassign Pins
  * ### Windows
    * Find `pins_arduino.h`  under ``C:\Users\USER_NAME\AppData\Local\Arduino15\packages\esp32\hardware\esp32\VERSION_OF_LIBRARY\variants\esp32``
    * Change
       ```
       static const uint8_t SDA = 21;
       static const uint8_t SCL = 22;
       ```
      to
       ```
       static const uint8_t SDA = 15;
       static const uint8_t SCL = 14;
       ```
    * ## Remember to switch it back after compile

*
   ### Mac
  *  dont ask me
## 5. Wire the hardware
* Check under `CameraLCD.fzz`
* ### After uploading the code, disconnect `GPIO 0` from `GND` (yellow wire).
