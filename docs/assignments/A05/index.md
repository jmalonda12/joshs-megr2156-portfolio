# A5 – Design for Strength and Stiffness I

## Objective

The objective of this assignment was to design a bracket based on the concept design in Appendix B to hold a horizontal force applied symmetrically by the polyester strap shown in Resource #1.

The bracket was divided into five features, A through E, as shown in Appendix C. Each feature was analyzed for both strength and stiffness to determine the required dimensions.

## Analyze

### Design Requirements

- Applied load: F = 600 lbf
- Safety factor: SF = 4
- Material: Aluminum 6061-T6
- Yield strength: Sy = 35,000 psi
- Young's modulus: E = 10,000,000 psi
- Maximum allowable deflection: δmax = 0.005 in
- Direct shear failure is neglected as instructed in the assignment
- The bracket is designed symmetrically
- The T beam is treated as rigid
- The loading is treated as static

### Allowable Stress

σallow = Sy / SF

σallow = 35,000 psi / 4

σallow = 8,750 psi

### Overall Analysis Approach

The bracket was divided into Features A through E. Each feature was analyzed using an appropriate strength-of-materials model. Both stress and stiffness were considered, and the larger required dimension was used as the governing design dimension.

---

# Feature A – Cantilever Beam

Appendix D specifies that Feature A is treated as a cantilever beam.

## Feature A – Stress Analysis

### Known

- F = 600 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- LA = 3.00 in
- Circular cross section

### Unknown

- Minimum diameter, dA

### Assumptions

1. Feature A will not fail due to direct shear stress.
2. The strap load is distributed symmetrically.
3. Feature A is modeled as a cantilever beam.
4. The cross section is circular.
5. The load is static.
6. The T beam is rigid.
7. A safety factor of 4 is used.

### Free Body Diagram

<img width="1222" height="1603" alt="Feature A Stress Analysis" src="https://github.com/user-attachments/assets/e36f0f69-1fd4-44b5-8710-bdc3f87b5ad6" />

### Algebraic and Numerical Solution

The bending stress equation for a circular section was used to determine the required diameter.

The calculations and numerical solution are shown in the image above.

Final stress dimension:

dA,stress = 1.28 in

---

## Feature A – Stiffness Analysis

### Known

- F = 600 lbf
- LA = 3.00 in
- E = 10,000,000 psi
- δmax = 0.005 in
- Circular cross section

### Unknown

- Minimum diameter, dA

### Assumptions

1. Feature A behaves as a cantilever beam.
2. Shear deflection is negligible.
3. The load is static.
4. The cross section is circular.
5. The maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1207" height="1590" alt="Feature A Stiffness Analysis" src="https://github.com/user-attachments/assets/3e0f2c4a-6630-4a06-b9fa-f17d171f7b81" />

### Result

dA,stiffness = 1.22 in

The stress requirement is larger than the stiffness requirement.

### Governing Requirement

Strength governs Feature A.

Final Feature A dimension:

dA = 1.28 in

---

# Feature B – Axially Loaded Bar

Appendix D specifies that Feature B is treated as an axially loaded bar.

## Feature B – Stress Analysis

### Known

- F = 600 lbf
- PB = 2F = 1,200 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Width, wB = 1.00 in

### Unknown

- Cross-sectional area, AB
- Thickness, tB

### Assumptions

1. Feature B will not fail due to direct shear stress.
2. The bracket is symmetric.
3. The load is distributed equally through the symmetric load path.
4. Feature B is modeled as an axially loaded bar.
5. The load is static.
6. The T beam is rigid.
7. A safety factor of 4 is used.

### Free Body Diagram and Calculation

<img width="1178" height="1574" alt="Feature B Stress Analysis" src="https://github.com/user-attachments/assets/5d5f4110-fc7c-4df5-9251-35f982d03282" />

### Algebraic Solution

σ = P / A

A = P / σallow

tB = AB / wB

### Numerical Solution

AB = 1200 / 8750

AB = 0.1371 in²

tB = 0.1371 / 1.00

