# IOT-Node
A Simple one way ESP-NOW Code (DHT11 &amp; OLED 

Full tutorial at https://cifertech.net/iot-node-esp-now-based-project/

#### In this project information from multiple ESP8266 boards via the ESP-NOW communication protocol with a one-to-Many scenario. several ESP boards send the data we want to one board. There is no such thing as a transmitter or receiver in ESP-NOW documents. Each ESP8266 board can be a transmitter or a receiver. However, we will use these terms to describe the status of each board in the project
![IMG_8100](https://user-images.githubusercontent.com/62047147/153008554-04e31421-38dc-4490-a67f-40418888fdaf.jpg)


#### In order to establish connections in this project, we use a PCB designed with the help of Altium Designer. This circuit includes the connections required for OLE modules and DHT11 sensor, as well as the power input and serial output to program the board. There is also a relay in this circuit that will not work due to a bug in this version of the PCB.
![bandicam 2022-01-29 13-33-37-955](https://user-images.githubusercontent.com/62047147/153008918-b0b9c117-9252-424f-83e4-6b1faca7e623.jpg)
