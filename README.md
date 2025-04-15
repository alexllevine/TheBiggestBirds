# TheBiggestBirds: Automatic Chicken Coop Door

Contributions made by Alexander Levine, Andrew LaJoie, Douglass Fissinger, Ethan Willford, Nathan Widman

# Problem Statement
To keep chickens safe during the night and allow free access in and out during the day, we need a door that will open and close when the chickens need it. This door needs to be secure enough to ensure nothing else besides the chickens can get into the coop. We also need to set parameters on the accessibility of the door depending on the time of day.

# Constraints
Budget: $120
Time: 8 weeks
Design Requirements:
10x12 inch door that opens either horizontally or vertically.
Must open completely with no obstruction to the space the door occupied previously.
Easy to use and not hinder the owner's capability to open the door manually.
# Solution
Design and build an Automatic Chicken Coop Door Opener that slides the door out of the way and opens by the chickens pecking a big red button to trigger the open mechanism. Chickens are attracted to the color red, which means they will be very interested in the button. Their curiosity will make them peck the button, which will open the door. Instead of using RFID tags, a remote control will be used to trigger the door opening.

![Solidworks Model of Moving Mechanism](https://drive.google.com/uc?export=view&id=1lRBZdM5yMjuBbjFVy8u6nn7dCYLygRdw)

# Design Function
Motor Control: A motor behind the door controls its movement along a track, allowing the door to slide open and close when the Arduino tells it to. The door opens horizontally to avoid crashing down upon the chickens.
Arduino Code: The Arduino is coded to open the door only when the button is pushed and the parameters are met (remote control signal and during the day).
Changes Since Milestone 1
Added wires to connect the big red button and remote control receiver to our breadboard.
Improved the code for a cleaner opening of the door.

![Printed Mechanism]()

# Frame
The frame we have built for our automatic chicken coop door. It has a length of 28 and ¾ inches and a height of 14 inches. It has a 4 by 8 inch shelf that will hold the electronics on it. It has two posts on the edges of the frame which will hold it up. The posts have a length of 4 inches and a height of 18 inches. These dimensions were chosen to match the dimensions of the rail for our device that opens the door. The frame and door are complete for now, we will change the frame in the future if problems occur during testing but as of now the door and frame are complete.

![Frame Front](https://drive.google.com/uc?export=view&id=1dgTzQ-ldX1J_N0ftF_o-xb4Q07xYQPj-)

![Frame ack]()

# Detailed Design
Mounting Bracket: The door is attached to a mounting bracket, which connects it to a gantry plate. The gantry plate serves as the main moving component. By attaching wheels to the gantry plate using screws and spacers, the door can smoothly move across the rail.
GT2 Timing Belt: The gantry plate is connected to a GT2 Timing Belt, linked to a pulley driven by a motor. A wheel guides the belt around the system.
Manual Mode: In case of failure, the system can go to manual mode by moving the door with its handle.

# Electrical Setup
Photocell and Resistor: Connecting a photocell and a resistor in series to a digital pin on an Arduino allows the voltage across the photocell to change based on ambient light levels. This setup helps determine if it's dark or bright, enabling the Arduino to trigger actions based on the light level.
Motor Control: A 12V 2-pin motor is connected to the Arduino board. Instead of an NPN MOSFET, a motor driver is used to control the motor. The motor driver allows for better control and protection of the motor.
PWM Signal: The motor speed can be controlled by varying the duty cycle of the PWM signal from the Arduino.
Remote Control: Instead of RFID, a remote control receiver is connected to the Arduino to trigger the door opening.
