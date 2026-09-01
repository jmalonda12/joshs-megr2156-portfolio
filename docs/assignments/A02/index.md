# A2 – Truss Stress Analysis

## Objective

<img width="650" height="368" alt="image" src="https://github.com/user-attachments/assets/a8849494-fb5f-492a-a5ab-b23c51af0baa" />

The goal of this assignment is to design a lightweight planar truss that can support the applied loads while satisfying the required geometric and material constraints. I will use a load of P = 20 kN, with a = 0.4 m and b = 0.3 m, as specified in the assignment. Point A is modeled as a pin support and point B as a roller support. The truss members will use the same cross-sectional area, and the connecting pins will also be identical. I will first determine the external reactions and internal member forces, then use the largest internal force to size the truss members with a factor of safety of 3.5. After sizing the pins using a factor of safety of 4, I will create the truss in CAD and compare the calculated weight with the CAD mass properties.

## Analyze

### 1. Initial Truss Geometry

<img width="1733" height="678" alt="image" src="https://github.com/user-attachments/assets/8c3b8653-3988-4368-8d03-492a6d132e93" />

I began the truss design by considering a simple triangulated geometry that could support the two applied loads while remaining straightforward to analyze and build. I selected the geometry with members AB, BC, BD, CD, and DA because it provides a stable load path between the supports and the loaded joints while keeping the number of members relatively small. The geometry follows the required dimensions of a = 0.4 m and b = 0.3 m, and I will use P = 20 kN at both C and D. I chose to keep the design simple so that I could verify the internal forces using the Method of Joints before sizing the members and pins.

<img width="1729" height="897" alt="image" src="https://github.com/user-attachments/assets/e04b427e-c7d2-4fbc-9592-1b7b3046c2a2" />

The dimensions of the members were determined from the geometry of the truss. The top member AB is 1.2 m long, while members BC and DA are each 0.5 m long. Member CD is 0.4 m long. The diagonal member BD has a length of approximately 0.854 m. These dimensions were used for the later force calculations and will also be used when creating the CAD model.

### 2. External Forces and Support Reactions

<img width="1801" height="1060" alt="image" src="https://github.com/user-attachments/assets/7e7b8927-cc48-45c2-bdea-73d4ed1407d7" />

Before solving for the internal member forces, I determined the reactions at supports A and B. I modeled A as a pin with horizontal and vertical reactions and B as a roller with a vertical reaction. The two applied loads are both 20 kN and act downward at points C and D. I used static equilibrium equations to determine the support reactions.

[INSERT YOUR HANDWRITTEN SUPPORT REACTION CALCULATIONS HERE]

The resulting support reactions are Ax = 0 kN, Ay = 20 kN, and By = 20 kN. The equal vertical reactions are consistent with the loading and symmetric geometry of the truss.

### 3. Free Body Diagrams and Internal Member Forces

<img width="1801" height="803" alt="image" src="https://github.com/user-attachments/assets/08849166-f279-4e17-a15a-04dd2b5e6e0c" />

After determining the support reactions, I used the Method of Joints to find the internal force in each member. I created a free body diagram for each joint and used the equilibrium equations in the horizontal and vertical directions. I started with the joints that had enough known forces to solve for the remaining unknown member forces. The member forces were first set up symbolically and then evaluated using the 20 kN loading.

[INSERT YOUR HANDWRITTEN JOINT CALCULATIONS HERE]

The diagonal members have an angle of approximately 36.87 degrees based on the 0.4 m horizontal distance and 0.3 m vertical distance. The calculated internal forces are:

- BC = 33.33 kN tension
- DA = 33.33 kN tension
- AB = 26.67 kN compression
- CD = 26.67 kN tension
- BD = 0 kN

The largest internal force is 33.33 kN, which occurs in members BC and DA. I will use this force for sizing the truss members in the next section.

### 4. Member Cross-Sectional Area

I will use the largest internal force from the truss analysis to determine the minimum required cross-sectional area of the members. The required factor of safety is 3.5, and the yield strength of the selected material will be used to determine the allowable stress.

[INSERT HANDWRITTEN MEMBER AREA CALCULATIONS HERE]

### 5. Truss Weight

After determining the required cross-sectional area, I will use the total length of the truss members and the material density to estimate the weight of the truss.

[INSERT HANDWRITTEN TRUSS WEIGHT CALCULATIONS HERE]

### 6. Pin Design

The connecting pins will be designed using hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in3. The pins will be designed as single-shear connections using the required factor of safety of 4.

[INSERT PIN FBD HERE]

[INSERT HANDWRITTEN PIN CALCULATIONS HERE]

### 7. Pin Weight

After determining the required pin cross-sectional area, I will use the pin dimensions and material density to calculate the approximate combined weight of the pins.

[INSERT HANDWRITTEN PIN WEIGHT CALCULATIONS HERE]

### 8. CAD Modeling and Verification

I will create the truss in SolidWorks using the calculated member dimensions and pin dimensions. The truss will be modeled as one part without the pins, and the pins will be modeled as cylinders with the required cross-sectional area and length. I will then use the CAD mass properties to determine the predicted weight and compare it with the hand calculation.

[INSERT CAD IMAGES HERE]

### 9. Comparison of Calculated and CAD Results

The hand-calculated weight and CAD-predicted weight will be compared to determine how closely the two methods agree. If there is a difference between the results, I will explain the reason for the difference based on the geometry, material properties, member dimensions, or modeling assumptions.

[INSERT COMPARISON HERE]

## Decide

### 1. Truss Geometry Decision

I decided to use a simple five-member truss consisting of AB, BC, BD, CD, and DA. I chose this geometry because it satisfies the required dimensions while keeping the structure simple enough to analyze using the Method of Joints. The design also provides a direct load path from the applied loads at C and D to the supports.

### 2. Material and Member Size Decision

I will use the calculated minimum cross-sectional area as the starting point for selecting the member geometry. The final member size will be based on the required factor of safety of 3.5 while also considering the weight of the truss and the ability to create the geometry in CAD.

### 3. Pin Design Decision

The pins will be designed using the required hardened tool steel properties and a factor of safety of 4. I will use a single-shear connection as specified in the assignment and select the pin dimensions based on the calculated minimum required area.

## Communicate

### 1. Engineering Lessons Learned

One of the main things I learned from this assignment is how the geometry of a truss affects the forces carried by each member. I also learned that it is important to determine the support reactions before solving the individual joints because those reactions become known forces in the joint free body diagrams. Working through the Method of Joints helped me connect the equilibrium equations to the actual forces in the truss members.

Another thing I learned was the difference between stress and strength. The member does not only need to support the applied load; its cross-sectional area has to be large enough that the resulting stress stays below the allowable stress when the required factor of safety is included. I will also be able to compare the theoretical design with the CAD model to see how closely the two methods agree.

### 2. Time Spent

I will record the actual total time spent completing the assignment after the truss, pin calculations, CAD model, and documentation are finished.

### 3. CAD File
<img width="1316" height="1724" alt="image" src="https://github.com/user-attachments/assets/60f5224f-6983-45db-9b0a-f216faf03e73" />
<img width="1619" height="585" alt="image" src="https://github.com/user-attachments/assets/83474453-bc87-4ccb-9de7-44f90aaca7a1" />

[INSERT LINK TO DOWNLOAD YOUR FINISHED CAD FILE HERE]
