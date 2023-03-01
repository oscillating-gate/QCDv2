QCD firmware version 2.1

Works on all PCB v2.x

Trigger303 Update environment setup
1. Plug USBASP to PC
2. Install libusb-win32 driver by Develop/Tools/zadig
3. Connect USBASP to QCD module's ISP header (Face red stripe to white line)

Trigger303 Update procedure:
1. Build .hex file with Microchip Studio (See Microchip Studio Project directory)
2. Copy .hex into Develop/Tools/avrdude-x.x-mingw32
3. Open Develop/Tools/avrdude-x.x-mingw32 in command prompt
4. Execute the command below:
    .\avrdude.exe -P usb -c usbasp -p atmega328p -U flash:w:QCDv2.hex -v -v

Changelog:
v2.1
Calibration mode to set Div/Mult detent positions

v2.0.1
Bug fixed to sync clock outputs

v2.0
Updated for ATMEGA328 chip
