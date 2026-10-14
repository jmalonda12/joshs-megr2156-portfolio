# A9 – Pulley System Design

## Objective

The objective of this assignment is to design a pulley system that transfers power between two parallel shafts. The design must meet the specified requirements for pulley diameter, shaft spacing, rotational speed, belt tension, and safety factor. I will use engineering calculations to determine the required belt dimensions, minimum shaft diameter, and journal bearing specifications. I will also design a supporting frame to hold the pulleys and shafts in the correct positions.

The design requirements are:

- **Pulley diameter:** Both pulleys must have a diameter of 3 inches.
- **Center distance:** The parallel shafts must be separated by 4–6 inches. I will use a center distance of 5 inches.
- **Rotational speed:** The operating speed must be between 1,000 and 2,000 rpm. I will use 1,500 rpm.
- **Static belt tension:** The belt tension must be between 4 and 6 lbf. I will use 5 lbf.
- **Pulley material:** The pulleys will be designed using aluminum.
- **Safety factor:** The design must satisfy a minimum safety factor of 3.
- **Belt material:** The belt is assumed to be polyurethane rubber with a yield strength of 3.25 MPa (471 psi) at 20% strain, based on the research paper “Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers.”

I will use these requirements to guide the calculations, component selection, and CAD design. The final design will include the belt, shafts, journal bearings, and a supporting frame.
## Belt Design

The first step in designing the pulley system was determining the belt dimensions and selecting a belt that would work with the two pulleys. I used the given pulley diameter of 3 inches, a center distance of 5 inches, a static belt tension of 5 lbf, and a safety factor of 3. I listed the knowns and unknowns, drew a free-body diagram (FBD) of the belt and pulley system, and developed the equations needed to calculate the tight-side and loose-side belt forces. I then used the polyurethane belt's specified yield strength to determine the required cross-sectional area and minimum belt diameter. Finally, I calculated the approximate belt length and used the results to identify a suitable belt from McMaster-Carr.
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/18a8fac8-6bb4-48fe-9a0b-5388b94c6c79" />

After solving for the required belt dimensions, I searched McMaster-Carr for a polyurethane round belt that would meet the design requirements. Based on my calculated minimum belt diameter of approximately 0.242 inches and an estimated belt length of 19.42 inches, I identified part 3044K608 as a potential option. The selected belt has a nominal diameter of 3/8 inch, which is larger than the calculated minimum diameter. Before finalizing the selection, I will verify that the product's available length and specifications are compatible with the pulley system.
<img width="1919" height="1090" alt="image" src="https://github.com/user-attachments/assets/f32081af-4c15-4d66-9f76-f62fff6f7c8d" />
After calculating the required belt diameter and approximate outer circumference, I searched McMaster-Carr for a suitable polyurethane round belt. I selected part 3044K608 as a potential option because it has a 3/8-inch diameter and an available outer circumference range of 12¼ to 24 inches, which includes my calculated belt length of approximately 19.42 inches. Its diameter is larger than my calculated minimum diameter, so it meets the preliminary size requirement. I will verify the final belt fit and tension before completing the design.
## Shaft Design
The next step was to determine the minimum shaft diameter needed to support the pulleys and transmit torque through the system. I started by listing the knowns and unknowns, then drew a free-body diagram (FBD) to show the forces acting on the shafts. Using the belt forces and pulley radius, I calculated the torque applied to the shaft. I then used the strength properties of 1060 hardened steel and the required safety factor of 3 to determine the minimum cross-sectional area and shaft diameter. These calculations helped establish a suitable shaft size for the pulley system.

<img width="1227" height="1282" alt="image" src="https://github.com/user-attachments/assets/e9771dbd-a8ee-493f-b4fb-dc19f2003a9b" />


After calculating the torque and minimum shaft diameter, I searched McMaster-Carr for a shaft that would meet the design requirements. I will select a shaft made from 1060 hardened steel with a diameter equal to or greater than my calculated minimum of approximately 0.101 inches. The selected shaft must also be compatible with the pulley bores and journal bearings. Before finalizing the selection, I will verify the shaft's material specifications and dimensions to ensure it meets the design requirements.
<img width="3807" height="1835" alt="image" src="https://github.com/user-attachments/assets/85e25a75-4e15-4406-9c63-8b38d0c9993f" />
## Journal Bearing Design

