# CAD
[The Prototype in Onshape] I kinda went ham on it, so I probably only need to tweak a few things before it's done.

![image](https://user-images.githubusercontent.com/60236713/121033188-f6c4e080-c779-11eb-812c-8172e47d30c3.png)
---
[The Finished Box] It took a while, but here is the finished box
![image](https://user-images.githubusercontent.com/60236713/121032411-40f99200-c779-11eb-8fd2-341d6d2728b0.png)

The dimensions of the box are 150 mm by 100 mm by 105 mm. I used the thicken tool by selecting a face and its parallel, on the New tab, with Direction 1 being 3 mm. (Repeat twice more) Deleted the core piece. Then I used the Laser Joint tool, selected all parts on the Automatic tab, and set # of pins to 2. I used the T Slot Joint tool to select all 4 faces of the tab the Laser Joint created on Part 1, set the specs to an ANSI #4 13 mm screw with a Hex Machine Nut with a close fit, 10 mm from the edge, 1 connector, clicked Equal Spacing and Add Nut Connector. I repeated this step for 4 more times, excluding parts 5&6. 

I made a sketch on part 6 to create a hole for the 9V battery pack, with screw holes to attach. I drew a rectangle, 63 mm by 90 mm, with a 90 mm centered construction line. The larger sides are equally distanced from the edges, but one of the smaller sides being 16.83 mm from the edge. On the opposite small side, I made a screw hole, 2.95 mm in diameter, 4.14 mm from the rectangle, and 8 mm from the rectangle's center line. I then mirrored the hole around the center line. Then I used Extrude, clicked Solid, Remove, selected the sketch, and Through All.


In the Assembly, I clicked Automatic Grouping to mate the faces together. I inserted my fan, a DC motor, my motor holder, a 9V battery pack, and LCD screen with backpack, a panel mount potentiometer, a panel mount LED, 2 panel mount switches, a T slot photointerupter, an ArduinoUno, an ArduinoUno prototyping shield, a mini breadboard, and 3 25x.5 Aluminum Hex Male Female standoffs. 

After mating the DC motor in the center of part 5 with its rounded sides facing the long edges, and the Photointerrupter's feet 53 mm from the center along the 90 mm center line, each with an offcet of -3 mm on the Y, I selected part 5 and clicked Edit In Context to make a sketch on it's face. I selected the outline of the DC motor and clicked the Use(Convert/Project) tool. I did the same for the 2 oval shaped holes on the Photointerupter. Then I created a 2 circles with a diameter of 3 mm, 8.73 mm from each flat edge of the DC outline. These will be for the motor holder.

I created the motor holder in a seperate document. I made my first sketch on the Top plane, I made a rectangle that is 16 mm by 11 mm, the 11 mm side are 8 mm from the Front plane, and one 16 mm side is 8 mm from the Right plane. There is a circle inside the rectangle that's center is along the Front plane, is 3 mm from the 16 mm side furthest from the Right plane, and has a diameter of 3 mm. I mirrored this rectangle and circle around the Right plane and exited the sketch. I Extruded Sketch 1 with a Blind depth of 5 mm, protruding upwards from the Top plane. Next I created a new sketch off the bottom face of Extrude 1. I created 2 rectangles that are 11 mm by 5 mm, their 11 mm side matches up with the existing rectangle's side closest to the origin. I Extruded both of them 13.6 mm, towards the Bottom plane. I created a new sketch off the bottom face of Extrude 2. I made a rectangle that connected all 6 outer edges of both existing(extruded) rectangles. I clicked Center Rectangle and selected the origin, then made the dimensions 9mm by 10 mm. I extruded this SKetch 3 with a Blind depth of 3 mm, towards the Bottom plane. Lastly, I clicked the Boolean tool, and selected all parts under the Union tab. Then, in the Assembly, I mated this holder inside the box, conecting it's holes to the screw hols I made earlier on the face of part 5.

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
