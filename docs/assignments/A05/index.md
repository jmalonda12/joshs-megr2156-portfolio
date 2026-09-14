# A5 – MEGR 2156 – Design for Strength and Stiffness I
## Assignment Requirements

- Applied load: **F = 600 lbf**
- Safety factor: **SF = 4**
- Material: **Aluminum 6061-T6**
- Yield strength: **Sy = 35,000 psi**
- Young's modulus: **E = 10,000,000 psi**
- Maximum allowable deflection: **δmax = 0.005 in**
- Direct shear failure is neglected as required by the assignment.
- The bracket is designed symmetrically.
- Features A through E are analyzed for both stress and stiffness.
## Objective

The objective of this assignment was to design a bracket based on the concept design in Appendix B to hold a horizontal force applied symmetrically by the polyester strap shown in Resource #1.

The bracket was divided into five features, A through E, as shown in Appendix C. Each feature was analyzed for both strength and stiffness to determine the required dimensions.
<img width="1737" height="987" alt="image" src="https://github.com/user-attachments/assets/2878f76a-664c-48fa-92e4-5d1746510195" />

# Analyze

## Design Requirements

- Applied load: **F = 600 lbf**
- Safety factor: **SF = 4**
- Material: **Aluminum 6061-T6**
- Yield strength: **Sy = 35,000 psi**
- Young's modulus: **E = 10,000,000 psi**
- Maximum allowable deflection: **δmax = 0.005 in**
- Direct shear failure is neglected as instructed in the assignment.
- The bracket is designed symmetrically.
- The T beam is treated as rigid.
- The loading is treated as static.

## Allowable Stress

σallow = Sy / SF

σallow = 35,000 psi / 4

σallow = **8,750 psi**

## Overall Analysis Approach

The bracket was divided into Features A through E. Each feature was modeled using an appropriate strength-of-materials analysis. Both stress and stiffness were checked, and the larger required dimension was used as the governing design dimension.

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

1. Feature A is modeled as a cantilever beam.
2. The 600 lbf load is applied at the free end of Feature A.
3. The bracket is symmetric.
4. The cross section is circular.
5. Direct shear failure is neglected.
6. The load is static.
7. The material remains in the elastic range.
8. The T beam is treated as rigid.
9. A safety factor of 4 is used.

### Free Body Diagram

<img width="1222" height="1603" alt="Feature A Stress Analysis" src="https://github.com/user-attachments/assets/e36f0f69-1fd4-44b5-8710-bdc3f87b5ad6" />
<img width="1207" height="1590" alt="Feature A Stiffness Analysis" src="https://github.com/user-attachments/assets/3e0f2c4a-6630-4a06-b9fa-f17d171f7b81" />
### Algebraic Solution

For a circular cross section:

I = πd⁴ / 64

c = d / 2

σ = Mc / I

Mmax = FL

Therefore:

σallow = 32FL / πd³

Solving for diameter:

dA = [32FL / (πσallow)]^(1/3)

### Numerical Solution

Mmax = (600)(3.00)

Mmax = **1,800 lbf·in**

dA = [32(600)(3.00) / (π)(8,750)]^(1/3)

dA = **1.28 in**

### Final Stress Dimension

**dA,stress = 1.28 in**

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
2. The load is applied at the free end.
3. Shear deflection is negligible.
4. The cross section is circular.
5. The material remains in the elastic range.
6. The maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation
<img width="1189" height="1552" alt="image" src="https://github.com/user-attachments/assets/3fa56ae1-1f34-426f-9e3a-769d6ae71ccb" />


### Algebraic Solution

For a cantilever beam with an end load:

δmax = FL³ / 3EI

For a circular cross section:

I = πd⁴ / 64

Therefore:

δmax = 64FL³ / 3πEd⁴

Solving for diameter:

dA = [64FL³ / (3πEδmax)]^(1/4)

### Numerical Solution

dA = [64(600)(3.00)³ / (3π)(10,000,000)(0.005)]^(1/4)

dA = **1.22 in**

### Comparison

dA,stress = 1.28 in

dA,stiffness = 1.22 in

Since:

