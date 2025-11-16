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
#include<reg51.h>
void main()
{
unsigned char x,y;
unsigned int i;
P1=0x00;
while(1)
	{   
	x=0x01;
	for(y=0;y<8;y++)	
		{
		P1=x;
    for(i=0;i<60000;i++);
    x=x<<1;
    }			
	}	
}
```


## Output:

<img width="1916" height="1109" alt="image" src="https://github.com/user-attachments/assets/c4d482d3-6c18-42a1-9a72-f1119aa182c6" />


## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

