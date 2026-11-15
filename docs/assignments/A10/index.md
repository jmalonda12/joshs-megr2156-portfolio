# A10 – Lead Screw Translating System

## Team Members
- Joshua Malonda
- Roncellis Marshall
- Brodie Jarvis

## Objective

The objective of this project is to design a mechanically driven lead screw translating system for a tensile testing machine capable of applying an axial tensile load of up to 2 kN. The system will use two synchronized lead screws to produce controlled and repeatable linear movement of a crosshead at speeds ranging from 1 to 50 mm/min.

The design focuses on selecting appropriate mechanical components, analyzing their structural strength, and developing a functional assembly that satisfies the project requirements.
<img width="455" height="574" alt="image" src="https://github.com/user-attachments/assets/9c0e34df-aa05-4e7e-bfc9-9e8f976b411f" />
### Design Requirements
- Maximum tensile load: 2 kN
- Crosshead speed: 1–50 mm/min
- Factor of safety: 4
- Maximum crosshead deflection: 0.1 mm
- Minimum lead screw length: 18 inches
- Two identical lead screws
- Mechanical operation without electronics or software
- Stable, compact, bench-top configuration
### Lead Screw Diameter
The first step in our design process was determining the minimum diameter required for the lead screws. I started by organizing the known values and identifying the unknown diameter that needed to be calculated. One important consideration was selecting a yield strength for the screw material. After researching steel material properties, I used an estimated yield strength of 300 MPa for the initial calculations. Using this value, the applied load shared between the two lead screws, and the required factor of safety of 4, I calculated a theoretical minimum diameter of approximately 4.12 mm. This result was relatively small, which indicated that we had flexibility when selecting a commercially available lead screw. Our team could therefore consider a larger diameter to provide additional strength and better accommodate the overall design requirements.
<img width="1261" height="1682" alt="image" src="https://github.com/user-attachments/assets/d0df7ce1-0772-4319-b8b7-d7693b1c4152" />
### Rotational Speed
For this part of the analysis, I needed to determine how fast the lead screws would have to rotate to produce the required crosshead movement. Since the final lead screw had not yet been selected, I initially considered lead distances ranging from 2 mm to 8 mm per revolution. Using the required linear travel speeds, I calculated the corresponding rotational speeds in RPM. This allowed me to establish a preliminary operating range and understand how the screw lead affects the movement of the crosshead. The results showed that the required rotational speed would remain relatively low, making the proposed system suitable for a mechanically driven design. After selecting the final lead screw, the RPM values would need to be recalculated using its actual lead.
<img width="1295" height="1705" alt="image" src="https://github.com/user-attachments/assets/0c0cd9c6-0bf5-46c4-99eb-cbdb46f83df7" />
### Lead Screw Torque
To determine the torque required to operate the lead screw system, I first researched the variables needed for the calculation. These included the coefficient of friction, major and minor thread diameters, and screw lead. Since some of these values depended on the component selection, I used preliminary estimates based on the available research. I used a friction coefficient of 0.15 and considered a lead screw diameter larger than the theoretical minimum of 4.12 mm. I increased the diameter to provide additional strength and selected dimensions close to a commercially available 1/2-inch Acme lead screw. Using these assumed thread dimensions and the torque equation, I calculated a required torque of approximately 1.27 N·m. This provided an initial estimate of the torque needed to move the applied load and helped us evaluate the feasibility of a manually operated system.
<img width="1287" height="1690" alt="image" src="https://github.com/user-attachments/assets/207d8dc9-a07a-47b6-9ca7-cfb3f40dd879" />
<img width="1281" height="1410" alt="image" src="https://github.com/user-attachments/assets/c457abac-e7f9-4803-86e1-34310600da0b" />
### Lead Screw Selection

After completing the preliminary diameter and torque calculations, I began researching commercially available lead screws that could be used in our design. I compared options from Roton and McMaster-Carr, paying attention to thread size, material, lead distance, and CAD file availability. We selected a 1018 low-carbon steel precision Acme lead screw with a nominal diameter of 1/2 inch and a lead of 0.100 inch per revolution. The screw has a right-hand thread and is supplied in a 3-foot length, which exceeds the minimum 18-inch length specified in the assignment. Its dimensions and thread configuration made it a suitable candidate for our initial design, while also providing a component that could be incorporated into our SolidWorks assembly.

