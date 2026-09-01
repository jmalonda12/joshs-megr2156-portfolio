# A2 – Truss Stress Analysis

## Objective

<img width="650" height="368" alt="Assignment Figure 1" src="https://github.com/user-attachments/assets/a8849494-fb5f-492a-a5ab-b23c51af0baa" />

The goal of this assignment is to design a lightweight planar truss that can support the applied loads while satisfying the required geometric and material constraints. I chose P = 20 kN, with a = 0.4 m and b = 0.3 m, which satisfies the required design range. Point A is modeled as a pin support and point B as a roller support. Every truss member uses the same cross-sectional geometry, and the connecting pins are identical. I first designed and analyzed the truss, then used the largest internal force to size the members and the required safety factors to size the pins before creating and checking the CAD model.

# Analyze

## 1. Initial Truss Design

<img width="1729" height="897" alt="Initial truss design sketches" src="https://github.com/user-attachments/assets/e04b427e-c7d2-4fbc-9592-1b7b3046c2a2" />

I started the design by considering different ways to connect the four joints while keeping the truss simple. My main goal was to create a structure that could carry the loads at C and D while still being easy to analyze using the Method of Joints. I wanted to avoid adding unnecessary members because the assignment focuses on creating a lightweight design.

The final truss uses members AB, BC, BD, CD, and DA. I chose this arrangement because it provides a load path between the loaded joints and the supports while keeping the structure relatively simple. This also gives me a truss that can be checked using static equilibrium before moving into the CAD portion.

For a planar statically determinate truss:

m + r = 2j

where:

m = number of members

r = number of support reactions

j = number of joints

For this truss:

m + 3 = 2(4)

m = 5

Therefore, the five-member configuration is appropriate for the four-joint truss with three support reactions.

<img width="1733" height="678" alt="Designed truss with dimensions" src="https://github.com/user-attachments/assets/8c3b8653-3988-4368-8d03-492a6d132e93" />

The selected geometry follows the required dimensions of a = 0.4 m and b = 0.3 m. The two applied loads are both P = 20 kN and act downward at joints C and D. These dimensions provide the basis for determining the individual member lengths and the angles used in the Method of Joints.

## 2. Truss Geometry and Member Lengths

After selecting the geometry, I determined the length of each member from the given dimensions. Member AB is 1.2 m long. Members BC and DA are each 0.5 m long, while member CD is 0.4 m long. Member BD spans 0.8 m horizontally and 0.3 m vertically.

For member BD:

BD = sqrt((0.8 m)^2 + (0.3 m)^2)

BD = 0.854 m

The diagonal members BC and DA form a 3-4-5 triangle. Therefore:

sin(theta) = 0.3 / 0.5

sin(theta) = 0.6

cos(theta) = 0.4 / 0.5

cos(theta) = 0.8

theta = 36.87 degrees

The total length of the truss members is:

L = 1.2 + 0.5 + 0.854 + 0.4 + 0.5

L = 3.454 m

These member lengths and angles were used in the force calculations and later in the CAD model. Determining the geometry before solving the forces also makes it possible to use the correct trigonometric relationships at each joint.

## 3. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/ba2c0ada-34e8-45bc-b82b-1bfd65c97ee8" />


Before solving for the internal member forces, I determined the reactions at supports A and B. Point A is a pin, so it has horizontal and vertical reactions. Point B is a roller, so it has a vertical reaction. The two applied loads are both P = 20 kN and act downward at C and D.

I used static equilibrium for the entire truss to determine the three support reactions. The support reactions are needed because they become known forces when the individual joints are analyzed.

### Symbolic Solution

From horizontal equilibrium:

Sum Fx = 0

Ax = 0

From vertical equilibrium:

Sum Fy = 0

Ay + By - 2P = 0

Taking moments about A:

Sum MA = 0

1.2(By) - P(0.4) - P(0.8) = 0

Solving for By:

1.2By = 1.2P

By = P

Substituting this into the vertical force equation:

Ay + P - 2P = 0

Ay = P

Therefore:

Ax = 0

Ay = P

By = P

