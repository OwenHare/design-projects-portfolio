# A10 – Lead Screw Translating System

## Lead screw design - Cooper R
Our goal is to design and build a mechanically driven tensile tester capable of applying up to 2 kN axial tensile load with a controllable crosshead speed from 1 to 50 mm/min. This is to be done with 2 screws that are at minimum 18 inches long. All calculations must use a safety factor of 4. To design the lead screw I first needed to find diameter. I compiled knowns and unknowns, drew an FBD and solved algebraically and numerically to get a diameter of .38 inches.


<img width="601" height="690" alt="image" src="https://github.com/user-attachments/assets/758ca33d-0152-41e9-a00a-7f78156a0bb4" />

I repeated this process twice for the rotational speed and torque and got a range of .032 - 1.59 rpm and 5908 Nmm respectively.


<img width="376" height="500" alt="image" src="https://github.com/user-attachments/assets/5c7bcae4-fdc1-427b-a7c5-6964d2355347" />

This lead me to select a 5/8 -8 Carbon steel lead screw, part number 989335A914, as the desired screw choice.

<img width="1529" height="806" alt="image" src="https://github.com/user-attachments/assets/25e23bce-16c2-4f05-9ca1-74aed89eae7a" />

Details below https://www.mcmaster.com/98935A914/
## Selecting nut and flange - Bobby D
The lead Screw was chosen to be 5/8 -8 Carbon steel lead screw with the part number 989335A914. For the nut, it would require the corresponding nut with the same specifications; the material is already chosen to be bronze, with all further testing to ensure that the given thread size for the bolt won’t fail under the given load. The image below shows the part on McMaster-Carr where the design specifications are given along with the 3D part model. The Thread type is Acme; the inner diameter to the base of the threads is 5/8 in (0.625 in); the total height is 1.25 in; the pitch is 0.125 in; the thread height is half the pitch; and the other measurements are unnecessary for the current calculations.
Here is the link to the website below: https://www.mcmaster.com/products/acme-lead-screws/nut-type~externally-threaded/nut-type~flange/material~bronze-1/material~932-bearing-bronze/thread-size~5-8-8/

<img width="612" height="370" alt="image" src="https://github.com/user-attachments/assets/784afa12-e997-4bbd-a685-28d1082c689c" />


On the website above, the Yield strength, a necessary upper limit to know, was not given and therefore had to be found on an alternative website. Also important to note as stated on the website above, there are two different types of bronze metals. Doing a little research at concast.com, 932 would function better, as it is the workhorse of industry. While 673 has better stress resistance, 932 self-lubricates, which is important when running up and down the leadscrew, reducing wear. The Yield strength for this specific alloy is 20 ksi.
The link to the PDF below is given here: https://morganbronze.com/wp-content/uploads/c932_bearing_bronze.pdf



<img width="468" height="310" alt="image" src="https://github.com/user-attachments/assets/981c07ce-6562-43dd-ac7e-01813abe2348" />







The given Knowns are a safety factor of 4, an allowed stress limit of 20 psi, and a pitch of 0.125 in; the object itself and material is a 5/8 – 8 932 bronze lead screw nut; the force is ½ the given load, and the given load for the assembly as a whole is 2kN. However, all the measurements are already in the US Customary System, so 2kN was converted to 449.62 lbf. The unknown value is a ratio; rather, to ensure that the stress experienced by the nut didn’t exceed the given material, the stress of the bearing nut multiplied by the safety factor, over the allowable stress, has to be less than 1. Using the given equations, the real stress was calculated to 2747.86 lbf*in, well within the stress allow.



<img width="454" height="576" alt="image" src="https://github.com/user-attachments/assets/93e65ac2-a118-42a8-9a37-b12fcc67e234" />


## Designing crosshead- Bobby D

In this section, we are tasked with designing a crosshead using simple beam design to calculate the necessary dimensions using the stress and vertical deflection equations. The total load is the same, and Aluminum was chosen as the material because it’s relatively easy to mill and affordable.
The first crosshead dimensional design is based on stress analysis; the base is 1.65 inches, as the diameter of the nut flange is 1.5, and this leaves 75 thou of clearance on either side. As for the length, none of the previous calculations answered, so the length was decided to be half the length of the Lead screws on either side, or 12 inches. The load multiplied by the safety factor is force P, and the height is the dimension being solved for. And additional documents were used in order to find the Yield strength of aluminum, which is 40 ksi and is listed below.
 For the stress equation, the height was derived to be 1.4 inches.


<img width="458" height="614" alt="image" src="https://github.com/user-attachments/assets/a36d0b07-dba1-480b-8a60-7011dbb9f36c" />




The second crosshead design is based on the max deflection, which is 0.01mm with a modulus of elasticity of 10,000 ksi, found with an outside source listed at the bottom. All other values remain the same. As the max deflection was given in mm, the deflection was converted to the U.S. customary system of measurement. The deflection in inches was 0.003937 in.
The height was derived to be 2.702 in.


<img width="464" height="617" alt="image" src="https://github.com/user-attachments/assets/05010cd6-fbb1-4ea3-96b7-938cfcb761a4" />



