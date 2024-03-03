# TL866II+, T48, T56 (XGecu) Programmers via XGPRO

This guide utilizes the TL866II+, T48, T56 series of programmers that you can buy off AliExpress.  
In the following guide, I'll using my T56 as an illustrative example.  

![T56_ICSP](images/ICSP.png)  

Download the latest version of XGPRO here:-  
http://www.xgecu.com/en/download.html

## Supported Platforms
PsNee V8 supports the following MCU's:  
- ATmega328(A/P/PA) @16Mhz  
- ATmega168(A/P/PA) @16Mhz

## Hardware Connection  
Connect the USBasp programmer to the Arduino Nano / Clone / Custom PCB using the corect ICSP (In Circuit Series Programmer) Header orientation below:-  

![NANO_ICSP](images/NANO_ICSP.png)

> TL866II+ ICSP Pinout Diagram

![TL866II_ICSP](images/T866II_ICSP.png)
  
> T48 ICSP Pinout Diagram  

![T48_ICSP](images/T866II_ICSP.png)


## Programming

![AVRDUDESS](images/AVRDUDESS.png)

Please follow the sequence in the diagram above.
1. Select the correct programmer in the dropdown list
2. Select the correct port > usb
3. Select the correct MCU > ATmega328P / ATmega168P
4. Select the correct pre-compiled HEX file that corresponds to your console:-
- https://github.com/nostalgic-indulgences/PSNee_V8/tree/main/HEX
5. Set your fuses based on the following criteria and ensure the "set fuses" checkbox is selected:- 
- JAP_FAT consoles: **L: EE | H: DF | E: FF**  
- All other consoles: **L: FF | H: DF | E: FF**
6. Select the tickbox to erase the flash of the MCU
7. Hit "**Program!**" and you are all set!
