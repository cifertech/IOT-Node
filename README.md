<div align="center">

  <img src="https://user-images.githubusercontent.com/62047147/195847997-97553030-3b79-4643-9f2c-1f04bba6b989.png" alt="logo" width="100" height="auto" />
  <h1>IOT Node</h1>
  
  <p>
    A Simple one way ESP-NOW Project (DHT11 &amp; OLED) 
  </p>
  
  
<!-- Badges -->

<p>
<a href="https://github.com/cifertech/IOT-Node" title="Go to GitHub repo"><img src="https://img.shields.io/static/v1?label=cifertech&message=IOT-Node&color=white&logo=github" alt="cifertech - IOT-Node"></a>
<a href="https://github.com/cifertech/IOT-Node"><img src="https://img.shields.io/github/stars/cifertech/IOT-Node?style=social" alt="stars - IOT-Node"></a>
<a href="https://github.com/cifertech/IOT-Node"><img src="https://img.shields.io/github/forks/cifertech/IOT-Node?style=social" alt="forks - IOT-Node"></a>
   
<h4>
    <a href="https://twitter.com/cifertech1">TWITTER</a>
  <span> · </span>
    <a href="https://www.instagram.com/cifertech/">INSTAGRAM</a>
  <span> · </span>
    <a href="https://www.youtube.com/c/cifertech">YOUTUBE</a>
  <span> · </span>
    <a href="https://cifertech.net/">WEBSITE</a>
  </h4>
</div>

<br />

<!-- Table of Contents -->
# :notebook_with_decorative_cover: Table of Contents

- [About the Project](#star2-about-the-project)
  * [Pictures](#camera-Pictures)
  * [Features](#dart-features)
- [Getting Started](#toolbox-getting-started)
  * [Schematic](#electric_plug-Schematic)
  * [Installation](#gear-installation)
- [Usage](#eyes-usage)
- [Contributing](#wave-contributing)
- [License](#warning-license)
- [Contact](#handshake-contact)

  

<!-- About the Project -->
## :star2: About the Project
In this project information from multiple ESP8266 boards via the ESP-NOW communication protocol with a one-to-Many scenario. several ESP boards send the data we want to one board. There is no such thing as a transmitter or receiver in ESP-NOW documents. Each ESP8266 board can be a transmitter or a receiver. However, we will use these terms to describe the status of each board in the project

<!-- Pictures -->
### :camera: Pictures

<div align="center"> 
  <img src="https://user-images.githubusercontent.com/62047147/195977373-216a5743-2175-45c6-837f-a79216e5ceb2.jpg" alt="screenshot" />
</div>

<!-- Features -->
### :dart: Features

- Transmission and display of temperature data
- Transmission and display of humidity data

<!-- Getting Started -->
## 	:toolbox: Getting Started

We used two ESP8266 boards, version 01, which are assembled in a personalized PCB, in one of the boards, or in other words, our nodes, an OLED display is installed to display the received items, and in the other board. A DHT11 sensor is installed to measure temperature and humidity.

- ESP8266-01
- Oled 0.91 SSD1306
- DHT11 sensor
- 10k resistance

<!-- Schematic -->
### :electric_plug: Schematic

In order to establish connections in this project, we use a PCB designed with the help of Altium Designer. This circuit includes the connections required for OLE modules and DHT11 sensor, as well as the power input and serial output to program the board. There is also a relay in this circuit that will not work due to a bug in this version of the PCB.

- ESP01 And Oled

| ESP01| Oled 0.96|
| ----   | -----|
| GPIO2 | SCK |
| GPIO0 | SDA |
| 3v3 | Vcc |
| GND | GND |

- ESP01 And DHT11

| ESP01| DHT11|
| ---- | -----|
| Tx  | Data |
| 3v3 | Vcc |
| GND | GND |


* Complete Schematic

<img src="https://user-images.githubusercontent.com/62047147/195977951-bcb13c2f-1a66-4a2e-a629-2610ba408244.jpg" alt="screenshot" width="800" height="auto" />

* 3D View 
<img src="https://user-images.githubusercontent.com/62047147/195978444-fc444762-ec16-4aa3-b4f8-dee0ee8a9e09.jpg" alt="screenshot" width="400" height="auto" />


<!-- Installation -->
### :gear: Installation

#### If you are interested in fully learning this project, you can see the [Tutorial blog](https://cifertech.net/iot-node-esp-now-based-project/) or the [YouTube video](https://www.youtube.com/watch?v=fXhsV-RXuXQ&t=11s) I made about this project.


- This part of the code is the MAC address of the Master board that is entered on all Slave boards.

```c++
uint8_t broadcastAddress[] = {0xFC, 0xF5, 0xC4, 0x82, 0xCD, 0x49};
```

- we mentioned that if the number of slaves increases, an ID will be specified for each board, in this line of code, you must make the relevant changes. In fact, each Slave board has its own unique ID.

```c++
#define BOARD_ID 1
```
   
   
   
<!-- Usage -->
## :eyes: Usage

Finally, after uploading both codes introduced in ESP8266 boards, all the mentioned items related to the prerequisite settings are observed. You will see the values displayed on the OLED display, or you can print the values on the Arduino software monitor serial if needed. Finally, the values will be sent by Slave boards to our Master board.

<!-- Contributing -->
## :wave: Contributing

<a href="https://github.com/cifertech/IOT-Node/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=cifertech/IOT-Node" />
</a>


<!-- License -->
## :warning: License

Distributed under the MIT License. See LICENSE.txt for more information.


<!-- Contact -->
## :handshake: Contact

CiferTech - [@twitter](https://twitter.com/cifertech1) - CiferTech@gmali.com

Project Link: [https://github.com/cifertech/IOT-Node](https://github.com/cifertech/IOT-Node)

