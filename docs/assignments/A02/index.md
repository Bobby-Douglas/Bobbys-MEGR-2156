# A2 – Truss Stress Analysis

In this assignment I am tasked with designing a 3d truss based on the certain parameters given by the image below

<img width="317" height="215" alt="download" src="https://github.com/user-attachments/assets/b7e82482-9cf4-43af-9b11-bee3fd566b31" /> 

The size of segment b is given as 0.3 meters, each segment a is given as 0.4 meters as they span from point A to point B. beams are made of A500 steel and the pins are harden tool steel, the load P at both point C and D are identical at 25 kg, converted to force its 245.25 Newtons. The total distance from point A to B is 1.2 meters, point A is stated to be a pin connection while point B is stated to be rolling joint. My initial step was to redraw the given model above to act as a visual before I solve for the distance between AD, and BC. As the distance from point A to B is 3 a segments long it’s easy to establish that distance, and as the distance between point C and D are 1 a length long it’s determined to be 0.4 m long. As for AD an BC, as it’s clearly a symmetrical trapezoid, it can be inferred that the distance of the both segments are equal. Using Pathagoreans Theorem, the distance comes out to 0.5m for both segments. From their I solve for the forces around joint D before making the incorrect assumption that I needed to multiply the load by the safety factor. Later down the line this becomes as headache as it forced have to take each given force and solve for it normally as multiple safety factors are used within this project.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/d5be176f-bf94-4ec2-aa36-336f6dca0c7e" />

I then go on to solve for the internal forces using the method of joints as a way to predetermine the necessary shape for the truss; Force P including the safety factor(Ps) was found to be 858.38 newtons, and referencing that the internal forces of beam AD were 1429.62 newtons, the internal force of DC was found to be 1143.25 newtons. Midway through Joint C I became skeptical of the force on DC as their were two equivalent masses yet I only accounted for 1 in the calculation. I then went back and referenced my Physics 1 notes regarding the relationship between two pendulums connected by a string, and 1 mass connected to a string that’s connected to a wall, confirming that the force on the segment in these cases are equal. As I predicted earlier the force BC is equivalent to force AD.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/2dd48323-d90c-48eb-9383-3b6a63b7afda" />

Based on my internal calculations, I made the assumption that 2 internal beams would be necessary to handle the load and made my choice on a trapezoidal shape. Creating a brand new point O, beams BO, AO, CO, and DO were added to the equation. BO and AO where 0.6m respectively, however CO and DO were found with Pythagoreans theorem, at the length 0.361 meters. With new beams, I retook the forces starting at with the external forces and working the way in. Ax was 0 newtons, Ay was equal to 858.38 newtons, By is equivalent to Ay.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/03716ce5-2b9e-4013-871f-41d8ec308a5d" />

I then find the internal forces using the external forces, at joint A the force in beam AD is equivalent to the previous calculation; beams AO, BO, and DC have an internal force of 1143.25 newtons. AD and BC remain at 1429.62 newtons each. The internal members CO and DO have an internal force of 0 newtons, as they only add extra weight to the final design; they were excluded. Making reducing the members from 7 to 4: AB, AD, BC, and DC. With AB being double the length of AO making it 1.2 m

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/57c56f79-fa83-4f60-a915-043b7cb5f6ff" />

After finding internal forces, time was taken out to list derived parameters, both with and without a safety factor to use in later calculations. 

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/d64871c0-9173-48bd-ba29-bee936fda278" />

Now it’s time to find the cross-sectional area of a beam, which left me confused as yield stress was required for the equation yet the the yield stress for A500 steel wasn’t listed; I ended up using the website tottentubes.com to find the stress yield. Using a square cross-sectional area as the stress yield is greater than any other shape at 269 Megapascals.  Using the yield stress equation I solved for the minimum required cross-sectional area for all members using the member under the most strain in the system, which was either BC or AD. The area was 5.32 mm^2.

Solving for density, and similarly the density for A500 wasn’t listed so I used suppliersonline.com which gave me a density of 7850 kg/m^3.  Using simple conversion to function with my previously found values, density became 7.85 g/mm^3.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/28e40728-3f5c-488c-8b09-d43d8b0e19af" />

Knowing the Lengths of each member of the truss  I then convert to mm and multiply the length by area, density, and finally the acceleration due to gravity to get the weight in newtons, which was 860.34 newtons.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/1b456b01-f907-4892-9c5b-0d12a7cb998d" />

Next I began to solve for the cross sectional area of the pins connecting each member, using the shear stress on a pin equation to. I found the pin under the most force and solved for the reaction load,  then using the sheer stress equation the cross sectional area was calculated to be 1.785mm^2, which took surprising long for me to solve as I kept converting m^2 into mm instead of mm^2. I also calculated the diameter for design steps during the CAD modeling phase.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/3e8628b2-90fb-45e2-9fb5-d84951e1248a" />

