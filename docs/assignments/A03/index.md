
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

I chose the maximum allowable load of **500 lbf** because designing for the highest required load gives the design a conservative loading condition. I used a circular bar with a diameter of **0.500 in**.

The final material selected in SolidWorks was **Aluminum 2219-T62**.

<img width="877" alt="Parametric CAD Model" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f">

*Figure 1. Parametric cylindrical bar with a 0.500 in diameter and approximately 36.90 in length.*

---

## 2. Material Selection

The selected material was **Aluminum 2219-T62**.

The SolidWorks material database lists an elastic modulus of approximately:

**E = 72,000 MPa**

Converting this value to psi:

**E ≈ 10.44 × 10⁶ psi**

This value is within the required range of:

**8.5 × 10⁶ to 11.5 × 10⁶ psi**

The SolidWorks material database also lists a yield strength of approximately:

**Sy = 290 MPa**

Converting to ksi:

**Sy ≈ 42.1 ksi**

This is greater than the required **40 ksi** yield-strength value.

Therefore, Aluminum 2219-T62 satisfies the required material-property range.

<img width="900" alt="Aluminum 2219-T62 Material" src="https://github.com/user-attachments/assets/ee3ba54a-24f1-404e-9892-bbce9e99191e">

*Figure 2. Aluminum 2219-T62 selected in the SolidWorks material database.*

---

## 3. Hand Calculation

### Known Values

The following values were used for the analytical calculation:

**F = 500 lbf**

**d = 0.500 in**

**E = 10.44 × 10⁶ psi**

**δmax = 0.009 in**

---

### Cross-Sectional Area

Because the bar has a circular cross section:

**A = πd² / 4**

Substituting the diameter:

**A = π(0.500 in)² / 4**

**A = 0.19635 in²**

---

### Axial Deflection Equation

For a uniform bar in direct tension:

**δ = FL / (AE)**

Solving for the required length:

**L = δAE / F**

Substituting the known values:

**L = (0.009 in)(0.19635 in²)(10.44 × 10⁶ psi) / (500 lbf)**

**L ≈ 36.90 in**

Therefore, the required bar length is approximately:

**L = 36.90 in**

---

### Check the Calculated Deflection

Using the calculated length, I checked the deflection again:

**δ = FL / (AE)**

**δ = (500 lbf)(36.90 in) / [(0.19635 in²)(10.44 × 10⁶ psi)]**

**δ ≈ 0.00900 in**

This matches the required maximum deflection of **0.009 in**.

Therefore, the analytical design satisfies the deflection requirement.

---

## 4. Parametric CAD Design

I created the bar in SolidWorks as a simple cylindrical part. The circular cross section was created with a diameter of **0.500 in**, and the bar length was determined from the axial deflection calculation.

The important part of the CAD model was making the design parametric instead of using only fixed dimensions. This allows the design to update automatically if the load, elastic modulus, maximum allowable deflection, or diameter is changed.

<img width="877" alt="Parametric CAD Model" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f">

*Figure 3. SolidWorks cylindrical bar showing the 0.500 in diameter and approximately 36.90 in length.*

---

## 5. SolidWorks Equations

I created global variables in SolidWorks for the main design parameters. These variables were connected to the CAD dimensions and equations.

The variables used were:

- **LOAD = 500 lbf**
- **E = 10.44 × 10⁶ psi**
- **MAXDEFLECTION = 0.009 in**
- **DIAMETER = 0.500 in**
- **AREA = π(DIAMETER)² / 4**

The cross-sectional area was defined using:

**A = πd² / 4**

The bar length was controlled using:

**L = δmaxAE / F**

In SolidWorks, this was entered using the global variables so that the length was equation-driven.

This caused the length of the extrusion to update automatically when the material properties or design variables were changed.

<img width="787" height="313" alt="image" src="https://github.com/user-attachments/assets/117884f8-5c86-42e2-8073-a25cf292a14d" />

*Figure 4. SolidWorks global variables and equations used to create the parametric model.*

---

## 6. Final CAD Geometry

The final design is a straight cylindrical aluminum bar with:

- **Diameter = 0.500 in**
- **Length ≈ 36.90 in**
- **Material = Aluminum 2219-T62**

The length is equation-driven, so it is controlled by the design variables rather than being an arbitrary fixed value.

The final geometry provides the required circular cross section and was used directly for the FEA study.

<img width="877" alt="Final CAD Geometry" src="https://github.com/user-attachments/assets/5d8fc709-2e61-48f0-8bf3-c68fd3d4650f">

*Figure 5. Final cylindrical CAD model used for the FEA study.*

---

# FEA Analysis

## 7. FEA Setup

A static FEA study was created in SolidWorks Simulation.

One circular end face of the bar was fixed to represent the support, while the opposite circular end face was subjected to the required tensile load.

The required load was:

**F = 500 lbf**

Since SolidWorks was displaying force in Newtons, I converted the load:

**500 lbf × 4.44822 N/lbf = 2224.1 N**

Therefore, the applied FEA load was:

**F = 2224.1 N**

