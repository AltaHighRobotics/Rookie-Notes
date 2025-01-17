## Making a web application

that can be accessed via browser to edit constants (such as speed and rotation) for real-time debugging.

Extras: Only show constants that the current robot has, Bookmark/Star specfic constants that we are testing, prevent the constant change from going over max limits

## Standardizing Robot commands/subsystems

So that we are able to copy files from other robot repositories without needing to completely configure it to the new robot: Plug-n-Play

Extras: When testing robots, check the constants to make sure that they are upper-case AND tell the programmer about it

## Add a versatile motor PID system
Using enum so that the programmers are able to just specify the robot type (most likely in constants) so that the motors fit to the robot, prevents the issue where basic driving code doesn't work across different machines

Extras: Add good documentation or a system where in the case where we have a new type of robot that the enum can be easily edited to match that robot