# A11 – Motor Selection

For A11, our team of 3 is tasked with continuing the design portion for a tensile tester. Including the leadscrews and crosshead from A10, we are to select a motor, fully design a frame, and design a floating bearing as part two of this two-part assignment. We are given a set of parameters, including a load capacity of 2 kN, a speed range of 1- 50 mm/min, an overall height of over 18 inches, and a safety factor of 4. Currently, the 5/8 -8 lead screw was chosen, the torque on the lead screw was derived to be 5908 Nmm, and the rpm in a range of 0.03 – 1.59.

<img width="878" height="745" alt="image" src="https://github.com/user-attachments/assets/1ccd9c5d-7319-486f-b4cb-6a63f3f2b7ce" />

## Motor Selection and Attachments 

### Motor Selection 

Before converting the torque and rpm into usable units for picking a specific motor, a stepper was chosen over a brush or servo motor. A Brush motor loses speed as the load increases, making it almost impossible to maintain the necessary force. A servo motor is the best choice as it maintains the most torque and smooth rotation at low speeds; however, it often costs at least 4 times more and requires fine-tuning. 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/2203b800-ba92-4116-b501-ffb790a55e3d" />

 To choose the proper stepper motor, the Torque of 5908 Nmm needed to be converted into ozf*in, the rpm is to low for the majority of the stepper motor specifications, but as it’s easily adjustable it was ignored in motor selection.  Converting the torque, we get 836.31 ozf*in.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/701a7a56-f9b3-422d-8695-78fa5e4fb28e" />

A NEMA 34 was chosen; it has a max holding torque of 1200 ozf*in and an RPM of 2700, which easily meets the requirements, and it costs $ 200 less than the next cheapest servo motor with similar specs.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/d52e8e96-842f-4a2d-8725-75beeeeff9b7" />

Here is the given speed-torque curve for the selected motor; this was not generated for this project but came from the product listing. 

<img width="787" height="597" alt="image" src="https://github.com/user-attachments/assets/fad43c55-a0e6-426a-8a89-fff23f20b39f" />

### Motor Mount design

For the given motor, A11 requires a motor mount bracket to be designed to secure the motor mount onto the frame, this design was given in the index for this assignment and will be used as the reference for the design

<img width="975" height="566" alt="image" src="https://github.com/user-attachments/assets/63493ea2-ee1c-4db9-a37e-4a435e253ce1" />

The dimensions of the for the brackets are needed, so the engineering drawing was recovered from the McMaster-Carr website. However, a few different dimensions are needed but not listed. The circular portions' inside and outside diameters, their thickness, and the distance from the center of the stepper motor's face to the center of each screw hole. To fill these discrepancies the 3D cad Model was downloaded and measured for the missing measurements. 

<img width="975" height="753" alt="image" src="https://github.com/user-attachments/assets/08f15826-4424-4564-a3fe-6ffeb53eb701" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/b0dcee35-e1c5-4250-8611-0b63b32f9ff1" />

Using the given measurements, the knowns and unknowns were listed, and the thickness of the mount was found using the bearing stress equation at each particular screw hole, based on the torque. The given thickness was 0.00285 inches, including the safety factor, which is low, but makes sense as the actual force on the bar is very low at each bolt location.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/677a30fa-86c0-4491-939e-2c5013bbc175" />

While the given thickness was 0.00285 in,  that thickness was too small for realistic use and didn’t give room to account for the thickness of the inside ring, which measured 0.065 in. So instead, an arbitrary thickness of 0.125 in was chosen, and the design was created based on the design specification given above.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/5b703a53-b395-40d5-9615-a2b6bf96fafb" />

### Coupler Connect

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



