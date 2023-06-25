# Porgramming V2 of IoT kit

For our version 2 of the IoT kit, we will use Visual Studio Code (VS Code), an open source code editor made by Microsoft. Various extensions can be added to VS Code and support particular programming languages, debuggers, and tools. We will use the ESP-IDF extension by Espressif.

However, sometimes, we want to use Espressif tools from a terminal within our Ubuntu VM. We can launch those tools within VS Code by opening a terminal with the ESP-IDF extension.

## VS Code + ESP-IDF
1. [Installation](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md)
2. [Basic use of the extension](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/basic_use.md)

Load, build and flash an example project
- Start VS Code
- File -> Open Folder 
  - Example project: /home/iot/esp/esp-idf/examples/wifi/scan
- ESP-IDF Build project
- ESP-IDF Flash device -> UART
  - If “No such file or directory: '/dev/ttyUSB1'”, pressing F1, typing "ESP-IDF: Select port to use:" -> /dev/ttyUSB0
  - During connecting to /dev/ttyUSB0, may need to hold the BOOT (IO0) button of the ESP32 until uploading starts
  - If still errors, unplug and re-plug the kit
  - If still errors, change a USB port since different USB ports may provide different power supplies
- ESP-IDF Monitor device
- Press reset button of the IoT kit
- File -> Close Folder
- Close a project

If IDF_PATH has issue, refer to 
[Add IDF_PATH & idf.py PATH to User Profile](https://docs.espressif.com/projects/esp-idf/en/v3.3.1/get-started-cmake/add-idf_path-to-profile.html)

### Load a project
Load a project by opening the project folder.

<img src="../../imgs/vscode-espidf-openfolder.png">

### Build, upload firmware via icons

<img src="../../imgs/vscode-espidf-icons.png">


## Native ESP-IDF programming environment
This is a great guide on [Get Started - ESP32 - — ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/).

Set up the environment variables
```
. $HOME/esp/esp-idf/export.sh
```
