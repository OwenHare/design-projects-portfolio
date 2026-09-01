# A2 – Truss Stress Analysis

## Objective

The objective of this assignment was to design and model a lightweight planar truss capable of supporting the prescribed loading while satisfying the required geometric, material, and safety factor constraints. The truss members were designed using A500 structural steel and were required to have identical cross-sectional geometry. The connecting pins were designed separately using hardened tool steel and a single shear failure model. The final design was modeled in Creo so that the predicted CAD weight could be compared with the analytically calculated weight.

The provided geometry uses a = 0.4 m, b = 0.3 m, and an applied load magnitude P = 25 kN. Point A is modeled as a pin support, while point B is modeled as a roller support. The upward load P is applied at point C, and the downward load P is applied at point D.

ORIGINAL DIAGRAM

The original problem diagram establishes the locations of points A, B, C, and D, the direction of the two applied loads, the support conditions, and the dimensions that must remain fixed throughout the design. These requirements provided the geometric limits used when selecting the final member arrangement.


## Analyze

I began the analysis by selecting a truss geometry that connected all four required points while remaining stable and limiting the amount of material required. After selecting the geometry, I calculated the member lengths and angles, determined the support reactions, and used the method of joints to solve the internal force carried by each member. The maximum internal force was then used to size all five members because the assignment requires them to have identical cross-sectional geometry.

[INSERT P1 HERE]

This calculation shows the selected five-member truss consisting of AB, BC, AC, CD, and AD. The required dimensions are shown around the selected geometry, and the stability check verifies that the configuration is statically determinate. This confirmed that the selected arrangement could be used for the remaining structural analysis.

[INSERT P2 HERE]

This calculation determines the lengths and angles of the members from the prescribed horizontal and vertical dimensions. Members BC and AD use the same geometry, while member AC has a different length and angle because it spans a greater horizontal distance. These geometric values were used when resolving member forces during the method of joints.

[INSERT P3 HERE]

This page shows the free body diagram of the entire truss and the calculation of the reactions at supports A and B. The applied loads and unknown support reactions were first considered before any individual joint was analyzed. The resulting reactions were then used as known forces in the following joint calculations.

[INSERT P4 HERE]

This page shows the analysis of Joint B. The known support reaction and the forces in members AB and BC were resolved using equilibrium. The calculation determined that BC is in compression while AB is in tension.

[INSERT P5 HERE]

This page shows the analysis of Joint D. Since the applied load at D was known, the forces carried by members AD and CD could be determined directly. Both members were found to be in tension.

[INSERT P6 HERE]

This page shows the analysis of Joint C after the forces in BC and CD were already known. The remaining unknown force in AC was calculated from equilibrium. Member AC was found to be in compression and carried the largest force magnitude in the truss.

[INSERT P7 HERE]

This page uses Joint A as a final equilibrium check and summarizes the internal forces in all five members. The results confirm that AB, CD, and AD are in tension while BC and AC are in compression. The force summary also identifies AC as the member carrying the greatest internal force.

After determining all of the member forces, the maximum force was used to calculate the minimum required member cross-sectional area. Using the largest member force ensures that every member satisfies the required safety factor even though the remaining members carry smaller loads.

[INSERT P8 HERE]

This calculation uses the largest internal member force, the selected steel yield strength, and the required safety factor to determine the minimum cross-sectional area. The resulting minimum area was approximately 481.6 square millimeters. This value established the minimum geometry that every member needed to maintain.

[INSERT P9 HERE]

This page documents the final member cross-section selection. A 22 mm by 22 mm cross section provides an area of 484 square millimeters, which is slightly greater than the calculated minimum. The resulting actual safety factor was approximately 3.52, which exceeds the required value of 3.5.

The analytical truss weight was then calculated before the pins were added. This calculation provides a simplified prediction that can later be compared with the more detailed Creo mass properties.

[INSERT P10 HERE]