**1.28 in > 1.22 in**

### Governing Requirement

**Strength governs Feature A.**

### Final Feature A Dimension

**dA = 1.28 in**

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

1. Feature B is modeled as an axially loaded bar.
2. The load is transferred through the symmetric load path.
3. PB = 2F = 1,200 lbf.
4. The cross section is rectangular.
5. Direct shear failure is neglected.
6. The load is static.
7. The material remains in the elastic range.
8. A safety factor of 4 is used.

### Free Body Diagram and Calculation
<img width="1198" height="1557" alt="image" src="https://github.com/user-attachments/assets/32c997ae-42ef-4994-aef8-43a923ac7cf8" />

<img width="1185" height="1087" alt="image" src="https://github.com/user-attachments/assets/13bd1067-380f-40c7-abee-7ccc236fce97" />


### Algebraic Solution

σ = P / A

A = P / σallow

For a rectangular cross section:

A = wt

Therefore:

tB = A / wB

### Numerical Solution

AB = 1200 / 8750

AB = **0.1371 in²**

tB = 0.1371 / 1.00

tB = **0.1371 in**

### Final Stress Dimension

**tB,stress = 0.1371 in**

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
3. The material remains in the elastic range.
4. The load is static.
5. The cross section is rectangular.
6. The maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1195" height="1531" alt="image" src="https://github.com/user-attachments/assets/b52478eb-eaa0-4b99-b52d-665f26bcf5f7" />

### Algebraic Solution

δ = PL / AE

Solving for area:

A = PL / Eδmax

For a rectangular cross section:

tB = AB / wB

### Numerical Solution

AB = (1200)(2.00) / (10,000,000)(0.005)

AB = **0.0480 in²**

tB = 0.0480 / 1.00

tB = **0.0480 in**

### Comparison

tB,stress = 0.1371 in

tB,stiffness = 0.0480 in

Since:

**0.1371 in > 0.0480 in**

### Governing Requirement

**Strength governs Feature B.**

### Final Feature B Dimension

**tB = 0.14 in**

---

# Feature C – Simply Supported Beam

Appendix D specifies that Feature C is treated as a simply supported beam with a concentrated load at the center.

## Feature C – Stress Analysis

### Known

- F = 600 lbf
- LC = 4.00 in
- wC = 1.00 in
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi

### Unknown

- Minimum beam thickness, tC

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The load is concentrated at the center.
3. The beam is symmetric.
4. The cross section is rectangular.
5. Direct shear failure is neglected.
6. The load is static.
7. The material remains in the elastic range.
8. A safety factor of 4 is used.

### Free Body Diagram

<img width="1214" height="1530" alt="image" src="https://github.com/user-attachments/assets/017d2b93-d9b3-41d4-b765-3dac18bb2be5" />


### Algebraic Solution

For a simply supported beam with a center load:

Mmax = FL / 4

For a rectangular cross section:

I = wt³ / 12

c = t / 2

σ = Mc / I

Therefore:

σ = 6M / wt²

Solving for thickness:

tC = [6M / (wσallow)]^(1/2)

### Numerical Solution

Mmax = (600)(4.00) / 4

Mmax = **600 lbf·in**

tC = [6(600) / (1.00)(8,750)]^(1/2)

tC = **0.642 in**

### Final Stress Dimension

**tC,stress = 0.642 in**

---

## Feature C – Stiffness Analysis

### Known

- F = 600 lbf
- LC = 4.00 in
- wC = 1.00 in
- E = 10,000,000 psi
- δmax = 0.005 in

### Unknown

- Minimum beam thickness, tC

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The load is concentrated at the center.
3. The beam is symmetric.
4. Shear deflection is negligible.
5. The cross section is rectangular.
6. The material remains in the elastic range.
7. Maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation
<img width="1222" height="1531" alt="image" src="https://github.com/user-attachments/assets/223e1e64-831a-4ccc-95d7-2fe7573d5a3b" />

### Algebraic Solution

For a simply supported beam with a center load:

δmax = FL³ / 48EI

For a rectangular cross section:

I = wt³ / 12

Therefore:

δmax = FL³ / 4Ewt³

