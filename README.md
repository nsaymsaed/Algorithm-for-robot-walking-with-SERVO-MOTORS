# Algorithm-for-robot-walking-with-SERVO-MOTORS
![Screenshot 2024-08-08 190950](https://github.com/user-attachments/assets/d534133a-4691-4d2b-836a-54864bdca4b9)

## Servo Motors

Servo motors typically have three wires, though the color might vary. Generally:

- Brown or Black: Ground
  
- Red: Power
  
- Yellow or White: Signal

To connect a servo motor to a breadboard, follow these steps:

1. Ground Connection: Connect the brown or black wire to the ground bus on the breadboard.
  
2. Power Connection: Connect the red wire to the power bus.
   
3. Signal Connection: Connect the yellow or white wire to one of the Arduino's digital pins.

This setup allows the Arduino to control the servo motor.

## Algorithms:

1- Servo library (#include <Servo.h>) 2- create a servo object for each motor it might help to give them names .

`Servo leg1;`

`Servo leg2;`

`Servo leg3;`

`Servo leg4;`


`Servo knee1;`

`Servo knee2;`

`Servo knee3;`

`Servo knee4;`

2-define srarting angle It helps to use variable to define the various angles that you want to move the legs to.

`//int start_code = 90;`


`int knee_delta = 60;`

`int leg_delta = 45;`

3-Now it's Time between motins(millisecond)

`int delayTime = 500;`


4- Attach the servo motors to the pins in your setup function. You need to connect each Servo object to an Arduino pin. Make sure to keep track of which motor is attached to which pin.

`leg1.attach(2);`

`leg2.attach(4);`

`leg3.attach(8);`

`leg4.attach(10);`


`knee1.attach(3);`

`knee2.attach(5);`

`knee3.attach(9);`

`knee4.attach(11);`

5- Set start angle for each motor Use the (write) command to set the starting position for each motor, for example:

6-Set start angle for each motor Use the (write) command to set the starting position for each motor, example:

leg1.write(start_code);

`leg2.write(start_code-leg_delta);`

`leg3.write(start_code+leg_delta);`

`leg4.write(start_code);`


`knee1.write(start_code);`

`knee2.write(start_code);`

`knee3.write(start_code);`

`knee4.write(start_code);`


7- Specify a long delay to give yourself time to put the robot down and ensure it’s standing up. For example: `delay(5000);`

8- Then Enter the `loop` function where you can program your gate. Use the appropriate commands to change the angle of each motor.

9- noe Use a `while` loop to incrementally change the angle by just one or two degrees at a time. This approach will result in smoother motion.

 