### Numerical Solution

Using P = 20 kN:

Ax = 0 kN

Ay = 20 kN

By = 20 kN

The equal vertical reactions result from the equal applied loads and their symmetric locations about the center of the truss. These reactions are then used as known forces when solving the individual joint free body diagrams.

## 4. Free Body Diagrams of the Joints

<img width="2414" height="1058" alt="Free body diagrams of joints A, B, C, and D" src="https://github.com/user-attachments/assets/0c7876db-0e37-4e6e-9565-ee938e1f2579" />

After finding the external reactions, I created free body diagrams for the joints of the truss. I used the Method of Joints to determine the forces carried by each member. The unknown member forces were initially assumed to be in tension, meaning the forces were drawn away from each joint.

I worked through the joints one at a time, starting with joints where the number of unknown forces allowed the equilibrium equations to be solved. The signs of the calculated forces were then used to determine whether each member was in tension or compression.

The joint free body diagrams show the applied loads, support reactions, member forces, and assumed force directions before solving the equilibrium equations. These diagrams provide the visual setup for the symbolic and numerical calculations that follow.

## 5. Symbolic Solution for Internal Member Forces

<img width="1476" height="1209" alt="Symbolic internal member force calculations" src="https://github.com/user-attachments/assets/c3da1bed-596d-4197-9015-50c95f821475" />

I used the Method of Joints to solve for the internal member forces symbolically before substituting the numerical value of P. I started with joints B and A because their support reactions are already known. I then used joints C and D to determine the remaining member forces.

For members BC and DA:

sin(theta) = 0.3 / 0.5

cos(theta) = 0.4 / 0.5

theta = 36.87 degrees

### Joint B

Using vertical equilibrium:

Sum Fy = 0

By - FBC sin(theta) = 0

Therefore:

FBC = By / sin(theta)

Since By = P:

FBC = P / sin(theta)

Using horizontal equilibrium:

Sum Fx = 0

FAB + FBC cos(theta) = 0

Therefore:

FAB = -FBC cos(theta)

Substituting FBC:

FAB = -(P / sin(theta))cos(theta)

FAB = -P cot(theta)

The negative sign indicates compression.

### Joint A

Using vertical equilibrium:

Sum Fy = 0

FAD sin(theta) - Ay = 0

Therefore:

FAD = Ay / sin(theta)

Since Ay = P:

FAD = P / sin(theta)

Using horizontal equilibrium:

Sum Fx = 0

FAB + FAD cos(theta) - Ax = 0

Since Ax = 0:

FAB + FAD cos(theta) = 0

Therefore:

FAB = -FAD cos(theta)

Substituting FAD:

FAB = -(P / sin(theta))cos(theta)

FAB = -P cot(theta)

The negative sign indicates compression.

### Joint C

Using vertical equilibrium:

Sum Fy = 0

FBC sin(theta) - P = 0

Therefore:

FBC = P / sin(theta)

Using horizontal equilibrium:

Sum Fx = 0

FCD - FBC cos(theta) = 0

Therefore:

FCD = FBC cos(theta)

Substituting FBC:

FCD = (P / sin(theta))cos(theta)

FCD = P cot(theta)

The positive result indicates that CD is in tension.

### Joint D

Member BD has a different angle because it spans 0.8 m horizontally and 0.3 m vertically. Let this angle be phi.

For member BD:

sin(phi) = 0.3 / sqrt((0.8)^2 + (0.3)^2)

cos(phi) = 0.8 / sqrt((0.8)^2 + (0.3)^2)

Using vertical equilibrium at joint D:

FAD sin(theta) + FBD sin(phi) - P = 0

Since:

FAD = P / sin(theta)

then:

P + FBD sin(phi) - P = 0

Therefore:

FBD = 0

The symbolic results for all five members are:

FBC = P / sin(theta)

FAD = P / sin(theta)

FAB = -P cot(theta)

FCD = P cot(theta)

FBD = 0

The negative sign for FAB indicates compression, while the positive results for FBC, FAD, and FCD indicate tension. Member BD is a zero-force member for this loading condition.

