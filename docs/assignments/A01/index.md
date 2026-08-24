# A1 – Build Your Professional Portfolio

## Objective
The goal of this assignment is to get my portfolio set up and establish how I want to document my engineering work this semester. I will look at other engineering portfolios to see what makes them useful, analyze a simple mechanical product to practice applying engineering concepts, and set some standards for how I will present my work going forward.

## Analyze
Task A: Portfolio Analysis

For this part, I looked at two engineering portfolios, Evan Hoerl's and Tyler Wisniewski's. I looked at the main pages and followed the project links and images to see how each portfolio actually presents engineering work. I focused on four things: how easy the site is to navigate, whether the work could be reproduced from the information provided, whether the engineering reasoning is shown, and whether the writing fits an engineering portfolio.

# Evan Hoerl Engineering Portfolio
(https://ejhoerl.github.io/)

Evan Hoerl's portfolio is easy to navigate because the main page separates his projects, work experience, and resume. The projects are listed individually, including three Purdue Formula SAE projects, an arcade cabinet, and a pinball cabinet. Each project has a separate link, so a reader does not have to search through one long page to find a specific project. From a navigation standpoint, I could find a specific type of project quickly because the project names are visible on the main page.

The portfolio is more limited when it comes to reproducibility. It gives the reader information about what Evan worked on and what his role was, but the main site does not provide all of the dimensions, calculations, material information, or manufacturing information needed to reproduce the projects from start to finish. For example, the Formula SAE projects identify his role on the chassis team, but knowing his role does not give another engineer enough information to recreate the chassis. I would need additional drawings, calculations, specifications, or other design documentation.

There is evidence of engineering reasoning, but it is not the main focus of the site. Evan explains his responsibilities and gives background about the engineering work he completed. His Daimler Trucks experience is a good example because he explains that his team worked on transmission gear sets and that he was exposed to different stages of the design process. However, the site does not consistently show the calculations, alternatives, or decision criteria behind individual designs. It tells the reader what he worked on more often than it shows exactly why a particular engineering decision was made.

The tone of the portfolio is appropriate for an engineering audience. The content focuses on projects, engineering experience, technical responsibilities, and skills. The resume and contact information are also easy to find. Overall, I think Evan's portfolio is effective for showing engineering experience and projects, but it would need more technical documentation for a reader to reproduce most of the work.

#### Tyler Wisniewski Engineering Portfolio
(https://tylerwisniewski.github.io/)

Tyler Wisniewski's portfolio is also easy to navigate. The main page separates Projects, About, Resume, and Sitemap, and the project section tells the reader to select the project images for more information. This gives a first-time visitor a simple way to move from the homepage into the actual engineering work. The individual project pages are also separated instead of putting every project into one document.

Tyler's portfolio is stronger in reproducibility than Evan's because some of the individual project pages include much more technical information. For example, the Mechatronics project explains the robot's ATmega microcontroller, C programming, color sensor, QTI sensors, and sheet-metal components. It also provides a final report and a video of the robot competing. His surfboard fin project goes even further by explaining the design goals, the FCS fin-box choice, the different fin geometries, CFD analysis, structural analysis, manufacturing process, and the results used to select the final design. This gives another engineer much more information about how the design was developed and why the final version was selected.

The portfolio also shows stronger evidence of engineering reasoning on the detailed project pages. The surfboard fin project is a good example because Tyler did not just show the final fin. He compared a Fat Fin and a Skinny Fin using analysis, reported the drag and lift results, checked the structural factor of safety, and then used those results to decide which design to manufacture. He also explains why he selected the FCS fin-box system and why he chose forged carbon fiber for manufacturing. This connects the analysis to the design decision instead of only showing the finished product.

The tone is appropriate for an engineering portfolio because the site focuses on projects, technical work, analysis, manufacturing, and results. Some of the writing is more casual than I would use in my own portfolio, but the technical sections still provide useful engineering information. The project pages also give the reader a better understanding of what Tyler actually did instead of only listing the project name.

# Comparison

The two portfolios have different strengths. Evan's portfolio is more focused on giving a quick overview of his engineering experience and making his projects easy to find. Tyler's portfolio provides more technical depth once the reader opens the individual project pages.

For navigation, I think both portfolios meet the basic requirement because the main projects can be found without spending much time searching. Tyler's site has a more structured navigation menu, while Evan's homepage puts the main projects directly on the page.

For reproducibility, Tyler's portfolio is stronger because some of his project pages include specific analysis methods, design parameters, numerical results, manufacturing information, and supporting files. Evan's portfolio gives useful information about his experience, but a reader would need additional engineering documentation to reproduce most of the projects.

For evidence of reasoning, Tyler's surfboard fin project was the strongest example I found. He compared two designs, analyzed their performance, checked the structural requirements, and used those results to choose the Skinny Fin for manufacturing. Evan's portfolio gives more information about his responsibilities and experience than about the complete decision process behind individual designs.

Both portfolios are useful examples, but I would take different things from each one. From Evan's portfolio, I like the simple way projects and experience are organized so a reader can find information quickly. From Tyler's portfolio, I like the amount of technical information included when explaining an actual design. For my own portfolio, I want to combine those two ideas by keeping the navigation simple while including the assumptions, calculations, alternatives, design decisions, and results needed for someone else to follow my work.

Task B:  Product Analysis
Product: Carabiner-Style Clasp Clip
a. What is the primary function of this product?
The primary function of this carabiner-style clasp is to provide a removable mechanical connection between an attached item and a loop, ring, or other support. The rigid body surrounds the attached item while the spring-loaded gate closes the opening to prevent the item from coming out during normal use. The gate can be pushed inward by the user to temporarily open the connection, allowing an item to be attached or removed without taking the clasp apart.
b.  Identify the governing model

For the primary load-carrying behavior of the clasp, I am using the average normal stress relationship:

σ = F/A

where:

- σ = average normal stress in the load-carrying section of the clasp
- F = tensile force carried by the clasp from the attached item
- A = cross-sectional area of the rigid body where the load is transmitted

This model relates the force carried by the clasp to the area of the material carrying that force. For the same applied force, a smaller cross-sectional area produces a higher average stress, while a larger cross-sectional area produces a lower average stress.

The clasp can also be treated as being in static equilibrium when it is holding a stationary load:

ΣF = 0

# i. Model and Variables

The main equation is:

σ = F/A

The variables are the applied tensile force F, the load-carrying cross-sectional area A, and the resulting average normal stress σ.

# ii. Assumption

I am assuming that the clasp is carrying a static tensile load and that the section being analyzed can be approximated as a uniform load-carrying cross section. This allows σ = F/A to be used as a simplified average-stress model. The actual stress will not be perfectly uniform, especially near the curved sections and gate connections.

c.Take photographs of each component
Main Body / Frame

<img width="950" height="650" alt="image" src="https://github.com/user-attachments/assets/467393f4-ff2f-46fd-9faf-e4f03a28fffd" />

The main body is a continuous curved metal frame that forms the main load-carrying part of the clasp. Its curved and elongated shape creates an opening for attaching an object while keeping material around the perimeter to carry the applied force. The rounded sections also avoid sharp changes in geometry where stress could become concentrated. The overall shape allows the force to be transferred through the metal frame rather than through the gate alone.

Spring-Loaded Gate

<img width="358" height="890" alt="image" src="https://github.com/user-attachments/assets/6ae0d6d4-5be4-4f2d-b195-711427db2dfc" />

The silver gate closes the opening in the main body. Its cylindrical shape allows it to move inward when a force is applied by the user and return toward the closed position after the force is removed. When closed, the gate blocks the opening and prevents an attached item from passing through the clasp. The gate is positioned along one side of the frame so the user can open the clasp without permanently deforming the main body.

Gate in the Open Position

<img width="730" height="589" alt="image" src="https://github.com/user-attachments/assets/c4501163-2cb8-4d17-ac91-91350f6bf441" />

When the gate is pushed inward, the opening in the frame becomes accessible. This geometry allows an object to be inserted into or removed from the clasp. The ends of the green frame and the gate are shaped so that the gate can move away from the frame during opening and return across the opening during closing. This provides the clasp with a reusable opening mechanism without permanently deforming the main frame.

Overall Clasp Geometry

<img width="1038" height="895" alt="image" src="https://github.com/user-attachments/assets/7dbcfe26-4e61-40c4-9993-012e8bcd8603" />

The overall geometry combines a rigid curved frame with a movable gate. The elongated shape provides a relatively large opening while maintaining a continuous load-carrying path around the outside. The gate is located on one side of the opening so the clasp can be opened and closed while the main frame remains rigid. This arrangement allows the product to perform its primary function of retaining an attached object while still allowing the object to be removed when the gate is opened.
### d. Patent Research

For the patent research, I found U.S. Patent US8234761B2, titled "Wire-gate carabiner." The patent lists Peter T. Gompert, Jacob Hall, Paul Terry, Benjamin Walker, and Bill Belcourt as the inventors. The patent describes a carabiner as a mechanical coupling device made around a frame and gate. The gate can move to create an opening and then return toward the closed position to retain an attached object. The patent is relevant to my product because my clasp uses the same basic mechanical concept of a rigid frame with a movable gate that creates a temporary opening. I am using this patent as a reference for the mechanism rather than claiming that this exact promotional clasp was manufactured under this patent.
### i. Alternative Solutions

A snap hook is an alternative because it uses a hook-shaped body and a movable closing member to retain an attached item.

A split ring is another alternative because it uses a continuous metal ring with overlapping coils. An item can be inserted between the coils and retained by the spring-like geometry of the ring. Unlike the clasp, it does not use a separate movable gate.
### ii. Design Decision

One design decision I noticed is the use of a separate movable gate instead of making the clasp completely closed. The gate creates a temporary opening while allowing the main frame to remain rigid. I think the designer chose this arrangement because the clasp needs to retain an attached item during use but also allow the user to attach or remove the item without permanently deforming the frame. The gate is placed along one side of the frame, which leaves most of the frame as a continuous load-carrying path while still providing an opening that can be operated by hand.

## Decide


## Communicate
About Me Joshua Malonda

I am a Mechanical Engineering student at the University of North Carolina at Charlotte. I chose mechanical engineering because I enjoy understanding how things work and figuring out how to make them work better. Through my classes, projects, research, and other engineering experiences, I have been able to work with mechanical design, CAD, computational tools, and hands-on systems. During my NSF REU research experience, I worked with Python, Linux, Git, and high-performance computing to help investigate materials and accelerate materials discovery. I have also worked on mechanical design projects involving CAD modeling, mechanisms, transportation systems, and designing within size, cost, and material constraints. These experiences have shown me that engineering is not just about getting an answer, but understanding why a solution works and whether it is actually the best option. As I continue through mechanical engineering, I am becoming an engineer who wants to combine analysis, design, and practical problem-solving. I also want to become better at communicating my reasoning so that other engineers can understand how I reached a decision and evaluate it for themselves. My goal is to continue building the technical and communication skills needed to contribute to real engineering projects and work effectively with other engineers.

To me, defending an engineering decision means being able to explain why I chose one solution over another and support that choice with engineering requirements, calculations, physical principles, testing, or other evidence. It is more than saying that something works or that I like one design better. I should be able to explain what requirements I considered, what alternatives were available, and why the final choice makes the most sense. At this point in my engineering education, I understand what it means to defend a decision, but I am still learning how to do it well. I can use calculations and engineering principles to support my work, but I need more experience clearly documenting my reasoning and comparing different solutions based on specific criteria. I think this is an important skill for me to develop because an engineer needs to be able to explain and stand behind their decisions, especially when working with other engineers or making decisions that affect a final design.

I spent approximately 6–8 hours over the course of two days working on this assignment, including reviewing the requirements, analyzing the product, researching supporting information, documenting my decisions, and developing my portfolio content.