Solving for thickness:

tC = [FL³ / (4Ewδmax)]^(1/3)

### Numerical Solution

tC = [600(4.00)³ / (4)(10,000,000)(1.00)(0.005)]^(1/3)

tC = **0.577 in**

### Comparison

tC,stress = 0.642 in

tC,stiffness = 0.577 in

Since:

**0.642 in > 0.577 in**

### Governing Requirement

**Strength governs Feature C.**

### Final Feature C Dimension

**tC = 0.642 in**

---

# Feature D – Axially Loaded Bar Model

## Feature D – Stress Analysis

### Known

- PD = 300 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Width, wD = 0.50 in

### Unknown

- Cross-sectional area, AD
- Required thickness, tD

### Assumptions

1. Feature D is modeled as an axially loaded bar based on the bracket geometry and the student example.
2. The load transferred to Feature D is 300 lbf.
3. The cross section is rectangular.
4. Direct shear failure is neglected.
5. The load is static.
6. The material remains in the elastic range.
7. A safety factor of 4 is used.

### Free Body Diagram and Calculation

<img width="1172" height="1246" alt="image" src="https://github.com/user-attachments/assets/c927b6b2-77b6-4f30-8139-346a2ffd4230" />


### Algebraic Solution

σ = P / A

A = P / σallow

A = wt

tD = AD / wD

### Numerical Solution

AD = 300 / 8750

AD = **0.03429 in²**

tD = 0.03429 / 0.50

tD = **0.06857 in**

### Final Stress Dimension

**tD,stress = 0.06857 in**

---

## Feature D – Stiffness Analysis

### Known

- PD = 300 lbf
- LD = 0.50 in
- E = 10,000,000 psi
- δmax = 0.005 in
- wD = 0.50 in

### Unknown

- Minimum cross-sectional area
- Minimum thickness, tD

### Assumptions

1. Feature D behaves as an axially loaded bar.
2. Shear deformation is negligible.
3. The load is static.
4. The material remains in the elastic range.
5. The cross section is rectangular.
6. Maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1180" height="1524" alt="image" src="https://github.com/user-attachments/assets/4289bf0e-e4d8-4ebb-803d-ce7d3549dffd" />


### Algebraic Solution

δ = PL / AE

A = PL / Eδmax

tD = AD / wD

### Numerical Solution

AD = (300)(0.50) / (10,000,000)(0.005)

AD = **0.00300 in²**

tD = 0.00300 / 0.50

tD = **0.00600 in**

### Comparison

tD,stress = 0.06857 in

tD,stiffness = 0.00600 in

Since:

**0.06857 in > 0.00600 in**

### Governing Requirement

**Strength governs Feature D.**

### Final Feature D Dimension

**tD = 0.06857 in**

---

# Feature E – Cantilever Beam

## Feature E – Stress Analysis

### Known

- F = 600 lbf
- LE = 2.00 in
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Width, wE = 1.00 in
- Rectangular cross section

### Unknown

- Minimum beam height, hE

### Assumptions

1. Feature E is modeled as a cantilever beam with an end load.
2. The cross section is rectangular.
3. Direct shear failure is neglected.
4. The load is static.
5. The material remains in the elastic range.
6. Shear deformation is neglected.
7. A safety factor of 4 is used.

### Free Body Diagram and Calculation

<img width="1216" height="1480" alt="image" src="https://github.com/user-attachments/assets/c54623c8-d05e-4d6c-883d-23df7537c66f" />


### Algebraic Solution

For a cantilever with an end load:

Mmax = FLE

For a rectangular cross section:

I = wh³ / 12

c = h / 2

σ = Mc / I

Therefore:

σ = 6M / wh²

Solving for height:

hE = [6M / (wσallow)]^(1/2)

### Numerical Solution

Mmax = (600)(2.00)

Mmax = **1,200 lbf·in**

hE = [6(1,200) / (1.00)(8,750)]^(1/2)

hE = **0.907 in**

### Final Stress Dimension

**hE,stress = 0.907 in**

---

## Feature E – Stiffness Analysis

### Known