## 6. Numerical Internal Member Forces

Using P = 20 kN and theta = 36.87 degrees, I evaluated the symbolic equations numerically. The numerical results provide the actual member forces that will be used to determine the critical force for member sizing. The sign of each result is also used to identify tension or compression.

### Member BC

FBC = P / sin(theta)

FBC = 20 / sin(36.87)

FBC = 33.33 kN

Therefore, BC is in tension.

### Member DA

FAD = P / sin(theta)

FAD = 20 / sin(36.87)

FAD = 33.33 kN

Therefore, DA is in tension.

### Member AB

FAB = -P cot(theta)

FAB = -20 cot(36.87)

FAB = -26.67 kN

The negative sign indicates that AB is in compression.

### Member CD

FCD = P cot(theta)

FCD = 20 cot(36.87)

FCD = 26.67 kN

Therefore, CD is in tension.

### Member BD

FBD = 0 kN

Therefore, BD is a zero-force member for this loading condition.

The final internal member forces are:

- BC = 33.33 kN tension
- DA = 33.33 kN tension
- AB = 26.67 kN compression
- CD = 26.67 kN tension
- BD = 0 kN

The largest internal force is 33.33 kN and occurs in members BC and DA. Since every truss member must have the same cross-sectional area, this force is used to size all of the truss members.

## 7. Member Cross-Sectional Area

<img width="2361" height="823" alt="Member cross-sectional area calculation" src="https://github.com/user-attachments/assets/8abf854b-1c61-4cd2-881a-1b0a4945489d" />

The largest internal force was used to determine the minimum cross-sectional area required for the truss members. The required factor of safety is 3.5. I selected A500 Grade B steel for the truss members and used a yield strength of approximately 317 MPa.

### Known Values

Fmax = 33.33 kN

FS = 3.5

sigma_y = 317 MPa

### Unknown

Amin = minimum required cross-sectional area

### Symbolic Solution

The allowable stress is:

sigma_allowable = sigma_y / FS

The normal stress relationship is:

sigma = F / A

Therefore:

Fmax / A <= sigma_y / FS

Solving for the minimum area:

Amin = Fmax(FS) / sigma_y

### Numerical Solution

Amin = (33,330 N)(3.5) / (317 x 10^6 N/m^2)

Amin = 3.68 x 10^-4 m^2

Amin = 368 mm^2

For a square member:

side = sqrt(368 mm^2)

side = 19.18 mm

Therefore, the theoretical minimum square member size is:

19.18 mm x 19.18 mm

This size was used as the basis for the CAD model. Because the same cross-sectional geometry is required for every element, the 368 mm^2 area is applied to all five truss members.

## 8. Approximate Weight of the Truss

The total length of the truss members is approximately 3.454 m. I used the calculated cross-sectional area and the density of steel to estimate the mass and weight of the truss. This theoretical result provides a baseline value that can later be compared with the CAD model.

Using a steel density of approximately 7850 kg/m^3:

m = rho A L

m = (7850 kg/m^3)(3.68 x 10^-4 m^2)(3.454 m)

m = 9.98 kg

The weight is:

W = mg

W = (9.98 kg)(9.81 m/s^2)

W = 97.9 N

Therefore:

W_truss,theoretical = 97.9 N

The theoretical truss member mass is approximately 9.98 kg, corresponding to a weight of approximately 97.9 N.

# Decide

## 9. Truss Member Design Decision

The largest internal force is 33.33 kN, so I used this force to size every truss member. The minimum required cross-sectional area is approximately 368 mm^2, which corresponds to a square member approximately 19.18 mm x 19.18 mm. Using the largest internal force for every member provides a consistent cross-section and satisfies the requirement that each element have the same cross-sectional geometry.

I used the calculated 19.18 mm x 19.18 mm size as the basis for the CAD model. Keeping the same cross-sectional geometry for every member also makes the design simpler to manufacture and model.

The final design was then transferred into CAD so that the geometry, connections, dimensions, and weight could be checked against the analytical calculations.

## 10. Pin Design

The connecting pins are required to be made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. The assignment requires a single-shear connection with a factor of safety of 4.

