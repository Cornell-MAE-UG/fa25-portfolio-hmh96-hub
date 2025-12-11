---
layout: project
title: Torque Wrench FEM Analysis
description: CAD and FEM Project
technologies: [Autodesk Fusion, ANSYS FEM software]
image: /assets/images/MaterialsFinal/seven.png
pics: /assets/images/MaterialsFinal/one.png, /assets/images/MaterialsFinal/two.png, /assets/images/MaterialsFinal/three.png, /assets/images/MaterialsFinal/four.png, /assets/images/MaterialsFinal/five.png, /assets/images/MaterialsFinal/six.png, /assets/images/MaterialsFinal/eight.png, /assets/images/MaterialsFinal/nine.png
---
Class: Mechanics of Materials (MAE 3270)

The final project for this course focused on designing a torque wrench capable of both applying a specified torque and measuring it through integrated strain gauges. Beginning with a baseline steel design, I assessed structural performance using hand calculations and finite element analysis. To enhance sensitivity and reduce weight, I used GRANTA materials indices to select an improved material and refined the geometry while still satisfying safety requirements for strength, fracture, and fatigue. I then validated the updated design in ANSYS, quantified strain at the gauge location, and confirmed that the resulting electrical output would support accurate torque measurement. The summary below outlines the key design choices and analyses that led to a fully functional, instrumented torque wrench.

5.2.1
Results

1. Image(s) of CAD model. Must show all key dimensions.

![Image 1]({{ "/assets/images/MaterialsFinal/one.png" | relative_url }}){: style="width:100%;" }

![Image 2]({{ "/assets/images/MaterialsFinal/two.png" | relative_url }}){: style="width:100%;" }

![Image 3]({{ "/assets/images/MaterialsFinal/three.png" | relative_url }}){: style="width:100%;" }

![Image 4]({{ "/assets/images/MaterialsFinal/four.png" | relative_url }}){: style="width:100%;" }

2.
Describe material used and its relevant mechanical properties.

Material: β-Ti alloy — Ti-12Mo-6Zr-2Fe (conservative values taken from Granta)
Material properties (imperial units):
Property
Value
Young's Modulus, E
13.1 × 103 ksi
Poisson's Ratio, ν
0.33
Yield Strength, σy
130 ksi
Fracture Toughness, KIC
80.1 ksi·√in
Fatigue Strength (106 cycles)
90 ksi

3.
Diagram communicating how loads and boundary conditions were applied to your FEM model.
![Image 5]({{ "/assets/images/MaterialsFinal/five.png" | relative_url }}){: style="width:100%;" }
Just the highlighted yellow part of the model has the zero displacement restraint applied too it.

4.
Normal strain contours (in the strain gauge direction) from FEM
![Image 6]({{ "/assets/images/MaterialsFinal/six.png" | relative_url }}){: style="width:100%;" }
Strain extremes reduce from the max and mins shown here at points further along the shaft not shown.

5.
Contour plot of maximum principal stress from FEM
![Image 7]({{ "/assets/images/MaterialsFinal/seven.png" | relative_url }}){: style="width:100%;" }
Stress extremes reduce from the max and mins shown here at points further along the shaft not shown.

6.
Summarize results from FEM calculation showing maximum normal stress (anywhere), load point deflection, strains at the strain gauge locations.
![Image 8]({{ "/assets/images/MaterialsFinal/eight.png" | relative_url }}){: style="width:100%;" }
Stress extremes reduce from the max and mins shown here at points further along the shaft not shown.
![Image 9]({{ "/assets/images/MaterialsFinal/nine.png" | relative_url }}){: style="width:100%;" }
The strain at the strain gauge is 1313.3 microstrain which matches the hand calculated value of 1396 microstrain.

7.
Torque wrench sensitivity in mV/V using strains from the FEM analysis

For a half-bridge configuration, the bridge output is given approximately by:
ΔV / V = (GF · ε) / 2
Gauge factor, GF = 2.0
Strain at gauge, ε = 1313 × 10⁻⁶
Substituting these values gives an output of approximately 1.313 mV/V at 600 in·lb, which exceeds the target sensitivity of 1.0 mV/V and indicates that the strain gauge signal is large enough for reliable measurement.

8.
Strain gauge selected (give type and dimensions). Note that design must physically have enough space to bond the gauges.

Type: 350 Ω linear foil gauge, 1-axis
Reference model: Omega SGD-3-350-LY13
Gauge grid length: ≈ 0.12 in (3 mm)
Grid width: ≈ 0.08–0.12 in
Backing / package size: ≈ 0.25 in × 0.15 in

The wrench handle has 0.75 in of flat width, so there is ample bonding area for the gauges. The gauges are aligned longitudinally to measure bending strain, with one on the top surface (tension) and one on the bottom surface (compression), arranged in a half-bridge to increase sensitivity and provide some temperature compensation.

