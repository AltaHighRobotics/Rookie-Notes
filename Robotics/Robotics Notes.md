Plans on what to do:

Make a web application that stores the robots constants so that it can be:

1. Accessed via IP in a browser
2. Change the robots constants by commiting to the robots constants file (In real time?)
3. Display current constants
4. Make sure that its showing the constants for the currenr robot (will not show vision constants when it is just a drifter robot)
5. Have the web interface (IAmGUI) be able to focus on specific constants that you want to change
6. When setting new values, they should not be going over the max amount

When making a new robot:

1. Be able to have standardized commands so that you can just drag the susbsytems/commands into the robot repository and it will work (template system?)
2. If you want to add a new feature to the robot (such as vision), so that they can just be inputted in the robot so that there doesn't have to be any tinkering between robots

Debugging:

1. Tell the programmers if their constant variable names are not uppercase
2. Have a enum that will be able to translate the current robot's motors (PID's) whether it is a drifter or tank so that it's motors are automatically set to the correct motors (standardization)

