# A2 – Truss Stress Analysis

## Objective

<img width="650" height="368" alt="image" src="https://github.com/user-attachments/assets/a8849494-fb5f-492a-a5ab-b23c51af0baa" />

The goal of this assignment is to design a lightweight planar truss that can support the applied loads while satisfying the required geometric and material constraints. I chose P = 20 kN, with a = 0.4 m and b = 0.3 m, which satisfies the required design range. Point A is modeled as a pin support and point B as a roller support. Every truss member uses the same cross-sectional geometry, and the connecting pins are identical. I first designed and analyzed the truss, then used the largest internal force to size the members and the required safety factors to size the pins before creating and checking the CAD model.

# Analyze

## 1. Initial Truss Design

<img width="1729" height="897" alt="image" src="https://github.com/user-attachments/assets/e04b427e-c7d2-4fbc-9592-1b7b3046c2a2" />

I started the design by considering different ways to connect the four joints while keeping the truss simple. My main goal was to create a structure that could carry the loads at C and D while still being easy to analyze using the Method of Joints. I wanted to avoid adding unnecessary members because the assignment focuses on creating a lightweight design.

For a planar truss, the relationship m + r = 2j can be used to determine the required number of members. There are 4 joints and 3 support reactions, so:

m + r = 2j

m + 3 = 2(4)

m = 5

Therefore, a statically determinate truss with these four joints and three reactions requires five members.

The final truss uses members AB, BC, BD, CD, and DA. I chose this arrangement because it provides a load path between the loaded joints and the supports while keeping the structure relatively simple.

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

The total member length is:

L = 1.2 + 0.5 + 0.854 + 0.4 + 0.5

L = 3.454 m

These member lengths and angles were used in the force calculations and later in the CAD model.

## 3. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/7e7b8927-cc48-45c2-bdea-73d4ed1407d7" />

Before solving for the internal member forces, I determined the reactions at supports A and B. Point A is a pin, so it has horizontal and vertical reactions. Point B is a roller, so it has a vertical reaction. The two applied loads are both P = 20 kN and act downward at C and D.

I used static equilibrium for the entire truss.

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

Substituting into the vertical force equation:

Ay + P - 2P = 0

Ay = P

Therefore, the symbolic support reactions are:

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

After finding the external reactions, I created free body diagrams for each joint of the truss. I used the Method of Joints to determine the forces carried by each member. The unknown member forces were initially assumed to be in tension, meaning the forces were drawn away from each joint.

I worked through the joints one at a time, starting with joints where the number of unknown forces allowed the equilibrium equations to be solved. The signs of the calculated forces were then used to determine whether each member was in tension or compression.

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

Using horizontal equilibrium:

FAB + FBC cos(theta) + FBD cos(phi) = 0

where:

sin(phi) = 0.3 / sqrt((0.8)^2 + (0.3)^2)

cos(phi) = 0.8 / sqrt((0.8)^2 + (0.3)^2)

The remaining equations show that:

FBD = 0

Therefore:

FAB = -FBC cos(theta)

Substituting FBC:

FAB = -(P / sin(theta))cos(theta)

FAB = -P cot(theta)

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

FAB = -P cot(theta)

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

However, because the force direction at C is opposite the assumed tension direction for CD, the member is in compression. Therefore:

FCD = -FBC cos(theta)

Substituting FBC:

FCD = -P cot(theta)

### Joint D

Using vertical equilibrium:

Sum Fy = 0

FAD sin(theta) + FBD sin(phi) - P = 0

Since:

FAD = P / sin(theta)

Then:

P + FBD sin(phi) - P = 0

Therefore:

FBD = 0

The symbolic results are therefore:

FBC = P / sin(theta)

FAD = P / sin(theta)

FAB = -P cot(theta)

FCD = -P cot(theta)

FBD = 0

The negative signs indicate compression for members AB and CD.

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

FCD = -P cot(theta)

FCD = -20 cot(36.87)

FCD = -26.67 kN

The negative sign indicates that CD is in compression.

### Member BD

FBD = 0 kN

Therefore, BD is a zero-force member for this loading condition.

The final internal member forces are:

- BC = 33.33 kN tension
- DA = 33.33 kN tension
- AB = 26.67 kN compression
- CD = 26.67 kN compression
- BD = 0 kN

The largest internal force is 33.33 kN and occurs in members BC and DA. Since every truss member must have the same cross-sectional area, this force is used to size all of the truss members.

## 7. Member Cross-Sectional Area

<img width="2361" height="823" alt="image" src="https://github.com/user-attachments/assets/8abf854b-1c61-4cd2-881a-1b0a4945489d" />

