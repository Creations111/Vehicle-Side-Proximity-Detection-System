# Vehicle Side Proximity Detection System
**Cornerstone of Engineering 1 - Northeastern University**
*Jonathan Lin | December 2025*

---

## Demonstration Video

[Version 1 Demonstration](https://youtube.com/shorts/AcROKL2eSVw)
[Detection System Project Demonstration](https://youtube.com/shorts/TaLlRtZOmOg)

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

| Component | Quanity | Purpose | Cost |
|---|---|---|---|
| Raspberry Pi (Pico) | 1 | Microcontroller runs the logic | $6.00 |
| Ultrasonic Distance Sensors (HC-SR04) | 2 | Measure distance to objects on each side | $6.00 | Servo Motors | 2 | Rotate sensors to sweep side fields of view | $8.00 |
| Buzzer | 1 | Audible alert when objects are close | $1.00 | 
| LED | 1 | Visual alert when object is close | $0.30 | 
| Breadboard | 1 | Connects all components | $5.00 | 
| Jumper Wires | Several | GPIO connections | N/A | 
| Laser-cut Plywood Enclosure | 1 | Houses the system: represnets the vehicle body | $6.00 |
| 3D Printed Sensors Mounts | 2 | Attaches distance sensors to servo motors | $2.00 |

---

## How It Works

```
Distance Sensor (Left)  ──┐
                           ├──► Raspberry Pi ──► Buzzer (beep frequency ∝ proximity)
Distance Sensor (Right) ──┘                 └──► LED   (flash frequency ∝ proximity)
        ↑
  Servo motor sweeps
  side field of view
```

1. Both servos motors continuously sweep left and right.
2. The distance sensors measure how far away nearest objects are.
3. The Raspberry Pi reads these values and maps proximity to alert buzzer and led to activate.
4. If an object is within the danger threshold, the buzzer and LED activate.
5. The closer the object is, the faster the buzzer beeps ad LED flashes.

---

## Design & Fabrication

- **Enclosure** was designed in **AutoCAD** and cut using a **laser cutter** at the Northeastern Makerspace.
- Holes were sized slightly smaller than each component's diameter to create a friction fit (buzzer, LED).
- Rectangular openings on top allow the servos to sit on it and rotate freely.
- A USB-C port opening on the side panel allowing power delivery from laptop.
- **3D printed mounts** hold the ultrasonic sensors onto the servo arms.

---

## Project Timeline

| Milestone | Date | Notes |
|---|---|---|
| Initial Check-In | Nov 9, 2025 | Motion sensor prototype scrapped due to heat-only detection |
| Middle Check-In | Nov 20, 2025 | Switched to distance sensors + servos; enclosure v1 designed |
| Final Showcase | Dec 3, 2025 | Fully functional: both sensors working simultaneously |

---

## Challenges

- **Initial prototype scrapped** - the motion sensor only detects heat-emitting/moving objects, making it useless for stationary obstacles like curbs.
- **Enclosure fit issues** - multiple laser-cut iterations were needed to get component holes and servo openings to the right dimensions. Costed material.
- **Group dynamics** - the majority of design, fabraiction, and coding was completed independently due to lack of group contribution.

---

## Lessons Learned

- Start early and work incrementally rather than in concentrated bursts.
- Break down problems systematically — identifying all failure points before coding saved significant debugging time.
- The Engineering Process is iterative; going "back to the drawing board" is part of the process, not a failure.
- Hiding wires and making hardware more secure (less tape, more 3D-printed brackets) would improve future builds.
- Communication could have been better especailly more attempts towards it and understanding other's thoughts before taking on all the burden. Communication towards one goal would have led towards a better project. 

---

## Ethical Considerations

- **Road safety motivation:** Inspired by real accidents in Massachusetts where side-blind zones led to pedestrian and cyclist injuries.
- **Material lifecycle:** Plywood enclosure can be recycled into mulch; deforestation impact is partially offset by regulated forestry practices.
- **Supply chain awareness:** Raspberry Pi chips rely on silicon, gallium, and germanium — minerals mined largely in China under potentially exploitative labor conditions.

---

## References

- [Plywood Environmental Impact — ArcherPly](https://www.archerply.com/the-environmental-impact-of-plywood-production-and-sustainable-practices.php)
- [Where Raspberry Pis Are Made — Raspberry Pi Magazine](https://magazine.raspberrypi.com/articles/where-raspberry-pis-are-made)
- [Mine to Microchip — CSIS](https://www.csis.org/analysis/mine-microchip)
- [Wood Waste Recycling Guide — BusinessWaste](https://www.businesswaste.co.uk/news/wood-waste-recycling-guide/)

---

## Acknowledgments

Project completed as part of **Cornerstone of Engineering 1** at Northeastern University. Full projects documentation and photos are in personal website linked above. 
