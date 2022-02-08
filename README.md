# IoT Lab Environment--Breadboard Version

Creating the environment
1. [Create Ubuntu VM from the .iso image](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview)
   - Ubuntu username: IoT; Password: toi
2. [Install VS Code](https://code.visualstudio.com/download)
3. [Install PlatformIO IDE for VSCode](https://platformio.org/install/ide?install=vscode)
4. Add the user IoT into the group dialout so that IoT can use ttyusb0
   - [Permission denied: '/dev/ttyUSB0](https://askubuntu.com/questions/133235/how-do-i-allow-non-root-access-to-ttyusb0)
     - sudo usermod -a -G dialout $USER
5. Programming 
   - Clone [ESP-IDF Components library](https://github.com/UncleRus/esp-idf-lib)
   - Use ESP-IDF on PlatformIO: [Espressif IoT Development Framework under PlatformIO](https://docs.platformio.org/en/latest/frameworks/espidf.html#examples)
     - Add EXTRA_COMPONENT_DIRS: 
```
list(APPEND EXTRA_COMPONENT_DIRS esp-aws-iot)
```
   - [Get started with ESP-IDF and ESP32-DevKitC: debugging, unit testing, project analysis](https://docs.platformio.org/en/stable/tutorials/espressif32/espidf_debugging_unit_testing_analysis.html)
   - Note: follow the steps. Otherwise, errors such as monitor speed rate may happen
   - [pio\libdeps\esp32dev\DHT sensor library\DHT_U.h:36:29: fatal error: Adafruit_Sensor.h: No such file or directory](https://community.platformio.org/t/pio-libdeps-esp32dev-dht-sensor-library-dht-u-h29-fatal-error-adafruit-sensor-h-no-such-file-or-directory/21861)
     - The solution is simple. Add the following include statements to main.cpp:
       - #include <Adafruit_Sensor.h>