Before the design phase, using the Master thesis provided as a reference in the resources section of this assignment, I roughly used this image for a design concept before creating the Multiview drawing.
<img width="360" height="308" alt="image" src="https://github.com/user-attachments/assets/67e467c2-0866-4187-98b5-4dae55825ebc" />


In the instructions, it asks for a Multiview sketch to be generated; however, it doesn’t expressly ask for a 3D model to be created, so instead a handmade design was created on paper. However, it’s missing any tolerance, and any holes are made exactly to the size of the 5/8 - 8 nut. All important measurements are included, and front, side, and top views are included along with an orthogonal view, along with units and the Part name. It’s a simple beam with an extra 1.5-inch section at the top to possibly create an insert, depending on the nature of the next assignment. The curved edges are to reduce stress, as was the case in the Bracket design in a previous assignment. The height chosen was based on the vertical deflection, as it met both stress and deflection requirements.
 
<img width="418" height="538" alt="image" src="https://github.com/user-attachments/assets/141c153e-a2f6-44f9-b7ba-a75f0db885ca" />

## Assembly- Cooper R
Since the cross head was designed first I needed to pick parts that could accomodate its size. From earlier diagrams I had decided the entire structure was at most 2 ft tall. Additionally the dimensions of Bobby's cross head means that the inner width of the frame must at least be 1 ft wide. I picked the frames accordingly and the rest of the parts fell into place.

<img width="400" height="528" alt="image" src="https://github.com/user-attachments/assets/0ef3502b-410a-4635-8084-3214cf8c6f44" />


## Cost of assembly- Owen S

We researched the costs of commercially available components selected for the tensile tester, including aluminum frame rails, carbon steel Acme lead screws, and 932 bearing bronze flange nuts. All components were selected from McMaster-Carr to ensure compatibility and simplify the assembly process.

The custom-designed aluminum crosshead is excluded from the cost analysis, as instructed by the assignment.

## Tabulating Costs- Owen S

| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
|---|---|---|---|---|---|
| 1 | 2 | Aluminum Frame Rail (4601N78) | $18.72 | $37.44 | [McMaster-Carr](https://www.mcmaster.com/4601N78) |
| 2 | 2 | Aluminum Frame Rail (4601N73) | $12.01 | $24.02 | [McMaster-Carr](https://www.mcmaster.com/4601N73) |
| 3 | 2 | 5/8"-8 Carbon Steel Acme Lead Screw, 24" (98935A914) | $9.79 | $19.58 | [McMaster-Carr](https://www.mcmaster.com/98935A914) |
| 4 | 2 | 5/8"-8 Acme Flange Nut, 932 Bearing Bronze (95120A119) | $138.20 | $276.40 | [McMaster-Carr](https://www.mcmaster.com/95120A119) |
| | | **Total Cost** | | **$357.44** | |

*Prices are preliminary and exclude shipping and taxes. Lead screw and nut prices are based on previously obtained reference values.*

## Cost Analysis- Owen S

The estimated total material cost is **$357.44**. The bronze flange nuts represent the largest expense at $276.40, followed by the frame rails at $61.46 and lead screws at $19.58.

Using standardized components reduces custom manufacturing requirements and provides downloadable CAD models. The custom aluminum crosshead is excluded from the cost estimate.

---

## Lessons Learned- Owen S

Throughout this assignment, we developed a better understanding of how mechanical components must function together to create a tensile tester capable of applying a controlled 2 kN load with a safety factor of 4.

One important lesson involved component compatibility. During the design process, we had to modify the crosshead because its original geometry interfered with a mounting bolt. Although the crosshead satisfied the initial strength and deflection calculations, this issue demonstrated the importance of accounting for mounting hardware and assembly clearances during the design stage.

We also learned how lead screw dimensions affect linear displacement and rotational speed, and how material properties influence the selection of bronze nuts and aluminum structural components. Researching commercially available parts reinforced the importance of balancing cost, manufacturability, and mechanical performance.

Overall, this assignment demonstrated that mechanical design is an iterative process requiring calculations, component selection, dimensional verification, and revisions to ensure the completed assembly functions as intended.

## Team Contributions and Time Spent- Owen S

**Total Time Spent: 6 Hours**

The assignment was completed over approximately 6 hours, with responsibilities divided among three team members.

| Team Member | Contribution |
|---|---|
| Cooper Radtke | Designed the lead screw system, including diameter, rotational speed, and torque calculations. |
| Bobby Douglas | Designed the crosshead, performed strength and deflection calculations, and selected the bronze nut and flange. |
| Owen Switzer | Tabulated component costs, verified part specifications, and performed quality control of the documentation and selected components. |

Throughout the assignment, we collaborated to ensure that the selected components met the design requirements and that the calculations, drawings, and documentation were consistent.

Assembly download [Frame assem (2) (1).zip](https://github.com/user-attachments/files/34953287/Frame.assem.2.1.zip)

Crosshead dowload[crosshead.prt.zip](https://github.com/user-attachments/files/34953309/crosshead.prt.zip)

McMaster parts list download [95120A119_932 Bearing Bronze Acme Flange Nut.zip](https://github.com/user-attachments/files/34953515/95120A119_932.Bearing.Bronze.Acme.Flange.Nut.zip)
