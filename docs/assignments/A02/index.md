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

The diagonal members BC and DA form a 3-4-5 triangle. Therefore, their angle is:

sin(theta) = 0.3 / 0.5

cos(theta) = 0.4 / 0.5

theta = 36.87 degrees

The total length of the truss members is:

L = 1.2 + 0.5 + 0.854 + 0.4 + 0.5

L = 3.454 m

These dimensions will be used in the force calculations and later in the CAD model.

## 3. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/7e7b8927-cc48-45c2-bdea-73d4ed1407d7" />

Before solving for the internal member forces, I determined the reactions at supports A and B. Point A is a pin, so it has horizontal and vertical reactions. Point B is a roller, so it has a vertical reaction. The two applied loads are both 20 kN and act downward at C and D.

I used static equilibrium for the entire truss.

### Symbolic Solution

Sum Fx = 0

Ax = 0

Sum Fy = 0

Ay + By - 2P = 0

Sum MA = 0

1.2(By) - P(0.4) - P(0.8) = 0

Solving for By:

By = P

Substituting into the vertical force equation:

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

The equal vertical reactions make sense because the two applied loads are equal and are positioned symmetrically about the center of the truss.

## 4. Free Body Diagrams of the Joints

<img width="1801" height="803" alt="image" src="https://github.com/user-attachments/assets/08849166-f279-4e17-a15a-04dd2b5e6e0c" />

After finding the external reactions, I created free body diagrams for the joints of the truss. I used the Method of Joints to determine the forces in each member. The unknown member forces were initially assumed to be in tension, meaning they were drawn away from the joint. If the calculated force is negative, the member is actually in compression.

I worked through the joints one at a time, using the known support reactions and applied loads to determine the remaining member forces.

## 5. Symbolic Solution for Internal Member Forces

<img width="1774" height="822" alt="image" src="https://github.com/user-attachments/assets/aafa579d-0a8a-4982-a8b1-bea02732daec" />

I first set up the equations symbolically before substituting P = 20 kN. This makes it easier to see how the internal forces depend on the applied load.

At joint B:

Sum Fy = 0

By - FBC sin(theta) = 0

FBC = By / sin(theta)

Since By = P:

FBC = P / sin(theta)

At joint A:

Sum Fy = 0

FAD sin(theta) - Ay = 0

FAD = Ay / sin(theta)

Since Ay = P:

FAD = P / sin(theta)

The remaining member forces were found by continuing the Method of Joints at joints C and D.

## 6. Numerical Internal Member Forces

Using P = 20 kN and theta = 36.87 degrees, the internal member forces are:

- BC = 33.33 kN tension
- DA = 33.33 kN tension
- AB = 26.67 kN compression
- CD = 26.67 kN tension
- BD = 0 kN

The largest internal force is 33.33 kN and occurs in members BC and DA. Since every truss member must have the same cross-sectional area, this force will be used to size all of the members.

## 7. Member Cross-Sectional Area

<img width="2361" height="823" alt="image" src="https://github.com/user-attachments/assets/8abf854b-1c61-4cd2-881a-1b0a4945489d" />

The largest internal force was used to determine the minimum cross-sectional area required for the truss members. The required factor of safety is 3.5.

I selected A500 Grade B steel for the truss members. The yield strength used for the calculation is approximately 317 MPa.

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

side = sqrt(368)

side = 19.18 mm

Therefore, the theoretical minimum square member size is approximately:

19.18 mm x 19.18 mm

## 8. Approximate Weight of the Truss

The total length of the members is approximately 3.454 m. I used the cross-sectional area from the previous section and the density of steel to estimate the mass and weight of the truss.

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

I will use this calculated size as the starting point for the CAD model. The CAD model will allow me to check the actual geometry and mass before deciding whether the member dimensions need to be adjusted.

## 10. Pin Design

The connecting pins are required to be made from hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. The assignment requires the connection to be designed as a single-shear connection with a factor of safety of 4.

The pin is designed based on the largest reaction load transferred through a joint. The largest joint reaction is 20 kN.

### Known Values

Vmax = 20 kN

FS = 4

Yield shear strength = 170 ksi

Density = 0.278 lb/in^3

### Pin Free Body Diagram

<img width="1316" height="1724" alt="image" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />

I modeled the connection as a single-shear pin. The shear force used for the pin design is based on the largest joint reaction.

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

The maximum reaction load is 20 kN.

20 kN = approximately 4496 lbf

A_pin,min = (4496)(4) / 170000

A_pin,min = 0.1058 in^2

The minimum diameter is:

d_min = sqrt(4(0.1058) / pi)

d_min = 0.367 in

Therefore, the theoretical minimum pin diameter is approximately 0.367 in.

This diameter will be used as the starting point when creating the pins in CAD.

## 11. Pin Weight

The combined weight of the pins will be determined after the final pin length and number of pins are established in the CAD model. I will use the calculated pin area, pin diameter, pin length, number of pins, and hardened tool steel density to determine the total pin weight.

[INSERT YOUR HANDWRITTEN PIN WEIGHT CALCULATION HERE]

# Communicate

## 12. Engineering Lessons Learned

One of the main things I learned from this assignment is how the geometry of a truss affects the forces carried by each member. I learned that the support reactions need to be determined before solving the individual joints because the reactions become known forces in the joint free body diagrams. Using the Method of Joints helped me connect the equilibrium equations to the actual tension and compression forces in the truss members.

I also learned the difference between stress and strength when sizing a structural member. The member cannot be sized only by looking at the applied force. Its cross-sectional area must be large enough to keep the stress below the allowable stress after the required factor of safety is applied.

The pin calculations showed me that the connections also have to be checked separately from the truss members. Even when the truss members are sized correctly, the pins still have to withstand the forces transferred through the joints. This helped me understand how the load moves through the entire structure instead of only focusing on the members.

The CAD portion will give me an opportunity to compare the theoretical design with the actual modeled geometry. This comparison will show how closely the hand calculations match the CAD model and will help identify any differences caused by the final dimensions or modeling decisions.

## 13. Mistakes and Adjustments

One adjustment I made during the design process was comparing possible truss arrangements before settling on the final five-member configuration. I wanted the structure to remain simple while still providing a clear load path between the applied loads and the supports.

I also had to carefully keep track of the geometry when determining the member lengths and angles. The diagonal members BC and DA use the 0.4 m horizontal distance and 0.3 m vertical distance, giving the 3-4-5 triangle used in the force calculations. Member BD spans a different horizontal distance, so its length must be calculated separately.

As I continue into the CAD portion, I will document any additional changes or mistakes instead of only showing the final model.

## 14. Time Spent

I will record the actual total time spent completing the assignment after the CAD model and final documentation are finished. This will include the time spent designing the truss, completing the calculations, sizing the members and pins, creating the CAD model, checking the results, and preparing the portfolio.

## 15. CAD File

The finished CAD file will be linked here after the CAD model is completed so that the TA can download the finished product.

[INSERT FINISHED CAD DOWNLOAD LINK HERE]
