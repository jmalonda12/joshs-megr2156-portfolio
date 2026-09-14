# A5 – Bracket Design for Strength and Stiffness

## Objective

The objective of this assignment was to design a bracket based on the concept design in Appendix B to hold a horizontal force applied symmetrically by the strap shown in the assignment.

The bracket was designed using:

- Applied load: F = 600 lbf
- Safety factor: SF = 4
- Material: Aluminum 6061-T6
- Yield strength: Sy = 35,000 psi
- Young's modulus: E = 10,000,000 psi
- Maximum allowable deflection: δmax = 0.005 in
- Direct shear failure neglected as instructed

The bracket was separated into five features, A through E, and each feature was analyzed for both strength and stiffness.

## Analyze

### Design Requirements

The design must satisfy:

- 500 lbf < F < 800 lbf
- Safety factor = 4
- Material must be Aluminum 6061-T6, ASTM A36 Steel, or Ti-6Al-4V
- Maximum deflection = 0.005 in
- Direct shear failure is neglected
- The bracket is designed symmetrically where applicable

### Material Properties

| Property | Value |
|---|---:|
| Material | Aluminum 6061-T6 |
| Yield Strength, Sy | 35,000 psi |
| Young's Modulus, E | 10,000,000 psi |
| Safety Factor | 4 |
| Allowable Stress | 8,750 psi |
| Maximum Deflection | 0.005 in |
| Applied Load | 600 lbf |

### Allowable Stress

σallow = Sy / SF

σallow = 35,000 / 4

σallow = 8,750 psi

---

# Feature A – Stress Analysis

Feature A was modeled as a cantilever beam as directed in Appendix D.

### Known Values

- F = 600 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- LA = 3.00 in
- Circular cross section

### Unknowns

- Minimum required diameter, d
- Maximum bending stress

### Assumptions

1. Feature A is modeled as a cantilever beam.
2. The right side of Feature A is fixed to Feature B.
3. The 600 lbf load is applied at the free end.
4. The load is applied symmetrically by the strap.
5. Direct shear failure is neglected.
6. The beam has a constant circular cross section.
7. Linear elastic beam theory is used.
8. A safety factor of 4 is used.

### Calculations

Maximum bending moment:

M = FL

M = (600)(3.00)

M = 1,800 lbf·in

For a circular section:

Z = πd³ / 32

Bending stress:

σ = M/Z

Set σ = σallow:

d = [32M/(πσallow)]^(1/3)

d = [32(1,800)/(π(8,750))]^(1/3)

d = 1.28 in

### Feature A Stress Result

Minimum required diameter:

dA,stress = 1.28 in

---

# Feature A – Stiffness Analysis

### Known Values

- F = 600 lbf
- E = 10,000,000 psi
- LA = 3.00 in
- δmax = 0.005 in
- Circular cross section

### Unknowns

- Minimum required diameter, d
- Moment of inertia, I

### Assumptions

1. Feature A is modeled as a cantilever beam.
2. The load is applied at the free end.
3. Shear deflection is negligible.
4. The beam has a constant circular cross section.
5. Linear elastic beam theory is used.

### Calculations

Cantilever tip deflection:

δ = FL³/(3EI)

For a circular section:

I = πd⁴/64

Therefore:

δ = 64FL³/(3Eπd⁴)

Solve for d:

d = [64FL³/(3Eπδmax)]^(1/4)

d = [64(600)(3.00)³/(3(10,000,000)π(0.005))]^(1/4)

d = 0.609 in

### Feature A Stiffness Result

Minimum required diameter:

dA,stiffness = 0.609 in

### Feature A Governing Requirement

Strength requires:

1.28 in

Stiffness requires:

0.609 in

Therefore, strength governs.

Final Feature A diameter:

dA = 1.28 in

---

# Feature B – Stress Analysis

Feature B was modeled as an axially loaded bar.

### Known Values

- F = 600 lbf
- PB = 2F = 1,200 lbf
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi
- Width, wB = 1.00 in

### Unknowns

- Cross-sectional area, AB
- Thickness, tB

### Assumptions

