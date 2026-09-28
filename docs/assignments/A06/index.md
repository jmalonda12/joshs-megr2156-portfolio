# A6 – Design for Strength and Stiffness II
<img width="932" height="440" alt="image" src="https://github.com/user-attachments/assets/406d13d9-980d-4b6c-bd99-aba3558eac91" />
<img width="1993" height="896" alt="image" src="https://github.com/user-attachments/assets/69766026-2eba-4f67-8f14-2cbb141d9576" />

## Objective

The objective of this assignment was to create a comprehensive parametric solid model and multi-view engineering drawing of a bracket. The design was based on the strength and stiffness analysis completed in the previous assignment. The main goal was to use the calculated engineering values to create a fully constrained parametric CAD model and then produce an engineering drawing with appropriate dimensions, tolerances, and functional fits.

The assignment required the design process to be documented from the initial analysis through the final CAD model and engineering drawing. The documentation includes the design calculations, parametric variables, CAD development, mistakes and corrections, final dimensions, engineering drawing, tolerances, lessons learned, and total time spent.

## Analyze

The design was developed using a stiffness-based approach. The primary design conditions used were:

- Applied force, F = 600 lbf
- Safety factor, SF = 4
- Yield strength, Sy = 35,000 psi
- Elastic modulus, E = 10,000,000 psi
- Maximum allowable deflection, dmax = 0.005 in
<img width="1507" height="788" alt="image" src="https://github.com/user-attachments/assets/e71c0b6a-b7cf-4665-ac8c-21730bfe9696" />
<img width="2048" height="713" alt="image" src="https://github.com/user-attachments/assets/4915d882-f199-4c55-8928-a8015046b09c" />

The final stiffness-based dimensions used for the bracket were:

| Parameter | Final Value |
|---|---:|
| A | 1.22 in |
| B | 0.048 in |
| C | 0.577 in |
| D | 0.006 in |
| E | 0.727 in |
| Overall Inside Width | 3.00 in |
| Slot Width | 1.00 in |
| Bottom Dimension | 1.048 in |

The bracket was designed symmetrically about the centerline. The dimensions were transferred into the CAD model as global variables so that the geometry could be controlled parametrically.

## Parametric Design

The model was created by establishing the major dimensions as CAD parameters and then using those parameters to control the geometry of the bracket.

The major parameters included A, B, C, D, and E along with the overall width, slot width, and bottom dimensions.

The purpose of using global variables was to avoid entering independent dimensions throughout the model. Instead, the dimensions were connected through the parametric design so that changes to the main design values could be reflected in the model.

The final model was based on the stiffness calculations rather than simply using fixed dimensions.

### CAD Model Sketch

<img width="1266" height="1224" alt="image" src="https://github.com/user-attachments/assets/938ee2f7-8808-4332-81d6-2bdd0f680ec3" />


The initial CAD sketch established the primary bracket profile and provided the foundation for the parametric model.

### Slot and Bracket Geometry

<img width="1270" height="1239" alt="image" src="https://github.com/user-attachments/assets/5d4f0942-a3f2-45f9-9fbe-cec3cf9f2de1" />


The slot and bracket geometry were developed using the required dimensions and symmetry about the centerline.

### Global Variables and Parametric Table

<img width="1296" height="1214" alt="image" src="https://github.com/user-attachments/assets/39fedb60-2c98-45eb-8c71-84a40ec22b76" />


The parametric table was used to define and control the important dimensions of the model. This allowed the design to be changed by modifying the variables rather than manually changing every individual feature.

## Analytical Design

### Stiffness Requirement

The final design was based on the requirement that the maximum allowable deflection was:

**dmax = 0.005 in**

The circular-section relationship used during the analytical design was:

**I = (πd⁴) / 64**

Solving for the required diameter gives:

**d = (64I / π)^(1/4)**

This relationship connects the required stiffness of the section to the required circular-section diameter. The analytical design values were transferred into the CAD global variables and used to establish the final geometry.

### Analytical Equation Used to Drive the CAD Model

The circular-section equations were incorporated into the parametric design process rather than treating the calculated dimensions as unrelated numbers.

The diameter relationship was expressed in the CAD parameter system using an equation based on the required area moment of inertia:

**d = ((64I) / π)^(1/4)**

The resulting parameter was then used in the model's global variables. This allowed the calculated design value to be connected directly to the CAD model.

If the analytical value was changed, the corresponding parametric dimension could change with it, allowing the dependent model geometry to maintain the established relationships.

## Decide

### Final Design Selection

The final design uses the stiffness-based dimensions from the analytical design.

<img width="1518" height="1320" alt="image" src="https://github.com/user-attachments/assets/d1ec8bf3-0391-4643-b28e-50355c512ed9" />


The final values are:

- A = 1.22 in
- B = 0.048 in
- C = 0.577 in
- D = 0.006 in
- E = 0.727 in
- Overall inside width = 3.00 in
- Slot width = 1.00 in
- Bottom dimension = 1.048 in

The model is symmetric about the centerline.

## Mistakes and Corrections

### Initial Use of Stress-Based Dimensions

One of the main mistakes during the design process was initially using the stress-based dimensions instead of the final stiffness-based dimensions.

The initial stress-based dimensions were:

- A = 1.28 in
- B = 0.140 in
- C = 0.650 in
- D = 0.070 in
- E = 0.907 in

These values were later identified as not being the final dimensions required for the stiffness-based design.

### Correction of Main Dimensions

The dimensions were corrected to the final stiffness-based values:

- A changed from 1.28 in to 1.22 in
- B changed from 0.140 in to 0.048 in
- C changed from 0.650 in to 0.577 in
- D changed from 0.070 in to 0.006 in
- E changed from 0.907 in to 0.727 in

