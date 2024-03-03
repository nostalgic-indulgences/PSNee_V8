# USBasp via AVRDUDESS

This guide utilizes the USBasp programmer that you can readily buy off AliExpress.  
Ensure it's the USBasp version with the 10-pin>6-pin adapter and not the USBISP variety.  

![AVRDUDESS](images/AVERDUDESS.png)  

Install the drivers for the USBasp programmer by following the steps here:-  
https://www.instructables.com/USBASP-Installation-in-Windows-10/

Download the latest version of AVERDUESS here:-  
https://blog.zakkemble.net/avrdudess-a-gui-for-avrdude/  

Connect the USBasp programmer using the corect ICSP (In Circuit Series Programmer) Header orientation below:-
  
![AVRDUDESS](images/AVERDUDESS.png)

## Supported Platforms
PsNee V8 supports the following MCU's:  
- ATmega328(A/P/PA) @16Mhz  
- ATmega168(A/P/PA) @16Mhz

## Hardware Connection  
Connect the USBasp programmer using the corect ICSP (In Circuit Series Programmer) Header orientation below:-
![AVRDUDESS](images/ICSP.png)

## Installation
Connect the programmer to the Arduino Nano via 6 pin header (or your custom chip)

Please follow the sequence in the diagram above.
1. Select the correct programmer in the dropdown list
2. Select the correct port > usb
3. Select the correct MCU > ATmega328P / ATmega168P
4. Select the correct pre-compiled HEX file that corresponds to your console:-
- https://github.com/nostalgic-indulgences/PSNee_V8/tree/main/HEX
5. Set your fuses based on the following criteria and ensure the "set fuses" checkbox is selected:- 
- JAP_FAT consoles: **L: EE | H: DF | E: FF**  
- All other consoles: **L: FF | H: DF | E: FF**
6. Hit "Program" and you're done!
