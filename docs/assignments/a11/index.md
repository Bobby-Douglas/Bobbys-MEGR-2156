# A11 – Motor Selection

For A11, our team of 3 is tasked with continuing the design portion for a tensile tester. Including the leadscrews and crosshead from A10, we are to select a motor, fully design a frame, and design a floating bearing as part two of this two-part assignment. We are given a set of parameters, including a load capacity of 2 kN, a speed range of 1- 50 mm/min, an overall height of over 18 inches, and a safety factor of 4. Currently, the 5/8 -8 lead screw was chosen, the torque on the lead screw was derived to be 5908 Nmm, and the rpm in a range of 0.03 – 1.59.

<img width="878" height="745" alt="image" src="https://github.com/user-attachments/assets/1ccd9c5d-7319-486f-b4cb-6a63f3f2b7ce" />


## 6 Motor Selection - Bobby Douglas 

Before converting the torque and rpm into usable units for picking a specific motor, a stepper was chosen over a brush or servo motor. A Brush motor loses speed as the load increases, making it almost impossible to maintain the necessary force. A servo motor is the best choice as it maintains the most torque and smooth rotation at low speeds; however, it often costs at least 4 times more and requires fine-tuning. 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/2203b800-ba92-4116-b501-ffb790a55e3d" />

 To choose the proper stepper motor, the Torque of 5908 Nmm needed to be converted into ozf*in, the rpm is to low for the majority of the stepper motor specifications, but as it’s easily adjustable it was ignored in motor selection.  Converting the torque, we get 836.31 ozf*in.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/701a7a56-f9b3-422d-8695-78fa5e4fb28e" />

A NEMA 34 was chosen; it has a max holding torque of 1200 ozf*in and an RPM of 2700, which easily meets the requirements, and it costs $ 200 less than the next cheapest servo motor with similar specs.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/d52e8e96-842f-4a2d-8725-75beeeeff9b7" />

Here is the given speed-torque curve for the selected motor; this was not generated for this project but came from the product listing. 

<img width="787" height="597" alt="image" src="https://github.com/user-attachments/assets/fad43c55-a0e6-426a-8a89-fff23f20b39f" />

## Motor Mount design - Bobby Douglas 

For the given motor, A11 requires a motor mount bracket to be designed to secure the motor mount onto the frame, this design was given in the index for this assignment and will be used as the reference for the design

<img width="975" height="566" alt="image" src="https://github.com/user-attachments/assets/63493ea2-ee1c-4db9-a37e-4a435e253ce1" />

The dimensions of the for the brackets are needed, so the engineering drawing was recovered from the McMaster-Carr website. However, a few different dimensions are needed but not listed. The circular portions' inside and outside diameters, their thickness, and the distance from the center of the stepper motor's face to the center of each screw hole. To fill these discrepancies the 3D cad Model was downloaded and measured for the missing measurements. 

<img width="975" height="753" alt="image" src="https://github.com/user-attachments/assets/08f15826-4424-4564-a3fe-6ffeb53eb701" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/b0dcee35-e1c5-4250-8611-0b63b32f9ff1" />

Using the given measurements, the knowns and unknowns were listed, and the thickness of the mount was found using the bearing stress equation at each particular screw hole, based on the torque. The given thickness was 0.00285 inches, including the safety factor, which is low, but makes sense as the actual force on the bar is very low at each bolt location.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/677a30fa-86c0-4491-939e-2c5013bbc175" />

While the given thickness was 0.00285 in,  that thickness was too small for realistic use and didn’t give room to account for the thickness of the inside ring, which measured 0.065 in. So instead, an arbitrary thickness of 0.125 in was chosen, and the design was created based on the design specification given above.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/5b703a53-b395-40d5-9615-a2b6bf96fafb" />

## Coupler Connect - Bobby Douglas 

