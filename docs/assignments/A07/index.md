Objective

The objective of this assignment is to improve the bracket design developed in Assignments #5 and #6 using finite element analysis (FEA). The goal is to develop a bracket with high stiffness, high strength, and low weight while maintaining the original assigned material.

The original design requirements from Assignment #5 include a 600 lbf applied load, Aluminum 6061-T6, a yield strength of 35,000 psi, a Young's modulus of 10,000,000 psi, a safety factor of 4, and a maximum allowable deflection of 0.005 in.

Three bracket designs will be evaluated. Each design will undergo static stress analysis, including appropriate loading, constraints, and mesh selection. The stress, displacement, and safety factor results will be checked for mesh convergence within a 7% difference, following the assignment instructions. The results will then be used to guide geometry modifications and compare the strength, stiffness, and mass of each design.

<img width="1007" height="896" alt="image" src="https://github.com/user-attachments/assets/6231dbe0-8824-404a-9cd8-19d550d3a756" />

<img width="1396" height="1199" alt="image" src="https://github.com/user-attachments/assets/65aa8f87-a960-4297-9443-3db7551db2f1" />
<img width="1356" height="1090" alt="image" src="https://github.com/user-attachments/assets/b417ef6e-4d69-4ff1-865c-50f776a59b2d" />
<img width="1347" height="1114" alt="image" src="https://github.com/user-attachments/assets/4a7c7b32-d96c-4160-ab89-83aa724535ea" />
The initial mass was approximately 1.33 lb, the factor of safety was 1.4, the maximum stress was 25,000 psi, and the maximum deflection was 0.0046 in.

### Design I: Increase Shaft Diameter

For my first design, I increased the shaft diameter from the original 1.22 inches to improve the bracket's stiffness and strength. I kept the assigned Aluminum 6061-T6 material and the 600 lbf load. After making the geometry change, I performed a static stress analysis and compared the results from different mesh sizes.

I checked the maximum stress, maximum displacement, and factor of safety using the percentage-difference formula. The geometry remained unchanged during each mesh comparison. If all three results converged within 7%, I used those results to evaluate the design. If they did not converge after three attempts, I used the results from the finest mesh, following the assignment instructions.
 Iteration 1
<img width="1624" height="483" alt="image" src="https://github.com/user-attachments/assets/847a0db6-f3ad-41c9-8638-86dceac549c2" />
<img width="1054" height="975" alt="image" src="https://github.com/user-attachments/assets/b1a7cd94-3d3f-4652-b32e-97ce0fe14e7e" />

### Mistake Identified

While working on my next iteration, I realized that the applied force was set incorrectly. Instead of using the intended 600 lbf load from my A5/A6 design requirements, the force was not set to the correct value. This meant that the previous simulation results could not be used for an accurate comparison and had to be disregarded.

I corrected the loading setup before continuing with the analysis. Although this meant restarting part of the process, I had a better understanding of how to set up the simulation and expected to complete the remaining steps more efficiently.

I also created an Excel calculator to make checking the percentage differences between mesh results faster. This helped organize the convergence calculations for maximum stress, displacement, and safety factor and made it easier to determine whether the results were within the required 7% difference.
### Initial Results

- **Material:** Aluminum 6061-T6
- **Applied Load:** 600 lbf
- **Maximum Allowable Deflection:** 0.005 in
- **Yield Strength:** 35,000 psi
- **Required Factor of Safety:** 4
- <img width="1599" height="454" alt="image" src="https://github.com/user-attachments/assets/14988e36-2265-4839-b1de-7bf86d30968e" />
Design 1: increase diameter
For my first iteration, i will increase the diameter to 2 inches.

### *Iteration 1: 2 in Diameter

Maximum stress = 2.60 × 10³ psi

Maximum deflection = 2.50 × 10⁻² in

Factor of safety = 13.46

The stress percentage difference was 23.61%, the deflection percentage difference was 32.43%, and the factor of safety percentage difference was 23.61%. These results were outside the required 7% convergence limit, so I needed to continue refining the mesh before proceeding to the next geometry change.

### *Iteration 2: 1.9 in Diameter*

### Iteration 2: 1.9 in Diameter

Maximum stress = 1,855 psi

Maximum deflection = 0.02935 in

Factor of safety = 18.87 (calculated from yield strength divided by maximum stress)

The reported stress percentage difference was 11.39%, the deflection percentage difference was 16.76%, and the safety factor percentage difference was 26.85%. These differences exceed the required 7% convergence limit, indicating that the mesh results had not converged. The maximum deflection also exceeded the allowable limit of 0.005 in. Comparing the 1.9-inch design with the 2.0-inch design suggests that reducing the shaft diameter increased deflection, so stiffness remains an important consideration.
iteration 2
<img width="1803" height="436" alt="image" src="https://github.com/user-attachments/assets/a250a50b-1aa0-4058-9413-7389ed5e47a3" />

### *Iteration 3: 1.85 in Diameter*
<img width="1693" height="496" alt="image" src="https://github.com/user-attachments/assets/3b08ed4c-88dc-4df8-a217-5733e57baf37" />

### Final Mesh-Validation Attempt: 1.85 in Diameter


The maximum stress percentage difference was 1.5%, the maximum deflection percentage difference was 8.55%, and the factor of safety percentage difference was 80.81%. The stress results were within the required 7% limit, but the deflection and factor of safety results were not. Since this was the third attempt, I used the results from the finest mesh for the next design stage, as specified in the assignment.

These results will serve as the baseline for the next design iteration:

