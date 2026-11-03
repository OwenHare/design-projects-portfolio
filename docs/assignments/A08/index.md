
# MEGR 2156 – Gearbox Design and Shaft Analysis

> **Portfolio Documentation Disclaimer:** I used external engineering tools, Onshape, and extensive AI-assisted formatting to organize and present this assignment. All original engineering calculations were performed by hand. AI was used to restructure the writing, organize tables and equations, and improve documentation quality; it was not used as a replacement for my engineering work. I intend to feature this gearbox as a staple project in my portfolio, hence the quality of structuring.

**Course:** MEGR 2156 – Design Projects Lab I  
**Project:** Gearbox Design  
**CAD Platform:** Onshape  
**Design Record Updated:** November 3, 2026

The final two-piece housing was reconstructed with native Onshape features. The previously imported assembly remains useful for illustrating the gearbox concept, but its STEP components do not preserve native feature history. The modeled graphite-lubricated sleeve bearings still require confirmation of their operating limits at the specified shaft speeds.

---

## 1. Requirements and Design Parameters

The gearbox was designed around an 18-tooth input pinion and a 48-tooth output gear. The required reduction is **24:9**, which is equivalent to the selected tooth ratio of **48:18**.

| Parameter | Input Shaft / Pinion | Output Shaft / Gear |
|---|---|---|
| Gear part number | McMaster 7880K19 | McMaster 7880K24 |
| Number of teeth | 18 | 48 |
| Diametral pitch | 48 | 48 |
| Pressure angle | 20° | 20° |
| Pitch diameter | 0.375 in | 1.000 in |
| Outside diameter | 0.420 in | 1.040 in |
| Shaft diameter × length | 0.125 × 1.000 in | 0.250 × 1.000 in |
| Rotational speed | 2,933.33 rpm | 1,100 rpm |
| Transmitted torque | 0.46875 in·lbf | 1.25 in·lbf |

### Gear Ratio and Center Distance

The tooth ratio is:

$$
\frac{N_{out}}{N_{in}}=\frac{48}{18}=\frac{24}{9}=2.6667
$$

Assuming ideal power transmission:

$$
n_{in}=1100\left(\frac{48}{18}\right)=\boxed{2933.33\ \text{rpm}}
$$

$$
T_{in}=1.25\left(\frac{18}{48}\right)=\boxed{0.46875\ \text{in·lbf}}
$$

The gear shaft center distance is calculated using the two pitch diameters:

$$
C=\frac{D_{p,in}+D_{p,out}}{2}
=\frac{0.375+1.000}{2}
=\boxed{0.6875\ \text{in}}
$$

---

## 2. Design I – Shaft Strength

### Known Values, Unknowns, and Shaft Free-Body Diagram

**Known:** Specified shaft sizes, shaft speeds, transmitted torques, a 20° gear pressure angle, and two bearing supports per shaft.

**To determine:** Gear tooth forces, support reactions, bending moment, bending stress, torsional stress, combined equivalent stress, and preliminary shaft material adequacy.

The shaft is represented as a simply supported beam with the gear centered between its bearing reaction points. The free-body diagram applies to either shaft under the simplified loading arrangement.

![Shaft free-body diagram showing bearing span and gear forces](Gearbox1.PNG)

*Figure 1. Free-body diagram with the 0.690 in bearing center span and gear mesh loading.*

### Gear Forces and Bearing Reactions

The output gear has a pitch diameter of 1.000 in and transmits 1.25 in·lbf of torque. Its tangential tooth force is:

$$
F_t=\frac{2T_{out}}{D_{p,out}}
=\frac{2(1.25)}{1.000}
=\boxed{2.50\ \text{lbf}}
$$

The radial gear force follows from the pressure angle:

$$
F_r=F_t\tan(20^\circ)
=2.50\tan(20^\circ)
=\boxed{0.910\ \text{lbf}}
$$

The combined transverse force magnitude is:

$$
F=\sqrt{F_t^2+F_r^2}
=\sqrt{2.50^2+0.910^2}
=\boxed{2.661\ \text{lbf}}
$$

For a centrally applied load, static equilibrium gives equal bearing reactions:

$$
\sum F=0,\qquad R_1+R_2=F
$$

$$
\sum M_{R_1}=0,\qquad R_2L-F\left(\frac L2\right)=0
$$

$$
R_1=R_2=\frac F2=\boxed{1.330\ \text{lbf}}
$$

With a bearing center span of $L=0.690$ in, the maximum bending moment is:

