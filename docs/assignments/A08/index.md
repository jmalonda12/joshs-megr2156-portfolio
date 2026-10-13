# Assignment 8: Gear Box Design

## Purpose

The goal of this assignment was to design a gearbox that can be assembled and taken apart. I used the given specifications to calculate shaft stress and determine the requirements for the journal bearings, including pressure, velocity, and thickness. I then used these calculations to guide the design of the gearbox housing in CAD. The gearbox uses two spur gears with a gear ratio of 24:9. The required output torque is 1.25 in·lbf, and the output speed is 1100 rpm. The input shaft has a diameter of 0.125 inches, while the output shaft has a diameter of 0.250 inches. Both shafts are 1 inch long. Throughout the assignment, I documented my calculations and design decisions while working toward a final gearbox model. The figure below shows the two gears that need to fit inside the housing.
<img width="848" height="711" alt="image" src="https://github.com/user-attachments/assets/f18c117e-91a6-4e05-b13f-388eeeac1042" />
## Input Shaft (Power-Transmission Shaft)

For the input shaft, I used the specified diameter of 0.125 inches and calculated the torsional shear stress using the input torque obtained from the gear ratio. I selected steel as the shaft material because it is commonly used for power-transmission applications. The calculated shear stress was approximately 1,222 psi. I will compare this value with the allowable shear stress for the selected steel to determine whether the shaft diameter is sufficient. My calculations and free-body diagram are shown below.
<img width="1276" height="905" alt="image" src="https://github.com/user-attachments/assets/1aa1d7e9-eca8-418b-99db-a50517ff3e64" />

## Output Shaft (Short Shaft)

For the output shaft, I used the same torsional shear stress equation as the input shaft. The main difference was that the output shaft has a diameter of 0.250 inches and carries a torque of 1.25 in·lbf. After calculating the shear stress, I found that it was lower than the stress in the input shaft because the larger diameter reduces the stress. I then compared the calculated stress with the allowable stress for the selected shaft material to check whether the diameter was sufficient. My calculations and free-body diagram are shown below.
<img width="1296" height="841" alt="image" src="https://github.com/user-attachments/assets/fbf452ac-69e7-4850-a08b-b122d546b121" />


## Journal Bearings (Pressure, Velocity, and PV Rating)

The journal bearings support the shafts while allowing them to rotate. I used a free-body diagram to identify the forces acting on the bearings and organized the known and unknown values before starting the calculations. I then calculated the bearing pressure, surface velocity, and PV value to check whether the selected bearing could handle the operating conditions. The results will be compared with the bearing's allowable PV rating to determine whether the selection is suitable. My calculations and free-body diagram are shown below.
<img width="1882" height="1406" alt="image" src="https://github.com/user-attachments/assets/93f2803f-e37e-4489-b9cc-4f5f31a14ab7" />

Knowns

Input shaft diameter: d_in = 0.125 in

Output shaft diameter: d_out = 0.250 in

Gear ratio: GR = 24/9 = 2.667

Output torque: T_out = 1.25 in·lbf

Output speed: n_out = 1100 rpm

Input speed: n_in = 1100(2.667) = 2933.3 rpm

Pressure angle: alpha = 20 degrees

Assumed output gear pitch diameter: d_p = 1.00 in

Assumed input bearing length: L_in = 0.375 in

Assumed output bearing length: L_out = 1.00 in

Assumed allowable PV rating for porous bronze: PV_allow = 50000 psi·ft/min

Unknowns

Radial gear force, F_r

Bearing pressure, P

Surface velocity, V

PV rating, PV

Solving Algebraically

Tangential gear force:

F_t = (2 * T_out) / d_p

Radial gear force:

F_r = F_t * tan(alpha)

Bearing pressure:

P = F_r / (d * L)

Surface velocity:

V = (pi * d * n) / 12

PV rating:

PV = P * V

Solving Numerically

1. Tangential gear force

F_t = (2 * 1.25) / 1.00

F_t = 2.50 lbf

2. Radial gear force

