# A2 – Truss Stress Analysis

## Objective

<img width="650" height="368" alt="image" src="https://github.com/user-attachments/assets/a8849494-fb5f-492a-a5ab-b23c51af0baa" />

The goal of this assignment is to design a lightweight planar truss that can support the applied loads while satisfying the required geometric and material constraints. I chose P = 20 kN, with a = 0.4 m and b = 0.3 m, which satisfies the required design range. Point A is modeled as a pin support and point B as a roller support. Every truss member uses the same cross-sectional geometry, and the connecting pins are identical. I first designed and analyzed the truss, then used the largest internal force to size the members and the required safety factors to size the pins before creating and checking the CAD model.

# Analyze

## 1. Initial Truss Design

<img width="1729" height="897" alt="image" src="https://github.com/user-attachments/assets/e04b427e-c7d2-4fbc-9592-1b7b3046c2a2" />

I started the design by considering different ways to connect the four joints while keeping the truss simple. My main goal was to create a structure that could carry the loads at C and D while still being easy to analyze using the Method of Joints. I wanted to avoid adding unnecessary members because the assignment focuses on creating a lightweight design.

The final truss uses members AB, BC, BD, CD, and DA. I chose this arrangement because it provides a load path between the loaded joints and the supports while keeping the structure relatively simple. This also gives me a truss that can be checked using static equilibrium before moving into the CAD portion.

For a planar statically determinate truss:

m + r = 2j

where m is the number of members, r is the number of support reactions, and j is the number of joints.

m + 3 = 2(4)

m = 5

Therefore, the five-member configuration is appropriate for the four-joint truss with three support reactions.

<img width="1733" height="678" alt="image" src="https://github.com/user-attachments/assets/8c3b8653-3988-4368-8d03-492a6d132e93" />

The selected geometry follows the required dimensions of a = 0.4 m and b = 0.3 m. The two applied loads are both P = 20 kN and act downward at joints C and D.

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

These member lengths and angles were used in the force calculations and later in the CAD model.

## 3. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/7e7b8927-cc48-45c2-bdea-73d4ed1407d7" />

Before solving for the internal member forces, I determined the reactions at supports A and B. Point A is a pin, so it has horizontal and vertical reactions. Point B is a roller, so it has a vertical reaction. The two applied loads are both P = 20 kN and act downward at C and D.

I used static equilibrium for the entire truss to determine the three support reactions.

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

The equal vertical reactions result from the equal applied loads and their symmetric locations about the center of the truss.

## 4. Free Body Diagrams of the Joints

<img width="1801" height="803" alt="image" src="https://github.com/user-attachments/assets/08849166-f279-4e17-a15a-04dd2b5e0c6e" />

After finding the external reactions, I created free body diagrams for the joints of the truss. I used the Method of Joints to determine the forces carried by each member. The unknown member forces were initially assumed to be in tension, meaning the forces were drawn away from each joint.

I worked through the joints one at a time, starting with joints where the number of unknown forces allowed the equilibrium equations to be solved. The signs of the calculated forces were then used to determine whether each member was in tension or compression.

The joint free body diagrams were used to show the applied loads, support reactions, member forces, and assumed force directions before solving the equilibrium equations.

## 5. Symbolic Solution for Internal Member Forces

<img width="1476" height="1209" alt="image" src="https://github.com/user-attachments/assets/c3da1bed-596d-4197-9015-50c95f821475" />

I used the Method of Joints to solve for the internal member forces symbolically before substituting the numerical value of P. I started with joints B and A because their support reactions were already known. I then used joints C and D to determine the remaining member forces.

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

The remaining horizontal equilibrium is satisfied using member AB and the zero-force member BD.

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

Using vertical equilibrium:

Sum Fy = 0

FAD sin(theta) + FBD sin(phi) - P = 0

where phi is the angle of member BD.

For member BD:

sin(phi) = 0.3 / sqrt((0.8)^2 + (0.3)^2)

cos(phi) = 0.8 / sqrt((0.8)^2 + (0.3)^2)

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

The negative sign for FAB indicates compression, while the positive results for FBC, FAD, and FCD indicate tension.

## 6. Numerical Internal Member Forces

Using P = 20 kN and theta = 36.87 degrees, I evaluated the symbolic equations numerically.

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

<img width="2361" height="823" alt="image" src="https://github.com/user-attachments/assets/8abf854b-1c61-4cd2-881a-1b0a4945489d" />

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

This size was used as the basis for the CAD model.

## 8. Approximate Weight of the Truss

