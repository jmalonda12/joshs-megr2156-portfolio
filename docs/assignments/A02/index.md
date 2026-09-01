# A2 – Truss Stress Analysis

## Objective

<img width="650" height="368" alt="image" src="https://github.com/user-attachments/assets/a8849494-fb5f-492a-a5ab-b23c51af0baa" />

The goal of this assignment is to design a lightweight planar truss that can support the applied loads while satisfying the required geometric and material constraints. I chose P = 20 kN, with a = 0.4 m and b = 0.3 m, which satisfies the range given in the assignment. Point A is modeled as a pin support and point B as a roller support. Every truss member will use the same cross-sectional area, and the connecting pins will be identical. I will first design and analyze the truss, then use the largest internal force to size the members and use the required safety factors to size the pins before creating and checking the CAD model.

# Analyze

## 1. Initial Truss Design

<img width="1729" height="897" alt="image" src="https://github.com/user-attachments/assets/e04b427e-c7d2-4fbc-9592-1b7b3046c2a2" />

I started the design by considering different ways to connect the four joints while keeping the truss simple. My main goal was to create a structure that could carry the loads at C and D while still being easy to analyze using the Method of Joints. I wanted to avoid adding unnecessary members because the assignment focuses on creating a lightweight design.

The final truss uses members AB, BC, BD, CD, and DA. I chose this arrangement because it provides a load path between the loaded joints and the supports while keeping the structure relatively simple. This also gives me a truss that can be checked using static equilibrium before moving into the CAD portion.

<img width="1733" height="678" alt="image" src="https://github.com/user-attachments/assets/8c3b8653-3988-4368-8d03-492a6d132e93" />

The selected geometry follows the required dimensions of a = 0.4 m and b = 0.3 m. The two applied loads are both P = 20 kN and act at joints C and D.

## 2. Truss Geometry and Member Lengths

After selecting the geometry, I determined the length of each member from the given dimensions. The top member AB is 1.2 m long. Members BC and DA are each 0.5 m long, while member CD is 0.4 m long. Member BD spans 0.8 m horizontally and 0.3 m vertically, giving a length of approximately 0.854 m.

The diagonal members BC and DA form a 3-4-5 triangle. Therefore, sin(theta) = 0.3 / 0.5 and cos(theta) = 0.4 / 0.5, giving theta = 36.87 degrees.

The total length of the truss members is L = 1.2 + 0.5 + 0.854 + 0.4 + 0.5 = 3.454 m.

These member lengths and angles will be used in the force calculations and later when creating the CAD model.

## 3. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/7e7b8927-cc48-45c2-bdea-73d4ed1407d7" />

Before solving for the internal member forces, I determined the reactions at supports A and B. Point A is a pin, so it has horizontal and vertical reactions. Point B is a roller, so it has a vertical reaction. The two applied loads are both P = 20 kN and act downward at C and D.

I used static equilibrium for the entire truss to determine the three support reactions.

### Symbolic Solution

From horizontal equilibrium, Sum Fx = 0, so Ax = 0.

From vertical equilibrium, Sum Fy = 0:

Ay + By - 2P = 0

Taking moments about A:

1.2(By) - P(0.4) - P(0.8) = 0

Solving for By gives By = P.

Substituting this into the vertical force equation gives Ay + P - 2P = 0, so Ay = P.

Therefore, the symbolic support reactions are Ax = 0, Ay = P, and By = P.

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

I used the Method of Joints to solve for the internal member forces symbolically before substituting the numerical value of P. I started with joints B and A because their support reactions are already known. I then used joints C and D to determine the remaining member forces.

For members BC and DA, the diagonal angle is theta = 36.87 degrees. The relationships for this angle are sin(theta) = 0.3 / 0.5 and cos(theta) = 0.4 / 0.5.

At joint B, vertical equilibrium gives:

By - FBC sin(theta) = 0

Therefore:

FBC = By / sin(theta)

Since By = P:

FBC = P / sin(theta)

At joint A, vertical equilibrium gives:

FAD sin(theta) - Ay = 0

Therefore:

FAD = Ay / sin(theta)

Since Ay = P:

FAD = P / sin(theta)

Using horizontal equilibrium at joint A:

FAB + FAD cos(theta) - Ax = 0

Since Ax = 0:

FAB = -FAD cos(theta)

Substituting FAD = P / sin(theta):

