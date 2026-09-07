# A3 – Parametric Design and FEA

## Objective

The objective of this assignment was to design a bar that satisfies a maximum allowable axial deflection while also checking the design using finite element analysis (FEA). The bar was required to have a circular cross section, be made from aluminum, and be subjected to a tensile load between 300 and 500 lbf. The maximum allowable deflection was 0.009 in, so I used the maximum allowed load of 500 lbf and created a parametric SolidWorks model that calculates the required bar length from the axial deflection equation.

The design was first analyzed using the direct axial deformation equation and then modeled parametrically in SolidWorks. After creating the model, I assigned an aluminum material, applied the tensile load and fixed support, generated a mesh, and ran a static FEA study. The FEA results were then compared with the hand calculation to determine how closely the two methods agreed.

---

# Analyze

## 1. Design Requirements

The main design requirements for the bar were:

- **Cross section:** Circular
- **Material:** Aluminum
- **Applied load:** 300–500 lbf
- **Maximum allowable deflection:** 0.009 in
- **Elastic modulus:** 8.5 × 10⁶ to 11.5 × 10⁶ psi
- **Required yield strength for the safety-factor check:** 40 ksi

I chose the maximum allowable load of **500 lbf** because designing for the highest required load gives the design a conservative loading condition. I used a circular bar with a diameter of **0.500 in**. The final material selected in SolidWorks was **Aluminum 2219-T62**.

<img width="877" height="1046" alt="Parametric CAD Model" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f" />

*Figure 1. Parametric cylindrical bar with a 0.500 in diameter and approximately 36.90 in length.*

---

## 2. Material Selection

The selected material was **Aluminum 2219-T62**. The SolidWorks material database lists an elastic modulus of approximately **72,000 MPa**, which is approximately **10.44 × 10⁶ psi**. This value falls within the required range of 8.5 × 10⁶ to 11.5 × 10⁶ psi.

The material database also lists a yield strength of approximately **290 MPa**, or about **42.1 ksi**. This is greater than the 40 ksi yield strength value specified for the safety-factor requirement.

Therefore, the selected material satisfies the required elastic modulus range and the yield-strength requirement.

<img width="796" height="316" alt="Aluminum 2219-T62 Material" src="https://github.com/user-attachments/assets/ee3ba54a-24f1-404e-9892-bbce9e99191e" />

*Figure 2. Aluminum 2219-T62 selected in the SolidWorks material database.*

---

## 3. Hand Calculation

### Known Values

The following values were used for the analytical calculation:

**F = 500 lbf**

**d = 0.500 in**

**E = 72,000 MPa**

Converting the elastic modulus to psi:

**E ≈ 10.44 × 10⁶ psi**

The maximum allowable deflection is:

**δₘₐₓ = 0.009 in**

### Cross-Sectional Area

Because the bar has a circular cross section:

**A = πd² / 4**

Substituting the diameter:

**A = π(0.500)² / 4**

**A = 0.19635 in²**

### Axial Deflection Equation

For a uniform bar in direct tension:

**δ = FL / (AE)**

Solving for the required length:

**L = (δₘₐₓ × A × E) / F**

Using the selected values:

**L = (0.009 × 0.19635 × 10.44 × 10⁶) / 500**

**L ≈ 36.90 in**

Therefore, the required bar length is approximately **36.90 in** for the selected diameter, load, material, and maximum allowable deflection.

---

## 4. Parametric CAD Design

I created the bar in SolidWorks as a simple cylindrical part. The circular cross section was created with a diameter of **0.500 in**, and the bar length was initially determined from the axial deflection calculation.

The important part of the CAD model was making the design parametric instead of using only fixed dimensions. This allows the design to update automatically if the load, elastic modulus, maximum allowable deflection, or diameter is changed.

<img width="877" height="1046" alt="Parametric CAD Model" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f" />

*Figure 3. SolidWorks cylindrical bar showing the 0.500 in diameter and approximately 36.90 in length.*

---

## 5. SolidWorks Equations

I created global variables in SolidWorks for the main design parameters. These variables were then connected to the CAD dimensions and equations.

The variables used were:

- **LOAD = 500 lbf**
- **E = 10.44 × 10⁶ psi**
- **MAXDEFLECTION = 0.009 in**
- **DIAMETER = 0.500 in**
- **AREA = π(DIAMETER)² / 4**

The cross-sectional area was defined using:

**A = πd² / 4**

The bar length was controlled using:

**L = (δₘₐₓ × A × E) / F**

This caused the length of the extrusion to update automatically when the material properties or design variables were changed.

<img width="795" height="325" alt="SolidWorks Equations" src="https://github.com/user-attachments/assets/a45ab1e4-bc01-4fa3-839e-5972f4f057ba" />

*Figure 4. SolidWorks global variables and equations used to create the parametric model.*

---

## 6. Final CAD Geometry

The final design is a straight cylindrical aluminum bar with a diameter of **0.500 in** and a calculated length of approximately **36.90 in**. The length is equation-driven, so it is controlled by the design variables rather than being an arbitrary fixed value.

