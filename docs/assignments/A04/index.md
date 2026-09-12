# A4 – Motor Mount Design

## Objective

The objective of this assignment was to design a motor mount for a 24 V DC gear motor. The motor mount needed to support an applied force of 300 N while keeping the maximum deflection at or below 0.30 mm.

The design was required to use a safety factor of 3 and one of the approved materials: ABS, PETG, or PLA. I selected PLA for the final design.

The motor weight was neglected as instructed.

---

## Analyze

### Feature 1 – Motor-Attached Feature

For Feature 1, I modeled the motor-attached section as a rectangular cantilever beam fixed at the wall. The given force was 300 N, and the motor/gearbox diameter was approximately 28 mm with an 18 mm shaft length.

The design values were:

- Applied force: **P = 300 N**
- Maximum allowable deflection: **δmax = 0.30 mm**
- Safety factor: **SF = 3**
- Material: **PLA**
- Young's modulus: **E = 1200 MPa**
- Yield strength: **Sy = 70 MPa**
- Beam length: **L = 50 mm**
- Beam width: **b = 30 mm**
- Moment arm: **e = 18 mm**

<img width="1227" height="1593" alt="Feature 1 knowns and assumptions" src="https://github.com/user-attachments/assets/7d57a651-efb1-4ae6-a7ce-ea256d8e4acd" />

### Free Body Diagram

The motor-attached section was treated as a cantilever beam with the 300 N force applied at the free end.

<img width="1283" height="1170" alt="Feature 1 free body diagram" src="https://github.com/user-attachments/assets/dad2fe55-1dbb-483d-8eb2-86fd45513815" />

### Bending Moment

The bending moment was calculated using:

M = Pe

M = (300 N)(18 mm)

M = **5400 N·mm**

For a rectangular cross section:

I = bh³/12

c = h/2

<img width="1243" height="1591" alt="Feature 1 bending moment and yield strength calculation" src="https://github.com/user-attachments/assets/385d77a2-e7c6-4a60-b262-3d28303e0760" />

### Yield Strength

The allowable stress was calculated using the safety factor:

σallow = Sy/SF

σallow = 70/3

σallow = **23.33 MPa**

Solving for the required height based on yield strength gave:

hσ = **6.80 mm**

### Maximum Deflection

The cantilever beam deflection equation was used:

δmax = ML²/(2EI)

For a rectangular cross section, this becomes:

δmax = 6ML²/(Ebh³)

Solving for the required height:

hδ = **19.57 mm**

Since the deflection requirement controlled the design:

hδ > hσ

19.57 mm > 6.80 mm

I rounded the required height up to:

**h₁ = 20 mm**

<img width="1248" height="1465" alt="Feature 1 deflection calculation and final height" src="https://github.com/user-attachments/assets/947c0705-4686-444f-bc2a-40fbe51ea33d" />

---

### Feature 2 – Wall-Attached Feature

Feature 2 was treated as another cantilever beam. The rigid wall was assumed to be capable of supporting the mounting bolts.

The selected dimensions were:

- Feature 2 length: **L₂ = 77 mm**
- Feature 2 width: **b₂ = 35 mm**
- Feature 1 height: **h₁ = 20 mm**

The effective distance used for the bending moment was:

d = L₂ + h₁ + 18

d = 77 + 20 + 18

d = **115 mm**

Therefore:

M₂ = Pd

M₂ = (300 N)(115 mm)

M₂ = **34,500 N·mm**

<img width="1210" height="1576" alt="Feature 2 knowns and free body diagram" src="https://github.com/user-attachments/assets/ac464533-108c-481d-ba05-137120489cbd" />

### Feature 2 Yield Strength

The required height based on yield strength was:

hσ = **15.92 mm**

### Feature 2 Maximum Deflection

The required height based on maximum deflection was:

hδ = **46.01 mm**

Because the deflection requirement controlled:

46.01 mm > 15.92 mm

The final selected height was rounded up to:

**h₂ = 47 mm**

Therefore, the final Feature 2 dimensions used in the CAD model were:

- **L₂ = 77 mm**
- **b₂ = 35 mm**
- **h₂ = 47 mm**

<img width="1208" height="1505" alt="Feature 2 calculations" src="https://github.com/user-attachments/assets/a9a92efa-a163-47d0-a469-2967b6b72469" />

---
## Mistakes / Design Changes
## Mistakes / Design Changes

During the design process, I noticed that there was uncertainty in the effective moment arm used for Feature 2. My original calculation used the Feature 2 dimensions and the motor shaft length to determine the effective distance:

d = L₂ + h₁ + 18 mm

d = 77 mm + 20 mm + 18 mm

d = 115 mm

Using this value, the original bending moment was:

M₂ = Pd

M₂ = (300 N)(115 mm)

M₂ = 34,500 N·mm

Using the original moment, the Feature 2 yield-strength calculation gave:

hσ = √[6M₂(SF)/(b₂Sy)]

hσ = √[6(34,500 N·mm)(3)/(35 mm)(70 MPa)]

hσ = 15.92 mm

The original maximum-deflection calculation gave:

hδ = ∛[6M₂L₂²/(Eb₂δmax)]

hδ = ∛[6(34,500 N·mm)(77 mm)²/((1200 MPa)(35 mm)(0.30 mm))]

hδ = 46.01 mm

Therefore, the original final Feature 2 height was rounded up to:

h₂ = 47 mm

After reviewing the Feature 2 geometry more carefully, I recognized that the moment arm for the wall-attached feature should be based on the horizontal distance from wall A to the line of action of the applied force. Using the Feature 1 length and shaft length, the alternative moment arm would be:

d = L₁ + 18 mm

d = 50 mm + 18 mm