tB = 0.1371 in

Final stress dimension:

tB,stress = 0.1371 in

---

## Feature B – Stiffness Analysis

### Known

- PB = 1,200 lbf
- LB = 2.00 in
- E = 10,000,000 psi
- δmax = 0.005 in
- wB = 1.00 in

### Unknown

- Minimum cross-sectional area
- Minimum thickness, tB

### Assumptions

1. Feature B behaves as an axially loaded bar.
2. Shear deformation is negligible.
3. The load is static.
4. The material remains in the elastic range.
5. The maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1198" height="1557" alt="Feature B Stiffness Analysis" src="https://github.com/user-attachments/assets/bef49559-3cc5-442b-a218-b64f33b1cdef" />

### Algebraic Solution

δ = PL / AE

A = PL / Eδmax

tB = AB / wB

### Numerical Solution

AB = (1200)(2.00) / (10,000,000)(0.005)

AB = 0.0480 in²

tB = 0.0480 / 1.00

tB = 0.0480 in

### Governing Requirement

Strength governs Feature B because:

0.1371 in > 0.0480 in

Final Feature B dimension:

tB = 0.14 in

---

# Feature C – Simply Supported Beam

Appendix D specifies that Feature C is treated as a simply supported beam with a concentrated load at the center.

## Feature C – Stress Analysis

### Known

- F = 600 lbf
- LC = 3.00 in
- wC = 1.50 in
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi

### Unknown

- Minimum beam thickness, tC

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The load is concentrated at the center.
3. The beam is symmetric.
4. The load is static.
5. Direct shear failure is neglected.
6. A rectangular cross section is used.

### Free Body Diagram

<img width="1185" height="1087" alt="Feature C Stress Analysis" src="https://github.com/user-attachments/assets/e3803924-bda5-4009-9fbe-dc652aa50bc1" />

### Algebraic Solution

Mmax = FL / 4

For a rectangular section:

I = wt³ / 12

c = t / 2

σ = Mc / I

### Numerical Solution

Mmax = (600)(3.00) / 4

Mmax = 450 lbf·in

Using σallow = 8,750 psi gives:

tC ≈ 0.454 in

Final stress dimension:

tC,stress = 0.46 in

---

## Feature C – Stiffness Analysis

### Known

- F = 600 lbf
- LC = 3.00 in
- wC = 1.50 in
- E = 10,000,000 psi
- δmax = 0.005 in

### Unknown

- Minimum beam thickness, tC

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The load is concentrated at the center.
3. Shear deflection is negligible.
4. The beam is symmetric.
5. The material remains in the elastic range.
6. Maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1195" height="1531" alt="Feature C Stiffness Analysis" src="https://github.com/user-attachments/assets/c2ec1663-c4a1-427c-95b1-40127bccaa59" />

### Algebraic Solution

δmax = FL³ / 48EI

I = wt³ / 12

### Numerical Solution

Using the required maximum deflection:

tC ≈ 0.378 in

Final stiffness dimension:

tC,stiffness = 0.38 in

### Governing Requirement

Strength governs Feature C because:

0.46 in > 0.38 in

Final Feature C dimension:

tC = 0.46 in

---

# Feature D

## Feature D – Stress Analysis

### Known

- F = 600 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Aluminum 6061-T6
- Bracket is symmetric

### Unknown

- Required Feature D dimensions

### Assumptions

1. Direct shear failure is neglected.
2. The load is static.
3. The T beam is rigid.
4. The bracket is symmetric.
5. The appropriate bending model is used for the Feature D geometry.
6. A safety factor of 4 is used.

### Free Body Diagram, Algebraic Solution, and Numerical Solution

<img width="1214" height="1530" alt="Feature D Stress Analysis" src="https://github.com/user-attachments/assets/e7deb04b-1c7b-47f8-bfbf-c5166e33678b" />

---

## Feature D – Stiffness Analysis

### Known

- F = 600 lbf
- E = 10,000,000 psi
- δmax = 0.005 in
- Aluminum 6061-T6
- Bracket is symmetric

