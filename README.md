##link to [Instructable](https://www.instructables.com/id/Standalone-ATmega328p-using-Internal-8-MHz-Clock/)##

# ATmega328p-pu-Bootloader-burner-sketch-uploader
Using this Repository you can minimise the size of your projects and make them a lot cheaper. This is done by reducing the number of components of the development board such as onboard LEDs, external Crystal oscillators, external Capacitors and many other redundant components built into the development boards.

List of Parts needed

1. 10K ohm resistors
2. ATmega328P-PU IC
3. Jumper Wires
4. LM7805 Voltage Regulator
5. Breadboard
6. Arduino Uno Development board

We also need Arduino IDE to Burn Bootloader and upload sketches to ATmega328P. You can download it from [here](https://www.arduino.cc/)

You also need to download Arduino on a Breadboard library. You can download it from [here](https://www.arduino.cc/en/Tutorial/ArduinoToBreadboard) according to your IDE version.

## Uploading Bootloader to ATmega 328P

The ATmega328P IC does not come preloaded with a Bootloader. The Bootloader is a set of code that allows the IC to interpret code that we upload using Arduino IDE.

**Steps to upload Bootloader to ATmega328P**

**Connect Arduino to ATmega328P as shown in the image.**

Connections are listed as follows:-

1. ATmega328P pin 7 => Vcc
2. ATmega328P pin 8 => Gnd
3. ATmega328P pin 20 => Vc
4. ATmega328P pin 22 => Gnd
5. ATmega328P pin 1 => pin D10 of Arduino
6. ATmega328P pin 17 => pin D11 of Arduino
7. ATmega328P pin 18 => pin D12 of Arduino
8. ATmega328P pin 19 => pin D13 of Arduino
9. pull up resistor across pin 1 of ATmega328P

**Add board to your IDE:**

> Make a folder named Hardware(if it is not present already) in your sketch folder and extract and copy the downloaded library to that folder.

> Restart the IDE and search for a new Board in menu of Tools > Board, you should see a new board named "ATmega328 on a breadboard (8MHz Internal Clock)". If you see this board everything is fine so far.

**Select Serial port.**

**Select programmer to "Arduino as ISP".**

**Burn Bootloader by going to Menu Tools > Burn Bootloader.**

## Sketch Uploader Circuit

You can upload sketches to ATmega328P using your Arduino board.

**Steps to upload sketches to ATmega328P**

**Remove IC from Arduino.**

**Connect Arduino to ATmega328P as shown in the image, **
**Connections are listed as follows:**

1. ATmega328P pin 7 => Vcc
2. ATmega328P pin 8 => Gnd
3. ATmega328P pin 20 => Vcc
4. ATmega328P pin 22 => Gnd
5. ATmega328P pin 1 => Reset pin of Arduino
6. ATmega328P pin 2 => pin 1 or RX pin of Arduino
7. ATmega328P pin 3 => pin 2 or TX pin of Arduino
8. pull up resistor across pin 1 of ATmega328P

**Upload Sketch to Atmega328P using Arduino IDE.**

**Connect pins to ATmega328P according to pin mapping diagram.**