The force was directed axially away from the fixed end so that the bar was placed in direct tension.

<img width="1000" alt="FEA Fixture and Force" src="https://github.com/user-attachments/assets/d0de36b4-68e5-4973-a26e-8fba92e93f1e">

*Figure 6. FEA setup showing the fixed circular end and 2224.1 N tensile load.*

---

## 8. Mesh

A mesh was generated over the entire cylindrical bar before running the static study.

The mesh divides the CAD geometry into smaller finite elements so that SolidWorks can calculate displacement and stress throughout the part.

The mesh covered the full length of the bar and was used for both the displacement and von Mises stress calculations.

<img width="1000" alt="FEA Mesh" src="https://github.com/user-attachments/assets/2ec0dfe0-71a8-4121-b4db-8d1db9b0aa80">

*Figure 7. Finite element mesh applied to the cylindrical bar.*

---

## 9. FEA Displacement Result

The displacement result was used to determine the maximum deflection of the bar under the 500 lbf tensile load.

The SolidWorks result showed a maximum displacement of:

**δFEA = 0.2287 mm**

Converting to inches:

**δFEA = 0.2287 mm / 25.4 mm/in**

**δFEA = 0.009004 in**

Therefore:

**δFEA ≈ 0.00900 in**

The required maximum deflection was:

**δmax = 0.009 in**

The FEA result is essentially equal to the required maximum deflection.

Therefore, the design satisfies the maximum deflection requirement.

<img width="2559" height="1207" alt="image" src="https://github.com/user-attachments/assets/c747e81d-64a8-4c8e-9bff-991235def8c9" />

*Figure 8. SolidWorks displacement result showing a maximum displacement of approximately 0.2287 mm (0.009004 in).*

---

## 10. FEA Von Mises Stress Result

The von Mises stress result was used to determine whether the bar remained below the required yield-strength limit.

The maximum von Mises stress from the SolidWorks result was approximately:

**σvm,max = 18.96 MPa**

Converting to ksi:

**18.96 MPa / 6.89476 = 2.75 ksi**

Therefore:

**σvm,max ≈ 2.75 ksi**

This stress is significantly lower than the required:

**Sy = 40 ksi**

<img width="2529" height="1228" alt="image" src="https://github.com/user-attachments/assets/b1b788c6-803c-4ed3-afb0-ed1f06ccb2c9" />


*Figure 9. SolidWorks von Mises stress result showing a maximum stress of approximately 18.96 MPa (2.75 ksi).*

---

## 11. Safety Factor

The assignment requires the safety factor to be checked using a yield strength of:

**Sy = 40 ksi**

The maximum von Mises stress from FEA was:

**σvm,max = 2.75 ksi**

The safety factor is:

**n = Sy / σvm,max**

Substituting:

**n = 40 ksi / 2.75 ksi**

**n ≈ 14.55**

Therefore:

**Safety Factor ≈ 14.5**

Since the safety factor is much greater than 1, the design remains below the required yield-strength limit.

For reference, the actual Aluminum 2219-T62 material database value is approximately **42.1 ksi**, but the required **40 ksi** value was used for the assignment safety-factor check.

---

# Decide

## 12. Hand Calculation vs. FEA

The analytical calculation predicted a maximum axial deflection of approximately:

**δhand ≈ 0.008998 in**

The SolidWorks FEA predicted:

**δFEA ≈ 0.009004 in**

The two results are extremely close.

This is expected because the model is a simple uniform cylindrical bar under direct axial tension, which is exactly the type of loading represented by the analytical equation.

The hand calculation provides a quick way to determine the required dimensions, while FEA provides a numerical solution over the actual CAD geometry.

---

## 13. Percent Difference

The percent difference between the analytical and FEA deflection results was calculated using:

**% Difference = |δFEA − δhand| / δhand × 100**

Using the calculated values:

**δhand = 0.008998 in**

**δFEA = 0.009004 in**

Therefore:

**% Difference = |0.009004 − 0.008998| / 0.008998 × 100**

**% Difference ≈ 0.067%**

The difference is very small, indicating excellent agreement between the hand calculation and the FEA result.

I would trust the FEA result more for the actual CAD model because it evaluates the geometry using finite elements. However, the analytical result is very useful for predicting the expected behavior and determining the initial dimensions before running FEA.

---

## 14. Pin-Hole Stress Concentration

The assignment also required consideration of the stress concentration caused by a pin hole in a bar under tension.

A transverse hole creates a local increase in stress around the edge of the hole.

For the stress-concentration estimate, the stress concentration factor, **Kt**, can be used with the nominal stress:

**σpeak = Kt × σnominal**

The assignment references a flat-bar transverse-hole stress-concentration chart.

Since the primary CAD model for this assignment uses a circular bar, the flat-bar chart does not exactly represent the cylindrical geometry. Therefore, this calculation is treated as an engineering approximation rather than an exact stress concentration for the cylindrical bar.

For a representative ratio of:

**d / W = 0.50**

a Peterson-style stress concentration chart gives approximately:

**Kt ≈ 2.16**

