```markdown
# Bracket FEA

## Objective

The purpose of this assignment was to use finite element analysis to evaluate and improve the bracket developed in the previous assignments. I used the FEA results to compare three separate designs based on maximum von Mises stress, maximum displacement, safety factor, and mass.

The same ASTM A36 steel material and a 1000 lbf downward load were maintained throughout all three designs so that the effect of each geometric change could be compared directly.

The original bracket was used as Design I.

![Original Bracket Geometry](A7_1.PNG)

## FEA Setup

The bracket was inserted into an Onshape assembly and a linear static simulation was created. A total downward force of 1000 lbf was applied to the cylindrical strap-support feature.

![FEA Load Setup](A7_2.PNG)

Since the bracket was being analyzed as a standalone component in Onshape, inertial relief was enabled during the simulations. The same loading and simulation setup was maintained for all three designs.

## Mesh Validation

Onshape Simulation uses an automatically generated adaptive mesh rather than exposing a manual element-size or element-count control. During each simulation, Onshape automatically refined the mesh and returned a green converged status.

Because Onshape does not display the final element count through this simulation workflow, the number of elements could not be directly recorded. The same adaptive meshing procedure was used for all three designs so that the results remained directly comparable.

# Design I

## Design I Geometry

Design I was the original bracket created during the previous strength and stiffness assignments. No geometric modifications were made before the first FEA simulation.

![Design I Geometry](A7_1.PNG)

## Design I Stress

The maximum von Mises stress for Design I was approximately **273,000 psi**. The maximum stress occurred near a junction between the side wall and the horizontal bracket members.

![Design I Stress](A7_3.PNG)

## Design I Safety Factor

The minimum safety factor for Design I was approximately **0.131**.

A safety factor below 1 indicates that the simulated stress exceeded the yield strength of the material under the modeled loading condition.

![Design I Safety Factor](A7_4.PNG)

## Design I Displacement

The maximum displacement for Design I was approximately **0.02343 m**. The greatest displacement occurred near the upper portion of the bracket.

![Design I Displacement](A7_5.PNG)

## Design I Mass

The original bracket had a mass of approximately **1.885 lb**.

![Design I Mass](A7_12.PNG)

# Design II

## Initial Design II Modification

I first experimented with adding fillets around the lower support region. I decided not to use this as the primary Design II modification because I wanted to isolate the effect of one major geometric change at a time.

![Initial Fillet Attempt](A7_6.PNG)

## Design II Geometry Modification

For Design II, I added a rectangular reinforcement plate to the underside of the main bracket housing.

The purpose of the plate was to increase the stiffness of the bottom section of the bracket and distribute the load over a larger structural area.

![Design II Geometry](A7_7.PNG)

## Design II Stress

The maximum von Mises stress decreased to approximately **159,900 psi**.

![Design II Stress](A7_8.PNG)

Compared with Design I, the maximum stress decreased by approximately **41%**.

## Design II Safety Factor

The minimum safety factor increased to approximately **0.224**.

![Design II Safety Factor](A7_9.PNG)

Compared with the original safety factor of 0.131, this was an increase of approximately **71%**.

## Design II Displacement

The maximum displacement decreased to approximately **0.01410 m**.

![Design II Displacement](A7_10.PNG)

This was approximately a **40% reduction in displacement** compared with Design I.

## Design II Mass

The reinforcement plate increased the mass of the bracket to approximately **2.022 lb**.

![Design II Mass](A7_11.PNG)

This represented an increase in mass of approximately **7.3%** compared with Design I.

# Design III

## Design III Geometry Modification

For Design III, I retained the reinforcement from Design II and made additional geometry changes.

Another rectangular baseplate was added using a **0.10 in extrusion**, and **0.10 in fillets** were added around selected transition regions.

The purpose of these changes was to further improve stiffness and reduce stress concentrations by smoothing sharp transitions in the load path.

![Design III Fillet Modification](A7_13.PNG)

Additional fillets were also added around the support and housing transition regions.

![Design III Additional Fillet](A7_14.PNG)

## Design III Stress

The maximum von Mises stress increased to approximately **288,000 psi**.

![Design III Stress](A7_17.PNG)

The maximum stress occurred near the lower side-wall and bottom-member junction.

The additional material therefore did not improve the stress performance compared with Design II.

## Design III Safety Factor

The minimum safety factor decreased to approximately **0.124**.

![Design III Safety Factor](A7_16.PNG)

This was lower than both Design I and Design II.

## Design III Displacement

The maximum displacement increased to approximately **0.02578 m**.

![Design III Displacement](A7_15.PNG)

The displacement was greater than the values obtained for both previous designs.

## Design III Mass

The final Design III mass was approximately **2.053 lb**.

![Design III Mass](A7_14.PNG)

# Design Comparison

| Result | Design I | Design II | Design III |
| --- | ---: | ---: | ---: |
| Maximum Stress | 273,000 psi | 159,900 psi | 288,000 psi |
| Maximum Stress Location | Side-wall/member junction | Upper side-wall/top-member junction | Lower side-wall/bottom-member junction |
| Maximum Displacement | 0.02343 m | 0.01410 m | 0.02578 m |
| Maximum Displacement Location | Upper bracket region | Upper bracket region | Upper bracket region |
| Mass | 1.885 lb | 2.022 lb | 2.053 lb |
| Minimum Safety Factor | 0.131 | 0.224 | 0.124 |
| Number of Elements | Automatic Adaptive Mesh | Automatic Adaptive Mesh | Automatic Adaptive Mesh |

# Final Design Selection

Based on the FEA results, **Design II was the strongest overall design of the three iterations**.

Compared with Design I, Design II:

- Reduced maximum stress from 273,000 psi to 159,900 psi.
- Reduced maximum displacement from 0.02343 m to 0.01410 m.
- Increased minimum safety factor from 0.131 to 0.224.
- Increased mass by only approximately 7.3%.

Design III contained additional material and fillets, but its performance became worse. Maximum stress increased to 288,000 psi, maximum displacement increased to 0.02578 m, and minimum safety factor decreased to 0.124.

This showed that simply adding material does not automatically make a component stronger or stiffer. The location and geometry of the added material can change the load path and create new stress concentrations.

# Mistakes and Adjustments

One adjustment during the design process involved deciding how to modify Design II. I initially experimented with fillets, but decided to use the baseplate as the primary modification so that I could evaluate the effect of one major geometric change independently.

Another important result occurred during Design III. I expected the additional baseplate and fillets to further improve the bracket. Instead, the FEA results showed that the additional changes increased both maximum stress and displacement.

This demonstrated the importance of using FEA results rather than assuming that additional material will improve a design.

# Lessons Learned

This assignment showed how finite element analysis can be used as an iterative design tool rather than only as a final verification method.

The stress plots made it possible to identify high-stress regions in the bracket and then modify the geometry based on those results.

Design II demonstrated that reinforcement in the correct location could significantly reduce both stress and displacement while adding relatively little mass.

Design III demonstrated that more material does not necessarily result in better structural performance. The geometry and location of the reinforcement influence how the load travels through the component.

I also learned that changing one portion of a structure can move the critical stress location to another area. This means that each geometric change needs to be evaluated using another FEA simulation rather than assuming that the change improved the entire component.

Onshape also uses an adaptive mesh during simulation. The mesh is automatically refined during the solution process until convergence is reached. This allowed each design to be evaluated using the same general numerical procedure even though a manual element count was not available.

# Time Spent

I spent approximately **2.5 Hours** completing the FEA simulations, modifying the bracket designs, comparing the results, and compiling the assignment into GitHub.

# CAD Download

[Download Bracket CAD File](https://cad.onshape.com/documents/c7fb525f3044bad3a86923b3/w/4980922cf18a1775be701a4f/e/341c2ebdf7423bd5064df323?renderMode=10&rightPanel=simulationPanel&uiState=6ae0384b0b64e8221b97fec8)

## Sources and AI Policy

*Open AI's ChatGPT was used in the making of this for formatting, and organizational purposes. All models, handwritten equations, and text has been handwritten by myself without the use of AI. Research of terminology was used through Google. Grammatical structure was completed with the assistance of Grammarly.*
```
