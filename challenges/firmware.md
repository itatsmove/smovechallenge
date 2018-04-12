# Firmware Challenge

In this challenge, you will be given a block diagram of a system which includes a Raspberry Pi and an Arduino (either Uno or Leonardo) connected together. Your objective is to implement source code for both Pi and Arduino to perform some tasks.

### System block diagram
<img width="628" alt="screen shot 2018-04-12 at 11 22 53 am" src="https://user-images.githubusercontent.com/5736715/38654811-de1d4dfa-3e43-11e8-832d-6d1f3cf5a3ec.png">

In the above figure, a PI communicates to an Arduino via I2C interface so that the Pi can control 2 Relays and read a fuel sensor voltage which are connected to the Arduino. The Pi will act as I2C master and Arduino will be I2C slave; the 7-bit I2C slave address can be arbitrary value. The two relays are connected to pin 3 and 5 while pin A0 is for fuel input ADC. There is an UART terminal which connect to the Pi via and USB to UART cable so that user can interface with the ralays and fuel sensor using a predefined AT command set.


Your tasks are to:
1. Write a Python script to receive/response to AT command from UART-Terminal (for example: we will use “/dev/tty-ACM0” as serial device name) and control the Arduino input/output interfaces, the AT command set will include following commands:

| Condition                | Terminal to Pi | Pi responses to terminal                                                                                                 |
|--------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------|
| Python script is started |                | ^RESET                                                                                                                   |
|                          | AT+RLYON=1     | ^OK<br />Then set command Arduino to turn on Relay 1                                                                          |
|                          | AT+RLYON=2     | ^OK<br />Then set command Arduino to turn on Relay 2                                                                          |
|                          | AT+RLYOFF=1    | ^OK<br />Then set command Arduino to turn off Relay 1                                                                         |
|                          | AT+RLYOFF=1    | ^OK<br />Then set command Arduino to turn off Relay 2                                                                         |
|                          | AT+SENS=?      | ^OK<br /><last fuel sensor read value (unit of 0.01V)><br /><br />for example: if sensor ADC value is 2.5V the Pi will respond: <br />^OK<br />250 |

All command and response will be followed by `<CR><LF>` characters. The Pi script also periodically (1 second) check for fuel sensor.



2. Write an Arduino script for the Arduino to:
  * Receive I2C commands from the Pi to turn on/off the two relays and response fuel sensor read value to the Pi
  * The Arduino’s pin 7 is to control power input to the Pi. The Arduino will reset the Pi if there is no I2C communication in 10 seconds

Note: you can design your own I2C message exchange between the Pi and Arduino, you can use any open-source library to support your scripts and please indicate libraries’ names in your scripts or a readme.