For the critical connection, I used the largest force transferred through the joint from the member-force analysis. The largest force used for the pin design is 33.33 kN. This provides a conservative check of the pin because the pin must safely transfer the force through the connection.

### Known Values

Vmax = 33.33 kN

FS = 4

tau_y = 170 ksi

rho_pin = 0.278 lb/in^3

Connection = single shear

### Unknown

A_pin,min = minimum required pin cross-sectional area

d_min = minimum required pin diameter

### Pin Free Body Diagram

<img width="1316" height="1724" alt="Pin free body diagram" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />

I modeled the connection as a single-shear pin. The critical pin is checked using the largest force transferred through the joint. The free body diagram was used to identify the shear force acting on the pin before calculating the required cross-sectional area.

### Symbolic Solution

The allowable shear stress is:

tau_allowable = tau_y / FS

The shear stress relationship is:

tau = V / A_pin

Therefore:

V / A_pin <= tau_y / FS

Solving for the minimum pin area:

A_pin,min = V(FS) / tau_y

For a circular pin:

A_pin = pi d^2 / 4

Therefore:

d_min = sqrt(4A_pin / pi)

Substituting the area equation gives:

d_min = sqrt(4V(FS) / (pi tau_y))

### Numerical Solution

The maximum shear force is:

Vmax = 33.33 kN

Converting to pounds-force:

Vmax = 33.33 kN(224.81 lbf/kN)

Vmax = 7492.9 lbf

The minimum pin area is:

A_pin,min = (7492.9 lbf)(4) / (170,000 lbf/in^2)

A_pin,min = 0.1763 in^2

The minimum diameter is:

d_min = sqrt((4)(0.1763 in^2) / pi)

d_min = 0.474 in

Therefore:

d_min = 0.474 in

The CAD model uses a pin diameter of:

d_CAD = 12.04 mm = 0.474 in

Therefore, the CAD pin diameter matches the calculated minimum required pin diameter.

## 11. Pin Weight

After determining the theoretical minimum pin diameter, I used the calculated diameter as the basis for the CAD pin. The pins were modeled as identical cylindrical parts, and four pins are used at the four truss joints. The pin weight was calculated using the specified hardened tool steel density and the dimensions used in the CAD model.

The CAD pin dimensions are:

d_pin = 0.474 in

L_pin = 1.96 in

Number of pins = 4

The cross-sectional area of one circular pin is:

A_pin = pi d^2 / 4

A_pin = pi(0.474 in)^2 / 4

A_pin = 0.1763 in^2

Using the hardened tool steel density:

rho_pin = 0.278 lb/in^3

The combined pin weight is:

W_pins = rho_pin(n)(A_pin)(L_pin)

W_pins = (0.278 lb/in^3)(4)(0.1763 in^2)(1.96 in)

W_pins = 0.386 lb

Converting to kilograms:

m_pins = 0.386 lb(0.453592 kg/lb)

m_pins = 0.175 kg

Therefore:

W_pins = 0.386 lb

m_pins = 0.175 kg

The four identical pins have an approximate combined mass of 0.175 kg.

# CAD Design

## 12. CAD Modeling

After completing the analytical calculations, I created the truss in SolidWorks. The CAD model was created using the calculated member cross-section and the required member lengths. The same cross-sectional geometry was used for each truss member so that the CAD model remained consistent with the analytical design.

The member cross-section used in the CAD model is:

19.18 mm x 19.18 mm

The pin diameter used in the CAD model is:

12.04 mm = 0.474 in

The pin length used in the CAD model is:

1.96 in

I created the member geometry and pin-hole locations first and then created the remaining members using the same cross-sectional dimensions. The completed members were positioned using the calculated truss geometry before the pins were added.

### Member AB

The first member was created using the calculated square cross-section and the required AB length of 1.2 m. The pin-hole locations were positioned so that the pin centers correspond to the required joint locations.

<img width="555" height="1163" alt="image" src="https://github.com/user-attachments/assets/669e0b7e-91f4-407c-8e60-f17657026b86" />

