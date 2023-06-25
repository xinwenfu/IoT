# ESP32

## Microcontroller (MCU)

A  is basically a small computer. It's a type of System on Chip (SoC). We know the CPU is the central processing unit or processor, the brain of a computer. However, the CPU needs other components to be really useful, such as RAM, I/O and flash storage. The MCU often has a CPU, main memory - RAM, and the other necessary components to execute code.

## ESP32

ESP32 is a MCU made by Espressif. It has a dual core processor clocked at 230 Mhz. It has a particular circuit to speed up the crypto algorithms like AES, SHA2 and RSA. The ESP32 has 520 KB of SRAM, Wi-Fi, bluetooth and 32 I/O pins. Those IO pins can interact with the external sensors, actuators and other things. Here is the block diagram of the ESP32 microcontroller. The ESP32 doesn't have the embedded flash itself.

![image](Espressif_ESP32_Chip_Function_Block_Diagram.png)

## ESP32 Module
Various *ESP32 modules* are created to include the ESP32 MCU, embedded flash, crystal (for the RTC), an antenna and other components and work fully as a computer. 
A module has the flash memory so that it can contain programs, data, configuration parameters and other data.
The flash is connected to the ESP32 via the SPI bus and the supported capacity is up to 16Mb.
The official Espressif module (ESP-WROOM-32) includes a 4Mb flash memory.
A crystal is basically a clock, which is needed by the CPU to run.
An antenna is needed by Wi-Fi and bluetooth to reach a decent communication range.
Different manufacturers may integrate different components onto the module.

## ESP32 Development Board 

An ESP32 development board may contain an ESP32 module and other supporting components on a printed circuit board (PCB) so that programmers can try to become acquainted with the ESP32. We may also test our project code on the development board.
In the real world, we may have to develop our own PCB with an ESP32 MCU or an ESP32 module to achieve desired functionalities.
For example we can integrate a SD card or sensors onto the PCB so that the ESP32 is used to read the sensor data data and store it on the SD card. Of course, the ESP32 supports WiFi and Bluetooth and can send the data over the Internet. 

![image](https://github.com/xinwenfu/IoT/blob/main/imgs/IoTkit-FrontBack.png)

Out IoT kit is a development board. The ESP-WROOM-32 module we use doesn't support USB, but UART. The micro-USB port on our IoT kit is used to power up the development board and program the ESP32. A USB-UART bridge chip on the development board is used to convert a USB signal into a UART signal. UART is a kind of communication protocol supported by most microcontrollers.

The pins on our IoT kit are the extension of the pins of the ESP32. Conductive traces on the PCB connect them together. The space between two pins on the ESP32 is very so small. It is not easy to connect extra components such as extra sensors to the ESP32. The extension pins on our IoT kit make it easy to connect extra components to the IoT kit. For example, our IoT kit can be used with a breadboard and jump wires to test various sensors.

There are various ESP32 development boards on market.


## Pin Layout