FAB = -P cos(theta) / sin(theta)

Therefore:

FAB = -P cot(theta)

At joint C, vertical equilibrium gives:

FBC sin(theta) - P = 0

This confirms:

FBC = P / sin(theta)

Using horizontal equilibrium at joint C:

FCD - FBC cos(theta) = 0

Therefore:

FCD = FBC cos(theta)

Substituting FBC = P / sin(theta):

FCD = P cos(theta) / sin(theta)

Therefore:

FCD = P cot(theta)

At joint D, member BD has a different angle because it spans 0.8 m horizontally and 0.3 m vertically. Let this angle be phi.

sin(phi) = 0.3 / sqrt(0.8^2 + 0.3^2)

cos(phi) = 0.8 / sqrt(0.8^2 + 0.3^2)

Using vertical equilibrium at joint D:

FAD sin(theta) + FBD sin(phi) - P = 0

Since FAD = P / sin(theta):

P + FBD sin(phi) - P = 0

Therefore:

FBD = 0

The symbolic results for all five members are therefore FBC = P / sin(theta), FAD = P / sin(theta), FAB = -P cot(theta), FCD = P cot(theta), and FBD = 0.

## 6. Numerical Internal Member Forces

Using P = 20 kN and theta = 36.87 degrees, I evaluated the symbolic equations numerically.

For member BC:

FBC = P / sin(theta)

FBC = 20 / sin(36.87)

FBC = 33.33 kN

Therefore, BC is in tension.

For member DA:

FAD = P / sin(theta)

FAD = 20 / sin(36.87)

FAD = 33.33 kN

Therefore, DA is in tension.

For member AB:

FAB = -P cot(theta)

FAB = -20 cot(36.87)

FAB = -26.67 kN

The negative sign indicates that AB is in compression.

For member CD:

FCD = P cot(theta)

FCD = 20 cot(36.87)

FCD = 26.67 kN

Therefore, CD is in tension.

For member BD:

FBD = 0 kN

Therefore, BD carries zero internal force for this loading condition.

The final internal member forces are:

- BC = 33.33 kN tension
- DA = 33.33 kN tension
- AB = 26.67 kN compression
- CD = 26.67 kN tension
- BD = 0 kN

The largest internal force is 33.33 kN and occurs in members BC and DA. Since every truss member must have the same cross-sectional area, this force will be used to size all of the truss members.

## 7. Member Cross-Sectional Area

<img width="2361" height="823" alt="image" src="https://github.com/user-attachments/assets/8abf854b-1c61-4cd2-881a-1b0a4945489d" />

The largest internal force was used to determine the minimum cross-sectional area required for the truss members. The required factor of safety is 3.5. I selected A500 Grade B steel for the truss members and used a yield strength of approximately 317 MPa.

### Known Values

Fmax = 33.33 kN

FS = 3.5

Yield strength = 317 MPa

### Symbolic Solution

The allowable stress is sigma_allowable = sigma_y / FS.

The normal stress relationship is sigma = F / A.

Therefore:

Fmax / A <= sigma_y / FS

Solving for the minimum area:

Amin = Fmax(FS) / sigma_y

### Numerical Solution

Amin = (33,330 N)(3.5) / (317 x 10^6 N/m^2)

Amin = 3.68 x 10^-4 m^2

Amin = 368 mm^2

For a square member:

side = sqrt(368)

side = 19.18 mm

Therefore, the theoretical minimum square member size is approximately 19.18 mm x 19.18 mm.

This theoretical size will be used as the starting point for the CAD model.

## 8. Approximate Weight of the Truss

The total length of the truss members is approximately 3.454 m. I used the calculated cross-sectional area and the density of steel to estimate the mass and weight of the truss.

Using a steel density of approximately 7850 kg/m^3:

m = rho A L

m = (7850)(3.68 x 10^-4)(3.454)

m = 9.98 kg

The weight is:

W = mg

W = (9.98)(9.81)

W = 97.9 N

Therefore, the theoretical weight of the truss is approximately 98 N.

# Decide

## 9. Truss Member Design Decision

The largest internal force was 33.33 kN, so I used this force to size every truss member. The minimum required cross-sectional area is approximately 368 mm^2, which corresponds to a square member approximately 19.18 mm x 19.18 mm.