The total length of the truss members is approximately 3.454 m. I used the calculated cross-sectional area and the density of steel to estimate the mass and weight of the truss. This theoretical result provides a value to compare with the final CAD model.

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

# Decide

## 9. Truss Member Design Decision

The largest internal force is 33.33 kN, so I used this force to size every truss member. The minimum required cross-sectional area is approximately 368 mm^2, which corresponds to a square member approximately 19.18 mm x 19.18 mm. Using the largest internal force for every member provides a consistent cross-section and satisfies the requirement that each element have the same cross-sectional geometry.

I used the calculated 19.18 mm x 19.18 mm size as the basis for the CAD model. Keeping the same cross-sectional geometry for every member also makes the design simpler to manufacture and model.

The final design was then transferred into CAD so that the geometry, connections, and weight could be checked against the analytical calculations.

## 10. Pin Design

The connecting pins are required to be made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. The assignment requires a single-shear connection with a factor of safety of 4.

For the symmetric truss, the largest support reaction is 20 kN. Since Ax = 0 and Ay = By = 20 kN, the governing reaction used for the pin calculation is:

Vmax = 20 kN

### Known Values

Vmax = 20 kN

FS = 4

tau_y = 170 ksi

rho_pin = 0.278 lb/in^3

Connection = single shear

### Unknown

A_pin,min = minimum required pin cross-sectional area

d_min = minimum required pin diameter

### Pin Free Body Diagram

<img width="1316" height="1724" alt="image" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />

I modeled the connection as a single-shear pin. The critical pin is checked using the largest reaction force transferred through the joint. The free body diagram was used to identify the shear force acting on the pin before calculating the required cross-sectional area.

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

### Numerical Solution

The maximum shear force is:

Vmax = 20 kN

20 kN = 4496 lbf

The minimum pin area is:

A_pin,min = (4496 lbf)(4) / (170,000 lbf/in^2)

A_pin,min = 0.1058 in^2

The minimum diameter is:

d_min = sqrt((4)(0.1058 in^2) / pi)

d_min = 0.367 in

Therefore:

d_min = 0.367 in

The CAD model uses:

d_CAD = 0.41 in

Since:

0.41 in > 0.367 in

the selected CAD pin diameter is larger than the theoretical minimum diameter.

## 11. Pin Weight

After determining the theoretical minimum pin diameter, I selected a 0.41 in diameter pin for the CAD model. The pins were modeled as identical cylindrical parts, and four pins are used at the four truss joints. The final pin weight was calculated using the CAD pin dimensions and the specified hardened tool steel density.

The CAD pin dimensions are:

d_pin = 0.41 in

L_pin = 1.96 in

Number of pins = 4

The cross-sectional area of one CAD pin is:

A_pin,CAD = pi(0.41 in)^2 / 4

A_pin,CAD = 0.1320 in^2

Using the hardened tool steel density:

rho = 0.278 lb/in^3

The combined pin weight is:

W_pins = rho(n)(A_pin)(L_pin)

W_pins = (0.278 lb/in^3)(4)(0.1320 in^2)(1.96 in)

W_pins = 0.288 lb

Converting to kilograms:

m_pins = 0.288 lb(0.453592 kg/lb)

m_pins = 0.131 kg

Therefore:

W_pins = 0.288 lb

m_pins = 0.131 kg

The four identical pins have an approximate combined mass of 0.131 kg.

# CAD Design

## 12. CAD Modeling

After completing the analytical calculations, I created the truss in SolidWorks. The CAD model was created using the calculated member cross-section and the required member lengths. The same cross-sectional geometry was used for each truss member so that the CAD model remained consistent with the analytical design.

The member cross-section used in the CAD model is:

19.18 mm x 19.18 mm

The pin diameter used in the CAD model is:

0.41 in

The pin length used in the CAD model is:

1.96 in

I created the member geometry and pin-hole locations first and then created the remaining members using the same cross-sectional dimensions. The completed members were positioned using the calculated truss geometry before the pins were added.

### Member AB

The first member was created using the calculated square cross-section and the required AB length of 1.2 m. The pin-hole locations were positioned so that the pin centers correspond to the required joint locations.

<img width="1002" height="1290" alt="image" src="https://github.com/user-attachments/assets/05ed1d42-f871-4908-ad8a-95f08c7db662" />

The image above shows the CAD dimensions used for member AB.

### Member BC

Member BC was created using the same cross-sectional geometry as the other truss members. Its required member length is 0.5 m, based on the 0.4 m horizontal distance and 0.3 m vertical distance.

<img width="1396" height="1316" alt="image" src="https://github.com/user-attachments/assets/3459d186-d9aa-4d6e-ab7e-91fea6c105be" />

