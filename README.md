# LED-Interfacing-Using-8051

## Aim:
To interface an LED with the 8051 microcontroller and control its operation.

## Apparatus Required:
•	Laptop with Keil uVision software
•	Proteus Design Suite

## Circuit Diagram Setup in Proteus:
1.	Open Proteus and create a new project.
2.	Add the following components from the library:
o	8051 Microcontroller (AT89C51)
o	LED
o	Resistor (330Ω)
o	Ground (GND) connection
3.	Connect the LED's anode to P1.0 of the microcontroller through a 330Ω resistor.
4.	Connect the cathode of the LED to GND.
5.	Save the design and proceed to programming in Keil.

## Algorithm:
1.	Configure P1.0 as an output port.
2.	Set P1.0 HIGH to turn ON the LED.
3.	Introduce a delay.
4.	Set P1.0 LOW to turn OFF the LED.
5.	Introduce a delay.
6.	Repeat the process continuously.


## Program:
```
ORG 0000
L:MOV DPTR,#0100H
MOV R1,#0AH
BACK: CLR A
MOVC A,@A+DPTR
MOV P2,A
ACALL D
INC DPTR
DJNZ R1,BACK
SJMP L
D:MOV R5,#05
B2:MOV R3,#255 
B1:MOV R4,#255
AG:DJNZ R4,AG
DJNZ R3,B1
DJNZ R5,B2
RET
ORG 0100H
DB 3FH,06H,5BH,4FH,66H,6DH,7DH,07H,7FH,6FH
END
```

## Output:
<img width="1379" height="745" alt="MPMC EXP 7" src="https://github.com/user-attachments/assets/a0ed47e3-894f-485e-9eb1-b28e3847354c" />



## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