The largest internal force was used to determine the minimum cross-sectional area required for the truss members. The required factor of safety is 3.5. I selected A500 Grade B steel for the truss members and used a yield strength of approximately 317 MPa.

### Known Values

Fmax = 33.33 kN

FS = 3.5

Yield strength = 317 MPa

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

The total length of the truss members is approximately 3.454 m. I used the calculated cross-sectional area and the density of steel to estimate the mass and weight of the truss.

Using a steel density of approximately 7850 kg/m^3:

m = rho A L

m = (7850 kg/m^3)(3.68 x 10^-4 m^2)(3.454 m)

m = 9.98 kg

The weight is:

W = mg

W = (9.98 kg)(9.81 m/s^2)

W = 97.9 N

Therefore, the theoretical weight of the truss members is approximately:

W_truss = 97.9 N

# Decide

## 9. Truss Member Design Decision

The largest internal force is 33.33 kN, so I used this force to size every truss member. The minimum required cross-sectional area is approximately 368 mm^2, which corresponds to a square member approximately 19.18 mm x 19.18 mm.

I used this calculated size as the basis for the CAD model. Using the same cross-sectional geometry for every member follows the assignment requirement and makes the design easier to manufacture and model.

The final CAD model was then checked to make sure the members connect correctly at all four joints and that the calculated dimensions are represented in the model.

## 10. Pin Design

The connecting pins are made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. The connection is modeled as a single-shear connection with a factor of safety of 4.

Because the truss is symmetric and Ax = 0, the resultant force transferred through each joint is 20 kN. Therefore, the governing pin shear force is:

Vmax = 20 kN

This value is used to size the identical pins.

### Known Values

Vmax = 20 kN

FS = 4

Yield shear strength = 170 ksi

Density = 0.278 lb/in^3

Connection type = single shear

### Pin Free Body Diagram

<img width="1316" height="1724" alt="image" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />

I modeled the connection as a single-shear pin. The governing joint force is used to determine the minimum required pin area.

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

Therefore, the theoretical minimum pin diameter is approximately:

d_min = 0.367 in

The CAD model uses a pin diameter of:

d_CAD = 0.41 in

Since:

0.41 in > 0.367 in

the CAD pin is larger than the theoretical minimum required diameter.

Therefore, the selected CAD pin satisfies the shear-stress requirement.

## 11. Pin Weight

The CAD pins were modeled using a diameter of 0.41 in and a length of approximately 1.96 in. Four identical pins are used in the completed truss assembly.

The cross-sectional area of one CAD pin is:

A_pin,CAD = pi(0.41 in)^2 / 4

A_pin,CAD = 0.1320 in^2

Using the hardened tool steel density:

rho = 0.278 lb/in^3

The total weight of the four CAD pins is estimated using:

W_pins = rho(n)(A_pin)(L_pin)

Using:

n = 4

A_pin = 0.1320 in^2

L_pin = 1.96 in

W_pins = (0.278 lb/in^3)(4)(0.1320 in^2)(1.96 in)

W_pins = 0.288 lb

Converting to kilograms:

m_pins = 0.288 lb(0.453592 kg/lb)

m_pins = 0.131 kg

The approximate combined weight of the four CAD pins is therefore:

W_pins = 0.288 lb

m_pins = 0.131 kg

# CAD Design

## 12. CAD Modeling

After completing the analytical calculations, I created the truss in SolidWorks. The CAD model was created using the calculated member cross-section and the required member lengths. The same cross-sectional geometry was used for each truss member.

The member cross-section used in the CAD model is approximately:

19.18 mm x 19.18 mm

The pin diameter used in the CAD model is:

0.41 in

The pin length used in the CAD model is:

1.96 in

The CAD model was built as individual members and pins before being assembled into the final truss.

### Member AB

The first member was created using the square cross-section and the calculated AB length. The pin holes were placed so that the pin centers correspond to the required joint locations.

<img width="1002" height="1290" alt="image" src="https://github.com/user-attachments/assets/05ed1d42-f871-4908-ad8a-95f08c7db662" />

The image above shows the CAD dimensions used for member AB.

### Member BC

Member BC was created using the same cross-sectional geometry as the other members. Its calculated center-to-center member length is 0.5 m.

<img width="1396" height="1316" alt="image" src="https://github.com/user-attachments/assets/3459d186-d9aa-4d6e-ab7e-91fa6c105be5" />

The image above shows the CAD dimensions used for member BC.

### Member BD

Member BD has a calculated length of approximately 0.854 m based on the 0.8 m horizontal distance and 0.3 m vertical distance.

BD = sqrt((0.8)^2 + (0.3)^2)

BD = 0.854 m

