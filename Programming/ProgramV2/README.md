# Porgramming V2 of IoT kit via VS Code + ESP-IDF

For our Version 2 of the IoT kit, we will use Visual Studio Code (VS Code), an open source code editor made by Microsoft. Various extensions can be added to VS Code and support particular programming languages, debuggers, and tools. We will use the ESP-IDF extension by Espressif.

However, sometimes, we want to use Espressif tools from a terminal. We can launch those tools within VS Code by opening a terminal with the ESP-IDF extension.

## Setup (Optional)
1. [Installation of VS Code ESP-IDF extension](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md)
2. [Basic use of the extension](https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/basic_use.md)

## Load, build and flash an example project

Please refer to [Get started with ESP32 via VS Code and the ESP-IDF extension](https://github.com/xinwenfu/tst-dht-lab).

### Load a project
Load a project by opening the project folder.

<img src="https://github.com/xinwenfu/IoT/blob/main/imgs/vscode-espidf-openfolder.png" width=720>

### Build, upload firmware via icons

<img src="https://github.com/xinwenfu/IoT/blob/main/imgs/vscode-espidf-icons.png" width=720>

## Native ESP-IDF programming environment
Within VS Code, on the menu bar, click *Terminal*->*New Terminal* to start a new terminal and use the native ESP-IDF programming environment.
This is a great guide on [Get Started - ESP32 - — ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/).

Set up the environment variables before using all the command line tools.
```
. $HOME/esp/esp-idf/export.sh
```