**Selected Component:**
- Manufacturer: McMaster-Carr
- Part Number: 99030A005
- Material: 1018 Low-Carbon Steel
- Nominal Diameter: 1/2 inch
- Thread Size: 10 TPI
- Lead: 0.100 inch/revolution
- Length: 3 feet
- Thread Direction: Right-hand

**Manufacturer Link:** [McMaster-Carr – 1018 Carbon Steel Precision Acme Lead Screw](https://www.mcmaster.com/99030A005/)<img width="1437" height="1365" alt="image" src="https://github.com/user-attachments/assets/8347cc11-9b5e-48c9-9b2c-be63a37f2846" />
### Nut and Flange Selection (Joshua Malonda)
The next part of the design process involved evaluating the bronze nut and flange assembly to ensure that its internal threads could withstand the forces generated by the lead screw system. The main focus was determining whether the engaged threads could safely support the applied load without experiencing excessive bending stress. I used the thread bending stress analysis and the required factor of safety to evaluate the nut's strength. Based on the initial calculations and available McMaster-Carr components, a 1/2"-10 bronze Acme flange nut was identified as a potential match for the selected lead screw. The matching thread specifications allow the nut to engage properly with the lead screw, while the bronze material provides a suitable option for the translating mechanism. The final selection will depend on verifying the calculated thread stresses against the manufacturer's specifications.
<img width="1297" height="1663" alt="image" src="https://github.com/user-attachments/assets/82331646-365a-42ed-9f44-37aae45410e1" />
### Crosshead Design (Joshua Malonda)
The crosshead design began with researching suitable materials that could provide enough strength and stiffness for the tensile testing machine. After comparing material options, I selected 6061 aluminum as the initial material for the crosshead because of its mechanical properties and suitability for machining. I also established some preliminary dimensions to create enough room for the lead screw and flange nut mounting locations. The mounting points were initially positioned 100 mm from each end of the crosshead, leaving sufficient space between the mounting holes and the outer edges. A total crosshead length of 250 mm was also considered to provide the desired spacing between the two lead screw assemblies. Additional analysis was needed to determine the appropriate width and height of the crosshead while meeting the strength and maximum deflection requirements.
<img width="1294" height="1723" alt="image" src="https://github.com/user-attachments/assets/6fe15d64-4ec1-4c80-8c88-a8e557d5992d" />
<img width="1318" height="974" alt="image" src="https://github.com/user-attachments/assets/bcdf346e-8428-4293-9428-75476ceb4d0d" />
Once the crosshead calculations were completed, I moved on to preparing the engineering drawings. I created the top, front, and side views to communicate the overall shape, dimensions, and mounting locations of the crosshead. These drawings provided a reference for the next stage of the project by giving my teammate the information needed to begin creating the crosshead model and incorporating it into the SolidWorks assembly.

## Tabulating Costs (Joshua Malonda)

To establish the material expenses for our design, I put together a cost breakdown of the components needed for the CAD assembly. In addition to the two lead screws and matching bronze flange nuts, I included the hardware required to attach the flange assemblies to the crosshead. This consisted of eight socket head screws and eight matching nuts. I also included a 10-foot section of T-slot aluminum framing rather than purchasing individual frame sections. This would allow us to cut the extrusion into the different lengths needed for the machine during assembly. The table below identifies each component by its manufacturer part number, required quantity, unit price, total price, and purchasing link.

| Item Number | Quantity | Component Description | Cost/Item | Total Cost | Purchase Link |
|---|---:|---|---:|---:|---|
| 99030A005 | 2 | 1018 Carbon Steel Precision Acme Lead Screw, Right Hand, 1/2"-10 Thread, 3 Feet Long | $17.84 | $35.68 | [McMaster-Carr](https://www.mcmaster.com/99030A005/) |
| 97790A110 | 2 | Precision Acme Bronze Flange Nut, 1/2"-10 Thread | $178.60 | $357.20 | [McMaster-Carr](https://www.mcmaster.com/97790A110/) |
| 91251A233 | 8 | Black-Oxide Alloy Steel Socket Head Screw, 4-40 Thread, 1-5/8" Long | $9.27 | $74.16 | [McMaster-Carr](https://www.mcmaster.com/91251A233/) |
| 92362A110 | 8 | Black-Oxide 18-8 Stainless Steel Narrow-Profile Hex Nut, 4-40 Thread | $8.14 | $65.12 | [McMaster-Carr](https://www.mcmaster.com/92362A110/) |
| 47065T882 | 1 | Black Double Six-Slot T-Slotted Aluminum Rail, 3" High × 1-1/2" Wide, Hollow, 10 Feet Long | $185.27 | $185.27 | [McMaster-Carr](https://www.mcmaster.com/47065T882-47065T881/) |
| **Total** | **21** | | **$399.12** | **$717.43** | |

## Parametric Modeling (Joshua Malonda)
The CAD development process began by transferring the crosshead dimensions from the engineering calculations into SolidWorks. I used the Equation Manager to define the main dimensions as variables, allowing changes to the design parameters to automatically update the model. This made it easier to maintain consistent dimensions without manually editing each feature. Once the initial crosshead geometry was created, I added the necessary details, including mounting holes and fillets. After completing the initial part model, I began assembling the crosshead with the bronze flange nut to establish how the components would fit together in the final design.
### Assembly Modifications and Component Integration

While putting the initial assembly together in SolidWorks, I found that some adjustments were needed to properly connect the crosshead and bronze flange. I reopened the individual part files and modified their mounting features to allow the components to be fastened together. This involved creating tapped holes in the crosshead and adding counterbored tapped holes to the flange. I also assigned the appropriate aluminum material to the crosshead model so its material properties were represented correctly in the CAD design. Once these changes were made, the components were ready to be incorporated into the complete assembly.
## Lessons Learned (Joshua Malonda)
Throughout this assignment, we learned how important it is to connect engineering calculations with the actual design of a mechanical system. We started with the given requirements and used them to determine the minimum lead screw diameter, rotational speed, and torque needed to move the crosshead. These calculations helped us narrow down our component options and compare different lead screws and bronze nut/flange assemblies on McMaster-Carr. One of the biggest challenges was finding components that met our design requirements while also being compatible with each other and suitable for our CAD assembly.

We also gained a better understanding of how small design decisions can affect the overall complexity of a project. For example, we originally considered threading the crosshead so that it would connect directly to the lead screw. After looking more closely at the assembly, we realized that this would create extra work and make the design more complicated than necessary. Instead, we made the hole in the crosshead slightly larger than the lead screw diameter and used the bronze nut/flange assembly to provide the threaded connection. This allowed us to use the manufactured thread components rather than trying to create and match threads ourselves in SolidWorks.

Another challenge was making sure that the individual parts would fit together correctly in the final assembly. We had to go back into the part files and make adjustments to the mounting features, including the tapped holes and flange connections. This showed us that a part can look correct on its own but still require changes once it is placed into an assembly. Using SolidWorks also helped us improve our understanding of parametric modeling and how changing dimensions or features can affect the rest of a design.

Looking back, there are a few things we could have done differently. We could have spent more time comparing components and confirming their dimensions before moving too far into the CAD assembly. This may have reduced the number of modifications we had to make later. We also could have planned the crosshead mounting features earlier and checked the fit between the lead screws, nuts, flanges, and crosshead before finalizing the design. Having a more organized plan for dividing the work and checking each other's calculations and models could have also made the process more efficient.

Overall, this assignment helped us understand that designing a mechanical system involves more than completing calculations. We had to research components, make decisions based on the design requirements, work through problems during CAD modeling, and make changes when our original ideas were more complicated than necessary. It was a good opportunity to improve our problem-solving, design, and teamwork skills while applying concepts from mechanical engineering to a practical project.

**Total Project Time:** Approximately 15 hours.
