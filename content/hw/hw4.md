---
title: "HW4"
date: 2018-04-17T13:04:56-05:00
draft: true
---

Released: 2019-02-14

Due: 2019-02-21

**NAME:**  
**HW: Time of Flight Measurement**

**Description**

The Time of Flight principle essentially uses the time that passes between two (or more) events to deduce information from a system. For example when we use ultrasonic sensing, we generate a pulse, and wait until we sense a reflected pulse from an object. Then we use the time difference, combined with a known speed of sound at a certain temperature to determine the distance from the sensor to the object. Modern Light Detection and Ranging (LIDAR) devices do the same thing using the speed of light.

![figure1](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/HW_TimeOfFlightMeasurement1.PNG)  

The figureshows an example of a Time of Flight device that was developed to measure the diameter and velocity of granular fertilizer particles. One of the complications was that the measurement sensors consisted of 5 mm wide OptoSchmitt sensors, which would make it impossible to detect a 1 mm particle. Therefore the shadow of the particles was magnified using two lenses as in a slide projector. By magnifying the image of the particles in real time (this is the beauty of using optical detection, the speed of light is approx. 300,000 km/s) it was possible to reliably detect particles with a size of 1 mm.



To analyze the working of the sensor, imagine that the round object on the left is moving upward at a constant velocity

![figure2](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/HW_TimeOfFlightMeasurement2.PNG)

while interrupting the dual optical detection layers. The graph shows the distance as a function of time, as a straight line, which implies that the velocity is constant, rendering the acceleration equal to zero. Under the assumption of a constant velocity, the time it takes an object to move through the distance ```b``` from layer 1 to layer 2 is Delta t_f. Therefore the velocity ```v_0``` is simply:

![figure](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/TF1.png)

The diameter of the object is represented by the time it takes to move the object through one of the light layers times the velocity of the object or:

![figure](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/TF2.png)

These relationships are easy to see in the case of a constant velocity, which implies zero acceleration. However, if there is a constant acceleration, it is not that obvious anymore, and we need to use proper analysis to find out how the dimensions of our object are related to the times measured. First, let's propose a (correct) equation that relates distance to time for the constant velocity case:

![figure](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/TF3.png)

To determine how our constant velocity ```v_0``` is related to the timing information, we can construct a relationship graph as shown in Figure. We know two measures 1) that the distance to move the particle from ```x(t_1)``` to ```x(t_2)``` is equal to ```b``` and 2) that the time associated with that movement is Delta ```t_f```. We also know that the the distance from ```x(t_1)``` to ```x(t_3)``` is equal to ```D```, which is the diameter (major axis) of our particles and that the time associated with this movement is Delta ```t_p```. We will use both these to determine the general equations to measure the velocity ```v_0``` and the particle diameter ```D``` as follows:

![figure](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/TF4-13.png)

![figure3](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/HW_TimeOfFlightMeasurement3.PNG)

Using the same methodology as shown for the constant velocity case, your job is to derive the equation for the Diameter of the particle as a function of the acceleration ```a```, the distance between the sensor layers ```b``` as well as Delta ```t_f``` and Delta ```t_p```. This means that the general equation of motion becomes:

![figure3](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/HW_TimeOfFlightMeasurement14.PNG)

Where a is a constant acceleration in ```ms^(-2)```. You do not need to solve for the acceleration a, you can leave it in the final equation for the diameter.

![figure3](https://github.com/ABE425/ABE425/blob/Rongliu/data/hw/hw_timeflight/HW_TimeOfFlightMeasurement15.PNG)

**Use LaTex functionality, so just continue this document, and extend it to include your answer. Submit the pdf file of this document and don't forget to put your name at the top.**

**Link**: [Visit the HM4](https://github.com/ABE425/ABE425/tree/master/data/hw/HW_TheveninEquivalents )

**Submission**:[SUBMIT YOUR HOMEWORK HERE]()

**Link to resource**: [LaTex_Guide](../../resources/LaTex_Guide.md)