The image above shows the CAD dimensions used for member AB. The member length is based on the required 1.2 m truss geometry.

### Member BC

Member BC was created using the same cross-sectional geometry as the other truss members. Its required member length is 0.5 m, based on the 0.4 m horizontal distance and 0.3 m vertical distance.

<img width="684" height="1254" alt="image" src="https://github.com/user-attachments/assets/a53dac97-7736-4f4f-8508-afd834e8f0a0" />


The image above shows the CAD dimensions used for member BC. The diagonal geometry corresponds to the 3-4-5 triangle used in the analytical calculations.

### Member BD

Member BD has a calculated length of approximately 0.854 m based on the 0.8 m horizontal distance and 0.3 m vertical distance.

BD = sqrt((0.8 m)^2 + (0.3 m)^2)

BD = 0.854 m

<img width="473" height="1081" alt="CAD dimensions for member BD" src="https://github.com/user-attachments/assets/88990fc7-d6a8-4fb9-8c15-d095cc170a17" />

The image above shows the CAD dimensions used for member BD. The CAD member follows the calculated 0.854 m geometry.

### Member CD

Member CD has a required center-to-center length of 0.4 m.

<img width="997" height="929" alt="image" src="https://github.com/user-attachments/assets/02b507df-1b1a-4782-9e98-75e302b83c1f" />


The image above shows the CAD dimensions used for member CD. The center-to-center distance between joints C and D is 0.4 m.

### Member DA

Member DA uses the same cross-sectional geometry as member BC and has a calculated length of 0.5 m. The member follows the same 0.4 m horizontal and 0.3 m vertical geometry as member BC.

The same dimensions were used for DA so that the two diagonal members remain identical. This maintains the requirement that each truss element have the same cross-sectional geometry.

## 13. Pin Model and Joint Connections

The pins were modeled as identical cylindrical parts using a 12.04 mm diameter and a 1.96 in length. The 12.04 mm diameter is approximately 0.474 in, which matches the calculated theoretical minimum pin diameter.
<img width="1002" height="1290" alt="CAD dimensions for member AB" src="https://github.com/user-attachments/assets/05ed1d42-f871-4908-ad8a-95f08c7db662" />


The image above shows the CAD pin dimensions. The pin diameter is 12.04 mm and the pin length is 1.96 in.

The pin holes were positioned at the member intersections so that the pins could transfer the joint forces through the connections. The same connection approach was used at each joint so that all four pins are identical.

<img width="684" height="1254" alt="CAD joint connection geometry" src="https://github.com/user-attachments/assets/e62008c4-88a5-4ddf-a652-78b88d35345e" />

The image above shows the connection geometry used in the CAD model. The member cross-section is maintained around the joint while providing the required hole for the pin.

## 14. Final Truss Assembly

After creating the individual members and pins, I assembled the truss in SolidWorks. The members were positioned so that their pin holes aligned at the four joints, and the cylindrical pins were inserted through the corresponding holes. The completed model was then checked to make sure the geometry matched the truss used in the analytical calculations.

The final design contains:

- Member AB
- Member BC
- Member BD
- Member CD
- Member DA
- Four identical pins

<img width="1742" height="663" alt="Final truss assembly" src="https://github.com/user-attachments/assets/1f50c38f-ce08-4b2b-9957-4366e7b252f4" />

The completed truss is shown above after the members were assembled. The member arrangement matches the five-member analytical truss used throughout the calculations.

<img width="2385" height="872" alt="Final 3D truss model" src="https://github.com/user-attachments/assets/92430af0-1402-4f61-b603-3c3d7525e05f" />

The completed 3D model provides a final visual check of the truss geometry, member connections, and pin locations. The final assembly also provides the geometry needed for the CAD verification and mass-property comparison.

## 15. CAD Verification

The final CAD model was checked against the analytical design before determining the final weight. I verified the member dimensions, pin diameter, pin length, joint locations, and overall truss geometry. The CAD model uses the same basic dimensions used during the hand calculations, while the actual CAD geometry includes the connection details and pin holes.

The member design was checked against the required minimum area:

A_required = 368 mm^2

The square member used in the design is:

19.18 mm x 19.18 mm

A_CAD = 19.18 x 19.18

A_CAD = 368 mm^2

Therefore, the CAD member cross-sectional area matches the required analytical area.

The pin design was also checked:

d_min = 0.474 in

d_CAD = 12.04 mm = 0.474 in

Therefore, the CAD pin diameter matches the calculated minimum required diameter.

The CAD geometry therefore maintains the required member cross-sectional area and the calculated minimum pin diameter. The final model can now be compared against the theoretical mass and weight.

## 16. CAD Mass Properties and Weight Comparison

The theoretical truss member weight calculated earlier was:

W_truss,theoretical = 97.9 N

The theoretical truss member mass was:

m_truss,theoretical = 9.98 kg

The approximate combined pin mass was:

m_pins = 0.175 kg

Therefore, the theoretical total mass including the pins is:

m_total,theoretical = 9.98 kg + 0.175 kg

m_total,theoretical = 10.155 kg

The corresponding theoretical total weight is:

W_total,theoretical = (10.155 kg)(9.81 m/s^2)

W_total,theoretical = 99.6 N

The theoretical result provides the expected mass and weight for comparison with the CAD Mass Properties result. The final SolidWorks Mass Properties value should be taken directly from the completed CAD model so that the analytical and CAD results can be compared accurately.

The percentage difference should be calculated using:

Percentage Difference = |W_CAD - W_theoretical| / W_theoretical x 100

The difference can be explained by the actual CAD geometry, including the pin holes, joint geometry, and any modeling assumptions.

# Communicate

## 17. Engineering Lessons Learned

One of the main things I learned from this assignment is how the geometry of a truss affects the forces carried by each member. I learned that the support reactions need to be determined before solving the individual joints because the reactions become known forces in the joint free body diagrams. Using the Method of Joints helped me connect the equilibrium equations to the actual tension and compression forces in the members.

I also learned the difference between stress and strength when sizing a structural member. The member cannot be sized only by looking at the applied force. Its cross-sectional area must be large enough to keep the stress below the allowable stress after the required factor of safety is applied.

The pin calculations showed me that the connections have to be checked separately from the truss members. A member can have enough strength while the connection still needs to be checked for shear. Designing the pin using the required safety factor helped me understand how the load is transferred through the connection.

The CAD portion showed me how the theoretical calculations translate into an actual three-dimensional design. I had to keep track of member lengths, cross-sectional dimensions, pin diameters, hole locations, and assembly constraints so that the final model matched the analytical design.

## 18. Mistakes and Adjustments

One adjustment I made during the design process was comparing possible truss arrangements before settling on the final five-member configuration. I wanted to keep the structure simple while still providing a clear load path between the applied loads and the supports.

I also had to carefully keep track of the geometry when determining the member lengths and angles. The diagonal members BC and DA use the 0.4 m horizontal distance and 0.3 m vertical distance, giving the 3-4-5 triangle used in the force calculations. Member BD spans a different horizontal distance, so its length was calculated separately.

Another important part of the process was checking the signs of the internal member forces. The Method of Joints initially assumes tension, but a negative result indicates compression. After checking the equilibrium equations, member AB was identified as a compression member, while BC, DA, and CD were identified as tension members. Member BD is a zero-force member for the selected loading condition.

I also caught and corrected an inconsistency in the pin documentation. An earlier value of 0.41 in was recorded for the pin diameter, but after checking the analytical calculation against the CAD dimension, the correct CAD value was identified as 12.04 mm, which is approximately 0.474 in. This corrected value is consistent with the calculated theoretical minimum pin diameter.

## 19. Time Spent

I spent approximately 15 hours completing this assignment. This included the truss design process, hand calculations, member and pin sizing, CAD modeling, assembly, checking the results, and documenting the work in my portfolio.

## 20. CAD File

The completed CAD files are provided below so that the TA can download and inspect the finished truss, individual components, pins, and assembly.

[Download A2 CAD Files](https://github.com/user-attachments/files/31675283/A2JOSh.zip)
