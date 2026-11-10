# A9 – Pulleys

## Objective

The objective of this assignment was to design a pulley system that transfers mechanical power between two parallel shafts. The design includes two 3-inch pulleys, a polyurethane round belt, hardened steel shafts, sintered-bronze journal bearings, and an aluminum supporting frame.

The design was evaluated using static equilibrium, belt friction, normal stress, torsional stress, bending stress, bearing PV ratings, and structural analysis.

The required minimum safety factor was 3.

## Design Requirements

| Parameter | Requirement | Selected Value |
|---|---|---|
| Pulley diameter | 3 in each | 3 in |
| Center distance | 4–6 in | 5 in nominal |
| Operating speed | 1000–2000 rpm | 1500 rpm |
| Static belt tension | 4–6 lbf | 5 lbf |
| Pulley material | Aluminum, ABS, or steel | 6061-T6 aluminum |
| Belt material | Polyurethane | Polyurethane |
| Minimum safety factor | 3 | 3 |

The calculations use a selected 2:1 tight-to-loose belt tension ratio, a preliminary friction coefficient of 0.25, and a symmetric shaft and bearing arrangement.

These are engineering assumptions used to establish a design operating point.

---

## 1. Belt and Pulley Design

### Design Approach

The first objective was to determine the forces acting on the tight and loose sides of the belt while transmitting power.

The static belt tension was selected as 5 lbf. An operating tension ratio of 2:1 was then assumed to determine the individual belt forces.

The difference between the tight-side and loose-side tensions determines transmitted torque. Their sum determines the resultant transverse force acting on each pulley.

The belt material was modeled as polyurethane rubber, with an assignment-specified yield strength of 471 psi at 20% strain.

Using a minimum safety factor of 3, the allowable stress was calculated, followed by the minimum cross-sectional area and diameter of the round belt.

### Knowns, Unknowns, and FBD

![Figure 1 - Belt and Pulley FBD](images/Belt1.jpg)

*Figure 1. Known parameters, unknown variables, and free-body diagram showing belt tensions, pulley reactions, and geometric constraints.*

### Symbolic Calculations

![Figure 2 - Belt Symbolic Derivations](images/Belt2.jpg)

*Figure 2. Symbolic derivations for tight-side tension, loose-side tension, transmitted torque, allowable belt stress, minimum area, and round-belt diameter.*

### Numerical Calculations

![Figure 3 - Belt Numerical Results](images/Belt3.jpg)

*Figure 3. Numerical calculations for belt forces, torque, cross-sectional area, minimum diameter, and the selected belt size.*

The calculated minimum belt area was approximately 0.04246 in².

A 0.250-inch-diameter polyurethane round belt was selected because its actual cross-sectional area of 0.04909 in² exceeds this minimum.

The calculated normal stress was approximately 135.8 psi, producing a tensile yield safety factor of 3.47.

### Friction and Belt Length

![Figure 4 - Friction and Belt Length](images/Belt4.jpg)

*Figure 4. Belt friction criterion, pulley wrap angle, circumference calculations, and preliminary belt elongation analysis.*

The capstan equation was used to evaluate the required friction capacity.

The minimum effective friction coefficient for the assumed 2:1 tension ratio was 0.221.

Using an assumed friction coefficient of 0.25 produces an idealized maximum tension ratio of approximately 2.19.

Because the selected ratio is 2.00, the arrangement satisfies the friction criterion under this assumption. Actual friction conditions must be confirmed before declaring the drive slip-free.

The installed outer circumference was calculated as approximately 20.210 inches, assuming a 3-inch effective belt pitch diameter.

A preliminary unloaded belt circumference of 19.5 inches was considered to develop the required pretension. The final unloaded length depends on actual belt stiffness and center-distance adjustment.

### Belt Selection

**Selected candidate:** McMaster-Carr polyurethane round belt.

- Nominal cross-sectional diameter: 1/4 in
- Material: Polyurethane rubber
- Catalog family: 3044K606
- Preliminary unloaded circumference: 19.5 in