$$
M_{max}=\frac{FL}{4}
=\frac{(2.661)(0.690)}4
=\boxed{0.459\ \text{in·lbf}}
$$

The assignment permits neglecting the moment associated with the radial tooth force. Retaining the radial-force contribution in this preliminary resultant-force calculation provides a conservative comparison, provided the force components are resolved consistently.

### Shaft Stress Equations

For a solid circular shaft, the nominal bending and torsional stresses are:

$$
\sigma_b=\frac{32M}{\pi d^3}
$$

$$
\tau=\frac{16T}{\pi d^3}
$$

Combined bending and torsion are screened using von Mises equivalent stress:

$$
\sigma_{VM}=\sqrt{\sigma_b^2+3\tau^2}
$$

| Stress Check | Input Shaft (0.125 in) | Output Shaft (0.250 in) |
|---|---:|---:|
| Nominal bending stress | 2,394 psi | 299 psi |
| Nominal torsional shear | 1,222 psi | 407 psi |
| Combined von Mises stress | 3,195 psi | 766 psi |

**Preliminary material screening:** A 1018 steel shaft was assumed with an allowable equivalent stress of 10,000 psi. Both specified diameters fall below that assumed allowable under the modeled static loads. This is not a final fatigue or manufacturing verification; actual shaft stock, strength, gear press fits, stress concentrations, and service conditions still need confirmation.

---

## 3. Design II – Journal Bearing Selection and PV

### Selected Sleeve Bearings

The modeled bearings are **graphite-lubricated SAE 841 bronze**, rather than oil-impregnated sleeves. Each shaft is supported by two bearings.

| Parameter | Input Sleeve | Output Sleeve |
|---|---|---|
| McMaster part number | 9368T96 | 9368T13 |
| Nominal shaft diameter / ID | 0.125 in | 0.250 in |
| Nominal bearing OD | 0.250 in | 0.375 in |
| Bearing length | 0.250 in | 0.250 in |
| Sleeve material | Graphite-lubricated SAE 841 bronze | Graphite-lubricated SAE 841 bronze |
| Bearings per shaft | 2 | 2 |
| Approximate load per bearing | 1.330 lbf | 1.330 lbf |

![Bearing free-body diagram showing reaction per sleeve](gearbox2.PNG)

*Figure 2. Each sleeve carries approximately 1.330 lbf under the centered gear-load assumption.*

### Bearing Pressure and Surface Speed

Projected bearing area is the shaft diameter multiplied by bearing length. Average projected pressure is:

$$
P=\frac{R}{dL_b}
$$

The journal surface speed, with $d$ in inches and $N$ in rpm, is:

$$
V=\frac{\pi dN}{12}\qquad [\text{ft/min}]
$$

The pressure-velocity index is:

$$
PV=P\,V
$$

For the **input sleeve**:

$$
P_{in}=\frac{1.330}{(0.125)(0.250)}\approx\boxed{42.6\ \text{psi}}
$$

$$
V_{in}=\frac{\pi(0.125)(2933.33)}{12}\approx\boxed{96.0\ \text{ft/min}}
$$

For the **output sleeve**:

$$
P_{out}=\frac{1.330}{(0.250)(0.250)}\approx\boxed{21.3\ \text{psi}}
$$

$$
V_{out}=\frac{\pi(0.250)(1100)}{12}\approx\boxed{72.0\ \text{ft/min}}
$$

| Bearing Result | Input Sleeve | Output Sleeve |
|---|---:|---:|
| Nominal ID × OD × length | 0.125 × 0.250 × 0.250 in | 0.250 × 0.375 × 0.250 in |
| Projected pressure, $P$ | 42.6 psi | 21.3 psi |
| Surface velocity, $V$ | 96.0 ft/min | 72.0 ft/min |
| Pressure-velocity, $PV$ | 4,086 psi·ft/min | 1,532 psi·ft/min |

McMaster provides load figures of **50 lb at 120 rpm** for 9368T96 and **100 lb at 120 rpm** for 9368T13 in the catalog information reviewed for this project. Those figures cannot be directly extended to operating speeds of approximately 2,933 rpm and 1,100 rpm. The calculated values are compared with a documented same-size alternative in Section 6, but that comparison is not a certification of the modeled graphite sleeves.

---

## 4. Design III – Sleeve Wall Thickness

The sleeve wall thickness can be determined directly from its inside and outside diameters.

**Known:** Bearing ID and OD from the selected component dimensions.  
**Unknown:** Wall thickness and a preliminary estimate of bearing wall stress.

$$
t=\frac{OD-ID}{2}
$$