To connect the Leads screw to the shaft of the stepper motor, we are to find a coupler to secure the two together. Searching for one with a low torque requirement meant that the main purpose was to find one that would connect to the 5/8 in lead screw and the ½ in shaft. Looking through McMaster–Carr, the precision flexible shaft coupler was chosen.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/dca17c00-e3b0-44b0-b9b4-92674579e961" />

We are tasked with either designing or selecting a coupler design, however as the shear torsional stress was given based off the material, and there wasn’t much room for choosing a secondary coupler with different dimensions. Instead of using the stress analysis to determine the inner and outer diameter, I confirmed that the stress on the coupler was less than the stress allowed for both bored holes.  Both of which came with stress values of less than 1 lbf/in^2, which is less than one-thousandth of the allowed stress.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/538a45dd-954b-406c-80c0-80f414d2ac55" />

For the outside websites listed and cad files shown, a list of each are accumulated below. 

Here are the given websites mentioned:

https://s3.amazonaws.com/xometry.craft/files/specsheets/ASM-Aluminum-6061-T6-Material-Data-Sheet.pdf

https://www.mcmaster.com/6259K35/

https://www.ezlok.com/303-stainless-steel-properties



CAD Links:	   

[Motor Cad.zip](https://github.com/user-attachments/files/35311433/Motor.Cad.zip)

## 4. Frame Connector Analysis Owen Switzer

### Frame Design

The frame retains two uprights, one top rail, a mid-height rail, and a moving crosshead. The clear span of the 40 Series top rail is 304.8 mm. Each lead screw transfers 1,000 N at the 2 kN test load. The analysis assumes 5.908 N·m per motor and a 35 mm screw offset. The required safety factor is 4.

![Front view of the single-rail frame in Onshape](single-rail-assets/A11_Owen3.jpg)

*Figure 1. Onshape model showing the top rail, corner gussets, and moving crosshead.*

![Onshape model](https://cad.onshape.com/documents/83e583c401f83cf1aef066d5/w/961b5aa68a69216805b43551/e/13353e8c436f19b80af2834e?renderMode=0&uiState=6b04d176934955b4bf799132) | [Download STEP](https://drive.google.com/file/d/1LDdD4cBsOxAlF0AWm4i417Tt2S1ZpgyX/view?usp=sharing)

### Knowns, Unknowns, and Free-Body Diagram

The unknowns are the joint reactions and the shear, pull-out, and slip capacity of the connector hardware. Symmetry gives a vertical reaction of 1,000 N at each end. Using a reaction spacing of 344.8 mm, the two motor torques produce a transverse reaction of 34.27 N at each end, acting in opposite directions. The 35 mm offset of each screw load produces a roll moment of 35 N·m at each end.

![Hand-drawn top-rail free-body diagram in elevation and plan](single-rail-assets/A11_Owen1.jpg)

*Figure 2. Top-rail free-body diagram showing the vertical loads, motor torques, and transverse reactions.*

### Connector Selection

One 80/20 40-4336 gusset is proposed at each top corner. It uses M8 hardware in the existing T-slots. With an assumed 18 mm contact lever arm and two bolts sharing the load, the preliminary demand per bolt is 0.97 kN in pull-out and 0.50 kN in shear. The shear estimate is based on the vertical reaction.

At a safety factor of 4, the required capacities are 3.89 kN in pull-out and approximately 2.00 kN in shear per bolt. The combined capacity and resistance to slipping along the upright T-slot still need verification.

![Hand calculations for frame reactions, connector loads, and top-rail safety factor](single-rail-assets/A11_Owen2.jpg)

*Figure 3. Hand calculations for the joint reactions, preliminary connector loads, and top-rail safety factor.*

### Top-Rail Stress Check

The fine-mesh results show a peak von Mises stress of approximately 39 MPa near the left end of the rail. Using the assumed yield strength of 172.37 MPa, the allowable stress for a safety factor of 4 is 43.09 MPa. The resulting top-rail safety factor is approximately 4.42, which meets the requirement for the modeled load case.

![Von Mises stress at the peak-stress cross-section and along the top rail](single-rail-assets/A11_Owen4.jpg)

*Figure 4. Fine-mesh stress at the critical cross-section and along the rail. The dashed line marks the 43.09 MPa allowable stress.*

## 5 Frame Analysis - Owen Switzer

The top rail was restrained at both ends and loaded with 1,000 N downward at each mount, plus the motor torque and screw-offset moment. The simulation converged. The deformation is exaggerated for visibility.

![Top rail deformation in Onshape](A11_Owen9.jpg)


## 6. Upright Finite Element Analysis - Owen Switzer

### Model Setup

The 609.6 mm upright uses the same heavy 40 Series 80/20 40-4040 extrusion as the top rail. The analysis uses a yield strength of 172.37 MPa for 6063-T6 aluminum. The foot face is fixed to represent a restrained base. The upper end carries 1,000 N of compression at a 35 mm offset and a transverse load of 34.27 N. The free-body diagram shows the more heavily bent upright.

![Upright free-body diagram](part6-assets/A11_owen7.jpg)

*Figure 5. Upright free-body diagram showing the fixed foot, eccentric compressive load, and transverse load.*

### Mesh Refinement and Stress Results

The upright was modeled with 3D solid wedge elements. Two refinements reduced the axial and cross-sectional element sizes at the slots and foot. The finest result uses linear superposition of two load cases solved on the same mesh.

| Mesh | Target size (mm) | Elements | Peak stress (MPa) | Grip-line motion (mm) |
|---|---|---:|---:|---:|
| 1 | 8 × 2.4 | 42,276 | 9.35 | 0.1141 |
| 2 | 5 × 1.55 | 138,226 | 9.45 | 0.1150 |
| 3 | 3.5 × 1 | 468,688 | 9.84 | 0.1153 |

For the 35 mm screw offset, peak von Mises stress was **9.84 MPa** at the outer edge of the extrusion, 2.73 mm above the foot. The yield safety factor was 172.37 / 9.843 = **17.51**, above the required 4 for this load case. From Mesh 2 to Mesh 3, peak stress increased by 4.1% and grip-line motion increased by 0.3%.

![Upright stress contour near the base and peak stress by height](part6-assets/A11_Owen5.jpg)

*Figure 6. Von Mises stress near the foot and peak stress along the upright for the 35 mm and 30 mm screw offsets.*

### Upright Deflection

At the 35 mm screw offset, the upright’s maximum vertical displacement was 0.0703 mm, and its top moved 0.985 mm sideways. Projecting the upper-end motion to the grip plane gave an estimated downward displacement of 0.1153 mm.

The eccentric compressive load and the transverse load bend the upright toward the screw plane. The bending moment is greatest near the fixed foot, where the stress peaks.

![Onshape view of the bent upright and its undeformed outline](part6-assets/A11_Owen8.jpg)

*Figure 7. Onshape deformation view showing the upright bending sideways from its fixed foot.*

### Design Refinement

Moving the screw load plane from 35 mm to 30 mm reduced peak stress from 9.84 MPa to 9.10 MPa and reduced sideways motion at the top from 0.985 mm to 0.885 mm, a reduction of about 10%. The critical section remained 2.73 mm above the foot. The shift retains the single-rail layout.

![Vertical and sideways displacement for both screw offsets](part6-assets/A11_Owen6.jpg)

*Figure 8. Vertical and sideways displacement along the upright for the 35 mm and 30 mm screw offsets.*

Check screw, bracket, and fastener clearance before moving the load plane. The model uses an idealized base restraint, and the grip-plane displacement is estimated from the upper-end motion.

[80/20 40-4040 profile and material properties](https://8020.net/40-4040.html)


## Bearing mount - Cooper Radtke 
In order to design a bearing mount with an RC3 fit I needed to look through the machinery's handbook. I listed my known outer diameter and needed tolerances for the design. From here I drew the FBD and proceeded to solve for the thickness and diameter of the inner wall using torque analysis equations.

 
## Clearances - Cooper Radtke 

### RC3 fit

| Feature | Size (in) | Limits (in) |
|---|---|---|
| Bore (hole) | 0.4375 | +0.0007 / −0.0000 → 0.4375 to 0.4382 |
| Journal (shaft) | 0.4375 | −0.0006 / −0.0010 → 0.4365 to 0.4369 |
| Clearance | n/a | 0.0006 min, 0.0017 max |

### Bolt clearance holes (1/4-20)

| Close fit | Normal fit |
|---|---|
| 0.266 in (17/64) | 0.281 in (9/32) |
| 0.2570 in (F) | 0.2656 in (17/64) |

0.281 selected

## Justification of dimensions - Cooper Radtke 

| Dimension | Value | Justification |
|---|---|---|
| Journal Ø | 0.4375 in | Below the Acme minor diameter (about 0.480 in), so the thread runs out at a shoulder. Within the 0.40–0.71 in RC3 size range. |
| Bore depth | 1.00 in | 0.75 in of bearing contact plus 0.25 in end gap for thermal growth and oil. |
| Bearing length | 0.75 in | L/D ≈ 1.7, inside the usual 1–2 range. Resists tilt without edge loading. |
| Shoulder stand-off | 0.125 in | Keeps the end floating. Acts as a safety stop if the coupling slips. |
| Boss Ø | 1.00 in | Leaves a 0.28 in wall around the bore. |
| Boss height | 1.25 in | 1.00 in bore plus 0.25 in floor. |
| Base plate | 3.00 × 2.00 × 0.375 in | 2.00 in covers both crossbar rails. 0.50 in edge distance on all bolt holes. |
| Bolt pattern | 2.000 × 1.000 in | 1.000 in lands bolts on the two slot centerlines. 2.000 in keeps bolt heads clear of the boss. |
| Axis location | Crossbar centerline | Midway between slot rows. Slot nuts slide, so the block can be aligned to the coupling. |
| Bolts | 1/4-20 × 3/4 SHCS | Pass the slot lip and fully engage the slot nut. |

<img width="896" height="910" alt="image" src="https://github.com/user-attachments/assets/28e8627f-09da-4dd7-b774-265455f7873d" />

## Tabulating costs - Cooper Radtke 
| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
|---|---|---|---|---|---|
| 1 | 2 | Aluminum Frame Rail (4601N78) | $18.72 | $37.44 | [McMaster-Carr](https://www.mcmaster.com/4601N78) |
| 2 | 2 | Aluminum Frame Rail (4601N73) | $12.01 | $24.02 | [McMaster-Carr](https://www.mcmaster.com/4601N73) |
| 3 | 2 | 5/8"-8 Carbon Steel Acme Lead Screw, 24" (98935A914) | $9.79 | $19.58 | [McMaster-Carr](https://www.mcmaster.com/98935A914) |
| 4 | 2 | 5/8"-8 Acme Flange Nut, 932 Bearing Bronze (95120A119) | $138.20 | $276.40 | [McMaster-Carr](https://www.mcmaster.com/95120A119) |
| 1 | 1 | Stepper motor (6627T671) | $210.56 | $210.56 | [McMaster-Carr] https://www.mcmaster.com/6627T671/ |
| 1 | 2 | Flexible shaft coupling( 6259K35) | $413.44 | $413.44 | https://www.mcmaster.com/6259K35/ |
| | | Labor Cost at 35/hr | | $420.00 |
| | | **Total Cost** | | **$1401.44** | |

## Communicate - Cooper Radtke 
We collectively worked 12 hours on this project. The most difficult part about working on this project was when multipart questions were split among two people. The frame FEA for example was worked on and developed independently by two people. This resulted in frames of two different constructions and the need to realign calculations in favor of one or the others model. We worked this out by deferring responibility to the prson more familiar with the part run tests to allow a smoother and quicker workflow.

