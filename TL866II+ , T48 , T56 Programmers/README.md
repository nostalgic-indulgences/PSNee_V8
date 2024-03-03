# TL866II+, T48, T56 (XGecu) Programmers via XGPRO

This guide utilizes the TL866II+, T48, T56 series of programmers that you can buy off AliExpress.  
In the following guide, I'll be using my T56 as an illustrative example.  
_For peeps who have the QFP32>DIP28 adapter, you can follow through most of the guide as well except that you will stick with the default ZIF socket interface!_

![T56_ICSP](images/ICSP.png)  

Download the latest version of XGPRO here:-  
http://www.xgecu.com/en/download.html

## Supported Platforms
PsNee V8 supports the following MCU's:  
- ATmega328(A/P/PA) @16Mhz  
- ATmega168(A/P/PA) @16Mhz

## Hardware Connection  
Connect your programmer to the Arduino Nano / Clone / Custom PCB using the appropriate ICSP (In Circuit Series Programmer) Header orientations below:-  

> Arduino Nano / Clone ICSP Pinout Diagram

![NANO_ICSP](images/NANO_ICSP.png)

> TL866II+ ICSP Pinout Diagram

![TL866II_ICSP](images/TL866II_ICSP.png)
  
> T48 ICSP Pinout Diagram  

![T48_ICSP](images/T48_ICSP.png)

> T56 ICSP Pinout Diagram  

![T56_ICSP](images/T56_ICSP.png)

## Programming

**_!!! Please note that the ICSP on the Arduino Nano / Clone boards are 5V intolerant !!!_**  
**_The Vcc output from the programmers are 5V only!!!_**  
**_Connect the board to the USB port directly for power. The on-board 3.3V LDO will step down the voltage accordingly._**

![XGPRO](images/XGPRO0.png)

Please follow the sequence in the diagram above.
> 1. Select the correct MCU in the dropdown list
  
![MCU_SELECT](images/XGPRO1.png)

  i. Type in the MCU of your choosing (ATmega328P / ATmega168P)  
  ii. Select the MCU in TQFP32 package _(Select DIP28 package if you're using the QFP32>DIP28 adapter)_
  
> 2. Select the correct connection interface type > "ICSP Port".  
>    Uncheck the "ISCP_VCC Enable" checkbox.

> 3. Check connectivity to the MCU by attempting a "Read" operation.  
>    If error, check all the connections again.
  
> 4. Download the appropriate HEX file that corresponds to your console:-  
https://github.com/nostalgic-indulgences/PSNee_V8/tree/main/HEX
  
Load the HEX file you have downloaded and leave all the settings as default.
  
![)AD_HEX](images/XGPRO2.png)

> 5. Select the "CONFIG" tab to set the fuses based on the 2 criteria below:-
    
**For ALL CONSOLES besides JAP_FAT version**

![ALL_EXCEPT_JAP_FAT](images/XGPRO32.png)

**For JAP_FAT CONSOLES only**
  
![JAP_FAT](images/XGPRO31.png)
  
  i. Select the checkboxes based on your console version  
  ii. Verify your fuse settings based on the following criteria:-
    
  **All CONSOLES besides JAP_FAT - L: FF | H: DF | E: FF**  
  **JAP_FAT consoles - L: EE | H: DF | E: FF**
  
> 6. Hit "**Prog.**" and you are all set!
