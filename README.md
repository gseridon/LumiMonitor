# Si7021 Temperature and Humidity Module
# Build Instructions
-----

## Author: Gino Seridon

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/EnclosedProject%231.jpg">

## Table of Contents
-----

1. [Introduction](https://github.com/gseridon/LumiMonitor#Introduction)
2. [Specifications](https://github.com/gseridon/LumiMonitor#Specifications)
3. [Design](https://github.com/gseridon/LumiMonitor#Design)
4. [Acquisition](https://github.com/gseridon/LumiMonitor#Acquisition)
5. [Assembly](https://github.com/gseridon/LumiMonitor#Assembly)
6. [Testing and Power Up](https://github.com/gseridon/LumiMonitor#Testing-and-Power-Up)
7. [Production Testing](https://github.com/gseridon/LumiMonitor#Production-Testing)

-----

## Introduction

-----

This readme will allow the user to build and assemble a functioning temperature and humidity reader using the si7021 sensor in conjunction with the Raspberry Pi 4.

The document will cover all points of the build, from the materials, budget and time commitment, to the mechanical assembly, testing, and power up. It will also cover all the problems that was encountered during the project, steps to take to prevent them from occurring, as well as highlighting steps that may cause problems in the future. 

While the project was completed over a 13-week semester, following this build instruction should allow the user to have an assembled and functional module within 4 hours, given that the required materials and components have already been ordered and ready to be used. 

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/ProjectSystemDiagram.png">

The system diagram above visualizes how the Si7021 Temperature and Humidity sensor retrieves data and interacts with the Raspberry Pi 4 to process the readings of the sensors.

-----

## Specifications

-----

A complete list of all parts, components, tools, and materials needed for this project will be listed below. Assuming that the user does not own the components, this will be the breakdown of the budget (in Canadian dollars, before shipping):

| Component                                                    | Price (CAD)       |
| ------------------------------------------------------------ | ----------------- |
| [Si7021 Temperature and Humidity Sensor Breakout Board](https://tinyurl.com/yybwv9qn) | $12.86            |
| [CanaKit Raspberry Pi 4 Starter Kit (4GB RAM)](https://tinyurl.com/vg57wxr) | $134.99           |
| [Printed Circuit Board (PCB)](https://www.seeedstudio.com/free-assembly-for-5-pcbs.html) | $5.21 ($3.92 USD) |
| [Clear Acrylic Casing](https://www.protocase.com/design/send-your-cad.php) | $35.00            |
| [Headers for the PCB ](https://tinyurl.com/ufy8mfr)          | $21.99            |
| [Jumper Wires](https://tinyurl.com/unpvbn7)                  | $15.99            |
| [22 Gauge Insulated Wires](https://tinyurl.com/wlea6bo)      | $18.99            |
| [Ethernet Cable](https://tinyurl.com/sbod2cs)                | $8.29             |
| [Ethernet-USB Adapter](https://tinyurl.com/tccs4yx)          | $20.05            |
| [Nuts and Bolts Kit](https://tinyurl.com/vyvv2pt)            | $31.98            |
| **Total**                                                    | **$305.25**       |

With these items, the cost will be **$305.25 + $39.70** in tax, totaling to **$344.93.** The Ethernet Cable and Ethernet-USB Adapter are optional, as the user will be able to connect their Raspberry Pi to a computer monitor if it has an HDMI port. If the monitor does not have an HDMI port, then the user must use the cable and adapter. The cost will be reduced depending on which items the user already has in possession.

The total cost of the budget will vary depending on the shipping cost, but it should be around the same price range. Considering that the Printed Circuit Board and Acrylic Casing has been obtained from Humber College, the price used for the PCB and the casing will be an accurate estimate.

The cost of shipping is not included as it can vary depending on different factors, such as the address on where the products will be shipped, the shipping method, and membership discounts/free shipping perks. 


-----

## Design

-----

The design files are important for the project, as they will dictate the appearance of the printed circuit board and the casing. The design of the printed circuit board is simplistic, as there are only four (4) pins used by the si7021 sensor and therefore the connections made from the sensor the RP4 are straightforward.

The creation and the design of the PCB is done using the free software <a href="https://fritzing.org/home/">“Fritzing.”</a> This program will provide a <a href="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/BreadboardV1.png">breadboard view</a> of the connections, a <a href="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/SchematicV1.png">schematic</a>, as well as a view of the <a href="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/PCBV1.png">printed circuit board</a>. There are two Fritzing files used: one to display the breadboard and the schematic, and another for the designed PCB (this will be the file used when creating the PCB).

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/PCBV1.png">

The design is simplistic and neat in order to reduce complications. The files can be tweaked for personal customization, but they are perfectly useable in terms of functionality. There were very little problems when designing the PCB, however, be mindful of the VIA hole size, as it may cause problems when finding a suitable size wire. Obtaining this component will be described later on in the Acquisition Section.

The enclosure is a design that was retrieved <a href="https://www.thingiverse.com/thing:3729316">online</a>. It uses cover design that allows the acrylic to bend over the raspberry pi, with several ventilation holes to help regulate the heat of the RP4.

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/EnclosureDesign.PNG">

The <a href="https://github.com/gseridon/LumiMonitor/blob/master/Mechanical/Raspberry_Pi_4_Model_B_Retro_Case_-_All_Parts_v2.0.cdr">design file</a> can be accessed and edited using the program “CorelDRAW”, which offers a 15-day trial for new users. 

Obtaining this component will be described in the Acquisition Section.


-----

## Acquisition

-----

The parts and components needed for this project is listed in the specification. They can be found online, and links are also provided in the specifications section. Allow a couple of days for delivery, depending on the shipping type used to deliver the parts.

Acquiring the PCB and the enclosure will require a bit more time, as they must be custom made based on the design files submitted. It takes around 4-5 business days to process the custom request and to have it delivered to a specified address. Plan ahead of time when it comes to this, as this will be the biggest cause of delays should there be problems down the line, especially when getting it replaced.


**The Printed Circuit Board**
-----

The PCB design will be sent to Seeedstudio, a company that can manufacture circuit boards. The company requests that the Gerber Files of the project be sent as ZIP or RAR files in order to proceed with the PCB manufacturing. 

To create an order with <a href="https://www.seeedstudio.com/free-assembly-for-5-pcbs.html">Seeedstudio</a>:

\-   Open the <a href="https://github.com/gseridon/LumiMonitor/blob/master/Electronics/GinoSeridon_TemperatureHumiditySensorWithoutPiV2.fzz">PCB Design File</a> in Fritzing

\-   Export the file as an Extended Gerber 

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/Acquisition1.png">

\-   Select a folder to export the files into

\-   Compress the folder into a ZIP or RAR file

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/Acquisition2.png">

\-   File is created

\-   Upload this newly created ZIP or RAR file on the Seeedstudio website and follow the steps online.

Note that if some of the PCB specifications are changed, the price will also change accordingly. The site will provide an estimate on how long it will take for the PCB to be manufactured and when it will arrive.


**The Enclosure**
-----

The enclosure design will be sent to Protocase, a company that can manufacture cases and enclosures, among other services. To request for a custom design enclosure, we must export the CorelDRAW file as a .dwg file. This file is uploaded into the repository and it will be used to place the order for the enclosure.

To order from Protocase:

\-   Access the website’s <a href="https://www.protocase.com/design/send-your-cad.php">page</a> for custom enclosure orders

\-   Send the design by selecting “Upload your file using request a quote form”

\-   Select “I have 3D CAD file(s) to upload”

\-   Upload the .dwg file

\-   Select “Part(s) or Enclosure(s) from other materials” for the type of enclosure

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/Acquisition3.png">

\-   Select the Material type as “Acrylic”, with a thickness of “ 0.118’’ | 3.0mm”

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/Acquisition4.png">

\-   Fill out the rest of the form with personal information and submit

\-   Wait for an email from Protocase; this will contain the quote on the enclosure

\-   Follow the email and steps for ordering the case.

Awaiting the PCB and the enclosure will take around a week, so keep that in mind when setting deadlines.


**Tools and Software**
-----

Lastly, on top of the parts, components, and materials needed for the project, there are also some tools required to setup and assemble the project. These tools include:

\-   Windows PC

\-   computer monitor (preferably with an HDMI port; if not, then an Ethernet cable and Ethernet-USB adapter is required)

\-   computer mouse

\-   computer keyboard

\-   ohmmeter

\-   solder iron and lead

\-   wire stripper

\-   wire cutter

\-   breadboard

\-   Phillips Screwdriver

Software programs needed include:

\-   <a href="https://fritzing.org/home/">Fritzing</a>

\-   <a href="https://www.coreldraw.com/en/pages/ppc/coreldraw/?pt=test&sourceid=cdgs2019-xx-ppc_brkws&x-vehicle=ppc_brkws&gclid=EAIaIQobChMI9fDNtuGp5gIVxZyzCh2-8QdQEAAYASAAEgL6B_D_BwE">CorelDRAW</a>

\-   <a href="https://www.balena.io/etcher/">balenaEtcher</a>
 

-----

## Assembly

-----


Once the components, tools, and materials have been acquired, the project can be assembled.


**Installing Raspbian onto the Rasberry Pi 4:**
-----

The Raspberry Pi must first be setup. On a running Windows Computer, download “Raspbian Buster with desktop and recommended software” from the <a href=” https://www.raspberrypi.org/downloads/raspbian/”>Raspberry Pi Website</a>. When that has completed, insert the microSD card into the USB reader (both from the Raspberry Pi Starter Kit) and then plug it in a USB port on the computer.

Launch balenaEtcher to mount the Raspbian into the microSD card. In balenaEtcher, select Raspbian as the Image, select the USB reader as the drive, and then click “Flash!” Wait for the Flashing and Validating to finish, and then safely eject the USB reader and leave it aside for the meantime.

Proceed by connecting the Raspberry Pi 4 to a mouse to its USB port, a keyboard to the other USB port, and its power supply to the microUSB port. The RP4 comes with its own HDMI cable, and it will be connect to the Pi’s HDMI port to a monitor’s HDMI port.

Place the microSD card in the microSD reader of the Raspberry Pi 4, then power up the Raspberry Pi using the power supply’s power button. The Operating System that was Flashed into the microSD card will automatically be installed on to the new Raspberry Pi. Follow the setup instructions that appear on the screen (and remember any password changes that are made), and the Raspberry Pi will be ready for future use. This section should not take more than half an hour, depending on download speed and processing speed.
 

**Si7021 Sensor/Header Soldering:**
-----

The Si7021 Temperature and Humidity Sensor should come with its own header. Since the header will not fit on the breakout board initially, use wire cutter so that there will only be 5 pins left on the header. The header will fit perfectly on the board, and the pins should then be soldered. Soldering the 3V pin is optional, as it will not be used. This should take no more than 10 minutes.

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/Assembly1.png">


**Soldering Headers and VIAs on the Printed Circuit Board:**
-----

Headers must be soldered on the printed circuit board in order to connect the raspberry pi and the sensor to it. There will be two headers needed for this: 1x5 header, and 2x3 header.

First, the 1x5 header will be soldered first. This header will be placed on the topside of the PCB, with the pins being soldered at the bottom side (for reference, the student name and pin names will be on the topside of the PCB). When the header is placed on the topside, turn over the PCB and proceed with soldering the pins to the board. Ensure that the solders are clean and that they do not make contact with other pins on the board. The pins to be soldered are GND, SCL, SDA, and 3vin (the labels can be found on the topside of the PCB); the lone pin without any connections does not need to be soldered.

The second header will then be soldered afterwards. This header will be placed on the bottom side of the PCB, with the pins being solder at the topside of the board. Place the header on the bottom side of the PCB, then turn over the PCB to proceed with soldering the pins. There will be two pins that do not need to be soldered, and it will be the two pins that do not have any connections or labels attached to them. The four pins that will be soldered are the GND, SCL, SDA, and 3Vin.

Finally, when both headers are soldered to the board, the VIAs will be soldered using the 22 gauge insulated wires (these will be thin enough that they will be able to fit through the VIAs). Use the wire stripper to remove the insulation, and fit the wire through the VIA. One end of the wire will be soldered, ensuring that the solder is making contact with the copper wiring on the board. After one end is finished, cut the other end of the wire on the opposite end of the soldered VIA. The remaining insulation is removed from the wire, and then the wire end is soldered to the copper around the VIA. The end result should look like a wire soldered on both ends that is passing through the VIA. Proceed to do these steps until all 4 of the VIAs are connected.

Try to make sure that the solder points are done quickly and neatly. If soldered for too long, some areas of the board may overheat and become unusable, which may cause problems down the line. Do not use too much solder, as it may melt over to neighbouring wires, causing a short in the circuit. Do not rush soldering, but it should not take longer than an hour for this section.

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/PCBSolderedV2Front.jpg">

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/PCBSolderedV2Back.jpg">


**Assembling the Enclosure with the Raspberry Pi:**
-----

**Note: Due to the nature of the enclosure, it is highly recommended that the Raspberry Pi 4, the Printed Circuit Board, and the Si7021 Temperature and Humidity Sensor are all configured, tested, and are fully functional before assembling them with the enclosure.

The enclosure is comprised of four pieces, the two side pieces, the bottom piece, and the large, overhead piece. Start by placing the raspberry pi on the bottom piece, aligning the case’s mounting holes with the Raspberry Pi’s. Secure the raspberry pi to the bottom piece using nuts and bolts.

Based on the orientation of the Raspberry Pi, the two side pieces of the enclosure should be attached to the bottom enclosure piece with accordance to the Raspberry Pi’s ports (one of the side pieces will have holes for the RP4’s ports, while the other does not). Use this knowledge to determine which side piece will fit with the bottom enclosure piece.

Attach the printed circuit board to the raspberry pi’s pins (the first 6 pins at the top of the pi, as seen on the breadboard connection), as well as four jumper wires on the proper pins of the circuit board (one for GND, SCL, SDA, and 3Vin).

Closing the case using the overhead piece is the trickiest part of using this case. Start on the end with the microSD card reader of the RP4. Fit the top piece of the enclosure to the bottom piece where the microSD card hole will be, and then use a single nut and bolt to hold and secure the two pieces together.

Slip the four jumper wires through the top slit near a mounting hole of the overhead piece. Connect these four jumper wires to the Si7021 sensor while keeping in mind the proper GND, SCL, SDA, and 3Vin pins. When the wires are connected, move the sensor so that it is resting on top of the case, and the breakout board’s mounting hole aligns with the mounting hole on the case. Use a nut and bolt to secure the sensor’s position. Afterwards, carefully bend the casing until it encloses the entire raspberry pi, and that it will connect to the bottom case piece on the other side. This side will also have another mounting hole to hold the case in its place using a nut and bolt. This part should take around half an hour, assuming the user takes their time and handles the components with care.

**The final result:**

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/EnclosedProject%235.jpg">

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/EnclosedProject%232.jpg">

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/EnclosedProject%233.jpg">
 

-----

## Testing and Power Up

-----

**Note: Due to the nature of the enclosure, it is highly recommended that the Raspberry Pi 4, the Printed Circuit Board, and the Si7021 Temperature and Humidity Sensor are all configured, tested, and are fully functional before assembling them with the enclosure.

Before testing the Raspberry Pi, the sensor and printed circuit board must be tested. It is simple enough to test: the soldered connections will be tested using an ohmmeter and some jumper wires. The sensor and printed circuit board can be plugged in a breadboard to make the connections clearer and easier to trace. Connect the PCB and sensor to the proper pins using jumper wires, connect it to a power supply, and then measure the resistance in the circuit. If the ohmmeter is reading an infinite resistance, it means that there is no electrical current flowing through the circuit that is being measured. If this is the case, look over the soldered pins and VIAs and ensure that the soldered points appear like a sloping hill, or a "Hershey Kiss".

Once it is verified that the PCB and sensor are soldered properly, the next step is to ensure that the Raspberry Pi is up to date with its libraries. Use the following commands from the command line to update the raspberry pi:

```
sudo apt-get install upgrade

sudo apt-get install update

sudo apt-get install i2c-tools
```
 

Once that’s done, run this command to install the Adafruit library:

```
sudo pip3 install adafruit-circuitpython-si7021
```
 
Then we need to enable the I2C bus on the Pi.

\-   Run sudo raspi-config

\-   Select Interfacing Options

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/TestingAndPowerUp1.png">

\-   Select P4 SPI

<img src="https://raw.githubusercontent.com/gseridon/LumiMonitor/master/Images/TestingAndPowerUp2.png">

\-   Select Yes when prompted to enable SPI and when asked about automatically loading the kernel module

\-   Select Finish and confirm that the system will reboot

To test the sensor, attach the printed circuit board to the raspberry pi’s pins (the first 6 pins at the top of the pi, as seen on the breadboard connection), as well as four jumper wires on the proper pins of the circuit board (one for GND, SCL, SDA, and 3Vin). Connect these four jumper wires to the Si7021 sensor while keeping in mind the proper GND, SCL, SDA, and 3Vin pins.

Run this command on the command line:

```
sudo i2cdetect -y 1
```

This will display the open address being used and will display a hexadecimal value representing the module. If the si7021 sensor is being detected properly the address that you will see will be 40.

After confirming that the sensor is being detected, write the code for the sensor. To create the file, type in the command line:

```
nano si7021_test_code.py
```

“si7021_test_code.py” is the file name. Write in the code in this file (this code is also uploaded in the <a href="https://github.com/gseridon/LumiMonitor/blob/master/Software/si7021_test_code.py">repository</a>):

```
import time
import board
import busio
import adafruit_si7021

# Create library object using our Bus I2C port
i2c = busio.I2C(board.SCL, board.SDA)
sensor = adafruit_si7021.SI7021(i2c)


while True:
    print("\nTemperature: %0.1f C" % sensor.temperature)
    print("Humidity: %0.1f %%" % sensor.relative_humidity)
    time.sleep(2)
```


To run this file, either find the file in the Pi’s directory and run the program using Python, or type in a command in the terminal:

```
python ./si7021_test_code.py
```

If all is working well, the sensor should be actively reading the temperature and humidity of its surroundings and updating these values every second on the screen.

<img src="https://github.com/gseridon/LumiMonitor/blob/master/Images/CodeTest.jpg">

This whole section should take around an hour, with variance depending on the speed of download.
 

-----

## Production Testing

-----

Based on the components alone, this project is realistically not viable for mass production due to the sheer price of the Raspberry Pi 4. The project can be done using an Arduino, which costs less than the Raspberry Pi, however the steps that will be taken to create a functional project may be vastly different compared to what was explained in this build.

Assuming that the Raspberry Pi 4 will be used for production testing, the actual testing for the components will be relatively simple. The PCBs will be mass soldered and will be tested for connectivity at the end of the production line using a simple resistance test. The main testing procedure for the sensor would be to connect it to a tester Raspberry Pi and attempting to detect the sensor through the I2C command. If the sensor’s address does not show, it will be sent to a reject pile to be checked for quality.

The case may need to be changed for mass production due to the delicate nature of the enclosure; breakage may occur more often without the constant supervision of human workers. Changing the enclosure to a case that can easily be assembled would be the better alternative.
