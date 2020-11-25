===============================================================================
HOW to upload firmware to the control board
1. Download Upload tool from the below link: https://github.com/ZONESTAR3D/Firmware-Upload-tool
2. refer to the guide in the link and upload firmware to the control board
===============================================================================

===============================================================================
If you have a 128x64 LCD screen please do the below steps on LCD MENU after upload firmware:
1. Initliza EEPROM:  Configuaration>>Advance settings>>Initlize EEPROM
2. Fine Tune PID parameter of hotend: Configuaration>>Advance settings>>Temperature>> PID AutoTune E1: 190, set to 200 if you used to print PLA filament and 240 degree if you used to print ABS filament, and then wait about 10 minute until it finished.

If you use TFT-LCD screen,  please do the below steps:
1. Initliza EEPROM: 
copy ResetNVRAM.gcode to the SD card and print it.

2. Fine Tune PID parameter of hotend: 
if you used to print PLA filament, copy CalNozzleTemp_200c.gcode to the SD card and print it, if you used to print ABS filament,
CalNozzleTemp_240c.gcode and print it.
===============================================================================

===============================================================================
About Features:
===============================================================================
Deafult features:
=============================================================================
1. TITAN Extruder:
In the older version, Z9 use a default extruder part, from 2020-05, we have upgraded it to Titan exturder, by using Titan extuder, it can provide more torque to extruder this feature is default on since V5.3

2. Power off after printer:
a POWER push button (Non self locking button) can be connected to the control 
board, when power on, you need to push button until LCD show LOGO, add a M81 
command in the ENDcode of slicing software, it can realize automatic shutdown 
after printing. 
NOTE: It is only shut down the control board, but not the Power supply
  Hardware:
  -a push button should connect to the power on jumper.
  -a LED connect to VCC & GND
this feature is default on since V5.3.x
Puchase link: https://www.aliexpress.com/item/1005001633938984.html

=============================================================================
Option feature:
=============================================================================
Filament run out sensor:
This feature is default on, don't need to upgrade the firmware please check on configuaration menu of the LCD screen to active it:
Purchase link: https://www.aliexpress.com/item/4001309957376.html

TMC220x:
TMC220x motor dirver is reversed on the work direction with A4988
PS:If you only changed (X, Y,Z) driver modules, please modify the X(YZ) motor wires and use the default firmware(without TMC220x at the firmware file name).
About the detail of how to modify the motor direction by modifying motor wire, please refer to "How to change the motor work direction.png" 
Puchase link: TMC2208: https://www.aliexpress.com/item/4000596369015.html
Puchase link: TMC2209: https://www.aliexpress.com/item/1005001664336751.html

TFT-LCD:  	 	
TFT-LCD screen use EXP1 connector pins of +5/GNG/D16/D17,it is connected to UART2 of ATMEGA2560
D16<=>TXD2 
D17<=>RXD2
ATTENTION: for ZRIB control board, TFT-LCD and LCD12864 can't work at the same time 
Puchase link: https://www.aliexpress.com/item/1005001314076252.html

Dual Z Driver:
Defaulf Z9 use a sync single Z drive system, you can upgrade it to dual Z motor with or without 2nd Z endstop.
Purchase link:  https://www.aliexpress.com/item/1005001633367116.html

3Dtouch:
Defaulf Z9 use a proximity sensor as a bed leveling sensor, if you upgrade it to BLtouch or 3D touch, please choose this firmware
Hardware:
D4 - SERVO PIN (S PIN of 3DTouch)
Z+ - Probe Pin (Z- PIN of 3DTouch)
Purchase link:  https://www.aliexpress.com/item/1005001464420529.html


