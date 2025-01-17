# Required Parts
## robot.py
### Use:
The main program that will be run on the actual robot when the code is deployed to it, can be used to run robotContainer.py which has most of the infastructure
### Path:
Main repository
### Connections:
#### Imports:
- commands2[^1]
- robotContainer.py[^2]
#### Deports to:
- NONE

## robotContainer.py
### Use:
Holds most of the robot's input commands, this is where you should put your controller commands to make the robot do stuff
### Path:
Main repository
### Connections:
#### Imports:
- wpilib[^1]
- constants[^2]
- subsystems[^2]
- commands[^2]
#### Deports:
- NONE

## constants.py
### Use:
Holds all the constants that are needed for the robot to follow, 
### Path:

### Connections:
#### Imports:
- NONE
#### Deports:
- robotContainer.py[^2]
- subsystems:[^2]
	- aprilTagSubsystem.py
	- driveSubsystem.py

## Subsystems folder
### Use:
For the different components that are being controlled by the robot, such as the driving motors being one subsytem, vision being another, and manipulators (arms/hands) being another
### Path:
Main repository

## Commands folder
### Use:
Will hold your commands for the robot that will be used to control how the robot acts, most commands are only linked with one button that controls the robot to do a single thing such as rotate robot arm or interact with apriltags
### Path:
Main repository




# Additional Parts (not included)
## dance.py
### Use:
While the button input is being held, it will run on a timer to move forward and backward on a steady beat
### Path:
Main repository / commands

## sneke.py
### Use:
While the button input is being held, it will run on a timer to move forward while turning left and right like a snake
### Path:
Main repository / commands

## forward.py
### Use:
Will move the robot straight forward as long as the button input is being held
### Path:
Main repository / commands





## Footnotes
[^1]: Libraries that are automatically installed with `robotpy sync` or with the installers
[^2]: These imports are from libaries that you create and are not automatically installed with `robotpy sync`