For the input sleeve:

$$
t_{in}=\frac{0.250-0.125}{2}=\boxed{0.0625\ \text{in}}
$$

For the output sleeve:

$$
t_{out}=\frac{0.375-0.250}{2}=\boxed{0.0625\ \text{in}}
$$

A simplified hoop-stress screening expression is:

$$
\sigma_h\approx\frac{Pr_i}{t}
$$

Using the previously calculated projected pressures:

$$
\sigma_{h,in}\approx\frac{(42.6)(0.0625)}{0.0625}=\boxed{42.6\ \text{psi}}
$$

$$
\sigma_{h,out}\approx\frac{(21.3)(0.125)}{0.0625}=\boxed{42.6\ \text{psi}}
$$

| Sleeve Property | Input | Output |
|---|---:|---:|
| Nominal ID | 0.125 in | 0.250 in |
| Nominal OD | 0.250 in | 0.375 in |
| Calculated wall thickness | 0.0625 in | 0.0625 in |
| Approximate hoop-stress screen | 42.6 psi | 42.6 psi |

**Limitation:** This is a simple uniform-pressure screening estimate. A real journal bearing has a nonuniform contact-pressure distribution and is affected by its press fit, installed bore, alignment, and lubrication. Supplier dimensions and required running clearance govern the final design.

---

## 5. Design IV – Two-Piece Housing Concept

### Housing Configuration and Materials

The enclosure was developed as two axial housing halves meeting at the gear midplane. Both halves have internal clearance for the gear arrangement and openings for sleeve bearing support. Four corresponding corner holes allow the housing to be secured with removable fasteners.

The native Onshape model contains the two editable housing components. An earlier imported assembly includes simplified M3 bolts and external nuts. Removing the fasteners is intended to permit separation of the upper housing and removal of the internal gear, shaft, and bearing components.

| Component | Preliminary Material / Specification |
|---|---|
| Upper and lower housing | 6061-T6 aluminum |
| Input and output shafts | 1018 steel |
| Sleeve bearings | SAE 841 bronze |
| Gear pair | Supplied brass gears |
| Fasteners | Steel M3 bolts and nuts |

### Housing Design Dimensions

| Feature | Dimension / Specification |
|---|---|
| Gear shaft center distance | 0.6875 in |
| Native outer body | 2.50 × 1.90 × 0.94 in |
| Native internal cavity | 2.00 × 1.24 × 0.44 in |
| Minimum nominal in-plane gear clearance | 0.10 in along cavity width |
| Largest gear axial end clearance | 0.0325 in per side |
| Corner fastening locations | Four aligned clearance holes |
| Corner hole diameter target | 0.128 in |

### Intended Assembly Sequence

1. Prepare the lower housing and fit the lower sleeve bearings.
2. Install the shaft-and-gear press-fit subassemblies.
3. Fit the upper bearing sleeves and position the upper housing.
4. Align the four corner fastener locations.
5. Secure the housing using bolts and nuts.
6. Confirm that the shafts rotate freely and that no internal components interfere.

Disassembly follows the reverse sequence. This describes the intended serviceability of the design; a fully mated, motion-tested assembly is still required to confirm that the physical sequence works as intended.

---

## 6. Bearing Speed, PV, and Running-Fit Verification

### Purpose of the Checks

Projected pressure ($P$) represents bearing load divided by the journal's projected area. Surface speed ($V$) represents the journal's motion relative to the bearing. The product ($PV$) provides a preliminary indication of frictional heating demand.

Bearing selection requires separate verification of the supplier's **pressure, velocity, and PV limits**. It also requires distinguishing two different fits:

- **Housing fit:** The bearing outside diameter is retained by an interference/press fit in the housing bore.
- **Running fit:** The installed sleeve inside diameter must leave sufficient clearance for the rotating journal.

The modeled McMaster bearings produce the following duty points:

| Verification Quantity | Input | Output |
|---|---:|---:|
| Projected pressure | 42.6 psi | 21.3 psi |
| Surface speed | 96.0 ft/min | 72.0 ft/min |
| PV | 4,086 psi·ft/min | 1,532 psi·ft/min |

The catalog load ratings quoted for the graphite-lubricated McMaster sleeves were specified at 120 rpm. Their approval at the actual design speeds and their installed bore clearances are **not yet verified**.

### Documented Same-Size Alternative: Oilite Bearings

A same-size oil-impregnated SAE 841 bronze alternative was documented using the following Oilite bearing designations:

- **Input:** Oilite AA227-02, nominal 1/8 × 1/4 × 1/4 in.
- **Output:** Oilite AA307-, nominal 1/4 × 3/8 × 1/4 in.

The supplier sheets referenced in the project PDF list the following maximum operating values for these alternatives:

| Limit | Published Maximum |
|---|---:|
| Pressure, $P$ | 2,000 psi |
| Velocity, $V$ | 1,200 ft/min |
| PV | 50,000 psi·ft/min |

The calculated duty points are below the published limits:

| Utilization of Limit | Input Bearing | Output Bearing |
|---|---:|---:|
| Pressure limit | 2.1% | 1.1% |
| Velocity limit | 8.0% | 6.0% |
| PV limit | 8.2% | 3.1% |

These comparisons establish preliminary catalog screening only. Temperature, alignment, lubrication, installation, loading distribution, and duty cycle must still be evaluated.

### Bearing Fits and Machining Requirements

| Fit Feature | Input: Oilite AA227-02 | Output: Oilite AA307- |
|---|---|---|
| Free bearing ID | 0.126–0.127 in | 0.251–0.252 in |
| Bearing OD | 0.252–0.253 in | 0.376–0.377 in |
| Recommended housing bore | 0.25082 ± 0.00050 in | 0.37474 ± 0.00050 in |
| Recommended shaft journal | 0.12303 ± 0.00020 in | 0.24789 ± 0.00020 in |
| Nominal radial support load | 1.330 lbf | 1.330 lbf |

Based on these dimensions, the approximate diametral press interference before elastic deformation is:

| Seat | Minimum Interference | Maximum Interference |
|---|---:|---:|
| Input bearing | 0.00068 in | 0.00268 in |
| Output bearing | 0.00076 in | 0.00276 in |

Pressing a porous bronze sleeve into a housing can reduce its internal bore diameter. The installed bore must therefore be checked before assuming that the shaft will rotate freely. A separate sintered-bronze design guide cited in the PDF recommends a minimum running clearance of approximately 0.0005 in for shafts under 0.760 in; this is a preliminary target, not a substitute for the selected supplier's installation instructions.

The Oilite journal specifications are smaller than the assignment's nominal 0.125 in and 0.250 in shafts. An alternative build would retain the required nominal shaft sizes at the gear press-fit locations while machining the journal sections to the supplier's dimensions.

At the minimum specified journal sizes of **0.12283 in** and **0.24769 in**, the preliminary combined equivalent shaft stresses increase to approximately **3,368 psi** and **788 psi**, respectively. Both remain below the assumed 10,000 psi screening allowable. The current straight-shaft CAD and nominal housing bores would require revision before this alternative could be described as physically assembled.

---

## 7. Design V – CAD Development and Pictures

### CAD Development Approach

The supplied 18-tooth and 48-tooth gear models were imported as STEP geometry. An initial Python/build123d model was used to create the shafts, sleeves, two housing sections, and simplified hardware as STEP parts. This version remains as an assembly concept in **Assembly 1**.

Because imported STEP geometry does not expose native Onshape sketch and extrusion history, the two-piece housing was later rebuilt in the **Parametric housing Part Studio**. The final native model uses sketches, extruded additions and removals, and a mirror operation. Both housing parts can be selected and edited independently.

The earlier imported assembly has no assembly mates and does not update automatically when the native housing Part Studio is edited. The two should therefore be treated as separate design iterations.

### Native Onshape Feature Summary

| Native Feature | Design Purpose |
|---|---|
| Sketch 1 / Extrude 1 | Centered 2.50 × 1.90 in base, extruded 0.47 in below the split plane |
| Sketch 2 / Extrude 2 | Centered 2.00 × 1.24 in pocket, cut 0.22 in into the lower half |
| Sketch 3 / Extrude 3 | Bearing seats at $x=\pm0.34375$ in, with nominal 0.250 and 0.375 in seat diameters |
| Sketch 4 / Extrude 4 | Four corner fastener profiles, cut through all |
| Mirror 1 | Upper housing created as a separate part mirrored about the Top split plane |

### Native Housing Screenshots

**Cavity dimensions**

![Dimensioned native housing cavity sketch](Gearbox6.png)

*CAD Figure 1. Dimensioned internal cavity sketch on the lower housing.*

**Bearing seat positions**

![Bearing seat sketch with gear shaft locations](Gearbox3.png)

*CAD Figure 2. Bearing-seat sketch showing the shaft positions and nominal sleeve housing diameters. The displayed sketch units may round the dimensions in meters.*

**Corner fastener locations**

![Corner fastener hole sketch](Gearbox7.png)

