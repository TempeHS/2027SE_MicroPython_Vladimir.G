# Project Title

Simple overview of use/purpose.

## Description

An in-depth paragraph about your project and overview of use.

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
## Robot requirements

### Probe 1 — "follow a marked path"
What colour and width is the line you'll design for? Why that choice given your colour sensor?
What happens if the robot momentarily loses the line? Stop? Spin? Reverse?
How tight can the curves be? What turning radius will your chassis support?
Is the line continuous or can it have gaps?
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
