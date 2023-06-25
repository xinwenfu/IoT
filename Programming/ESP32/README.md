# ESP32

## Microcontroller

A microcontroller is basically a small computer. It's called a System on Chip which may be abbreviated to SoC. System on Chip means that everything is put on one chip
and that chip is the main component of the computer. If you are given just a CPU you cannot really do anything because we also need accessories. We need a  motherboard, main memory - RAM, we need to get user input with a keyboard, and we need many other things to actually utilize and communicate with the cpu. We need to utilize a lot more than just the cpu to get it to  can work on and execute the code. The microcontroller normally has everything it needs to execute code; it has a CPU, flash memory, main memory - RAM, and the other necessary accessories to execute code.

Let's first look at the ESP8266, the predecessor of the esp32. Both ESP8266 and ESP32 are microcontrollers. 
The ESP8266 is a kind of  system on a chip. It has a lot of things already integrated on the chip so it's ready to be integrated intowith  your product. The ESP8266 was pretty good, and is very cheap and very robust. When the ESP8266 first came out the firmware was really bad, the firmware of the chip was developed by amateurs. However they found the chip was very powerful, so the maker community developed alternative frameworks like the NodeMCU which is the most popular one, and the one we are using. The problem with the ESP8266 is that it has no security, and that's why in September 2016 they released another version of a similar chip. The ESP32.



Slide 4: ESP32

Compared with the ESP8266 the ESP32 is actually pretty powerful, it's dual core
processor clocked at 230 Mhz. This is a very powerful CPU compared with other low power microcontrollers, as many of the low power microcontrollers run at about 14 or 16 megahertz.  The reason they are clocked at low speeds isis that they want to achieve no energy consumption.  This one i guess is not really designed for low power consumption products because the cpu speed is so high. The ESP32 can run all the crypto algorithms even just using the software without hardware accelerators, but it also has the hardware acceleration. This means it has a particular circuit to speed up the crypto algorithms like AES, SHA2 and RSA. The ESP32 chips support acceleration of RSA but even if you just use the software itself and you don't use the hardware acceleration it's pretty decent.  People often think IoT  uses low end components a kind of a really low end of uh stuff,that don't support encryption and other things but that's wrong. Even the 14 MHz microcontroller can do all the crypto calculations “”. The main only reason IoT devices are not secureyou know lt is not secure is a is people don't know how to program them to be secure.When you program those chips and you want to add security encryption and other security features things into your software you have to learn more things.  The SRAMram  of the ESP32 is about 520 kilobytes, it has Wi-Fi, bluetooth and it also has a 32 IO pins. Those IO pins can interact with the external sensors, actuators and other things as there is almost an unlimited number of possibilities with what you can interact with using them . 

Slide 5: Block Diagram

Here is the block diagram of the ESP32 microcontroller. On the left there is a block for SPI which is a communication port. This is a module itself; the ESP32 doesn't have the embedded flash itself; it is something you can add to the module. The embedded flash is added so you can put your code on it and the ESP32 can store and access it. The ESP32 has all the communication ports as well. The problem is that you need the flash, clock and other things to directly use the ESP32 chip.

Slide 6: ESP32 Modules

That's why we have something called an ESP32 module. The What happens is the ESP32 System on Chip is as we know missing a few things necessary for direct use. That's why people make ESP32 modules, for example a module will add the following components to the ESP32 system on chip. A module will add a flash memory so that it can contain firmware and data, a crystal and it is basically a clock this is necessary as a cpu runs on clock signals, and an antenna so that wi-fi bluetooth can reach a reasonable decent distance.

This module contains the ESP32 system on chip, flash memory, antenna, and a clock integrated inside this chip so it's become another system on  chip which you  can use directly. These modules are more for practical use as you don't have to add all the necessary components manually yourself. It integrates the ESP32 and other necessary accessories, and you may want to integrate other things into these modules, think well i want a sd card and the one i want to integrate sd card into hereif you are the manufacturer you can., as t They design the modules so if you want to add a SD card to the module directly you have to be the manufacturer, They just added those components to esp32 so this will work as a minimum System on Chip. There are different versions of modules for the ESP32, and you can see here the version on the left  is
called the ESP-WROOM-32 and the one on the right is an ESP-32S. Manufacturers integrate different components onto the module, or they may have different layout or some other things but the core part is still the ESP32.


