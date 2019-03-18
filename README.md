# Density-Based-Traffic-Control-System-
This is an arduino based project showing how to control traffic based on its density. 

Nowadays, controlling the traffic has become a major issue because of rapid increase in automobiles and also because of large time delays between traffic lights. So, in order to rectify this problem, we have gone for density based traffic lights system. 

This project requires an Arduino and Ultrasonic sensors.

In this system, we use Ultrasonic sensors to measure the traffic density. We have arranged one Ultrasonic sensor for each road; these sensors always sense the traffic on that particular road. All these sensors are interfaced to the microcontroller(ATMEGA328P). Based on these sensors, microcontroller detects the density and controls the traffic system.

The ultrasinic sensors are used to detect the distance from the closest object i.e a car. Here  it is assumed that the sensors are placed on the road at some distance from the intersection , such that the greater the distance the lesser the number of cars on that particular road . This is data is used to optimze the required timing for each traffic signals.
