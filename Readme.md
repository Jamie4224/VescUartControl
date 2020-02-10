## Improved RollingGeckos VescUartControl library

Added functions to RollingGeckos library for reading and setting the mcconfig via UART. Works with Vesc Version 3.41.

### Updated By Jamie4224 for VESC FW 4.02
For example to adjust the max speedlimit or powerlimit 
with the help of a small mcu (ESP8266 etc.)
Can be used to change of motor profile via wifi.

Won't be able to run on Atmega32p (Arduino Nano / Uno 2k is to little memory) 
ESP8266/ESP32 works fine. 

Example "VescUartSample.ino" got tested on my Vesc6 and works fine.

Usage: 

VescUartGet(mc_configuration mcVal) fills the struct mcVal with the 
current mc-config. returns 1 if successful communication with vesc, 0 if not.

VescUartSet(mc_configuration mcVal) write the struct mcVal to the vesc. 
returns 1 if successful communication with vesc, 0 if not.

VescUartGet(bldcMeasure values) fills the struct values with the 
current telemetry data like before. returns 1 if successful communication with vesc, 0 if not.
