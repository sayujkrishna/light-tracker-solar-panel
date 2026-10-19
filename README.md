# Light Tracking Solar Panel

A project I made in my first year of ECE, for my Introduction to Electronics course. It turns a small solar panel toward a light source using only analog components. There is no Arduino and no code.

The solar panel is mounted on the platform as the part being aimed. It is not connected to the circuit, which runs on a 9V battery.

## What I used
- TDA2822 IC
- 2 x LDR (light sensors)
- 2 x 10K resistors
- Mini solar panel
- Geared DC motor
- 9V battery
- Switch
- Breadboard and jumper wires
- Cardboard for the base and panel mount

## How I made it

The circuit is powered by a 9V battery through a switch. The positive terminal goes to the VCC pin of the TDA2822 and the negative goes to ground. The two LDRs and the two 10K resistors connect to the input pins of the IC, and the DC motor connects to its two output pins.

For the body, I made a cardboard base and mounted the solar panel on top of it, with the LDR sensors on the panel so they face the same way as the panel. The geared motor sits under the panel, so when the motor turns, the panel turns with it.

## How it works
The two LDRs are connected in series across the battery. The point between them gives a voltage that changes with how much light falls on each one. The two 10K resistors give a fixed reference voltage.

The TDA2822 compares these two voltages and drives the motor, so the panel turns toward the side with more light. When both LDRs get equal light, the motor stops.

The TDA2822 is normally an audio amplifier IC, but here it is used to drive the motor.

## How I tested it
I first simulated the circuit in Tinkercad to check that it worked. Then I built it on a breadboard.
I tested it in a dark room with a phone flashlight. I moved the light left and right and watched the panel turn toward it. I have not tested it outdoors in real sunlight.

## Demo
See `demotracker.mp4` in this repo.


## What I learned
I built this before I knew Arduino, so I learned how to take a circuit from simulation to a working build: testing it in Tinkercad, wiring it on a breadboard, and mounting it.