d = 68 mm

The corresponding bending moment would then be:

M₂ = Pd

M₂ = (300 N)(68 mm)

M₂ = 20,400 N·mm

Using this moment, the Feature 2 yield-strength requirement would be:

hσ = √[6M₂(SF)/(b₂Sy)]

hσ = √[6(20,400 N·mm)(3)/(35 mm)(70 MPa)]

hσ = 12.24 mm

The corresponding maximum-deflection requirement would be:

hδ = ∛[6M₂L₂²/(Eb₂δmax)]

hδ = ∛[6(20,400 N·mm)(77 mm)²/((1200 MPa)(35 mm)(0.30 mm))]

hδ = 38.62 mm

This would result in an alternative Feature 2 height of approximately:

h₂ = 39 mm

For this assignment, I kept the original Feature 2 dimensions and CAD model at 47 mm so that the calculations, isometric sketch, parametric model, and final CAD design remained consistent with one another. Documenting this difference helped me understand how important it is to establish the correct moment arm and geometry before completing the beam calculations and CAD model.
## Decide

### Final Dimensions

Based on the bending stress and deflection calculations, the final dimensions selected for the motor mount were:

| Feature | Dimension |
|---|---:|
| Feature 1 Length | 50 mm |
| Feature 1 Width | 30 mm |
| Feature 1 Height | 20 mm |
| Feature 2 Length | 77 mm |
| Feature 2 Width | 35 mm |
| Feature 2 Height | 47 mm |
| Material | PLA |
| Safety Factor | 3 |
| Maximum Deflection | 0.30 mm |

The deflection requirement controlled both features because the height required for deflection was greater than the height required for yield strength.

### Isometric Design

I created an isometric sketch using the calculated dimensions before creating the final CAD model.

<img width="1228" height="1572" alt="Final isometric sketch" src="https://github.com/user-attachments/assets/48c8283f-5b7f-4aa7-bd5a-6bd5899acf9a" />

### Parametric CAD Model

I used SolidWorks to create the motor mount as a parametric model. The main dimensions were entered as global variables so that the design could be modified while keeping the important dimensions connected.

<img width="1086" height="1019" alt="SolidWorks global variables" src="https://github.com/user-attachments/assets/f2db82fa-a50d-4852-b467-dcd5c677bf52" />

---

## Communicate

### Motor Mount Features

The motor mounting area was designed around the approximately 28 mm motor/gearbox diameter. A center hole with a diameter of 6 mm was included for the motor shaft.

Four additional mounting holes were placed around the motor mounting area. The holes have a diameter of **3.4 mm** and are positioned on a **22 mm bolt circle**.

<img width="3424" height="1238" alt="Motor mounting hole pattern" src="https://github.com/user-attachments/assets/f729c9f8-7076-4b5e-b7b8-d4bed039128f" />

### Wall Mounting Holes

Four 3.4 mm clearance holes were also added to the wall-attached section so that bolts could be used to attach the motor mount to the rigid wall.

<img width="2099" height="1623" alt="Wall mounting holes" src="https://github.com/user-attachments/assets/8d5be413-1ad7-450b-8ddb-08e18703d88d" />

### Final CAD Model

The final SolidWorks model incorporates the calculated beam dimensions, motor mounting features, shaft clearance, and wall mounting holes.

<img width="2499" height="1620" alt="Final motor mount CAD model" src="https://github.com/user-attachments/assets/366c1409-9a62-440c-ab5c-e7a6228bc741" />
<img width="2649" height="1620" alt="Motor pocket" src="https://github.com/user-attachments/assets/a556f9a3-666d-4004-be61-3891a6cc98e8" />
<img width="963" height="425" alt="image" src="https://github.com/user-attachments/assets/d9f03b91-6a5f-4a3d-89f0-e7bd25f2e9bb" />
### Motor Pocket

The motor seating area was created using the motor dimensions. The outer motor/gearbox diameter was modeled as approximately 28 mm, with additional clearance for the motor to sit properly.



---

## Research

I looked at existing motor mounting designs to compare different approaches to securing gear motors and attaching them to a larger structure.

One example is the Pololu machined aluminum bracket for 37D gearmotors. It uses mounting holes to secure the motor to the bracket and additional holes to attach the bracket to another surface. :contentReference[oaicite:1]{index=1}

Another example is the Pololu stamped aluminum L-bracket, which uses multiple mounting holes and provides an L-shaped mounting configuration similar to the concept used in this assignment. :contentReference[oaicite:2]{index=2}

I also reviewed McMaster-Carr's motor bracket options to compare different commercial motor mounting configurations. :contentReference[oaicite:3]{index=3}

### Research Links

- [Pololu Machined Aluminum Bracket for 37D Gearmotors](https://www.pololu.com/product/1995)
- [Pololu Stamped Aluminum L-Bracket for 37D Gearmotors](https://www.pololu.com/product/1084)
- [McMaster-Carr Motor Brackets](https://www.mcmaster.com/products/motor-brackets/)

---

## Lessons Learned

This assignment helped me better understand how bending stress and beam deflection affect mechanical design. I learned that a design can satisfy the yield-strength requirement but still need to be made thicker because of deflection.

For this design, deflection controlled the required height of both features. I also gained more experience using SolidWorks to create a parametric model, add mounting holes, and use dimensions from calculations to create the final part.

---

## Time

This project took approximately **7 hours** to complete.

---

## CAD File

The SolidWorks CAD file for the completed motor mount is included below.

**(https://mail.google.com/mail/u/1?ui=2&ik=4e9b2dd91e&attid=0.1&permmsgid=msg-a:r3681669250132297329&view=att&disp=safe&realattid=f_mtytunng0&zw)**