### Unknown

- Required Feature D stiffness dimension

### Assumptions

1. Shear deflection is negligible.
2. The load is static.
3. The T beam is rigid.
4. The bracket is symmetric.
5. Maximum allowable deflection is 0.005 in.

### Free Body Diagram, Algebraic Solution, and Numerical Solution

<img width="1172" height="1246" alt="Feature D Stiffness Analysis" src="https://github.com/user-attachments/assets/a69bbfd6-7c85-46d7-9640-fc2455bd304f" />

---

# Feature E

## Feature E – Stress Analysis

### Known

- F = 600 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Aluminum 6061-T6
- Bracket is symmetric

### Unknown

- Required Feature E dimensions

### Assumptions

1. Direct shear failure is neglected.
2. The load is static.
3. The T beam is rigid.
4. The bracket is symmetric.
5. The appropriate bending model is used for the Feature E geometry.
6. A safety factor of 4 is used.

### Free Body Diagram, Algebraic Solution, and Numerical Solution

<img width="1180" height="1524" alt="Feature E Stress Analysis" src="https://github.com/user-attachments/assets/784a750c-970a-4e70-9a89-25015fed0a22" />

---

## Feature E – Stiffness Analysis

### Known

- F = 600 lbf
- E = 10,000,000 psi
- δmax = 0.005 in
- Aluminum 6061-T6
- Bracket is symmetric

### Unknown

- Required Feature E stiffness dimension

### Assumptions

1. Shear deflection is negligible.
2. The load is static.
3. The T beam is rigid.
4. The bracket is symmetric.
5. Maximum allowable deflection is 0.005 in.

### Free Body Diagram, Algebraic Solution, and Numerical Solution

<img width="1189" height="1430" alt="Feature E Stiffness Analysis" src="https://github.com/user-attachments/assets/01b73812-58a7-446a-ae07-96c74952057d" />

---

# Decide

## Governing Design Requirements

For each feature, the stress and stiffness dimensions were compared. The larger required dimension was selected as the final design dimension.

The strength requirement governs Features A, B, and C based on the calculations shown above.

The final dimensions are represented in the multiview drawings below.

# Communicate

## Multiview Drawing – Stress Dimensions

The first multiview drawing shows the bracket dimensions determined from the stress analysis.

<img width="1193" height="1552" alt="Multiview Stress Dimensions" src="https://github.com/user-attachments/assets/9f5ce3ca-fe18-4fbd-833e-bbc313ec8268" />

## Multiview Drawing – Stiffness Dimensions

The second multiview drawing shows the bracket dimensions determined from the stiffness analysis.

<img width="1737" height="987" alt="Multiview Stiffness Dimensions" src="https://github.com/user-attachments/assets/bf206601-5bd4-441a-9dda-4003d64547b4" />

# Lessons Learned

This assignment helped me understand how strength and stiffness both affect the design of a mechanical component. A dimension that is sufficient for strength may still be too flexible, so both requirements need to be checked before selecting the final dimension.

I also learned that the governing requirement can change depending on the feature. For Features A, B, and C, the stress requirement was larger than the stiffness requirement, so strength governed the final dimensions.

Another important lesson was the effect of error propagation. Since the bracket is divided into connected features, a value calculated for one feature can be used when determining later dimensions. An error in an earlier load or dimension could therefore affect the rest of the design. Rechecking intermediate calculations helped prevent this from carrying through the final design.

One assumption used in the assignment was that direct shear failure could be neglected, as specifically stated in the directions. If direct shear were significant, an additional shear-stress analysis would be required and the required dimensions could increase.

The multiview drawings also showed me why it is important to look at a design from multiple views. The dimensions calculated from the stress and stiffness analyses need to be transferred correctly to the different views so the final design is consistent.

# Time Spent

I spent approximately **8 hours** completing this assignment.
<img width="1222" height="1531" alt="image" src="https://github.com/user-attachments/assets/8c189656-8cfe-40ce-aec0-07bca77ae6ae" />