The next step was to design journal bearings to support the shafts and allow the pulleys to rotate smoothly. I started by listing the knowns and unknowns and drawing a free-body diagram (FBD) to show the forces acting on the shaft and bearings. I then calculated the bearing pressure and the shaft's linear velocity. Using these values, I determined the pressure-velocity (PV) value and compared it with the ratings of available bearing materials. Finally, I used the results to select a suitable journal bearing material for the pulley system.
<img width="1312" height="1199" alt="image" src="https://github.com/user-attachments/assets/b0bceb91-87d1-4223-b8c3-16f888687978" />

<img width="602" height="821" alt="image" src="https://github.com/user-attachments/assets/fa0476ff-f4af-4933-9ffb-40c471b0f99f" />
Based on my calculated values and the application limits in Machinery's Handbook, Table 4, I selected porous bronze as the preliminary journal bearing material. My calculated pressure-velocity (PV) value was 982.36 psi·ft/min, which is below the table's maximum PV limit of 50,000 psi·ft/min for porous bronze. I then searched McMaster-Carr for a journal bearing compatible with the selected 1/4-inch shaft. Before finalizing the selection, I will verify the bearing's dimensions, load capacity, and suitability for the operating speed.
<img width="1322" height="1270" alt="image" src="https://github.com/user-attachments/assets/2716b55c-70ab-4e9b-93fc-874fbff30549" />
Based on the calculated bearing pressure, surface velocity, and pressure-velocity (PV) value, I selected an oil-embedded 841 bearing bronze sleeve bearing as the preliminary bearing choice. I selected McMaster-Carr part 7639N11, which is designed for a 1/4-inch shaft and has a length of 1/2 inch. The bearing is lubricated with embedded synthetic oil and has a listed dynamic radial load capacity of 200 lb at 120 rpm. I will verify its suitability for the system's 1,500 rpm operating speed before finalizing the design.
## Frame Design

The final section of the assignment was to design a frame to support the pulley system. I planned the frame to hold the two shafts and journal bearings in position while maintaining the required 5-inch center distance between the pulleys. For the material selection, I considered strength, stiffness, weight, cost, and ease of fabrication. I also considered using an Ashby plot to compare material density with mechanical strength. Since the frame needs to support the rotating components without excessive bending or movement, the material must be strong and stiff enough for the expected loads. My final material selection will be based on these requirements and the engineering analysis of the frame.
<img width="532" height="408" alt="image" src="https://github.com/user-attachments/assets/a94f6be9-ebe2-4612-abd1-e681516a2374" />
I used the Young’s modulus–density Ashby plot to compare material classes based on stiffness and weight. The plot shows that metals generally provide higher stiffness than polymers and foams, while natural materials and some composites can offer lower density. For my pulley frame, I considered the need to support the shafts and bearings while limiting weight and avoiding excessive deflection. I will use these factors, along with cost and ease of fabrication, to justify the final frame material selection.
### Frame Design

Finally, I developed a preliminary frame design to support the pulley system. I chose a compact bracket-style frame to hold the journal bearings and keep the shafts aligned at the required 5-inch center distance. I planned to use rounded corners and fillets to reduce unnecessary material and avoid sharp corners. The final design will need to provide enough stiffness and strength to support the rotating components without excessive deflection. I will verify the frame dimensions and material choice based on the expected loads and ease of fabrication.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/88abf13a-ec4a-4551-a055-a36e2c9e67ee" />

## Lessons Learned
In this assignment, I learned how to calculate the required belt and shaft dimensions for a pulley system and how belt tension affects the forces acting on the shafts. I also learned how to calculate journal bearing pressure, surface velocity, and the pressure-velocity value to help select a suitable bearing material. Using the Machinery's Handbook table helped me understand how material limits affect bearing selection. Finally, I learned how an Ashby plot can be used to compare materials based on stiffness and density when choosing a frame material.


I hand-drew my initial sketches and used AI to enhance them into cleaner, more detailed images. The results turned out really well and made my designs easier to understand and present in my report.
This assignment took me approximately 3 and a half hours to complete.