1. Feature B is modeled as an axially loaded bar.
2. The symmetric load path produces PB = 2F.
3. The load is distributed uniformly over the cross section.
4. Direct shear failure is neglected.
5. Linear elastic behavior is assumed.

### Calculations

PB = 2F

PB = 2(600)

PB = 1,200 lbf

Axial stress:

σ = P/A

Solve for area:

A = P/σallow

A = 1,200/8,750

A = 0.1371 in²

Since:

A = wt

tB = A/w

tB = 0.1371/1.00

tB = 0.1371 in

### Feature B Stress Result

Minimum required thickness:

tB,stress = 0.1371 in

Selected thickness:

tB = 0.14 in

---

# Feature B – Stiffness Analysis

### Known Values

- PB = 1,200 lbf
- E = 10,000,000 psi
- LB = 2.00 in
- δmax = 0.005 in
- wB = 1.00 in

### Unknowns

- Required area, AB
- Required thickness, tB

### Assumptions

1. Feature B is modeled as an axially loaded bar.
2. Shear deflection is negligible.
3. The bar has a constant cross section.
4. Linear elastic behavior is assumed.

### Calculations

Axial deflection:

δ = PL/(AE)

Solve for area:

A = PL/(Eδmax)

A = (1,200)(2.00)/[(10,000,000)(0.005)]

A = 0.0480 in²

Thickness:

tB = A/w

tB = 0.0480/1.00

tB = 0.0480 in

### Feature B Stiffness Result

Minimum required thickness:

tB,stiffness = 0.0480 in

### Feature B Governing Requirement

Strength requires:

0.1371 in

Stiffness requires:

0.0480 in

Therefore, strength governs.

Final Feature B thickness:

tB = 0.14 in

---

# Feature C – Stress Analysis

Feature C was modeled as a simply supported beam with a concentrated load at the center as directed in Appendix D.

### Known Values

- F = 600 lbf
- LC = 4.00 in
- wC = 1.00 in
- SF = 4
- Sy = 35,000 psi
- σallow = 8,750 psi

### Unknowns

- Minimum required thickness, tC
- Maximum bending stress

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The 600 lbf load is applied at the center.
3. The beam has a rectangular cross section.
4. Direct shear failure is neglected.
5. Linear elastic beam theory is used.

### Free Body Diagram

The center load is supported equally:

RA = RB = F/2

RA = RB = 600/2

RA = RB = 300 lbf

### Calculations

Maximum moment:

Mmax = FL/4

Mmax = (600)(4.00)/4

Mmax = 600 lbf·in

For a rectangular section:

I = wt³/12

c = t/2

Bending stress:

σ = Mc/I

Therefore:

σ = 6M/(wt²)

Solve for thickness:

t = √[6M/(wσallow)]

t = √[6(600)/(1.00)(8,750)]

t = 0.641 in

### Feature C Stress Result

Minimum required thickness:

tC,stress = 0.641 in

Selected thickness:

tC = 0.65 in

---

# Feature C – Stiffness Analysis

### Known Values

- F = 600 lbf
- LC = 4.00 in
- E = 10,000,000 psi
- wC = 1.00 in
- δmax = 0.005 in

### Unknowns

- Required thickness, tC
- Moment of inertia, I

### Assumptions

1. Feature C is modeled as a simply supported beam.
2. The load is concentrated at the center.
3. Shear deflection is negligible.
4. The beam has a constant rectangular cross section.
5. Linear elastic beam theory is used.

### Calculations

Maximum center deflection:

δ = FL³/(48EI)

For a rectangular section:

I = wt³/12

Substitute:

δ = FL³/(4Ewt³)

Solve for thickness:

t = [FL³/(4Ewδmax)]^(1/3)

t = [(600)(4.00)³/(4(10,000,000)(1.00)(0.005))]^(1/3)

t = 0.577 in

### Feature C Stiffness Result

Minimum required thickness:

tC,stiffness = 0.577 in

### Feature C Governing Requirement

Strength requires:

0.641 in

Stiffness requires:

0.577 in

Therefore, strength governs.

Final Feature C thickness:

tC = 0.65 in

---

# Feature D – Stress Analysis

The Feature D stress analysis and FBD are shown in the calculation image below.

