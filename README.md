# CAD
[The Prototype in Onshape] I kinda went ham on it, so I probably only need to tweak a few things before it's done. (I actually had to redo the whole thing 😭)

![image](https://user-images.githubusercontent.com/60236713/121033188-f6c4e080-c779-11eb-812c-8172e47d30c3.png)(https://cvilleschools.onshape.com/documents/b60c5c3ae011e78cf6a2a1bd/w/4e3c6e2f779413a1c7802b2b/e/10d812ac343aef4f061d0bf0)

---
[The Finished Box] It took a while, but here is the finished box
![image](https://user-images.githubusercontent.com/60236713/121032411-40f99200-c779-11eb-8fd2-341d6d2728b0.png)(https://cvilleschools.onshape.com/documents/4cafc404dbc2d78c76f5d503/w/d911d8f5b4fcbf83750c56b5/e/5ba1d3ddd6fdd5eba1eda622)

The dimensions of the box are 150 mm by 100 mm by 105 mm. I used the thicken tool by selecting a face and its parallel, on the New tab, with Direction 1 being 3 mm. (Repeat twice more) Deleted the core piece. Then I used the Laser Joint tool, selected all parts on the Automatic tab, and set # of pins to 2. I used the T Slot Joint tool to select all 4 faces of the tab the Laser Joint created on Part 1, set the specs to an ANSI #4 13 mm screw with a Hex Machine Nut with a close fit, 10 mm from the edge, 1 connector, clicked Equal Spacing and Add Nut Connector. I repeated this step for 4 more times, excluding parts 5&6. 

I made a sketch on part 6 to create a hole for the 9V battery pack, with screw holes to attach. I drew a rectangle, 63 mm by 90 mm, with a 90 mm centered construction line. The larger sides are equally distanced from the edges, but one of the smaller sides being 16.83 mm from the edge. On the opposite small side, I made a screw hole, 2.95 mm in diameter, 4.14 mm from the rectangle, and 8 mm from the rectangle's center line. I then mirrored the hole around the center line. Then I used Extrude, clicked Solid, Remove, selected the sketch, and Through All.

In the Assembly, I clicked Automatic Grouping to mate the faces together. I inserted my fan, a DC motor, my motor holder, a 9V battery pack, and LCD screen with backpack(use automatic grouping), a panel mount potentiometer, a panel mount LED, 2 panel mount switches, a T slot photointerupter, an ArduinoUno, an ArduinoUno prototyping shield, a mini breadboard, and 3 25x.5 Aluminum Hex Male Female standoffs. 

After mating the DC motor in the center of part 5 with its rounded sides facing the long edges, and the Photointerrupter's feet 53 mm from the center along the 90 mm center line, each with an offcet of -3 mm on the Y, I selected part 5 and clicked Edit In Context to make a sketch on it's face. I selected the outline of the DC motor and clicked the Use(Convert/Project) tool. I did the same for the 2 oval shaped holes on the Photointerupter. Then I created a 2 circles with a diameter of 3 mm, 8.73 mm from each flat edge of the DC outline. These will be for the motor holder.

I used Edit In Context on part 2 in the Assembly. I created 3 circles with a diameter of 3.2 mm. The first is 3.22 mm from the shorter edge (never the tab), and 28.06 mm from the the longer edge (the one connecting to part 6). The second circle is also 3.22 mm from the shorter edge (that connects to part 4) and 55.96 mm from the longer edge. The third circle is 55.62 mm from the shorter edge and 22.96 mm from the longer edge. I Extruded this with Remove and Through All. Then, I went back to the Assembly and  mated the male side of the standoffs to the inside of the holes. Then I mated the round female edge of the standoff to the corresponding holes of the Arduino. Then I mated a hole on the Arduino (corresponds to the first circle I described in the sketch) to the matching hole on the Prototyping shield, with an offcet of -3 mm on the Y and another offcet of 12 on the Z.

I clicked Edit In Context on part 4 in the Assembly. I selected the cord ports on the Arduino and used the Use tool and made the outlines into Construction lines. I created construction lines in an X pattern on both rectangular outlines to find the center. Then I used Center Rectangle to make 2 rectangles on their centers (each rectangle should be around 3 mm wider and taller than the ports), then I Extruded this sketch using Remove and Through All. Lastly, I mated the bottom face of the Minibreadbord to the top of the Prototyping shield. 

Part 1 is the face that holds the LCD+backpack, potentiometer, LED, and 2 switches. I mated the top face of the blue backpack base to the bottom face of part 1 with an offcet of -3 mm on the Z (with the small sides facing parts 3&4). I clicked Edit In Context on part 1 and made an outline of the LCD screen using the Use and Construction tools. I then made a center rectangle, using the outline's center, with the dimensions 26 mm by 72.5 mm. I then transferes the 4 holes from the backpack with the Use tool. Then I Extruded this sketch with Remove and Through All.

Still on part 1, we're now making the holes to hold the potentiometer, LED, and 2 switches. In same sketch a before, I made a circle in the corner of parts 5&4, with a diameter of 7.5 mm, and 10 mm from both sides. Inside the circle, I made center the midpoint of a construction line that is 3 mm long. Then I made 2 more more construction lines that extend from the tips of the center line to the edges of the circle. Then I use the Trim tool to delete the section of the circle between the construction lines. I finish the rectangle with another construction line, and then use that same line as the top of a new rectangle. I created 2 lines from the vertices(that break the circle) that are 5 mm long. I connected those 2 lines with another 3 mm line, to create a keyhole shape.
In the corner of parts 4&6, I created 3 more holes. Two circles that both have a diameter of 6.4 mm and are 7 mm from the closest edge of part 4. The first hole is 7 mm from the closest edge of part 6, and the second hole is 17 mm way. The third hole has a diameter of 7.9 mm, is 7 mm from the closest edge of part 6, and 22 mm from the closest edge of part 4.

I created the motor holder in a seperate document. I made my first sketch on the Top plane, I made a rectangle that is 16 mm by 11 mm, the 11 mm side are 8 mm from the Front plane, and one 16 mm side is 8 mm from the Right plane. There is a circle inside the rectangle that's center is along the Front plane, is 3 mm from the 16 mm side furthest from the Right plane, and has a diameter of 3 mm. I mirrored this rectangle and circle around the Right plane and exited the sketch. I Extruded Sketch 1 with a Blind depth of 5 mm, protruding upwards from the Top plane. Next I created a new sketch off the bottom face of Extrude 1. I created 2 rectangles that are 11 mm by 5 mm, their 11 mm side matches up with the existing rectangle's side closest to the origin. I Extruded both of them 13.6 mm, towards the Bottom plane. I created a new sketch off the bottom face of Extrude 2. I made a rectangle that connected all 6 outer edges of both existing(extruded) rectangles. I clicked Center Rectangle and selected the origin, then made the dimensions 9mm by 10 mm. I extruded this SKetch 3 with a Blind depth of 3 mm, towards the Bottom plane. Lastly, I clicked the Boolean tool, and selected all parts under the Union tab. Then, in the Assembly, I mated this holder inside the box, conecting it's holes to the screw hols I made earlier on the face of part 5. (https://cvilleschools.onshape.com/documents/0f8b2a51cc92348b934510e0/w/3e83eac2f9a20232cfd2899f/e/52d9edfd123a169f3a78e3b6)

The last piece is the pinwheel part, which I created in a seperate document. I made a sketch on the Front plane, put a center circlepoint on the origin with a diameter of 10 mm. I Extruded this sketch Blind with the first Depth direction being 2.5 mm, and the second 6 mm. Then I clicked the Helix tool, Height and Pitch, selected the edge of sketch 1, Clockwise, with a Height of 1, a Helical Pitch of 6 mm, and a Stanrt Angle of 0. I created a second sketch on the Front plane, a single line along the Top plane, that starts 5 mm from the origin, and has a length of 28 mm. I then used the Sweep tool on the Surface tab, selected the edge of sketch 2 for Edges, and selected the small line made from the Helix tool for the Curve Path. Then I clicked the Thicken tool, the Add tab, and selected the cylindrical face of Extrude 1 and the Face of Sweep 1, the 1st Direction set to .75 mm and the 2nd Direction set to .25 mm. Next, I used the Fillet tool, selected the edge of Thicken 1 under the Edges tab,Tangent Propogation, Circular Cross Section, a radius of 5 mm, and Allow Edges to Overflow. I used another FIllet, selected the vertices of the wedge shape that is Thicken 1, with the same specifications as the previous Fillet. I used the Split tool with the Parts tabs, and selected Part 1 under Parts to Split, and Face of Thicken 1 under Entities to Split with, and selecten Keep Tools. I made a sketch on the Right plane, and I mad along the Top plane, 5 mm long, a single line from the origin along the Top plane. I use the Circular Pattern tool, use a Part Pattern, select part 2 as the Entity to pattern, and the line from sketch 3 as the Axis of Pattern, an angle of 360, Instance count of 5, Equal Spacing. I used the Boolean tool, clicked Union, and selected all parts. I create one last sketch from the bottom circular face. I put one circle on the origin, with a diameter of 2.44 mm. I click Extrude, Remove Sketch 4, Blind, with a depth of 8 mm. Finally, in the Assembly, I mate the interior cylindrical face with the cylindrical face of the little peg that comes out of the DC motor.
(https://cvilleschools.onshape.com/documents/ad5f9951d4d490e4b34d4ece/w/bd4328a33842edf365522523/e/578d4ac466878da8171ac69f)

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