<img width="473" height="1081" alt="image" src="https://github.com/user-attachments/assets/88990fc7-d6a8-4fb9-8c15-d095cc170a17" />

The image above shows the CAD dimensions used for member BD.

### Member CD

Member CD has a center-to-center length of 0.4 m.

<img width="614" height="1178" alt="image" src="https://github.com/user-attachments/assets/8fc6c945-5775-48c0-8635-3b66ba050b23" />

The image above shows the CAD dimensions used for member CD.

### Pin Model

The pins were modeled as identical cylindrical parts. The CAD pin diameter is 0.41 in and the pin length is approximately 1.96 in.

<img width="877" height="840" alt="image" src="https://github.com/user-attachments/assets/93bea659-5c6b-4009-a900-482daa5f83dc" />

The image above shows the CAD pin dimensions.

## 13. Final Truss Assembly

After creating the individual members and pins, I assembled the parts in SolidWorks. The members were positioned so that their pin holes align at the four truss joints. Four identical pins were then inserted into the joint locations.

The final assembly contains:

- Member AB
- Member BC
- Member BD
- Member CD
- Member DA
- Four identical truss pins

<img width="684" height="1254" alt="image" src="https://github.com/user-attachments/assets/e62008c4-88a5-4ddf-a652-78b88d35345e" />

The completed CAD assembly shows the individual members connected at the four joints.

<img width="1742" height="663" alt="image" src="https://github.com/user-attachments/assets/1f50c38f-ce08-4b2b-9957-4366e7b252f4" />

The completed truss is shown above after the members were assembled.


The final assembled model with the pin connections is shown above. The CAD model maintains the same basic geometry used in the analytical calculations.

## 14. CAD Mass Properties and Verification

The final step was to check the completed CAD model using SolidWorks Mass Properties. This allows the modeled mass and weight to be compared with the theoretical calculations.

The theoretical member weight calculated previously was:

W_theoretical,truss = 97.9 N

The CAD model was checked using the Mass Properties tool to determine the actual modeled mass and weight. The CAD result should include the actual modeled member geometry, holes, and pins.

The difference between the theoretical and CAD values can be caused by the additional material around the pin holes, the exact member lengths used in CAD, the pin dimensions, and other geometric details included in the final model.

The Mass Properties result provides the final verification that the CAD model represents the calculated design.

# Communicate

## 15. Engineering Lessons Learned

One of the main things I learned from this assignment is how the geometry of a truss affects the forces carried by each member. I learned that the support reactions need to be determined before solving the individual joints because the reactions become known forces in the joint free body diagrams. Using the Method of Joints helped me connect the equilibrium equations to the actual tension and compression forces in the truss members.

I also learned the difference between stress and strength when sizing a structural member. The member cannot be sized only by looking at the applied force. Its cross-sectional area must be large enough to keep the stress below the allowable stress after the required factor of safety is applied.

The pin calculations showed me that the connections also have to be checked separately from the truss members. Even when the truss members are sized correctly, the pins still have to withstand the forces transferred through the joints. This helped me understand how the load moves through the entire structure instead of only focusing on the members.

The CAD portion showed me how the theoretical calculations translate into an actual three-dimensional design. I had to keep track of member lengths, cross-sectional dimensions, pin diameters, hole locations, and assembly constraints so that the final model matched the analytical design.

## 16. Mistakes and Adjustments

One adjustment I made during the design process was comparing possible truss arrangements before settling on the final five-member configuration. I wanted the structure to remain simple while still providing a clear load path between the applied loads and the supports.

I also had to carefully keep track of the geometry when determining the member lengths and angles. The diagonal members BC and DA use the 0.4 m horizontal distance and 0.3 m vertical distance, giving the 3-4-5 triangle used in the force calculations. Member BD spans a different horizontal distance, so its length was calculated separately.

Another important adjustment was checking the signs of the internal member forces. The Method of Joints initially assumes tension, but negative results indicate compression. After checking the equilibrium equations, members AB and CD were identified as compression members, while BC and DA were identified as tension members. Member BD is a zero-force member for the selected loading condition.

I also compared the theoretical pin diameter with the diameter used in CAD. The theoretical minimum diameter is approximately 0.367 in, while the CAD model uses a 0.41 in pin. The larger CAD diameter provides additional margin above the theoretical minimum.

## 17. Time Spent

I spent approximately 15 hours completing this assignment. This included the truss design process, hand calculations, member and pin sizing, CAD modeling, assembly, checking the results, and documenting the work in my portfolio.

## 18. CAD File

The completed CAD files will be provided with the portfolio so that the TA can inspect the individual members, pins, and final assembly.
[A2JOSh.zip](https://github.com/user-attachments/files/31675283/A2JOSh.zip)

