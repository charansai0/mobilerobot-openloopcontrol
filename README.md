# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:  Start

<br/>

Step2: From robomaster import robot

<br/>

Step3: Initialize the type

<br/>

Step4: Run the program to move the robo moster through our condition 

<br/>

Step5: Close

<br/>

## Program
```
DEVOLOPED BY : V.CHARAN SAI
REF NUM : 21003158

from robomaster import robot
import time

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")   
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=80,g=255,b=30,effect="on")
    ep_chassis.move(x=0, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=100,b=255,effect="on")
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=70,b=255,effect="on")
    ep_chassis.move(x=-2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")  
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")  
    ep_chassis.move(x=0, y=0, z=90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=80,g=255,b=30,effect="on")
    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=1).wait_for_completed()
  

    ep_chassis.drive_speed(x=0.2,y=0,z=50)
    time.sleep(20)
    ep_chassis.drive_speed(x=0,y=0,z=0)

    ep_chassis.drive_speed(x=0,y=0.2,z=50)
    time.sleep(20)
    ep_chassis.drive_speed(x=0,y=0,z=0)

   
    for i in range(10):
        ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")   
        time.sleep(0.1)
        ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")
        time.sleep(0.1)
        ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")
        time.sleep(0.1)        
    
    print("Completed...")

    ep_chassis.drive_speed(x=0,y=0.2,z=100)
    time.sleep(20)
    ep_chassis.drive_speed(x=0,y=0,z=0)
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")
    time.sleep(0.1)

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
## Start position
![OUTPUT](https://github.com/charansai0/mobilerobot-openloopcontrol/blob/main/V.jpeg?raw=true)
## End position
![OUTPUT](https://github.com/charansai0/mobilerobot-openloopcontrol/blob/main/VVV.jpeg?raw=true)



<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:
 
## video link:
(https://drive.google.com/file/d/1JJtvYTXumGIbHnUX9b-qx_PxUiulqjkj/view?usp=sharing)

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
