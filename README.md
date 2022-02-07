# IoT

Creating the environment
1. [Create Ubuntu VM from the .iso image](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview)
   - Ubuntu username: IoT; Password: toi
2. [Install VS Code](https://code.visualstudio.com/download)
3. [Install PlatformIO IDE for VSCode](https://platformio.org/install/ide?install=vscode)
4. Add the user IoT into the group dialout so that IoT can use ttyusb0
   - [Permission denied: '/dev/ttyUSB0](https://askubuntu.com/questions/133235/how-do-i-allow-non-root-access-to-ttyusb0)
     - sudo usermod -a -G dialout $USER
5. Programming 
   - [Get started with ESP-IDF and ESP32-DevKitC: debugging, unit testing, project analysis](https://docs.platformio.org/en/stable/tutorials/espressif32/espidf_debugging_unit_testing_analysis.html)
   - Note: follow the steps. Otherwise, errors such as wrong baud rate may happen