- **Maximum Stress:** 2,048 psi
- **Maximum Deflection:** 0.03187 in
- **Factor of Safety:** 17.09 (calculated using 35,000 psi divided by 2,048 psi)
- **Mass:** 1.34 lb
<img width="1763" height="496" alt="image" src="https://github.com/user-attachments/assets/f15684c6-84cd-47f3-8dd5-ae4b6d86c4f1" />
### **Design II: Adding Fillets**
<img width="933" height="858" alt="image" src="https://github.com/user-attachments/assets/ff267a0e-9de7-41c8-adff-ca62be8f6aed" />

I added 0.10-inch fillets to the inner and back edges of the bracket to reduce stress concentrations. I then ran the simulation using a fine mesh to evaluate how the changes affected the maximum stress, maximum deflection, and factor of safety.

### *Iteration 1: 0.10 in Fillet*

- **Maximum Stress:** \(3.316 \times 10^2\) psi
- **Maximum Deflection:** \(7.108 \times 10^{-3}\) in
- **Factor of Safety:** \(4.177 \times 10^6\)

The percentage differences were 144% for maximum stress, 127% for maximum deflection, and 111% for the factor of safety. These results were outside the required 7% convergence limit, so I needed to continue checking the mesh. Even a small change to the bracket's geometry can significantly affect the calculated stress and deflection. I will compare the results from different mesh sizes before proceeding to the next iteration.
<img width="1761" height="433" alt="image" src="https://github.com/user-attachments/assets/a3a24b8a-7923-40d3-82b7-051b9ad2ad0d" />

### *Iteration 2: 0.02 in Fillet*
<img width="1588" height="458" alt="image" src="https://github.com/user-attachments/assets/c2cef8e1-d9e8-4a5e-85c3-8479581d2825" />
For this iteration, I reduced the fillet size to 0.02 inches to see how a smaller fillet affected the bracket's stress, deflection, and factor of safety.

- **Maximum Stress:** \(2.8 \times 10^4\) psi
- **Maximum Deflection:** \(4.6 \times 10^{-3}\) in
- **Factor of Safety:** 1.25

The smaller fillet leaves a sharper transition around the corners, which can increase stress concentrations compared with a larger fillet. I will compare different mesh sizes on this same geometry to check whether the maximum stress, deflection, and factor of safety converge within the required 7% difference. If the results do not converge after three attempts, I will use the results from the finest mesh before proceeding to the next design change.
iteration 3 
<img width="2060" height="515" alt="image" src="https://github.com/user-attachments/assets/d2ef57f5-ee3e-42b3-9cf6-0a30b6be0069" />
### *Iteration 3: 0.001 in Fillet*

For this iteration, I reduced the fillet size to 0.001 inches to evaluate how a much smaller fillet affected the bracket's stress, deflection, and factor of safety.

- **Maximum Stress:** \(3.2 \times 10^4\) psi
- **Maximum Deflection:** \(4.8 \times 10^{-3}\) in
- **Factor of Safety:** 1.09
- **Mass:** 1.48 lb

The results show that the smaller fillet can increase stress concentrations around the corners. After the third mesh-convergence attempt, I would use the results from the finest mesh if the values did not converge within the required 7% difference. These results would then become the baseline for Design III, where I would focus on reducing the bracket's mass while maintaining sufficient strength and stiffness.

### **Design III: Removing Material**
<img width="1218" height="1125" alt="image" src="https://github.com/user-attachments/assets/d46282a1-2147-46e4-a2f6-48b772110380" />
For my third design, I added two circular holes with a 0.5-inch radius to reduce the bracket's mass while maintaining its strength and stiffness. I then evaluated how removing material affected the maximum stress, maximum deflection, and factor of safety.

### *Iteration 1: 0.5 in Radius Holes*

- **Maximum Stress:** \(2.9 \times 10^4\) psi
- **Maximum Deflection:** \(5.1 \times 10^{-3}\) in
- **Factor of Safety:** 1.21
- **Mass:** 1.29 lb

Removing material reduced the overall mass of the bracket, but the holes may also introduce stress concentrations around their edges. I would compare different mesh sizes on this geometry to check whether the maximum stress, deflection, and factor of safety converge within the required 7% difference. If the results do not converge after three attempts, I would use the results from the finest mesh. The final design should balance weight reduction with adequate strength and stiffness.
<img width="1681" height="467" alt="image" src="https://github.com/user-attachments/assets/4db6820f-c651-4f13-97f0-005db3262be8" />
### Reflection

This assignment helped me understand how finite element analysis can be used to improve a mechanical design. I learned that changing the geometry of a bracket can affect its maximum stress, deflection, factor of safety, and mass. Adding fillets can help reduce stress concentrations, while removing material with holes can reduce weight but may also affect the bracket's strength.

One of the most important parts of this assignment was understanding mesh convergence. Changing the mesh size can affect the calculated results, so it is important to compare different mesh sizes before making geometry changes. I also learned that stress, deflection, and factor of safety must all be checked because one result alone does not determine whether a design is acceptable.

Another lesson I learned was the importance of balancing strength, stiffness, and weight. A lighter bracket is not necessarily a better design if it becomes too flexible or experiences excessive stress. In future designs, I would spend more time validating my simulation setup and comparing the results before deciding which geometry changes to make.

The total time I spent completing this assignment was **5 hours**.
Part link
https://mail.google.com/mail/u/0?ui=2&ik=4e9b2dd91e&attid=0.1&permmsgid=msg-a:r1446276862203762957&view=att&disp=safe&realattid=f_mv71gdob0&zw