The final geometry provides the required circular cross section and was used directly for the FEA study.

<img width="877" height="1046" alt="Final CAD Geometry" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f" />

*Figure 5. Final cylindrical CAD model used for the FEA study.*

---

# FEA Analysis

## 7. FEA Setup

A static FEA study was created in SolidWorks Simulation. One circular end face of the bar was fixed to represent the support, while the opposite circular end face was subjected to the required tensile load.

The required load was **500 lbf**. Since SolidWorks was displaying force in Newtons, the load was converted using:

**500 lbf × 4.44822 N/lbf = 2224.1 N**

Therefore, the applied FEA load was:

**F = 2224.1 N**

The force was directed axially away from the fixed end so that the bar was placed in direct tension.

<img width="2555" height="1095" alt="FEA Fixture and Force" src="https://github.com/user-attachments/assets/d0de36b4-68e5-4973-a26e-8fba92e93f1e" />

*Figure 6. FEA setup showing the fixed circular end and 2224.1 N tensile load.*

---

## 8. Mesh

A mesh was generated over the entire cylindrical bar before running the static study. The mesh divides the CAD geometry into smaller finite elements so that SolidWorks can calculate the displacement and stress throughout the part.

The mesh covered the full length of the bar and was used for both the displacement and von Mises stress calculations.

<img width="2558" height="1027" alt="FEA Mesh" src="https://github.com/user-attachments/assets/2ec0dfe0-71a8-4121-b4db-8d1db9b0aa80" />

*Figure 7. Finite element mesh applied to the cylindrical bar.*

---

## 9. FEA Displacement Result

The displacement result was used to determine the maximum deflection of the bar under the 500 lbf tensile load.

The SolidWorks result showed a maximum displacement of:

**δ = 0.2287 mm**

Converting to inches:

**δ = 0.2287 / 25.4**

**δ = 0.009004 in**

Therefore:

**δ_FEA ≈ 0.00900 in**

This is essentially equal to the required maximum deflection of **0.009 in**.

Therefore, the design satisfies the maximum deflection requirement.

<img width="2555" height="1095" alt="FEA Displacement Result" src="https://github.com/user-attachments/assets/d0de36b4-68e5-4973-a26e-8fba92e93f1e" />

*Figure 8. SolidWorks displacement result showing a maximum displacement of approximately 0.2287 mm.*

---

## 10. FEA Von Mises Stress Result

The von Mises stress result was used to determine whether the bar remained below the required yield-strength limit.

The maximum von Mises stress from the SolidWorks result was approximately:

**σᵥₘ,ₘₐₓ = 18.9 MPa**

Converting to ksi:

**18.9 MPa ≈ 2.74 ksi**

Therefore:

**σᵥₘ,ₘₐₓ ≈ 2.74 ksi**

This stress is significantly lower than the required **40 ksi** yield-strength value.

<img width="2558" height="1027" alt="FEA Von Mises Stress" src="https://github.com/user-attachments/assets/2ec0dfe0-71a8-4121-b4db-8d1db9b0aa80" />

*Figure 9. SolidWorks von Mises stress result showing a maximum stress of approximately 18.9 MPa.*

---

## 11. Safety Factor

The safety factor was calculated by comparing the material yield strength to the maximum von Mises stress.

Using the SolidWorks material value:

**Sᵧ = 290 MPa**

and:

**σᵥₘ,ₘₐₓ = 18.9 MPa**

The safety factor is:

**n = Sᵧ / σᵥₘ,ₘₐₓ**

**n = 290 / 18.9**

**n ≈ 15.3**

The calculated safety factor is much greater than 1. Therefore, the bar does not exceed the material yield strength under the applied 500 lbf tensile load.

---

# Decide

## 12. Hand Calculation vs. FEA

The analytical calculation predicted a maximum axial deflection of approximately:

**δ_hand ≈ 0.008998 in**

The SolidWorks FEA predicted:

**δ_FEA ≈ 0.009004 in**

The two results are extremely close. This is expected because the model is a simple uniform cylindrical bar under direct axial tension, which is exactly the type of loading represented by the analytical equation.

The hand calculation provides a quick way to determine the required dimensions, while FEA provides a numerical solution over the actual CAD geometry.

---

## 13. Percent Difference

The percent difference between the analytical and FEA deflection results was calculated using:

**% Difference = |δ_FEA − δ_hand| / δ_hand × 100**

Using the calculated values:

**δ_hand ≈ 0.008998 in**

**δ_FEA ≈ 0.009004 in**

Therefore:

**% Difference ≈ 0.064%**

The difference is very small, indicating excellent agreement between the hand calculation and the FEA result.

I would trust the FEA result more for the actual CAD model because it evaluates the geometry using finite elements. However, the analytical result is very useful for predicting the expected behavior and determining the initial dimensions before running FEA.

---

## 14. Pin-Hole Stress Concentration

The assignment also required consideration of the stress concentration caused by a pin hole in a bar under tension. A transverse hole creates a local increase in stress around the edge of the hole.

For the stress-concentration estimate, the stress concentration factor (**Kₜ**) can be used with the nominal stress:

**σ_peak = Kₜ × σ_nominal**

The assignment references a flat-bar transverse-hole stress-concentration chart. Since the primary CAD model for this assignment uses a circular bar, the flat-bar chart does not exactly represent the cylindrical geometry. Therefore, this calculation is treated as an engineering approximation rather than an exact stress concentration for the cylindrical bar.

For a representative ratio of:

**d / W = 0.50**

a Peterson-style stress concentration chart gives approximately:

**Kₜ ≈ 2.16**

Using the FEA nominal stress of approximately:

**σ_nominal = 2.74 ksi**

The estimated peak stress is:

**σ_peak = Kₜ × σ_nominal**

**σ_peak = (2.16)(2.74)**

**σ_peak ≈ 5.92 ksi**

Using the required **40 ksi** yield-strength value:

**n = 40 / 5.92**

**n ≈ 6.76**

Therefore, even with the estimated stress concentration, the estimated stress remains below the required 40 ksi yield-strength value.

No additional FEA was performed for the hole because the assignment specifically asks for the stress concentration to be estimated using **Kₜ** and the nominal FEA stress rather than rerunning the FEA.

---

## 15. Design Decision

The final design uses a **0.500 in diameter** cylindrical aluminum bar with an equation-driven length of approximately **36.90 in**. The design was created to reach the maximum allowable deflection of **0.009 in** under the required **500 lbf** load.

The FEA displacement was approximately **0.00900 in**, which agrees extremely closely with the analytical prediction. The maximum von Mises stress was approximately **2.74 ksi**, which is substantially below the **40 ksi** yield-strength requirement.

Based on the deflection and stress results, the design satisfies the main requirements of the assignment. The stress-concentration estimate also indicates that the design would remain below the required yield-strength value under the assumed hole condition.

---

# Communicate

## 16. Mistakes and Adjustments

One mistake I made during the modeling process was initially creating the wrong type of hole while working through the stress-concentration portion of the assignment. The hole was created along the axis of the cylindrical bar instead of representing the transverse-hole condition described by the stress-concentration reference.

I recognized the mistake before using the geometry for additional FEA and removed the hole so that the original FEA model would remain unchanged. I then treated the pin-hole portion as a **Kₜ calculation** using the existing nominal FEA stress, which follows the assignment instruction not to rerun the FEA for the hole.

Another adjustment was making sure that the elastic modulus used in the parametric calculation matched the selected SolidWorks material. After selecting Aluminum 2219-T62, the elastic modulus was updated to approximately **10.44 × 10⁶ psi**, which caused the equation-driven bar length to update automatically.

---

## 17. Engineering Lessons Learned

This assignment helped me understand how analytical equations can be connected directly to a parametric CAD model. Instead of choosing a length manually, I was able to use the axial deflection equation to make the length respond automatically to changes in load, material properties, diameter, and allowable deflection.

I also learned how FEA can be used to verify a hand calculation. For this simple axial-loading problem, the hand calculation and FEA results were almost identical, which helped show why analytical equations are useful for simple geometries and loading conditions.

Another important lesson was that boundary conditions and load directions have a major effect on FEA results. The fixed support and tensile load had to be applied to the correct end faces and in the correct direction. I also learned that stress concentrations should be considered separately from the nominal stress because holes and other geometric features can increase the local stress.

---

## 18. Time Spent

I spent approximately **[ENTER YOUR ACTUAL TIME]** working on this assignment.

This included time spent creating the cylindrical CAD model, setting up the SolidWorks equations, selecting the aluminum material, creating the FEA study, applying the fixture and tensile load, generating the mesh, running the simulation, checking the displacement and stress results, and completing the calculations and documentation.

---

## 19. CAD File

The final SolidWorks CAD file is provided below.

**[Download the A3 Parametric Bar CAD File](YOUR-GITHUB-CAD-FILE-LINK-HERE)**

The CAD model contains the parametric cylindrical bar used for the analysis and FEA study.

---

# Final Results

| Design Parameter | Final Value |
|---|---:|
| Cross section | Circular |
| Diameter | 0.500 in |
| Length | ≈ 36.90 in |
| Material | Aluminum 2219-T62 |
| Elastic Modulus | ≈ 10.44 × 10⁶ psi |
| Applied Load | 500 lbf |
| FEA Load | 2224.1 N |
| Analytical Deflection | ≈ 0.00900 in |
| FEA Maximum Deflection | ≈ 0.00900 in |
| Percent Difference | ≈ 0.064% |
| Maximum Von Mises Stress | ≈ 2.74 ksi |
| Material Yield Strength | ≈ 42.1 ksi |
| Safety Factor | ≈ 15.3 |
| Estimated Kₜ | ≈ 2.16 |
| Estimated Peak Hole Stress | ≈ 5.92 ksi |
| Estimated Hole Safety Factor | ≈ 6.76 |

Overall, the final design met the required deflection and stress requirements for the selected loading condition. The close agreement between the hand calculation and SolidWorks FEA also provided confidence that the parametric design and simulation setup were working correctly.
