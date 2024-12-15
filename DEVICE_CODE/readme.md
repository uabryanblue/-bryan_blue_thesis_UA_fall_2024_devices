# 735nm Project  

This project required the created of multiple MicroPython programs to run on the different ESP8266 microcontrollers. There are three major components and a calibration routine.  
  
## 735nm_calibrate  
A basic code base that allows the calibration of k-type thermocouples (TC) using the Temperature Relay Control hardware. It is a command line, interactive program that records off a user supplied id for the TC and a reference temperature. The code then runs a routine that periodically reads values until a specified number of consecutive readings have a range of a specified precision. Most readings were recorded with a range of no more than 0.75 degrees celcious. This can be controlled using the constants that are defined at the top of main.py.  
  
## 735nm_data_logger  
An ESP8266 microcontroller based data logger. It receives all packets from the other remote sensors and records the information into appropriate files on a microSD card. System logs, TRC values, and aspirated readings from a BME280 board.  
<more here>  
  
## 735nm_TRC  
Temperature Relay Control (TRC) code that uses five k-type thermocouples to create a sensor/control system that uses on/off control on a relay to monitor and adjust the attached heating pad. Temperatures of the heated leaf and a control leaf are measured to turn the heating pad on/off based on the desired temperature range that needs to be achieved.  
<more here>  
  
## 735_THP  
A BME280 based aspirated temperature, humidity, and pressure sensor.  
<more here>  