I will use this calculated size as the starting point for the CAD model. Using the same cross-sectional geometry for every member follows the assignment requirement and makes the design easier to manufacture and model.

The final CAD model will be checked to make sure the geometry remains stable and that the calculated member size is represented correctly.

## 10. Pin Design

The connecting pins are required to be made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. The assignment requires a single-shear connection with a factor of safety of 4.

For the pin design, I used the largest force transferred through the critical joint based on the member-force analysis. The maximum shear force used in my handwritten calculation is 33.33 kN.

### Known Values

Vmax = 33.33 kN

FS = 4

Yield shear strength = 170 ksi

Density = 0.278 lb/in^3

### Pin Free Body Diagram

<img width="1316" height="1724" alt="image" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />

I modeled the connection as a single-shear pin. The critical pin is checked using the largest shear force transferred through the joint.

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

The maximum shear force used for the pin calculation is 33.33 kN.

33.33 kN = 7492 lbf

Using the required factor of safety:

A_pin,min = (7492 lbf)(4) / (170,000 lbf/in^2)

A_pin,min = 0.1763 in^2

For a circular pin:

d_min = sqrt(4(0.1763) / pi)

d_min = 0.474 in

Therefore, the theoretical minimum pin diameter is approximately 0.474 in.

This diameter will be used as the starting point when creating the pins in CAD.

## 11. Pin Weight

<img width="2385" height="872" alt="image" src="https://github.com/user-attachments/assets/92430af0-1402-4f61-b603-3c3d7525e05f" />

After determining the pin area and diameter, I calculated the approximate combined weight of the four identical pins. The pin length was based on the thickness of the truss members, with the pin length taken as three times the member thickness.

The member thickness is approximately 19.18 mm, which is approximately 0.755 in.

Therefore:

L_pin = 3(0.755 in)

L_pin = 2.265 in

The combined pin weight is:

W_pins = rho(4)(A_pin)(L_pin)

W_pins = (0.278 lb/in^3)(4)(0.1763 in^2)(2.265 in)

W_pins = 0.444 lb

Converting to kilograms:

m_pins = 0.444 lb(0.453592 kg/lb)

m_pins = 0.201 kg

Therefore, the approximate combined weight of the four pins is 0.444 lb, or approximately 0.201 kg.

# Communicate

## 12. Engineering Lessons Learned

One of the main things I learned from this assignment is how the geometry of a truss affects the forces carried by each member. I learned that the support reactions need to be determined before solving the individual joints because the reactions become known forces in the joint free body diagrams. Using the Method of Joints helped me connect the equilibrium equations to the actual tension and compression forces in the truss members.

I also learned the difference between stress and strength when sizing a structural member. The member cannot be sized only by looking at the applied force. Its cross-sectional area must be large enough to keep the stress below the allowable stress after the required factor of safety is applied.

The pin calculations showed me that the connections also have to be checked separately from the truss members. Even when the truss members are sized correctly, the pins still have to withstand the forces transferred through the joints. This helped me understand how the load moves through the entire structure instead of only focusing on the members.

The CAD portion will allow me to compare the theoretical design with the actual modeled geometry. I will use the CAD model to verify the dimensions, calculate the mass properties, and determine whether any changes are needed before finalizing the design.

## 13. Mistakes and Adjustments

One adjustment I made during the design process was comparing possible truss arrangements before settling on the final five-member configuration. I wanted the structure to remain simple while still providing a clear load path between the applied loads and the supports.

I also had to carefully keep track of the geometry when determining the member lengths and angles. The diagonal members BC and DA use the 0.4 m horizontal distance and 0.3 m vertical distance, giving the 3-4-5 triangle used in the force calculations. Member BD spans a different horizontal distance, so its length was calculated separately.

Another important part of the process was checking the calculations before moving into CAD. The member area, truss weight, pin area, and pin weight were all calculated from the selected load and material properties so that the CAD model can be compared against the theoretical results.

As I continue into the CAD portion, I will document any additional changes or mistakes instead of only showing the final model.

## 14. Time Spent

## 14. Time Spent

I spent approximately 15 hours completing this assignment. This included the truss design process, hand calculations, member and pin sizing, CAD modeling, checking the results, and documenting the work in my portfolio.
## 15. CAD File

The finished CAD file will be linked here after the CAD model is completed so that the TA can download the finished product.

[INSERT FINISHED CAD DOWNLOAD LINK HERE]
