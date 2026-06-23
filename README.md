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

The robot will be able to follow a distinct red line displayed on warehouse floor. The marked line will be ten cm in widith.
PiicoDev VEML6040 colour sensor (I²C) is able to detect any colour since it has full RBGW, for simplicity the robot will follow a distinc red line.
If the robot loses the line, it will stop, and reverse to the last known location of the line.
The robot will expect only straight lines, the robot will have the ability to turn in a spot. The turning radious of the chassis is three hundred and sixty degrees.
The robot will expect a continous line with no breaks.

### Probe 2 — "avoid obstacles"
What counts as an obstacle? A box on the floor? A person? A wall?
How close is too close? How did you arrive at that number?
What does the robot do when it sees one? Stop? Re-route? Wait?
Two rangefinders point where? Why?
### Probe 3 — "communicate its current state"
List every distinct state the robot can be in. (Hint: there are more than three.)
What information does a supervisor need at a glance vs on request?
The OLED is 128×64. What can realistically fit?
How will the supervisor know the robot has crashed vs finished vs is thinking?
### Probe 4 — "who else cares?"
Beyond the supervisor, who is affected by the robot's behaviour? (Floor workers? Maintenance? You as the developer?)

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