Here I calculated the the total pin weight, first converting the given density of 0.278 lbm/in^3 into 7711.2 kg/m^3. Then I found the required length of the pins based on with of the plates cross sectional areas that would be held together by each pin,  and converted it to meters. Solving for the mass in Newtons was 6.24x10^-4 newtons.  And the total weight of all the pins of the system was 2.5x10^-3 newtons.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/d8b41b60-bc04-4c59-9772-cca9b9bbef29" />

As I began the 3d modeling phase I had seen the example A2 project example and wanted to copy it immediately; however, I was limited do to the nature of the shear equation that I used. An Y head connection requires a double shear calculation and I only did a single shear calculation, knowing that I drew up a quick design to have an idea of what connections I would be using.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/fa5cbf52-b1d8-4d6a-b101-b65632f08c4f" />

Beginning the CAD model, the 3d square beam has a cross sectional area of 5.32 mm^2 with a side length of 2.31mm

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/4727f7d9-0d38-4d65-a18c-59b3ad56321f" />

The length of This specific beam is 400mm and is beam DC, other corresponding beam lengths are 500mm for beams BC and AD, and 1200mm for beam AB

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/930b487d-c5b7-4cb8-b3b8-3b87dbf17a47" />

The radius of the pin hole is 1.52 mm, 0.01 mm larger than the radius for the pin for allowance; the center is 1.155 mm away from the bottom, top, and outside edge. With a extrude cut through all.

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/f210b7a2-d5b7-490a-a383-6d00c37a94a2" />

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/5d64ac51-f260-4ac4-b0d5-838b0edc4447" />

The diameter of the pin is 1.51mm with a cross sectional area of 1.785 mm^2, it’s length was determined by the 2 times the side length of a single beam as it connects 2 beams together across faces.

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/ea4c0de0-afa5-4f46-9a85-8783d64bc817" />

<img width="973" height="564" alt="image" src="https://github.com/user-attachments/assets/564e2244-45fd-4ed5-acf7-9b4d4f23fc1e" />

That is the coincidence connection between beam AB and Beam AD, this is pre pin connection.

<img width="974" height="563" alt="image" src="https://github.com/user-attachments/assets/7cb1cba0-51ba-4888-8019-308d752c6a29" />

This is the coincident connection between AB, BC, and AD, I had trouble aligning the pin holes while maintaining the shape and ended up deleting the model and starting again. I have no idea why that worked but it did.

<img width="974" height="563" alt="image" src="https://github.com/user-attachments/assets/8c513d09-620a-4bac-925b-53ca7247252e" />

This is the process of connecting the four pins into the model, I used two different coincident constraints, one to put the pin in the hole and the second to maintain a flush look.

<img width="974" height="563" alt="image" src="https://github.com/user-attachments/assets/f7a60f32-0f4e-4e6d-ac0d-673e5b75498f" />

<img width="974" height="563" alt="image" src="https://github.com/user-attachments/assets/341e13c4-7c84-4622-909f-3df9281d59df" />

The final Truss model, however, I still have to determine the mass properties in the cade mode, then by hand determine the weight of the truss based on the mass.

<img width="973" height="563" alt="image" src="https://github.com/user-attachments/assets/b04ac07b-1864-47f0-9e1a-88f1a82a2ab9" />

As A500 steel isn’t a provided model for creo parametric I had to go into a separate screen and create the material to be used in the model, going into files, prepare, mass properties, change, then clicking the top right corner to create  and putting in the density and name before clicking confirm and using it for mass, then repeat the step for Tool_steel.

<img width="965" height="1271" alt="image" src="https://github.com/user-attachments/assets/5b7207c0-3cfe-4677-9492-257318d05760" />

After running the Mass program on Creo I got the Mass 01.089017 x10^-4 Tonne, it’s not a usable unit so I’ll have to convert it  on paper to something more recognizable before finding the weight.

<img width="975" height="908" alt="image" src="https://github.com/user-attachments/assets/5ad90a4c-b0cb-4ff5-91f0-38693103d168" />

After converting Tonnes into kilograms, I’m left with the mass 0.1089017 kg which I can Now use to find the weight in Newtons. Using the gravity constant 9.81 m/s^2, I determined the weight of the truss to be 1.068 newtons.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/ad80ea43-94c6-47e2-b40e-2230963b3da5" />