<img src="PASTE_FEATURE_D_STRESS_IMAGE_LINK_HERE" alt="Feature D Stress Analysis">

The calculation includes the required known values, unknowns, assumptions, FBD, algebraic solution, and numerical solution.

---

# Feature D – Stiffness Analysis

The Feature D stiffness analysis and FBD are shown in the calculation image below.

<img src="PASTE_FEATURE_D_STIFFNESS_IMAGE_LINK_HERE" alt="Feature D Stiffness Analysis">

The calculation uses the required maximum deflection of 0.005 in and neglects shear deflection as directed by the assignment.

---

# Feature E – Stress Analysis

The Feature E stress analysis and FBD are shown in the calculation image below.

<img src="PASTE_FEATURE_E_STRESS_IMAGE_LINK_HERE" alt="Feature E Stress Analysis">

The calculation includes the required known values, unknowns, assumptions, FBD, algebraic solution, and numerical solution.

---

# Feature E – Stiffness Analysis

The Feature E stiffness analysis and FBD are shown in the calculation image below.

<img src="PASTE_FEATURE_E_STIFFNESS_IMAGE_LINK_HERE" alt="Feature E Stiffness Analysis">

The calculation uses the required maximum deflection of 0.005 in and neglects shear deflection as directed by the assignment.

---

# Decide

## Final Design Dimensions

The final dimensions are selected using the larger requirement from the stress and stiffness analyses.

| Feature | Stress Requirement | Stiffness Requirement | Governing | Final Dimension |
|---|---:|---:|---|---:|
| A | 1.28 in diameter | 0.609 in diameter | Strength | 1.28 in |
| B | 0.1371 in thickness | 0.0480 in thickness | Strength | 0.14 in |
| C | 0.641 in thickness | 0.577 in thickness | Strength | 0.65 in |
| D | See calculation | See calculation | See calculation | See multiview |
| E | See calculation | See calculation | See calculation | See multiview |

The selected dimensions are rounded up from the minimum calculated dimensions so that the design does not fall below the required strength or stiffness dimensions.

## Governing Failure Mode

For Features A, B, and C, the strength requirement governs over the stiffness requirement.

Feature A is the clearest example:

- Strength diameter = 1.28 in
- Stiffness diameter = 0.609 in

Therefore, the stress requirement controls the final Feature A diameter.

The final design dimensions were selected based on the governing requirement for each feature.

---

# Communicate

## Multiview Drawing – Stress Calculated Dimensions

The following multiview drawing shows the bracket using the dimensions determined from the stress analysis.

<img src="PASTE_MULTIVIEW_STRESS_IMAGE_LINK_HERE" alt="Multiview Drawing - Stress Calculated Dimensions">

## Multiview Drawing – Stiffness Calculated Dimensions

The following multiview drawing shows the bracket using the dimensions determined from the stiffness analysis.

<img src="PASTE_MULTIVIEW_STIFFNESS_IMAGE_LINK_HERE" alt="Multiview Drawing - Stiffness Calculated Dimensions">

## Final CAD Model

The final CAD model was created using the calculated governing dimensions and the required fit dimensions from the assignment.

[CAD Download Link](PASTE_CAD_DOWNLOAD_LINK_HERE)

## Design Changes

The final design dimensions were updated based on the governing stress and stiffness requirements. The dimensions shown in the final CAD model and multiview drawings correspond to the final selected design.

The Feature A stiffness calculation was also kept consistent with the 3.00 in cantilever length used in the stress analysis.

## Lessons Learned

This assignment showed me that a mechanical design cannot be based on only one type of analysis. Each feature must be checked for both strength and stiffness because either requirement can control the final dimension.

I also learned that errors in an earlier feature can affect later dimensions because the features are connected and the load path continues through the bracket. Checking intermediate values before using them in the next feature helps prevent errors from carrying through the design.

For the governing requirement, Features A, B, and C were controlled by strength rather than stiffness. This showed that increasing the section size to satisfy the stress requirement also provided more stiffness than the minimum required.

One important assumption was neglecting direct shear failure as instructed by the assignment. If direct shear were not negligible, an additional shear-stress check would be required and could increase the required dimensions.

Total time spent on the assignment: [ENTER ACTUAL TIME] hours.