F_r = 2.50 * tan(20 degrees)

F_r = 0.910 lbf

3. Input Bearing

Assume d = 0.125 in, L_in = 0.375 in, and n_in = 2933.3 rpm.

Bearing pressure:

P_in = 0.910 / (0.125 * 0.375)

P_in = 19.41 psi

Surface velocity:

V_in = (pi * 0.125 * 2933.3) / 12

V_in = 95.99 ft/min

PV rating:

PV_in = 19.41 * 95.99

PV_in = 1863 psi·ft/min

4. Output Bearing

Assume d = 0.250 in, L_out = 1.00 in, and n_out = 1100 rpm.

Bearing pressure:

P_out = 0.910 / (0.250 * 1.00)

P_out = 3.64 psi

Surface velocity:

V_out = (pi * 0.250 * 1100) / 12

V_out = 71.99 ft/min

PV rating:

PV_out = 3.64 * 71.99

PV_out = 262.1 psi·ft/min

Comparison with Allowable PV Rating

Assumed allowable rating:

PV_allow = 50000 psi·ft/min

Input bearing:

1863 < 50000

Output bearing:

262.1 < 50000

These preliminary PV values are below the assumed allowable rating. The bearing dimensions, actual material rating, gear pitch diameter, and radial loading must be verified before these results are treated as final.

## Journal Bearing Thickness

For the bearing thickness, I used the bearing material's load capacity and the force acting on the bearing to determine the minimum thickness required. I organized the known and unknown values and used a free-body diagram to identify the resultant force. After calculating the required thickness, I would select a practical thickness that provides adequate support and fits within the gearbox design. The calculations and free-body diagram are shown below.
Journal Bearing Thickness
<img width="1892" height="709" alt="image" src="https://github.com/user-attachments/assets/0f7983b4-8687-43e6-a883-39eedc1eb486" />

Knowns

Input shaft diameter: d_in = 0.125 in

Output shaft diameter: d_out = 0.250 in

Tangential gear force: F_t = 2.50 lbf

Radial gear force: F_r = 0.910 lbf

Allowable bearing pressure: P_allow = 4500 psi

Unknown

Minimum bearing wall thickness: t

Free-Body Diagram

Draw the bearing cross-section and show the resultant load acting on the bearing.

Solving Algebraically

Resultant force:

F_result = sqrt(F_t^2 + F_r^2)

Bearing cross-sectional area:

A = F_result / P_allow

For the cylindrical bearing wall:

A = (pi/4) * ((d + t)^2 - d^2)

Equating the areas:

F_result / P_allow = (pi/4) * ((d + t)^2 - d^2)

Solving for wall thickness:

t = sqrt((4 * F_result)/(pi * P_allow) + d^2) - d

Solving Numerically

Resultant force:

F_result = sqrt((2.50)^2 + (0.910)^2)

F_result = 2.660 lbf

Input bearing:

t_in = sqrt((4 * 2.660)/(pi * 4500) + (0.125)^2) - 0.125

Output bearing:

t_out = sqrt((4 * 2.660)/(pi * 4500) + (0.250)^2) - 0.250

The calculated minimum thicknesses must be rounded appropriately and compared with the actual wall thickness of the selected bearings before finalizing the design.
The output-shaft journal bearing I selected was the Mil. Spec. Oil-Embedded 841 Bronze Sleeve Bearing for a 1/4-inch shaft diameter, with a 3/8-inch housing ID and a length of 1/2 inch (McMaster-Carr part 7639N11). I chose this bearing because its oil-embedded bronze material helps reduce friction and wear while supporting the rotating shaft. Its dimensions also fit the 1/4-inch output shaft and provide a clear target for designing the housing. McMaster-Carr lists a dynamic radial load capacity of 200 lb at 120 rpm, so I would compare the bearing’s published specifications with my calculated pressure, surface velocity, and PV requirements before confirming the final selection.
<img width="1410" height="717" alt="image" src="https://github.com/user-attachments/assets/06035e01-3f10-4cf9-a20f-898e3de150fb" />
## Sketch of Vision