*CAD Figure 3. Four corner fastener profiles before the final through cut. An initially oversized profile was corrected to the target hole diameter.*

**Finished lower housing**

![Finished lower gearbox housing](Gearbox4.png)

*CAD Figure 4. Finished native lower housing showing the recessed pocket, bearing seats, and mounting holes.*

**Completed two-part native housing**

![Two-part native housing and feature tree](Gearbox8.png)

*CAD Figure 5. Two housing parts and their editable native Onshape feature tree.*

**Additional native housing capture**

![Additional completed housing CAD capture](Gearbox5.png)

*Supplementary CAD view. A second capture of the completed native housing, retained with the project image set.*

### Earlier Imported Gearbox Assembly

**Closed assembly concept**

![Complete imported gearbox assembly](Gearbox9.png)

*CAD Figure 6. Earlier imported assembly concept with the upper and lower housing sections, shafts, sleeve locations, and simplified fastening hardware.*

**Internal gear arrangement**

![Imported gearbox with top housing hidden](Gearbox10.png)

*CAD Figure 7. Imported assembly with the upper housing hidden to expose the gear, shaft, and bearing arrangement.*

The imported assembly views demonstrate the intended component arrangement. They are not evidence of native feature history or a validated kinematic assembly.

---

## 8. Checks, Mistakes, and Lessons Learned

### Gear and Housing Clearance Checks

For the 1.040 in outside-diameter output gear and the 1.24 in cavity width, nominal lateral clearance is:

$$
C_{lateral}=\frac{1.24-1.040}{2}
=\boxed{0.100\ \text{in per side}}
$$

Along the shaft-center direction, the output gear's extreme radius from the housing origin is:

$$
x_{max}=0.34375+\frac{1.040}{2}
=0.86375\ \text{in}
$$

With a 2.00 in cavity length, the remaining clearance to that cavity end is:

$$
C_{end}=1.000-0.86375
=\boxed{0.13625\ \text{in}}
$$

For an assumed 0.375 in gear thickness inside the 0.44 in total axial cavity, the nominal end clearance is:

$$
C_{axial}=\frac{0.44-0.375}{2}
=\boxed{0.0325\ \text{in per side}}
$$

| Clearance Check | Nominal Result |
|---|---:|
| Largest gear lateral clearance | 0.100 in per side |
| Largest gear clearance toward cavity end | 0.13625 in |
| Largest gear axial end clearance | 0.0325 in per side |

These calculations check nominal envelope dimensions only. They do not prove dynamic gear meshing, hub clearance, shaft retention, or manufacturable fits. A mated assembly using the actual gear STEP solids should be inspected before fabrication.

### Revisions and Problems Encountered

- **Fastening hardware:** The initial imported concept did not visibly include fasteners. Four simplified bolts and nuts were added to communicate the intended assembly method.
- **Editable CAD requirement:** The first housing arrived as imported STEP geometry, which lacked native Onshape feature history. The housing was rebuilt using native sketches, extruded cuts, and a part mirror.
- **Corner hole correction:** One mounting-hole profile in Sketch 4 was initially larger than intended and was corrected before the final design views.
- **Exploded assembly:** An earlier exported STEP exploded view visually collapsed component locations after import into Onshape. It does not demonstrate a functional disassembly motion.
- **Bearing terminology:** Catalog review confirmed that the modeled McMaster sleeves are graphite-lubricated. The alternative Oilite sleeves are oil-impregnated, and those material descriptions should not be interchanged.

### Engineering Lessons

The 18/48-tooth gear pair satisfies the specified 24:9 ratio. The bearing review also demonstrated why load capacity at a low reference rpm is not sufficient to approve a sleeve at operating speed, and why the housing press fit and shaft running fit require separate dimensions.

Creating the upper housing by mirroring the lower geometry helped maintain matching pocket and fastener placement. However, the nominal 1.000 in shaft length relative to the 0.94 in total housing thickness leaves only approximately:

$$
\frac{1.000-0.940}{2}=\boxed{0.030\ \text{in per side}}
$$

of shaft protrusion if centered. An external coupling would therefore need longer shafts or a revised housing arrangement. A split-line seal also remains to be designed.

---

## 9. Conclusion

I spent around 8 hours working on this assignment over the course of 3 days. 3 Hours were spent designing the CAD models while the other 5 had been spent through documentation and revisions. You can download the folder to access the parts and assemblies [here](https://drive.google.com/drive/folders/1oqGdbSh4yhDBONOkbHgVbcroTp35oyNG?usp=sharing) through OnShape.
