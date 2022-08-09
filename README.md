# SofarSolar-esphome-HomeAssistant
sofar solar integration

if you ever need to get solar production info from sofar solar 4ktlm-g2 or any other RS 485 connected solar inverter. We'll be using ESP8266 MCU and esphome integration. 

you need some 
1) ESP8266 MCU board
2) MAX485 or MAX3485 TTL to RS485 board


Connections:

ESP ----> TTL conversion unit

DI6 (RX) ---- RO

DI5 (READY) --- DE+RE (short them)

DI7 (TX)   ---- DI

Vin --- VCC

GND --- GND

RS485 - to A and B


loosely based on https://github.com/cmcgerty/Sofar2mqtt , so  you can use the connection images .

install esphome on your laptop/device

run "esphome run esp-config.yaml" to upload to device over usb, after that you can push it by OTA. You should get an IP in log.

then just add a device in home assistant, integration name esphome - and IP from previous step

connection image:

![image](https://user-images.githubusercontent.com/30725259/183476696-01aa7e7d-daf3-4743-8eff-4946b4aa1f20.png)

![image](https://user-images.githubusercontent.com/30725259/183583805-1b7c1d04-2118-447c-a932-b01329ccc8cd.png)

you can scan by free modbus master tool (2.0.3.0 by Graham A Ross) to find the required registry value

![image](https://user-images.githubusercontent.com/30725259/183636515-77bb27c7-dc96-438a-8e06-47df4e9a86cf.png)

