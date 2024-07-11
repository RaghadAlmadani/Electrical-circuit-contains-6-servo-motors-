# Electrical-circuit-contains-6-servo-motors-
Create an electrical circuit contains 6 servo motors using simulation websites here I will use [Tinkercad](https://www.tinkercad.com/dashboard).

### Defintions:

 <img src="https://th.bing.com/th/id/OIP.32uGkXWuex0kAledYhpcBQAAAA?rs=1&pid=ImgDetMain" width="200" />
- Electrical circuit -> is a system of interconnected components that allows electric current to flow, powering electronic devices by controlling the movement of electricity.
 <img src="https://www.homelearningschool.co.uk/wp-content/uploads/2020/03/tinkercad.png" width="200" />
- Tinkercad -> is a user-friendly web app by Autodesk for creating 3D models, circuits, and simulations, ideal for hobbyists, students, and educators. It offers a simple drag-and-drop interface to design and prototype projects virtually.
<img src="https://content.instructables.com/FWL/9DXP/ITW2CVXM/FWL9DXPITW2CVXM.png?auto=webp&fit=bounds&frame=1auto=webp&frame=1&height=300" width="200" />
- Arduino UNO -> is a popular microcontroller board based on the ATmega328P chip. It's widely used in electronics projects and prototyping due to its ease of use and versatility. The Uno board includes digital and analog input/output pins that can be programmed to interact with various sensors, actuators, and other electronic components. It's known for being beginner-friendly while offering enough capabilities for more advanced projects, making it a staple in the maker and DIY electronics communities.
<img src="https://th.bing.com/th/id/R.e612e0b934fdd882f2baf2ebbe8d57f8?rik=4p%2fIVyL6GnyS7A&riu=http%3a%2f%2fmlab.taik.fi%2fpaja%2fwp-content%2fuploads%2f2011%2f04%2fbreadboard.jpg&ehk=wKlsmG0RIkkiKdxdkMpJHs7RyRFP8TVNj%2fQeJYZQHyQ%3d&risl=&pid=ImgRaw&r=0" width="200" />
- Breadboard -> is a solderless prototyping board used to build and test electronic circuits. It features a grid of holes into which components can be inserted and connected without soldering. This allows for easy experimentation and modification of circuit designs, making it a valuable tool for both beginners and experienced electronics enthusiasts.
<img src="https://bestarduino.com/upload/201902/06/201902061139001202.jpg" width="200" />
- Sevro motor -> is a device that translates an electrical signal into precise mechanical motion. It typically consists of a motor, a position sensor, and a control circuit. Servo motors are widely used in applications requiring accurate control of position, speed, and acceleration, such as robotics, industrial automation, and remote-controlled systems.
<img src="https://miro.medium.com/v2/resize:fit:458/0*Usnapdl7EGPLHhwI" width="200" />
- Potentiomenter -> is a variable resistor with three terminals, typically used to adjust electrical resistance in a circuit manually. It is commonly used for volume controls, tuning circuits, and setting bias voltages in electronic devices.<br><br>

**signals:** <br>
 
 <img src="https://www.pcbmay.com/wp-content/uploads/2021/11/Figure-09-Visual-Representation-Of-Analog-And-Digital-Signals.jpg" width="300" />
 
- Digital signal ->  is a type of signal used in electronics and telecommunications that represents data as discrete values, typically binary numbers (0 and 1). These signals are characterized by their distinct, finite levels and are processed and transmitted using digital techniques.
  
- Analog signal -> An analog signal is a continuous electrical signal that varies smoothly and continuously over time. It can represent any value within a range of values and is used in various electronic systems to convey information through continuously varying quantities such as voltage, current, or frequency. Analog signals are fundamental in applications such as audio transmission, analog sensors, and traditional television signals.



-----------------------------------------------------------------------
<code style=" color : yellow ">First I made sweep and knob circuits to understand more how to dell with one servo motor.</code>

### Sweep circuit:
Hardware Required:
 1. Servo motor : servo motor can rotate from 0 to 180 degree and it typically operate within a voltage range of 4.8V to 6V.
 2. Breadboard
 3. Arduino UNO

![Screenshot 2024-07-11 132742](https://github.com/RaghadAlmadani/Electrical-circuit-contains-6-servo-motors-/assets/173769867/4290b9ac-d426-443f-bfa3-e83b150a482e)
Servo motor have 3 colored wires the red wire is power wire and the brown or black is ground wire finally the yellow or orenage wire is a signal wire. I conected the signl wire (the orenage wire) in port 9 because Pulse Width Modulation (~PWM) provides a convenient way to control the position or angle of the servo shaft Therefor, we use when are using servo motor. Moreover, I conected  the red wire to the power 5V and the brown to the ground in the breadboard.
![Screenshot 2024-07-11 133238](https://github.com/RaghadAlmadani/Electrical-circuit-contains-6-servo-motors-/assets/173769867/6af360d2-2cb4-40c0-bd2f-aed39fed8249)
I started the programming by defining a verable called position in the blocks code and let it equal to 0, then I add 2 count blocks (loops) one of them was count up from 0 to 180 and the other is count down form 180 to 0 then I add the rotate servo block and attach it to pin 9 and let it rotate to position value finally I add wait block (delay) and let it wait for 20 millisecond whiches equal to 0.02 second.  Here is the link of the [circuit](https://www.tinkercad.com/things/9QQNlbxfdLT-surprising-inari/editel?sharecode=lC9VaYxA6jU2fZtkLEXeG8DD8-tF6FxE_uv3prxWn6Q)

### Knob circuit:
Hardware Required:
1. Servo motor : servo motor can rotate from 0 to 180 degree and it typically operate within a voltage range of 4.8V to 6V.
 2. Breadboard
 3. Arduino UNO
 4. 10k ohm Potentiometer : send a value to the board that start from 0 to 1023.
    
![Screenshot 2024-07-11 151030](https://github.com/RaghadAlmadani/Electrical-circuit-contains-6-servo-motors-/assets/173769867/268c64e7-f05c-4c1f-b467-e60dcd5d1e4d)
Potentiometer have three pins the midle pin is wiper that must conect to analog pin I conected to A0 pin the two side pins are terminal pins I conected terminal 1 to the ground and terminal 3 to the power. However, servo motor conection is the same as sweep circuit.
![Screenshot 2024-07-11 161654](https://github.com/RaghadAlmadani/Electrical-circuit-contains-6-servo-motors-/assets/173769867/1f507326-a8a4-4d21-abf2-0321eb503d54)
I started to define two varibles potentiometer = the analog pin A0 and output_value is the variable to read the value from the analog pin. Then I used map block to change the values of potentiometer 
 to start at 0 and end at 180 and assined it to output_value. Finally, I add the rotate servo block and attach it to pin 9 and let it rotate to output_value. Here is the link of the [circuit](https://www.tinkercad.com/things/ddw6430NktS-smashing-rottis-habbi/editel?sharecode=q7akzQ9tq4KS-Zp3zBp0JrAU8Yp_mC8HpW0iAl1gJok)

### Sweep circuit contains 6 servo motors:
Hardware Required:
 1. Six Servo motor :
>[!NOTE]
>servo motor can rotate from 0 to 180 degree and it typically operate within a voltage range of 4.8V to 6V.
 2. Breadboard
 3. Arduino UNO

![Screenshot 2024-07-11 223248](https://github.com/user-attachments/assets/68a108b8-61ac-4b60-b15a-c11f2647c1ae)
> [!CAUTION]
> Each servo takes from 4.8V to 6V if there are 6 servo motors we have to add external power otherwise the USB port will be rounded even the ardunio uno board may round. However, if we conect it with power supply whos voltage more than 6V it will round the 6 servo motors as shown bellow.
![Screenshot 2024-07-11 223947](https://github.com/user-attachments/assets/98514013-7491-48a2-9a60-5420ce5bcf36)

![Screenshot 2024-07-11 223202](https://github.com/user-attachments/assets/83472e1f-b9fe-4b36-b97b-52637de755ac)
same as the sweep circuit with one servo motor but I made every 2 motors to move together. Here is the link of the [circuit](https://www.tinkercad.com/things/34LVQlcF9ve-dazzling-esboo-amberis/editel?sharecode=KoOVPr19EWMq-lVqSuXAxJN3a5pq68oB5D2N8N5cnxY)

### Knob circuit contains 6 servo motors:
Hardware Required:
 1. Six Servo motor :
>[!NOTE]
>servo motor can rotate from 0 to 180 degree and it typically operate within a voltage range of 4.8V to 6V.
 2. Breadboard
 3. Arduino UNO
 4. Four 10k ohm Potentiometer
![Screenshot 2024-07-11 231718](https://github.com/user-attachments/assets/f79b05a7-6134-49be-bc11-9239f6c9e8ff)
![Screenshot 2024-07-11 231750](https://github.com/user-attachments/assets/e56b40cc-4d9d-4c94-b14b-fb6f3644d672)
same as the knob circuit each servo have the potentiometer that move it. Here is the link of the [circuit](https://www.tinkercad.com/things/ej8Jc41Nr5Q-brilliant-duup/editel?sharecode=GrG7I2pHWsLFbWUuAQh5ClteB4skJzNe8yh2e6xc52s)