Over the course of this project, an engineering lesson learned during this process is to fail faster. For this project, my biggest challenge and reason for it being late is due to procrastination in each section. I would finish one part, then the load of the second and confusion regarding conversion and what the next step was held me back. It wasn’t until I embraced the mistakes that I began to make any progress. Like when dealing with the Safety factor when constructing the beam, I didn’t read ahead and multiplied the safety factor by the load P, and had to convert all the internal forces I found back after that part as I needed those forces without that safety factor so I could apply another safety factor. Could I have taken a break, given up, yes but instead I kept moving forward. Engineering is about failing, making mistakes, and fixing said mistakes; the faster you can do that the easier projects become. 

This project was a lot more than I initially planned for, taking me upwards of 20 hours to complete. Although it's definitely not worth that much time, as most of it was due to constant distractions and poor time management. From testing different truss constructions to the extensive documentation, not to mention Creo being one of the worst CAD programs. I feel like my explanations are a little wordy and resemble more of a paper or biographical format. Leaving much to be desired in the information section.

**Likelihood of failure modes in truss components** 

Before I begin on the likelihood of failure modes in truss components, I will say despite the orientation the major risk to all of the truss members is deformation at the joints as the metal is weakened as the whole removes a considerable amount of steal leaving a thinner barrier compared to the rest, so for all, technically it’s rupture at connections. For this section I will be using AI to help discover sources.

**Member AB**: As the top beam or the top cord of the truss it’s under compression force, and due to the lack of internal beam members the beam is at risk of Buckling due to its slender geometry. A500 steel is known for it’s ductility in normal temps but can become brittle in colder temperatures. One modification that could reduce the likelihood of such failure is adding diagonal internal beams to the structure to help support load in case of bucking
**Members BC and AD**: both Truss members are under equivalent tension from loads P, and as such the most likely form of failure would be from yielding or the material being stretched past steels elastic limit causing the beam to elongate. Under Normal conditions a A500 steel is ductile and would stretch once it’s limit is reached. One modification to avoid such buckling would be to include internal diagonal beams to reduce the load on the outside beams and help increase the load carriable.
**Member DC**: As the bottom cord of the truss, the most likely failure would be failure from yielding as it’s under tensile extreme tensile force. Steel as an element is very ductile and would yield long before it ruptures. The only way to prevent yielding would be by adding 1 internal horizontal beam stretching from both ends or 2 diagonal internal member to reduce the tension on that piece.

**Pin connections**: As the steel pin of the truss holding the members together using too steel, the most likely type of failure would be a fracture. Tool steel is incredibly hard and strong, but once the moment is exceeded, the pin is very brittle due to the hardening process and will most likely snap.  The best prevention method would be to replace the metal all together and switch to a more high impact and ductile steel that would do better in the conditions. 

AI questions asked regarding the failure points the truss members include, “Is steel ductile or brittle in normal conditions”, “Is a steel beam under compression more likely to yield, buckle, or fracture?”.  “Is a diagonal steel beam under tension more likely to yield, buckle, or fracture?”, “can you provide me with sources for why yielding is the primary risk”. And “Likely failure of a tool steel pin connection”

**LINKS BELOW**

My CAD file for the 3d truss [ [CAD folder.zip](https://github.com/user-attachments/files/31731550/CAD.folder.zip)]

PDF for my A2 assignment [[Bobbys-MEGR-2156_docs_assignments_A02_index.md at main · Bobby-Douglas_Bobbys-MEGR-2156.pdf](https://github.com/user-attachments/files/31732396/Bobbys-MEGR-2156_docs_assignments_A02_index.md.at.main.Bobby-Douglas_Bobbys-MEGR-2156.pdf)
]

**Work cited:**
1. TEVEMA
TEVEMA Marketing. "Can Steel Fail in Compression? Uncovering the Facts." TEVEMA, 6 May 2024, www.tevema.com/can-steel-fail-in-compression/. 
2. Fire Engineering
Havel, Gregory. "Construction Concerns: Truss Failure." Fire Engineering, 29 Dec. 2008, www.fireengineering.com/fire-safety/construction-concerns-truss-failure/. 
3. Hawkins Forensic Investigation
Dang, Yang. "Investigations Into Steel Structure Failures Part I: Failure Mechanisms." Hawkins Forensic Investigation, 5 Jan. 2022, www.hawkins.biz/insight/steel-structure-failure-mechanisms/. 
4. Fushun Special Steel
"Why Do Metals Suddenly “Break”?" FuShun Special Steel, 19 June 2025, www.fushunspecialsteel.com/why-do-metals-suddenly-break/. 
5. My Digital Publication
"Article 3992080." MyDigitalPublication, lsc-pagepro.mydigitalpublication.com/publication/?i=702230&article_id=3992080&view=articleBrowser.
6. ASM International
"Failures of Tools and Dies." ASM International Digital Library, dl.asminternational.org/handbooks/edited-volume/151/chapter/3443095/Failures-of-Tools-and-Dies-1 

