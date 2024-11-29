

# Modbus library for STM32 Microcontrollers - CMSIS V1

This is a fork of (https://github.com/alejoseb/Modbus-STM32-HAL-FreeRTOS) modified to use FREERTOS CMSIS V1. 

For more information about examples and use, please refer to the original repository.

## Recommended Modbus Master and Slave testing tools for Linux and Windows

### Master and slave Python library

Linux/Windows: https://github.com/riptideio/pymodbus

### Master client Qmodbus
Linux:    https://launchpad.net/~js-reynaud/+archive/ubuntu/qmodbus

Windows:  https://sourceforge.net/projects/qmodbus/

### Slave simulator
Linux: https://sourceforge.net/projects/pymodslave/

Windows: https://sourceforge.net/projects/modrssim2/

## TODOs:
- Implement isolated memory spaces for coils, inputs and holding registers.
- Implement wrapper functions for Master function codes. Currently, telegrams are defined manually. 
- Improve function documentation
- ~~MODBUS TCP implementation improvement to support multiple clients and TCP session management~~ (10/24/2021)
- ~~Improve the queue for data reception; the current method is too heavy it should be replaced with a simple buffer, a stream, or another FreeRTOS primitive.~~ Solved Queue replaced by a Ring Buffer (03/19/2021)
- ~~Test with Rs485 transceivers (implemented but not tested)~~ Verified with MAX485 transceivers (01/03/2021)
- ~~MODBUS TCP implementation~~ (28/04/2021)
