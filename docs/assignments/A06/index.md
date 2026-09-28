# A6 – Design for Strength and Stiffness II

## Objective

The objective of this assignment was to continue the bracket design from the previous assignment by creating a fully parametric CAD model and a detailed multi-view engineering drawing.

The design was developed using engineering calculations to determine the important dimensions. The main goals were to:

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

# Analyze

## Design Parameters

The following parameters were used in the CAD model:

| Parameter | Value |
|---|---:|
| Applied Load, F | 600 lbf |
| Safety Factor, SF | 4 |
| Yield Strength, Sy | 35,000 psi |
| Young's Modulus, E | 10,000,000 psi |
| Maximum Deflection, dmax | 0.005 in |
| Cylinder Diameter, A | 1.22 in |
| Vertical Member, B | 0.048 in |
| Lower Horizontal, C | 0.577 in |
| Inner Vertical, D | 0.006 in |
| Upper Section, E | 0.727 in |
| Overall Inside Width | 3.00 in |
| Slot Width | 1.00 in |
| Bottom Dimension | 1.048 in |

The bracket was designed symmetrically about the centerline. The 1.00 in slot was maintained between the two inner vertical faces.

## Parametric Modeling

The dimensions were entered into the CAD software as global variables/parameters instead of creating the model entirely from fixed dimensions. This allows the geometry to update when a parameter changes.

The final stiffness-based dimensions used in the model were:

