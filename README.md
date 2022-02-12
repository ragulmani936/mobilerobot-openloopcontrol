# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
### Step1:
Initiate the MobileRobot.

### Step2:
Connect your PC with the MobileRobot.

### Step3:
Open Python program.

### Step4:
Program the movements of the robot using python code.

### Step5:
Execute the python program.

## Program
```
from robomaster import robot
import time

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led

    for i in range(10):
        ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")   
        time.sleep(0.5)
        ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
        time.sleep(0.5)
        break
        
    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-120, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=180, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-30, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-120, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=2).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=-30, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=2).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=180, xy_speed=2).wait_for_completed()
    ep_robot.close()
    ~~~

## MobileRobot Movement Image:

![robo](https://github.com/ragulmani936/mobilerobot-openloopcontrol/blob/main/img/robot.jpeg)

Insert image here




## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