This correction was important because the final CAD model needed to represent the stiffness-based design calculations.

### Correction of Dependent Dimensions

The bottom dimensions also required correction.

The original bottom dimensions were:

- 1.140 in
- 0.140 in

These were corrected to:

- 1.048 in
- 0.048 in

The correction ensured that the final geometry matched the corrected stiffness-based dimensions.

### Effect of Parametric Variables

Using global variables made the correction process easier because the major design dimensions were controlled through the parametric system. Instead of rebuilding the entire model from the beginning, the design variables could be changed and the relationships between the model features could be maintained.

This demonstrated the advantage of parametric modeling when engineering dimensions change during the design process.

## Engineering Drawing

### Multi-View Engineering Drawing

<img width="1558" height="1009" alt="image" src="https://github.com/user-attachments/assets/02cadac9-562f-4da3-b52c-7411a1168c1d" />


The final engineering drawing represents the completed bracket using multiple views and the required dimensions.

The drawing includes the major geometric features needed to manufacture and inspect the part, including the bracket profile, slot, cylindrical features, overall dimensions, and functional dimensions.

### Third-Angle Projection

The engineering drawing uses third-angle projection for the multiview representation. The views were arranged to communicate the geometry of the bracket clearly and consistently.

### Sliding Fits and Gap Tolerances

The design includes three different sliding-fit conditions over the rigid T-beam feature. The gap dimensions were selected so that the required clearances correspond to the intended fit conditions.

The drawing therefore distinguishes between functional dimensions associated with the sliding interfaces and dimensions that are primarily used to define the overall geometry.

### Tolerance Block

The drawing uses the following general tolerance block:

- X.X ± 0.02 in
- X.XX ± 0.01 in
- X.XXX ± 0.005 in

The purpose of the tolerance block is to establish the allowable variation for dimensions based on the number of decimal places shown.

## Tolerance Reflection

### Tighter Tolerance

A dimension associated with the functional sliding-fit interface requires a tighter tolerance because the clearance directly affects how the mating components fit and move relative to one another.

The tighter tolerance class is:

**X.XXX ± 0.005 in**

A tighter tolerance is appropriate for a functional mating feature because excessive dimensional variation could change the intended clearance and affect the sliding fit.

### Looser Tolerance

A non-critical dimension that does not directly control the sliding interface can use the looser tolerance class:

**X.X ± 0.02 in**

A looser tolerance is appropriate for a non-critical feature because small dimensional variation in that feature does not directly determine whether the mating components will function.

### Manufacturing Considerations

Using a tight tolerance on every dimension would increase manufacturing difficulty and potentially increase manufacturing cost. Tight tolerances should therefore be applied where they are functionally necessary, while non-critical dimensions can use larger allowable variation.

This assignment demonstrated that tolerances should be connected to the function of the feature rather than automatically making every dimension as precise as possible.

## Design Documentation Process

The design process was documented throughout the assignment with screenshots of the CAD model, sketches, parametric table, corrected design, and final engineering drawing.

The documentation shows the progression from the initial design through the corrected stiffness-based model.

The main documentation stages were:

1. Review the assignment requirements.
2. Identify the required strength and stiffness design values.
3. Establish the major CAD dimensions.
4. Create the initial sketch and bracket geometry.
5. Create global variables and parametric relationships.
6. Develop the slot and T-beam geometry.
7. Compare the initial stress-based dimensions with the required stiffness-based dimensions.
8. Correct the major design parameters.
9. Correct the dependent bottom dimensions.
10. Verify the final stiffness-based geometry.
11. Create the multi-view engineering drawing.
12. Apply dimensions and tolerances.
13. Review the final design and document lessons learned.

## Lessons Learned

One of the main lessons learned was the importance of connecting engineering calculations to the CAD model instead of treating the calculated dimensions as independent values. The stiffness calculation provided the engineering basis for the circular-section dimension, while the CAD global variables allowed the resulting design values to control the model.

Another important lesson was the difference between designing for strength and designing for stiffness. The initial stress-based dimensions were different from the final stiffness-based dimensions. The correction showed that satisfying a strength requirement does not automatically mean that the design satisfies a stiffness requirement.

The assignment also demonstrated the importance of checking dependent dimensions after changing a major parameter. The bottom dimensions had to be corrected after the primary dimensions were changed so that the final geometry remained consistent with the stiffness-based design.

Another lesson was the importance of tolerances in engineering drawings. Functional sliding-fit features require tighter dimensional control because the gap directly affects how the components interact. Non-critical dimensions can use larger tolerances because small variations do not significantly affect the function of the part.

The use of global variables also demonstrated the value of parametric CAD modeling. When the design values changed, using global variables made it easier to update the model and maintain the relationships between features.

## Time Spent

Total time from the beginning of the assignment through completion was approximately:

**7 hours**

The time included reviewing the requirements, completing the design calculations, creating the parametric CAD model, correcting the design dimensions, creating the engineering drawing, applying tolerances, checking the final model, and documenting the process.

## Final Design Summary

The final bracket design was based on the stiffness requirements and used the following primary values:

- Applied force: **600 lbf**
- Safety factor: **4**
- Yield strength: **35,000 psi**
- Elastic modulus: **10,000,000 psi**
- Maximum allowable deflection: **0.005 in**
- A: **1.22 in**
- B: **0.048 in**
- C: **0.577 in**
- D: **0.006 in**
- E: **0.727 in**
- Overall inside width: **3.00 in**
- Slot width: **1.00 in**
- Bottom dimension: **1.048 in**
- Design symmetry: **About the centerline**

## Final CAD File



