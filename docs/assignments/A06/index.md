# A6 – Design for Strength and Stiffness II

## Objective

The objective of this assignment was to continue the bracket design from the previous assignment by creating a fully parametric CAD model and a detailed multi-view engineering drawing.

The design was developed using the results from the previous strength and stiffness analysis. The main goals were to:

- Create a parametric solid model.
- Use engineering calculations to determine important dimensions.
- Create a fully dimensioned multi-view engineering drawing.
- Apply appropriate engineering tolerances.
- Use third-angle projection.
- Document the design process, mistakes, and lessons learned.
- Create a CAD model that can be modified parametrically.
- Provide the finished CAD files for download.

The total time spent completing the assignment was approximately **4 hours**.

---

## Analyze

### Design Parameters

The following parameters were used in the CAD model:

| Parameter | Value |
|---|---:|
| Applied Load, F | 600 lbf |
| Safety Factor, SF | 4 |
| Yield Strength, Sy | 35,000 psi |
| Young's Modulus, E | 10,000,000 psi |
| Maximum Deflection, dmax | 0.005 in |
| Cylinder Diameter, A | 1.28 in |
| Vertical Member, B | 0.140 in |
| Lower Horizontal, C | 0.650 in |
| Inner Vertical, D | 0.070 in |
| Upper Section, E | 0.907 in |
| Overall Inside Width | 3.00 in |
| Slot Width | 1.00 in |
| Bottom Left Dimension | 1.140 in |
| Bottom Right Dimension | 0.140 in |

The bracket was designed symmetrically about the centerline. The 1.00 in slot was maintained between the two inner vertical faces.

### Parametric Modeling

The dimensions were entered into the CAD software as global variables/parameters instead of creating the model entirely from fixed dimensions. This allows the geometry to update when a parameter changes.

The major stress-based dimensions used in the final model were:

- **A = 1.28 in**
- **B = 0.140 in**
- **C = 0.650 in**
- **D = 0.070 in**
- **E = 0.907 in**

The parametric table was used to control the geometry and maintain relationships between the different features.

### Analytical Equation

One of the dimensions was driven using the stress-based analytical equation rather than simply entering a manually calculated value.

For the inner vertical feature, the CAD parameter was expressed using the design variables:

**D = (2 × F × LD × SF) / (E × dmax)**

Using the design parameters:

- F = 600 lbf
- SF = 4
- E = 10,000,000 psi
- dmax = 0.005 in
- LD = 0.75 in

the CAD model produced the required stress-based dimension for the feature.

The equation was entered directly into the CAD parameter table so that the dimension could respond to changes in the design variables.

### Design Changes

During the modeling process, the dimensions from the previous analysis were transferred into the parametric model. Rather than changing individual sketch dimensions throughout the model, the global parameters were used to control the important features.

This made the model easier to modify and reduced the amount of manual rework required when dimensions were changed.

---

## Decide

### Final Design

The final design uses the stress-based dimensions from the analysis:

- **Cylinder diameter: 1.28 in**
- **Vertical member: 0.140 in**
- **Lower horizontal: 0.650 in**
- **Inner vertical: 0.070 in**
- **Upper section: 0.907 in**

The overall inside width remains **3.00 in**, and the slot width remains **1.00 in**.

The bracket is symmetric about the centerline and is designed to fit over the rigid T-beam specified in the assignment.

### Tolerances

The engineering drawing uses the required tolerance block:

- **X.X ± 0.02 in**
- **X.XX ± 0.01 in**
- **X.XXX ± 0.005 in**

Tighter tolerances were used where dimensions affect the fit and function of the bracket.

The sliding-fit areas are functionally important because they interface with the rigid T-beam. These dimensions require greater control than features that do not directly affect the fit.

A tighter tolerance was therefore applied to functional/mating dimensions, while less critical dimensions can use a looser tolerance.

Using the tightest tolerance on every dimension would increase manufacturing difficulty and cost without providing a functional benefit for non-critical features.

---

## Communicate

### Engineering Drawing

A fully dimensioned multi-view engineering drawing was created in CAD.

The drawing includes:

- Top view
- Front view
- Right-side view
- Isometric view
- Dimensions
- Engineering tolerances
- Centerlines
- Hidden lines where applicable
- Third-angle projection
- Title block
- Tolerance block

The drawing communicates the final geometry and dimensions required to manufacture the bracket.

### Final Drawing Dimensions

The final stress-based dimensions shown on the drawing are:

| Feature | Dimension |
|---|---:|
| Cylinder Diameter (A) | 1.28 in |
| Vertical Member (B) | 0.140 in |
| Lower Horizontal (C) | 0.650 in |
| Inner Vertical (D) | 0.070 in |
| Upper Section (E) | 0.907 in |
| Overall Inside Width | 3.00 in |
| Slot Width | 1.00 in |
| Bottom Left Dimension | 1.140 in |
| Bottom Right Dimension | 0.140 in |

### Design Documentation

The design process was documented using screenshots of the CAD model, sketches, parametric table, and engineering drawing.

The documentation shows how the design progressed from the calculated dimensions to the final parametric model and engineering drawing.

### Mistakes and Corrections

One challenge during the process was transferring the calculated dimensions into the parametric CAD model while maintaining the required geometric relationships.

Another important check was making sure the dimensions in the engineering drawing matched the final parametric model. The dimensions were reviewed and corrected so that the drawing represented the final stress-based design rather than values from an earlier version of the model.

The distinction between the stress-based and stiffness-based dimensions was also important. The final model and drawing were checked against the selected stress-based design values.

### Lessons Learned

This assignment demonstrated the importance of using parametric modeling for engineering design. Instead of treating every dimension as an independent value, global variables can be used to control the geometry and preserve relationships between features.

I also learned that engineering drawings must be checked against the actual CAD model. A dimension can appear correct in a calculation but still be incorrect on the final drawing if it is not connected to the correct model feature.

Another lesson was the importance of tolerances. Functional mating surfaces require tighter dimensional control because small dimensional changes can affect whether the parts fit together. Non-critical features do not necessarily require the same level of precision.

The assignment also reinforced the importance of documenting the design process. Including the calculations, parametric table, sketches, model, drawing, mistakes, and final results makes the engineering process easier for another person to understand and reproduce.

### Time Spent

**Total time: approximately 4 hours**

### Final Files

The completed CAD files and engineering drawing are included with this assignment for download and evaluation.

---

<img width="1296" height="1214" alt="image" src="https://github.com/user-attachments/assets/83dc659b-3618-45aa-bf9a-bba1f9191cdb" />
<img width="1270" height="1239" alt="image" src="https://github.com/user-attachments/assets/d6034d8d-b07e-4762-97ea-c48e984775d0" />
<img width="1558" height="1009" alt="image" src="https://github.com/user-attachments/assets/867a4567-235c-4cd4-b962-d989066164b6" />
