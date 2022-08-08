# SofarSolar-esphome-HomeAssistant
sofar solar integration

if you ever need to get solar production info from sofar solar 4ktlm-g2 or any other RS 485 connected solar inverter. We'll be using ESP8266 MCU and esphome integration. 

you need some 
1) ESP8266 MCU board
2) MAX485 or MAX3485 TTL to RS485 board


Connections:
ESP ---- TTL conversion unit
DI6 (RX) ---- RO
DI5 (READY) --- DE+RE (short them)
DI7 (TX)   ---- DI
Vin --- VCC
GND --- GND

RS485 - to A and B

loosely based on https://github.com/cmcgerty/Sofar2mqtt , so  you can use the connection images .