If you just have a CPU you have to add all the other things yourself, so that you can use this CPU. The System on Chip means they already add the necessary components so you can at least run code. If it is not a System on Chip and just a CPU you have to add all other necessary components to make it a minimum working unit.
The ESP32 SoC has ROM SRAM and other components but it does not have flash memory, so you can see the difference.
SoC is a minimum working unit!


Slide 7: Flash
{Image on Slides}

This is the  flash (see highlighted aria of image), when you remove the cover of the larger ESP32 module this is the inside. They integrated a lot of other things around the ESP32 chip, you can see the flash and other supporting circuits. This image is of the ESP-WROOM-32 this is the one we are using.  People may be confused about the relationship between the ESP32 module (The large silver/metal square with ESP-WROOM-32 on it) and the larger device it is located on. 




Slide 8: Development Board 

The ESP32 module is on a PCB board which provides and extends the functionality of the ESP32 module by connecting it to more circuits. This whole thing is called a development board. Normally they are used for testing your project. You can use the whole development board on your product but normally this is just for you to test your code and see if it works. In the real industry you have to develop your own circuits around the ESP32 modules. Normally you purchase a ESP32 module and you develop your own board and then everything will work. For example you can integrate a SD card or other sensors onto your own board. This development board is designed for you to do the testing.


This image is of the development board,  it has a so we add the micro-USB port which is used to so you can power up the development board and ESP32module easily. This micro-USB port also works as a data communication channel. You can see labeled in the image a USB-UART bridge, the ESP32 module itself doesn't support usb. We use this bridge, the USB-UART chip to convert the USB signal into a UART signal. UART is another kind of communication protocol supported by most microcontrollers. That's why we needed this bridge, this chip to convert the micro usb signal into the url signal so that the ESP32 can understand the signal. Why do we have so many legs along the sides? 

Those legs are only the extension of the legs of the microcontroller itself, there are wires from
the chips legs here to the large legs on the side of the board here . The reason this is done is  the space between two legs on the chip of the microcontroller is very so small. This makes it very hard for normal people to use. To try and solder something onto the leg of the chip is very hard, but soldering it onto the larger leg, which is connected to the chip’s leg by a wire, is much easier. The larger legs are an extension of the chip module itself as they are directly connected by a wire.

Normally you do not use a development board in the final production, it is used to test to code.



Slide 9: ESP32-WROOM-32

The ESP-WROOM-32, this is the one module made by one manufacturer and this is one kind of ESP32 module. We have the USB-UART bridge mentioned before, this provides up to 3 Mbps of transfer rates. There are two buttons on the development board. One is called reset, this means you want to restart the code execution from the beginning inside of this chip. The boot button is used when flashing the code, you push the button and you can flash your code into the chip. Sometimes you may not have to press the boot button to get the firmware download to work,if you cannot flash your code into the microcontroller you need to push the boot button. The micro-USB port acts as both a power supply and data communications cable, the cable used must contain both a power and data line. If the cable only has a power line you will be unable to communicate with the device. The IO pins, the legs on the sides of the development board, some legs are power or ground but most are for IO some will be for input, and others output. Input is sending data into the chip, and output is sending data out of the chip, most legs are for both input and output - two way communication, but some are for only input or only output.


Slide 10: Pin Layout

This is the layout for those IO pins. On the left, are all the pins. You should assume the function of this chip has a micro-USB port, and you need to orient your device to be the same as the one in the diagrams. The top left pin is a power source of 3.3V, that's why  have this cable inserted to this legs column allowing this board to serve as a power source. Our sensor needs a power source and that's why we connect the 3.3V leg to the positive leg of the sensor.

The top right pin is the  ground leg, and because we need a loop, a closed circuit both a power and a ground we connect the ground leg of the ESP32 to the negative leg of the sensor. The data leg of the sensor is connected to GPIO port 22. GPIO stands for General Purpose Input Output and GPIO22 is used for a particular communication protocol I2C. This sensor is using the I2C protocol which is why we need to connect the dataline of the sensor to GPIO22, if this is not done it will not work. Different sensors will use different protocols, you will need to look at the documentation of a particular sensor to see which pin you will need to connect it to.    


Slide 11: Chart of IO pins



This is the definition of all the IO pins and all the legs. you need to refer to this chart here to
understand the layout. 
