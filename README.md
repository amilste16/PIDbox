# CAD
[The Prototype in Onshape](https://cvilleschools.onshape.com/documents/b60c5c3ae011e78cf6a2a1bd/w/4e3c6e2f779413a1c7802b2b/e/10d812ac343aef4f061d0bf0)
I kinda went ham on it, so I probably only need to tweak a few things before it's done.
[The Finished Box](![image](https://user-images.githubusercontent.com/60236713/121032411-40f99200-c779-11eb-8fd2-341d6d2728b0.png)
---
# Code
[First Draft Psuedo Code]
Code to turn on the box. 
Specifically the fan.
A code to tell the fan how fast it should spin and its limit.
Also to tell it that its limit is close and it should slow down.
We also need a code to tell us the speed of the fan and how close it is from its limit.
A couple of codes for the circuit to know what to do with certain wires.
A code that will turn on an LED that will on when the box is on. (Optional)
---
[Planning Doc](https://docs.google.com/document/d/1k4LJgq82fT34C9mZyrUpwUVt9hEWU7Jjr8YUoJkSeJ4/edit?usp=sharing)

# Code for LCD

from lcd.lcd import LCD

from lcd.i2c_pcf8574_interface import I2CPCF8574Interface

#some LCDs are 0x3f... some are 0x27.

lcd = LCD(I2CPCF8574Interface(0x3f), num_rows=2, num_cols=16)