```text
A = 1.22 in
B = 0.048 in
C = 0.577 in
D = 0.006 in
E = 0.727 in

The other important dimensions were:

Overall Inside Width = 3.00 in
Slot Width = 1.00 in
Bottom Dimension = 1.048 in
Maximum Deflection = 0.005 in

The parametric table was used to control the geometry and maintain relationships between the different features.

CAD Model Sketch

Slot and Bracket Geometry

The 1.00 in slot was maintained between the two inner faces, with the bracket remaining symmetric about the centerline.

Analytical Equation

The stiffness design was based on limiting the maximum allowable deflection to:

dmax = 0.005 in

A circular-section relationship used in the stiffness design relates the area moment of inertia to the diameter:

I = (pi*d^4)/64

Solving for the diameter gives:

d = (64*I/pi)^(1/4)

This relationship allows the required stiffness to be related to the required circular-section diameter.

The analytical design values were transferred into the CAD global variables so that the model could be controlled parametrically instead of relying only on manually entered dimensions.

The CAD parameter table allowed the model to respond when a controlling design variable was changed.

Parametric Table

The parametric table shows the global variables and relationships used to control the CAD model.

Decide
Final Design

The final A6 design uses the stiffness-based dimensions.

The final values are:

A = 1.22 in
B = 0.048 in
C = 0.577 in
D = 0.006 in
E = 0.727 in

The remaining major dimensions are:

Overall Inside Width = 3.00 in
Slot Width = 1.00 in
Bottom Dimension = 1.048 in
Maximum Deflection = 0.005 in

The final design maintains symmetry about the centerline and the required 1.00 in slot.

Mistakes and Corrections

One of the main mistakes during the modeling process was initially using the stress-based/reference dimensions when setting up the CAD model.

The original stress-based dimensions were:

A = 1.28 in
B = 0.140 in
C = 0.650 in
D = 0.070 in
E = 0.907 in

These dimensions were initially transferred into the model because they were available from the previous design analysis and were useful as a reference for building the geometry.

After reviewing the stiffness requirements, I realized that the final A6 design needed to use the stiffness-based dimensions instead.

The dimensions were corrected as follows:

A: 1.28 in -> 1.22 in
B: 0.140 in -> 0.048 in
C: 0.650 in -> 0.577 in
D: 0.070 in -> 0.006 in
E: 0.907 in -> 0.727 in

The bottom dimensions also had to be updated because they depend on the B dimension.

The original bottom dimensions were:

Bottom Left = 1.140 in
Bottom Right = 0.140 in

After changing B from 0.140 in to 0.048 in, the corresponding bottom dimensions were updated to:

Bottom Left = 1.048 in
Bottom Right = 0.048 in

This correction was important because leaving the original stress-based dimensions in the drawing would have caused the engineering drawing and final stiffness-based design to disagree.

The final stiffness-based values used in the completed design are:

A = 1.22 in
B = 0.048 in
C = 0.577 in
D = 0.006 in
E = 0.727 in

This mistake showed me that dimensions from an earlier design cannot simply be transferred into a new design without checking what design requirement they satisfy. The stress-based values and stiffness-based values are different because they come from different design requirements.

Using global variables made the correction easier because the dimensions could be changed in the parameter table instead of manually changing every dependent sketch dimension.

Corrected Stiffness-Based Design

This image shows the corrected stiffness-based design dimensions used for the final A6 model and drawing.

Tolerances

The engineering drawing uses the required tolerance block:

X.X ± 0.02 in
X.XX ± 0.01 in
X.XXX ± 0.005 in

Tighter tolerances are important for dimensions that affect the fit and function of the bracket.

The sliding-fit areas are functionally important because they interface with the rigid T-beam. These dimensions require greater control than features that do not directly affect the fit.

A tighter tolerance is therefore appropriate for functional or mating dimensions, while less critical dimensions can use a looser tolerance.

Using the tightest tolerance on every dimension would increase manufacturing difficulty, inspection requirements, and cost without providing a functional benefit for non-critical features.

Communicate
Engineering Drawing

A fully dimensioned multi-view engineering drawing was created in CAD.

The drawing includes:

Top view
Front view
Right-side view
Isometric view
Dimensions
Engineering tolerances
Centerlines
Hidden lines where applicable
Third-angle projection
Title block
Tolerance block

The drawing communicates the final geometry and dimensions required to manufacture the bracket.

Final Engineering Drawing

The final drawing shows the stiffness-based dimensions and the required engineering drawing information.

Final Drawing Dimensions

The final stiffness-based dimensions shown on the drawing are:

Feature	Dimension
Cylinder Diameter (A)	1.22 in
Vertical Member (B)	0.048 in
Lower Horizontal (C)	0.577 in
Inner Vertical (D)	0.006 in
Upper Section (E)	0.727 in
Overall Inside Width	3.00 in
Slot Width	1.00 in
Bottom Dimension	1.048 in

The final drawing was checked against the parametric model so that the dimensions communicate the same final design.

Design Documentation

The design process was documented using screenshots of the CAD model, sketches, parametric table, global variables, and engineering drawing.

The screenshots show the progression from the initial CAD setup through the corrected stiffness-based design and final engineering drawing.

Global Variables and Equations

The global variables and equations were used to control the model parametrically.

Lessons Learned

This assignment demonstrated the importance of using parametric modeling for engineering design.

Instead of treating every dimension as an independent value, global variables can be used to control the geometry and preserve relationships between features.

I also learned that engineering calculations must be connected to the actual CAD model. A dimension may be correct for one design requirement but not correct for another. In this assignment, the stress-based dimensions were initially used as a reference, but the final design required the stiffness-based dimensions.

The main dimensional changes were:

A = 1.28 in -> 1.22 in
B = 0.140 in -> 0.048 in
C = 0.650 in -> 0.577 in
D = 0.070 in -> 0.006 in
E = 0.907 in -> 0.727 in

This showed me the importance of checking whether the dimensions being used actually correspond to the selected design requirement.

I also learned that engineering drawings must be checked against the actual CAD model. A dimension can appear correct in a calculation but still be incorrect on the final drawing if it is not connected to the correct model feature.

Another lesson was the importance of tolerances. Functional mating surfaces require tighter dimensional control because small dimensional changes can affect whether the parts fit together. Non-critical features do not necessarily require the same level of precision.

The assignment also reinforced the importance of documenting the design process. Including the calculations, parametric table, sketches, model, drawing, mistakes, and final results makes the engineering process easier for another person to understand and reproduce.

Time Spent

Total time: approximately 4 hours

The time included:

Reviewing the design requirements
Reviewing the stiffness calculations
Setting up the SolidWorks global variables
Creating the parametric model
Identifying the incorrect stress-based dimensions
Updating the model to the stiffness-based dimensions
Checking dependent dimensions
Creating the engineering drawing
Adding dimensions and tolerances
Reviewing the final CAD model
Documenting the design process
Final Files

The completed CAD files and engineering drawing should be included with the assignment for download and evaluation.

The repository should contain the final SolidWorks CAD file and documentation.

Suggested repository structure:

A6/
├── README.md
├── CAD/
│   └── Bracket_Final.SLDPRT
└── images/
    ├── cad-sketch.png
    ├── slot-geometry.png
    ├── parametric-table.png
    ├── stiffness-design.png
    └── final-drawing.png

The final CAD file should be uploaded so the TA can download and inspect the parametric model.
