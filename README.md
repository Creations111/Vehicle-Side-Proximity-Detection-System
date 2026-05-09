# Vehicle Side Proximity Detection System
**Cornerstone of Engineering 1 - Northeastern University**
*Jonathan Lin | December 2025*

---

## Overview

Modern vehicles are equipped with front and rear proximity sensors, but the **sides of a car remain largely unprotected**. This project addresses this issue by building a side-proximity detection system using a Raspberry Pi, ultrasonic distance sensors mounted on servo motors, a buzzer, and an LED. The contraption is housed in a laser-cut plywood enclosure designed to resemble a car.

As an object approaches either side of the enclosure, the buzzer and LED respond with increasing frequency, alerting the "driver" of nearby obstacles.

---

## Problem Statement

Side-blind zones in cars can create dangerous scenerios - especailly for cyclists, motorcyclists, and pedestrians. A child on a bicycle making a turn alongside a vehicle is a real-world case where side sensors could prevent a life-threatening collision. This project explores how such a system could be designed and prototyped to combat that.

---

## Solution

After evaluating multiple alternatives using a **Kepner-Tregoe Decisions Analysis**, the winning solution was:

> **Two ultrasonic distance sensors mounted on servo motors, a Raspberry Pi, a Buzzer, and an LED

The servos rotate the sensors to sweep the full side view of the vehicle. As an objects gets closer:
- The **buzzer** beeps with increasing frequency
- The **LED** flashes with increasing frequency
- No alerts fires if the object is beyond the threshold distance (preventing false alarms)

---

## Components