![Uploading image.png…]()

I decided to design the gearbox as a two-piece housing with a top and bottom section that can be fastened together with screws. This design makes it easier to assemble and disassemble the gearbox when maintenance or adjustments are needed. I included holes at the corners for the fasteners and an enclosed space for the gears, shafts, and journal bearings. I used this sketch as a starting point for creating the two housing halves in CAD. The sketch below shows my initial design idea.

image

## Generating a CAD Model

Creating the CAD model took more time than I originally expected because I had to make sure all the parts fit together correctly. I started by using parametric equations to define the main dimensions of the gearbox so I could make adjustments without having to redesign everything. I then worked on the top and bottom housing halves, making room for the gears, shafts, and journal bearings. I also added the mounting holes so the two halves could be fastened together and taken apart when needed. Throughout the process, I made adjustments to the dimensions to improve the fit and make sure the final design matched the assignment requirements.
<img width="1307" height="569" alt="image" src="https://github.com/user-attachments/assets/604c4c57-c028-4b3e-a11d-4422a29c06f1" />
I downloaded the necessary parts and started putting the gearbox together in CAD. I experimented with two different housing shapes before deciding to go with the simpler design. My original idea was more complicated than I expected, and I realized it would require more CAD skills and time than I had available. I decided to focus on a design that I could build accurately while still meeting the assignment requirements.
<img width="1908" height="796" alt="image" src="https://github.com/user-attachments/assets/66464a66-2daa-445e-a97d-14655ca916aa" />
I initially tried to make the housing symmetrical by splitting it into two halves. However, I had trouble separating the halves correctly in the assembly, so I decided to start over and create each half as a separate piece. This approach gave me more control over the dimensions and made it easier to assemble the gearbox and make adjustments as needed.
<img width="889" height="620" alt="image" src="https://github.com/user-attachments/assets/1eec0bd5-a07c-4f80-9ed2-7506d8f709cf" />
I originally thought I could extrude multiple moving parts together, but I later realized that approach would not work the way I expected. I started over, keeping only the main frame of the housing and creating holes for the shafts that would hold the gears. I placed the gears first to make sure they fit properly, then gradually added the other components. However, I worked on the design without the top half of the housing, which I later regretted because it would have helped me check the clearances and fit of all the components earlier in the process.
<img width="785" height="643" alt="image" src="https://github.com/user-attachments/assets/0f09fa4a-4efb-4d5c-8000-c47242183f1e" />
After spending several hours getting the gears to rotate properly, I moved on to designing the top half of the gearbox. Most of that process went smoothly until I noticed that the holes in the top and bottom halves were not lining up. This was confusing because I had copied the bottom half into a separate file and used it as the starting point for the top. After spending more time troubleshooting, I realized that some of the dimensions for the top and bottom had been reversed. I manually corrected the dimensions until the holes lined up properly. Once everything matched, I added the screw holes and hex nut holes so the two halves could be fastened together.
<img width="847" height="534" alt="image" src="https://github.com/user-attachments/assets/bbcc46a8-e0cc-4ff2-a1be-8f2e11b300e1" />
Below is the final result of my gearbox design. After working through the challenges with the gears, housing, and alignment, I was finally able to get everything assembled the way I wanted. Take a moment to enjoy the finished design!
<img width="891" height="678" alt="image" src="https://github.com/user-attachments/assets/5ac41e70-69eb-4117-92a0-20690df945a8" />
## Lessons Learned
I learned a lot more about SolidWorks while working on this assignment. Every time I think I am getting comfortable with the software, I run into a new challenge that forces me to learn something else. I spent many hours working on this gearbox, from getting the gears to rotate properly to making sure the top and bottom halves lined up. Looking back at how far I have come since first starting SolidWorks, I can tell that I am developing a useful new skill. One of my biggest takeaways was learning to pay closer attention to dimensions and orientation when flipping or modifying parts. I will definitely remember that lesson for future CAD projects.