The nominal FEA stress was:

**σnominal = 2.75 ksi**

The estimated peak stress is:

**σpeak = Kt × σnominal**

**σpeak = (2.16)(2.75 ksi)**

**σpeak = 5.94 ksi**

The required yield-strength value is:

**Sy = 40 ksi**

The estimated safety factor with the stress concentration is:

**n = Sy / σpeak**

**n = 40 ksi / 5.94 ksi**

**n ≈ 6.73**

Therefore, even with the estimated stress concentration, the estimated peak stress remains below the required **40 ksi** yield-strength value.

No additional FEA was performed for the hole because the assignment specifically asks for the stress concentration to be estimated using **Kt** and the nominal FEA stress rather than rerunning the FEA for the hole.

---

## 15. Design Decision

The final design uses a:

- **0.500 in diameter**
- **36.90 in long**
- **Aluminum 2219-T62**
- **500 lbf tensile load**

The design was created to reach the maximum allowable deflection of:

**δmax = 0.009 in**

The FEA displacement was:

**δFEA = 0.009004 in**

which agrees extremely closely with the analytical prediction.

The maximum von Mises stress was approximately:

**σvm,max = 2.75 ksi**

The required yield-strength value was:

**Sy = 40 ksi**

This resulted in a safety factor of approximately:

**n = 14.5**

The estimated stress concentration around the representative pin-hole condition resulted in:

**σpeak ≈ 5.94 ksi**

with an estimated safety factor of:

**n ≈ 6.73**

Based on the deflection, stress, and stress-concentration results, the design satisfies the main requirements of the assignment.

---

# Communicate

## 16. Mistakes and Adjustments

One mistake I made during the modeling process was initially creating the wrong type of hole while working through the stress-concentration portion of the assignment.

The hole was created along the axis of the cylindrical bar instead of representing the transverse-hole condition described by the stress-concentration reference.

I recognized the mistake before using the geometry for additional FEA and removed the hole so that the original FEA model would remain unchanged.

I then treated the pin-hole portion as a **Kt calculation** using the existing nominal FEA stress, which follows the assignment instruction not to rerun the FEA for the hole.

Another adjustment was making sure that the elastic modulus used in the parametric calculation matched the selected SolidWorks material.

After selecting Aluminum 2219-T62, the elastic modulus was updated to approximately:

**E = 10.44 × 10⁶ psi**

This caused the equation-driven bar length to update automatically to approximately:

**L = 36.90 in**

---

## 17. Engineering Lessons Learned

This assignment helped me understand how analytical equations can be connected directly to a parametric CAD model.

Instead of choosing a length manually, I was able to use the axial deflection equation to make the length respond automatically to changes in load, material properties, diameter, and allowable deflection.

I also learned how FEA can be used to verify a hand calculation.

For this simple axial-loading problem, the hand calculation and FEA results were almost identical, which helped show why analytical equations are useful for simple geometries and loading conditions.

Another important lesson was that boundary conditions and load directions have a major effect on FEA results. The fixed support and tensile load had to be applied to the correct end faces and in the correct direction.

I also learned that stress concentrations should be considered separately from the nominal stress because holes and other geometric features can increase the local stress.

---

## 18. Time Spent

I spent approximately **7 HOURS** working on this assignment.

This included time spent creating the cylindrical CAD model, setting up the SolidWorks equations, selecting the aluminum material, creating the FEA study, applying the fixture and tensile load, generating the mesh, running the simulation, checking the displacement and stress results, and completing the calculations and documentation.

---

## 19. CAD File

The final SolidWorks CAD file is provided below.

https://mail.google.com/mail/u/0?ui=2&ik=4e9b2dd91e&attid=0.3&permmsgid=msg-a:r-6223622566548494709&th=1a07a6c98092aa27&view=att&disp=safe&realattid=f_mtqtpkuw0&zw

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
| FEA Maximum Deflection | ≈ 0.009004 in |
| Percent Difference | ≈ 0.067% |
| Maximum Von Mises Stress | ≈ 2.75 ksi |
| Required Yield Strength | 40 ksi |
| Actual Material Yield Strength | ≈ 42.1 ksi |
| Safety Factor using 40 ksi | ≈ 14.5 |
| Estimated Kt | ≈ 2.16 |
| Estimated Peak Hole Stress | ≈ 5.94 ksi |
| Estimated Hole Safety Factor | ≈ 6.73 |

Overall, the final design met the required deflection and stress requirements for the selected loading condition.

The analytical calculation predicted approximately **0.00900 in** of deflection, while the SolidWorks FEA predicted **0.009004 in**, giving a percent difference of only approximately **0.067%**.

The maximum von Mises stress was approximately **2.75 ksi**, which is well below the required **40 ksi** yield-strength value and gives a safety factor of approximately **14.5**.

The stress-concentration estimate also showed that the representative pin-hole condition would remain below the required yield-strength value, with an estimated safety factor of approximately **6.73**.

The close agreement between the hand calculation and SolidWorks FEA provided confidence that the parametric design and simulation setup were working correctly.