[McMaster-Carr Round Belts](https://www.mcmaster.com/products/round-belts/round-belts-8/)

The selected belt diameter exceeds the calculated minimum requirement, and the preliminary length is within the available product family's circumference range.

---

## 2. Shaft Design

### Design Approach

The second objective was to determine the minimum shaft diameter needed to transmit torque while resisting deformation and yielding.

Hardened AISI 1060 steel was selected for the shafts.

A representative yield strength of 75,100 psi was used for the specified quenched-and-tempered material condition.

The shaft analysis began with pure torsion and was extended to combined bending and torsion.

The belt exerts a resultant transverse force of 10 lbf on each pulley. With two symmetrically positioned bearings, this produces a 5 lbf reaction at each bearing.

### Knowns, Unknowns, and FBD

![Figure 5 - Shaft FBD](images/Belt5.jpg)

*Figure 5. Shaft design parameters and free-body diagram showing the applied belt load, two bearing reactions, and support spacing.*

### Symbolic Torsion Analysis

![Figure 6 - Shaft Symbolic Derivation](images/Belt6.jpg)

*Figure 6. Polar moment of inertia, torsional stress relationship, allowable shear stress, and symbolic minimum shaft diameter.*

The solid circular shaft was analyzed using the polar moment of inertia and maximum torsional shear stress.

A von Mises yield criterion was applied to determine the minimum shaft diameter for the required safety factor.

### Numerical and Combined-Stress Analysis

![Figure 7 - Shaft Numerical Analysis](images/Belt7.jpg)

*Figure 7. Numerical shaft sizing, maximum bending moment, combined-stress calculations, and actual safety-factor verification.*

The torsion-only minimum shaft diameter was approximately 0.1208 inches.

The combined bending and torsion analysis increased the calculated minimum diameter to approximately 0.1326 inches.

A nominal shaft diameter of 0.250 inches was selected.

The analysis used the reduced bearing-journal diameter of approximately 0.2464 inches for a conservative stress comparison.

The resulting von Mises stress was approximately 3,900 psi, giving a yield safety factor of 19.25.

This satisfies the specified safety-factor requirement under the idealized loading assumptions.

Additional manufacturing details such as keyways, shoulders, retaining grooves, and stress concentrations would require further evaluation.

---

## 3. Journal Bearing Design

### Design Approach

The journal bearings were designed to support shaft rotation while carrying the radial forces produced by belt tension.

Four sleeve bearings were proposed, with two bearings supporting each shaft.

Oil-impregnated sintered bronze was selected because the porous metal structure retains lubricant and provides a compact bearing solution.

The bearing design was evaluated using three operating parameters:

1. Projected bearing pressure
2. Shaft surface velocity
3. Pressure-velocity (PV) rating

Material selection was based on the operating limits listed in *Machinery's Handbook*, 31st Edition, page 2440, Table 4, "Application Limits — Sintered Metal and Nonmetallic Bearings."

### Knowns, Unknowns, and FBD

![Figure 8 - Journal Bearing FBD](images/Belt8.jpg)

*Figure 8. Journal bearing knowns, unknowns, radial bearing reaction, shaft loading, and sleeve-bearing geometry.*

### Symbolic and Numerical Calculations

![Figure 9 - Journal Bearing Calculations](images/Belt9.jpg)

*Figure 9. Symbolic pressure, velocity, and PV equations, followed by numerical calculations and minimum bearing-length derivation.*

The calculated bearing operating parameters were:

- Projected pressure: 36.08 psi
- Shaft surface velocity: 96.76 ft/min
- PV rating: 3,491 psi·ft/min

The projected bearing area was determined from journal diameter multiplied by bearing length.

The calculated operating values were compared with the bearing manufacturer's allowable pressure, speed, and PV ratings.

### Bearing Material Selection

![Figure 10 - Bearing Material Verification](images/Belt10.jpg)

*Figure 10. Sintered-bronze bearing limits, conservative continuous-use PV comparison, actual PV safety margin, and selected bearing length.*

**Selected bearing:** Oilite AA304-05.

| Property | Value |
|---|---:|
| Material | Oil-impregnated sintered bronze |
| Nominal inside diameter | 0.250 in |
| Nominal outside diameter | 0.375 in |
| Bearing length | 0.5625 in |
| Maximum pressure | 2000 psi |
| Maximum surface velocity | 1200 ft/min |
| Maximum PV | 50,000 psi·ft/min |

[Oilite AA304-05 Specifications](https://oilite.com/product/AA304-05)

A conservative continuous-operation PV guideline of 20,000 psi·ft/min was used for the design comparison.

The calculated PV margin was 5.73, exceeding the required factor of 3.

The required minimum bearing length was approximately 0.2945 inches.

The selected length of 0.5625 inches exceeds the calculated requirement.

The PV margin represents an operating design margin rather than a conventional material yield safety factor.

---

## 4. Frame Design and Engineering Analysis

### Frame Concept

The final section involved designing a structural frame capable of supporting the two parallel shafts while maintaining their center distance and alignment.

A two-plate aluminum frame was proposed, consistent with the general arrangement shown in the assignment's Appendix A.

6061-T6 aluminum was selected for the frame because of its machinability, relatively low density, and structural stiffness.

The frame uses the following preliminary dimensions:

| Parameter | Value |
|---|---:|
| Overall plate length | 6.50 in |
| Width | 1.25 in |
| Thickness | 0.5625 in |
| Nominal shaft center distance | 5.00 in |
| Nominal bearing opening | 0.375 in |
| Material yield strength | 40,000 psi |
| Elastic modulus | 10 × 10⁶ psi |

### Frame FBD

![Figure 11 - Frame Design FBD](images/Belt11.jpg)

*Figure 11. Frame geometry, structural material properties, and opposing compressive loads produced by the shaft-bearing reactions.*

The frame was modeled as a member subjected to axial compression.

Under the symmetric loading assumption, each plate carries equal and opposing 5 lbf forces directed toward the center of the pulley system.

### Frame Structural Analysis

![Figure 12 - Frame Structural Calculations](images/Belt12.jpg)

*Figure 12. Net cross-sectional area, axial compressive stress, yield safety factor, second moment of area, Euler buckling estimate, and axial deformation.*

The resulting calculations gave:

- Net cross-sectional area: 0.4922 in²
- Axial compressive stress: 10.16 psi
- Nominal compressive yield safety factor: approximately 3,938
- Idealized Euler critical load estimate: approximately 73,191 lbf
- Axial deformation: approximately 5.08 × 10⁻⁶ in

The calculated axial stress is substantially below the selected aluminum yield strength.

The Euler critical load is retained as an analytical estimate. Since the member is relatively stocky and the elastic Euler estimate exceeds the material-yield threshold, that value should not be interpreted as a verified physical buckling capacity.

The frame requires appropriately dimensioned bearing fits and adjustable mounting provisions for belt pretension.

Additional manufacturing analysis would be required for bearing-seat stresses, fastening, motor torque reaction, and full-assembly alignment.

---

## 5. Design Refinements and Engineering Observations

The design process required several analytical refinements.

Initially, belt tension was considered as a prescribed stationary force. During the operating analysis, the tight-side and loose-side tensions were separated to determine transmitted torque and resultant shaft loading.

A friction verification was then included to determine whether the proposed tension ratio could operate without slipping. This identified the importance of pulley surface conditions and groove geometry.

For the shaft, the torsion-only diameter was supplemented with a combined bending-and-torsion analysis because the belt also exerts a transverse load.

For the bearings, pressure and velocity were evaluated independently before combining them into a PV rating. A conservative continuous-use PV guideline was also used.

The frame analysis included compression, deformation, and an idealized buckling calculation. The interpretation of the buckling result requires consideration of the applicability of Euler's equation.

These refinements clarified how the operating assumptions affect component selection. No physical prototype testing was performed or documented.

---

## 6. Engineering Lessons Learned

This assignment demonstrated how individual mechanical components interact in a belt-driven power transmission system.

One important distinction was the relationship between belt tension and transmitted torque. The difference between the tight-side and loose-side tensions determines torque, while the sum of those forces contributes to the transverse loading of the pulley shaft. This distinction affects both power transmission and structural design.

I also learned how torsional loading and bending loading must be considered together when designing rotating shafts. Calculating the minimum diameter using torsion alone did not fully represent the shaft's operating condition. Applying the von Mises criterion provided a combined-stress evaluation.

The journal-bearing analysis demonstrated the significance of the PV rating. The bearing's suitability depends not only on its radial loading capacity but also on the relative sliding velocity between the shaft and bearing surface. These operating parameters influence frictional heating and lubrication requirements.

Finally, the frame analysis emphasized the importance of identifying a load path before selecting structural equations. The calculated axial stresses were small for the proposed geometry, but maintaining shaft alignment, specifying bearing fits, and providing adequate mounting support remain necessary aspects of a complete mechanical design.

---

## 7. Time Documentation

| Activity | Time | Description |
|---|---:|---|
| Handwritten calculations | 4.5 hours | FBDs, symbolic derivations, numerical calculations, belt sizing, shaft analysis, bearings, and frame |
| Assignment documentation | 1.5 hours | Organizing photographs, written explanations, references, and design summary |
| **Total time** | **6 hours** | **Assignment 8 completion** |

---

## 8. Final Design Summary

| Design Component | Final Selection | Calculated Result |
|---|---|---|
| Pulley diameter | 3 in | Equal pulleys |
| Nominal center spacing | 5 in | Within 4–6 in |
| Operating speed | 1500 rpm | Within 1000–2000 rpm |
| Static belt tension | 5 lbf | Within 4–6 lbf |
| Tight-side tension | Assumed 2:1 ratio | 6.667 lbf |
| Loose-side tension | Assumed 2:1 ratio | 3.333 lbf |
| Belt diameter | 0.250 in | FS = 3.47 |
| Transmitted torque | Ideal operating point | 5.00 lbf·in |
| Transmitted power | Excluding losses | 0.119 hp |
| Shaft diameter | 0.250 in nominal | Combined FS = 19.25 |
| Journal bearing | Oilite AA304-05 | PV = 3491 |
| Bearing length | 0.5625 in | PV margin = 5.73 |
| Frame | 6061-T6 aluminum | Axial yield FS ≈ 3938 |

The proposed design meets the calculated strength and operating-margin requirements under the stated assumptions. Actual belt friction, belt stiffness, heat-treatment properties, and assembly details require verification before manufacturing.

---

## References

1. **Machinery's Handbook, 31st Edition.** Industrial Press, 2020. Page 217, Table 2, *Table of Simple Stresses*. Page 2440, Table 4, *Application Limits — Sintered Metal and Nonmetallic Bearings*.  
   [Simple Stresses](https://online.flippingbook.com/view/954192180/228/)  
   [Journal Bearing Materials](https://online.flippingbook.com/view/954046886/1103/)

2. **D. J. Dunn.** *Solid Mechanics — Dynamics: Tutorial — Pulley Drive Systems*. Assigned reading.

3. **McMaster-Carr.** *Polyurethane Rubber Round Belts*. Catalog family 3044K606.  
   [Product Reference](https://www.mcmaster.com/products/round-belts/round-belts-8/)

4. **Oilite.** *AA304-05 Oil-Impregnated Bronze Sleeve Bearing*. Manufacturer dimensions and operating limits.  
   [Product Specifications](https://oilite.com/product/AA304-05)

5. **SDP/SI.** *An Introduction to Porous Metallic Bearings*. PV limits and continuous-operation guidelines.  
   [Bearing Design Reference](https://sdp-si.com/Design-Data/Porous-Metal-Bearings.php)

6. **MatWeb.** *AISI 1060 Steel, Oil Quenched and Tempered*. Shaft material properties.  
   [Material Data](https://www.matweb.com/search/DataSheet.aspx?MatGUID=81cbba576fcc4bb0ab3fbecb47edcd6e)

7. **ASM / MatWeb.** *Aluminum 6061-T6*. Aluminum material properties.  
   [Material Data](https://asm.matweb.com/search/specificmaterial.asp?bassnum=ma6061t6)

8. **Wang et al.** *Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers*. Polymer, 163, 2019, pp. 154–161. The assignment-specified 471 psi belt strength was used for the analysis.  
   [Research Article](https://doi.org/10.1016/j.polymer.2018.12.062)

---
