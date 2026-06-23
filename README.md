# Project Title

A warehouse needs an autonomous robot that can follow a marked path between picking stations and avoid obstacles that workers leave in the aisles. 
The robot must communicate its current state to a human supervisor at a glance.

## Description

## Getting Started

### Dependencies

* Describe any prerequisites, libraries, OS version, etc., needed before installing program.
* ex. Windows 10

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```
code blocks for commands
```
## Hardware

| Component | Quantity | Role |
| --- | --- | --- |
| Raspberry Pi Pico | 1 | Microcontroller |
| Custom power conditioner board | 1 | Voltage regulation |
| LiPo 18650 battery | 2 | Power supply |
| PiicoDev ultrasonic rangefinder (I²C) | 2 | Distance sensing |
| PiicoDev SSD1306 OLED display (I²C) | 1 | Supervisor display |
| PiicoDev VEML6040 colour sensor (I²C) | 1 | Surface / line colour |
| Line‑following sensors (digital and analog GPIO) | as needed | Path detection |

## Probe Brief

### Probe 1 — "follow a marked path"

The robot will be able to follow a distinct high contrast red line displayed on warehouse floor. The marked line will be five cm in widith.
The PiicoDev VEML6040 colour sensor (I²C) is able to detect any colour since it has full RBGW. For simplicity the robot will follow a distinc red line.
If the robot loses the line, it will stop, and reverse to the last known location of the line, scanning the floor to see for the line.
The robot will expect only straight lines, the turning radius of the chassis is zero degrees becuase the robot can turn in a standing spot.
The robot will expect a continous line with no breaks.

### Probe 2 — "avoid obstacles"

An obstacle is considered anything that obstructs the line. The robot will classify the obstacles into two catagories, moving and non moving by decting for change in distance using ultrasonic sensor.
Too close to the obstacles will be considered twenty centermeters. This number was dervided to leave a gap the size of itself infront of the object.
When the obstacle is detected, if it is non moving, the robot will trace the obstacle around to locate the line again, if the object is moving, the robot will wait for the moving object to move.
The robots ultrasonic sesnsors will be both posiitioned at the front at sliglt angles to create a line of sight in the shape of a cone.

### Probe 3 — "communicate its current state"

The robot will have the following states, idle, following line, moving forwards, reversing, waiting, turning, emergency, communicating.
The supervisor will need the state and condition of the robot at glance, on request how close the robot is from tranporting items from one picking station to another.
The OLED can realstically display the current state of the robot on top, in blue text on black background.
The supervisor will know if the robot has crashed if it is the emergency state, if the robot is finsihed it will go the communication state, update the supervisor before returning to idle, if the robot is thinking, the state will be updated via the communication state.

### Probe 4 — "who else cares?"

The people that will be affected by the robots behaviours are floor workers, maintenance, anyone who walks across the warehouse will be impacted. The developer will be impacted by liability if the robot does not work via the code. Workers within the warehouse will be impacted as they adapt to the robots working schedule, speed and preformance.

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Mr Jones
ex. [@benpaddlejones](https://github.com/benpaddlejones)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]() or see [branch]()
* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Acknowledgments

Inspiration, code snippets, etc.
* [Github md syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [TempeHS MicroPython template](https://github.com/TempeHS/TempeHS_MicroPython_DevContainer)