- F = 600 lbf
- LE = 2.00 in
- E = 10,000,000 psi
- δmax = 0.005 in
- wE = 1.00 in

### Unknown

- Minimum beam height, hE

### Assumptions

1. Feature E behaves as a cantilever beam.
2. The load is applied at the free end.
3. Shear deflection is negligible.
4. The cross section is rectangular.
5. The load is static.
6. The material remains in the elastic range.
7. Maximum allowable deflection is 0.005 in.

### Free Body Diagram and Calculation

<img width="1193" height="1552" alt="image" src="https://github.com/user-attachments/assets/2da1f58b-b490-4c73-87b6-d6a17c52ac6f" />

### Algebraic Solution

For a cantilever beam with an end load:

δmax = FL³ / 3EI

For a rectangular cross section:

I = wh³ / 12

Therefore:

δmax = 4FL³ / Ewh³

Solving for height:

hE = [4FL³ / (Ewδmax)]^(1/3)

### Numerical Solution

hE = [4(600)(2.00)³ / (10,000,000)(1.00)(0.005)]^(1/3)

hE = **0.727 in**

### Comparison

hE,stress = 0.907 in

hE,stiffness = 0.727 in

Since:

**0.907 in > 0.727 in**

### Governing Requirement

**Strength governs Feature E.**

### Final Feature E Dimension

**hE = 0.907 in**

---

# Decide

## Final Design Dimensions

The stress and stiffness requirements were compared for each feature. The larger required dimension was selected as the governing design dimension.

| Feature | Stress Requirement | Stiffness Requirement | Governing Requirement | Final Dimension |
|---|---:|---:|---|---:|
| A | 1.28 in | 1.22 in | Strength | **1.28 in** |
| B | 0.1371 in | 0.0480 in | Strength | **0.14 in** |
| C | 0.642 in | 0.577 in | Strength | **0.642 in** |
| D | 0.06857 in | 0.00600 in | Strength | **0.070 in** |
| E | 0.907 in | 0.727 in | Strength | **0.907 in** |

The final design dimensions were selected based on the governing stress or stiffness requirement for each feature. The selected dimensions were rounded up where necessary for the final design.

---

# Communicate

## Multiview Drawing – Stress Dimensions

The multiview drawing below shows the dimensions determined from the stress analysis.



## Multiview Drawing – Stiffness Dimensions

The multiview drawing below shows the dimensions determined from the stiffness analysis.



---

# Process Documentation

## Design Process

The design was developed by starting with Feature A and then using the resulting dimensions and load path to determine the dimensions of the following features. The bracket was analyzed using both stress and stiffness requirements.

## Design Changes and Corrections

During the calculations, an initial approach was checked against the cantilever-beam model required by Appendix D. The calculation was corrected to use the appropriate cantilever bending relationship and the required safety factor of 4.

The corrected Feature A calculations resulted in:

- Stress requirement: **dA = 1.28 in**
- Stiffness requirement: **dA = 1.22 in**
- Governing dimension: **dA = 1.28 in**

The calculations were checked before using the resulting dimensions in the remaining feature analyses.


# Lessons Learned

## Lessons Learned

This assignment helped me understand how both strength and stiffness affect the design of a mechanical component. A feature that is strong enough can still deflect too much, so both requirements need to be checked before selecting the final dimension.

For this design, strength governed Features A through E because the required stress dimensions were larger than the required stiffness dimensions. This showed me that the governing requirement must be checked separately for every feature rather than assuming one requirement controls the entire bracket.

I also learned about error propagation. Feature A is analyzed first and its dimensions affect the geometry and load path used for the remaining features. An error in an earlier load or dimension could therefore carry into later calculations. Rechecking the intermediate calculations and comparing the final dimensions against the drawings helped catch inconsistencies before finalizing the design.

One important assumption was neglecting direct shear failure, as instructed by the assignment. If direct shear were significant, an additional shear-stress analysis would be required and the required dimensions could increase.

Another lesson was the importance of keeping the calculations and drawings consistent. The minimum calculated dimension and the final selected design dimension must be clearly distinguished so that the multiview drawings match the final design.

# Time Spent

I spent approximately **8 hours** completing this assignment.