This page combines the lengths of all five members to determine the total nominal truss member length. The selected cross-sectional area and steel density were then used to determine the volume, mass, and weight of the truss. The simplified analytical calculation predicts a truss weight of approximately 128.7 N before the pins are included.

The pins were analyzed separately because the assignment requires a single shear analysis rather than the axial stress model used for the truss members. The loads at each joint were compared first so that the largest load could be used for the identical pin design.

[INSERT P11 HERE]

This page compares the resultant forces associated with joints A, B, C, and D. Joints C and D each carry the largest load of 25 kN, so 25 kN was selected as the governing pin load. The sketch on the right represents the single shear condition used for the pin analysis.

[INSERT P12 HERE]

This calculation uses the governing 25 kN pin load, the specified hardened tool steel shear yield strength, and the required safety factor of 4. The resulting minimum pin area was approximately 85.32 square millimeters, corresponding to a theoretical minimum diameter of approximately 10.42 mm. An 11 mm diameter was selected for the final design.

[INSERT P13 HERE]

This page calculates the weight of the selected pins using an 11 mm diameter, a 22 mm length, and the specified hardened tool steel density. The weight of one pin was calculated first and then multiplied by four because the final design uses four identical pins. The combined pin weight was approximately 0.631 N.

[INSERT P14 HERE]

This page combines the analytical truss weight and the combined pin weight to determine the predicted total weight of the finished structure. The resulting hand calculated weight was approximately 129.33 N, corresponding to a mass of approximately 13.18 kg. Space was also included for the Creo mass and percent difference so the analytical prediction could be compared with the final CAD model.

## Decide
_Which geometry did you select, and why?._

I selected a five-member truss consisting of members AB, BC, AC, CD, and AD. I selected this geometry because it provides a stable and statically determinate structure while using a limited number of members. Using fewer members would reduce weight further, but the structure would no longer provide the required stability. The selected geometry therefore minimizes unnecessary material while satisfying the structural requirements of the assignment.

The analysis showed that member AC carried the largest internal force, so the common member dimensions were selected based on this governing condition. A 22 mm by 22 mm cross section was selected because it slightly exceeds the calculated minimum area while maintaining identical geometry for every member. An 11 mm diameter by 22 mm long pin was selected because it exceeds the calculated minimum pin diameter and matches the thickness of the truss.

The analytical dimensions were then transferred into Creo to create the final CAD design.

[INSERT Cr1 HERE]

The initial Creo sketch reproduces the five-member geometry selected during the analytical portion of the assignment. The primary horizontal and vertical dimensions were entered first so that the CAD joint locations matched the geometry used during the hand calculations.

[INSERT DUPLICATE OF Cr1 HERE IF YOU WANT TO USE BOTH]

This screenshot shows the same initial geometry from the CAD development process and provides additional evidence that the original analytical dimensions were entered before the members were given physical width.

[INSERT Cr2 HERE]

Additional constraints were added to verify the member geometry before the physical member profiles were created. The diagonal member dimensions were checked against the values obtained during the analytical geometry calculations so that later CAD operations would not change the joint locations.

[INSERT DUPLICATE OF Cr2 HERE IF USING IT]

This screenshot provides another view of the constrained analytical geometry. It shows the same five-member arrangement before the cross-sectional dimensions and joint regions were added.

[INSERT Cr3 HERE]

The centerline geometry was then used to construct the physical member boundaries. Parallel sketch geometry was created around each original member line so that all five members could maintain the selected 22 mm width.

[INSERT DUPLICATE OF Cr3 HERE IF USING IT]

This screenshot shows the member-width construction at another point in the sketch development. The original analytical member locations remain visible while the additional parallel geometry defines the material that will form the actual truss.

[INSERT Cr4 HERE]

Circular regions with a diameter of approximately 36 mm were added at joints A, B, C, and D. These enlarged regions provide additional material surrounding the pin holes and allow the members meeting at each joint to form a continuous part.

[INSERT DUPLICATE OF Cr4 HERE IF USING IT]