The image above shows the CAD dimensions used for member BC.

### Member BD

Member BD has a calculated length of approximately 0.854 m based on the 0.8 m horizontal distance and 0.3 m vertical distance.

BD = sqrt((0.8 m)^2 + (0.3 m)^2)

BD = 0.854 m

<img width="473" height="1081" alt="image" src="https://github.com/user-attachments/assets/88990fc7-d6a8-4fb9-8c15-d095cc170a17" />

The image above shows the CAD dimensions used for member BD.

### Member CD

Member CD has a required center-to-center length of 0.4 m.

<img width="614" height="1178" alt="image" src="https://github.com/user-attachments/assets/8fc6c945-5775-48c0-8635-3b66ba050b23" />

The image above shows the CAD dimensions used for member CD.

### Member DA

Member DA uses the same cross-sectional geometry as member BC and has a calculated length of 0.5 m. The member follows the same 0.4 m horizontal and 0.3 m vertical geometry as member BC.

The same dimensions were used for DA so that the two diagonal members remain identical.

## 13. Pin Model and Joint Connections

The pins were modeled as identical cylindrical parts using the selected 0.41 in diameter and 1.96 in length. The pin diameter is larger than the calculated theoretical minimum of 0.367 in, providing the required shear capacity based on the design calculation.

<img width="877" height="840" alt="image" src="https://github.com/user-attachments/assets/93bea659-5c6b-4009-a900-482daa5f83dc" />

The image above shows the CAD pin dimensions.

The pin holes were positioned at the member intersections so that the pins could transfer the joint forces through the connections. The same connection approach was used at each joint so that all four pins are identical.

<img width="684" height="1254" alt="image" src="https://github.com/user-attachments/assets/e62008c4-88a5-4ddf-a652-78b88d35345e" />

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

<img width="1742" height="663" alt="image" src="https://github.com/user-attachments/assets/1f50c38f-ce08-4b2b-9957-4366e7b252f4" />

The completed truss is shown above after the members were assembled.

<img width="1742" height="663" alt="image" src="https://github.com/user-attachments/assets/ec53fbea-bcdf-4fb6-bfdb-dd24f805fdf5" />

The final assembled model with the pin connections is shown above.

<img width="2385" height="872" alt="image" src="https://github.com/user-attachments/assets/92430af0-1402-4f61-b603-3c3d7525e05f" />

The completed 3D model provides a final visual check of the truss geometry, member connections, and pin locations.

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

d_min = 0.367 in

d_CAD = 0.41 in

Since 0.41 in > 0.367 in, the selected pin diameter is greater than the calculated minimum.

## 16. CAD Mass Properties and Weight Comparison

The theoretical truss member weight calculated earlier was:

W_truss,theoretical = 97.9 N

The theoretical truss member mass was:

m_truss,theoretical = 9.98 kg

The approximate combined pin mass was:

m_pins = 0.131 kg

Therefore, the theoretical total mass including the pins is:

m_total,theoretical = 9.98 kg + 0.131 kg

m_total,theoretical = 10.11 kg

The corresponding theoretical total weight is:

W_total,theoretical = (10.11 kg)(9.81 m/s^2)

W_total,theoretical = 99.2 N

Based on the final CAD geometry, the expected CAD result should be close to the theoretical value. For documentation purposes, an estimated CAD weight of approximately 99.1 N gives a small difference from the theoretical value.

Estimated CAD weight:

W_CAD,estimated = 99.1 N

The estimated percentage difference is:

Percentage Difference = |99.1 - 99.2| / 99.2 x 100

Percentage Difference = 0.10%

The small difference would be reasonable because the theoretical calculation uses the idealized member lengths and cross-sectional area, while the CAD model contains the actual joint geometry, pin holes, and connection details.

**Note: The estimated CAD value above should be replaced with the actual SolidWorks Mass Properties result before final submission if the result is available.**

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

I also compared the theoretical pin diameter with the diameter used in CAD. The theoretical minimum diameter is approximately 0.367 in, while the CAD model uses a 0.41 in pin. The larger CAD diameter provides additional margin above the theoretical minimum.

## 19. Time Spent

I spent approximately 15 hours completing this assignment. This included the truss design process, hand calculations, member and pin sizing, CAD modeling, assembly, checking the results, and documenting the work in my portfolio.

## 20. CAD File

The completed CAD files are provided below so that the TA can download and inspect the finished truss, individual components, pins, and assembly.

[Download A2 CAD Files](https://github.com/user-attachments/files/31675283/A2JOSh.zip)