This screenshot provides another view of the four enlarged joint regions after they were dimensioned. The joint circles are centered on the same locations established by the original analytical geometry.

[INSERT Cr5 HERE]

The member boundaries and circular joint regions were then combined into the completed two-dimensional truss profile. The screenshot shows the final 22 mm member widths, enlarged joint regions, and the 11 mm hole dimensions incorporated into the sketch before the truss was converted into a solid.

[INSERT DUPLICATE OF Cr5 HERE IF USING IT]

This screenshot documents the same completed sketch geometry immediately before extrusion. It provides additional evidence that the final two-dimensional profile contains all five members as one continuous truss shape.

[INSERT Cr6 HERE]

The completed sketch was extruded to a thickness of 22 mm. This converted the two-dimensional profile into the three-dimensional truss while maintaining the selected 22 mm by 22 mm cross section along the straight portions of the members.

[INSERT DUPLICATE OF Cr6 HERE IF USING IT]

This screenshot provides another view of the extrusion operation and shows the three-dimensional form produced from the final sketch. The 22 mm extrusion depth matches the selected truss thickness used during the analytical design.

[INSERT Cr7 HERE]

The completed truss part is shown after creating the four 11 mm pin holes. Each hole was located at one of the four original joint centers so that the pin locations remained consistent with the analytical geometry. At this stage, the truss exists as one continuous CAD part as required by the assignment.

[INSERT Cr8 HERE]

The steel material properties were assigned to the completed truss part. The material density was set to represent the steel used during the analytical weight calculation so that the Creo mass properties could later provide a meaningful comparison with the hand calculated result.

[INSERT Cr9 HERE]

A separate pin part was created using the dimensions selected from the pin analysis. The pin was modeled as an 11 mm diameter cylinder with a length of 22 mm. The 22 mm length matches the thickness of the truss, while the 11 mm diameter exceeds the calculated minimum required diameter.

[INSERT Cr10 HERE]

The truss and pin components were then placed into a Creo assembly. This screenshot shows the pin being positioned within one of the 11 mm joint holes. The same separately modeled pin component was used at each joint because the assignment requires all pins to have identical geometry.

[INSERT Cr11 HERE]

The final assembly shows the complete truss with four identical pins installed at joints A, B, C, and D. The truss remains one CAD part while the same pin part appears four times in the assembly. This completed assembly represents the final CAD implementation of the analytical design.

[INSERT CREO MASS PROPERTIES SCREENSHOT HERE WHEN COMPLETED]

The completed CAD model was evaluated using Creo mass properties to determine its predicted mass and weight. This result can be compared with the hand calculated mass of approximately 13.18 kg. Any difference between the two values is expected because the analytical calculation simplifies the member geometry, while Creo includes the enlarged joint regions, removed pin-hole material, and exact pin geometry.

## Communicate

This assignment demonstrated that the geometry of a truss must be established before the member dimensions can be selected because the geometry determines how the external loads are distributed throughout the structure. The method of joints allowed the force in each member to be determined, and the member carrying the greatest force was then used to size every member according to the required safety factor.

I also learned that different components of the same structure may require different stress models. The truss members were evaluated using axial loading, while the connecting pins were evaluated using single shear. The pin design therefore required a separate material property, safety factor, and minimum area calculation from the calculations used for the truss members.

Finally, translating the analytical design into Creo showed that a simplified structural calculation does not represent every detail of the final geometry. The pin holes remove material from the joints, while the enlarged circular joint regions add material that is not included in the simplified member-length weight calculation. Comparing the hand calculated weight with the Creo mass properties provides a way to evaluate how closely the analytical model predicts the final physical design.

I spent approximately 7 hours completing this assignment, including the structural analysis, member and pin sizing, weight calculations, CAD modeling, material assignment, and final assembly in Creo. A significant portion of this time was spent refining the CAD geometry to maintain the required member cross-sectional area around the pin joints and ensuring the final model accurately represented the analytical design.
