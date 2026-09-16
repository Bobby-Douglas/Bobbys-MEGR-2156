# A4 – Motor Mount

## Initial: knowns and unknowns 

The goal of this assignment is to create an engine mount for the given Engine with given specifications with a Cad software. Obtain shear stress and deflection using hand calculations, with a load based not on the engines mass but in the Load being applied. The given Load P is 300 Newtons, we are told to split up the Calculation of the mount into 2 separate features, a simple cantilever beam and a ceiling mount. We are given a Safety factor of 3 and must find a height, base, and Length that that prevents a deflection of 0.03mm and a max shear stress based on either PLA, PETG, or ABS Material

<img width="192" height="154" alt="image" src="https://github.com/user-attachments/assets/fcf1482b-0d2f-4d7f-a670-27dd965ec550" />

<img width="975" height="303" alt="image" src="https://github.com/user-attachments/assets/5aa54413-5fc8-4d46-b54c-7839f72f3f30" />

For the Material, PETG was chosen as it better handles the shock and conditions brought upon by a motor. While it’s less heat resistant than ABS it better handles force absorption for long term usage. For the given material we are given a range listed below, a Tensile strength Between 20 and 100 MPa, a Yield strength of 28.8 to 101MPa, a elongation at break of 3.2 to 376 %, and a elongation at yield of 2.7 to 576%, and a modulus of Elasticity of .110 to 20 GPa. The design specifications for the engine are a screw hole 0f 3.4mm, a Shaft diameter of 6 mm, a shaft base diameter of 18mm, a shaft base height of 2 mm, a applied diameter of 22mm for the location of the 4 screw holes, and total diameter of 28 mm. The unknowns we were searching for was a long list, however after looking back the only unkowns where length, base, and height. It was then reasoned that being given the limits range for Shear stress and the max deflection, those would be the equations used primarily for finding the cross sectional geometry of each feature, solving primarily for height.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/3d2610fa-2c44-4a3e-a326-b411b8be137e" />

## Feature #1

As the first feature is began there are too many variable to solve for in deflection and Shear stress equations for the free floating section. the height and length were decided based on convenience of assembly. For Length 50 mm was chosen as to allow for plenty of clearance room when installing the engine onto the mount, and the base as 30 mm as it’s just 2mm wider than the diameter of the brush engine. That leaves just height. Using the previously modeled equations I derive the height from shear stress equation as17.32 mm, however it didn’t pass the deflection test so I revised to solve for height derived from the deflection equation, which gave a height of 19.574 mm or 20 rounded for convience, and after doing the Shear stress test it passed all necessary requirements including the safety factor. The height, Length, base, and cross sectional area are given below. 

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/047aba64-1ea4-4628-8a2f-dddb33529e27" />

## Feature #2

Moving onto the second feature, or the ceiling mount an assumption was made that due to previous height calculation, deriving from deflection equation would make the most sense. The decided Length for this section was 25 mm as it’s length wasn’t quite as important as before, it’s base however was 30mm to maintain a flush look with feature one during cad production. After deriving h from the deflection equation wear left with a height of 9.787mm. surprisingly the height that would accommodate the required deflection including the safety factor, was still unable to pass the shear stress test which is different from the previous feature. 

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/81f21ba7-f87d-4e11-99a1-246e41e4c0c6" />

## Revision: Feature #2

beginning numerical calculation again, instead solving for h derived from the shear stress equation. Height or h was found to be 12.25mm, which was rounded up to 15mm for convenience as each other portion of cross sectional geometry were multiples of 5, it also drastically reduces cost as more precision requires a lot more money. Using the deflection test it was able to pass including the safety factor. 

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/8bb6536e-5860-4bf8-8a4e-cf16bc027fa8" />

Here is an isometric view of the structure as it is to be built within cad, including the drill hole features and extruded round cuts allowing for a better and more seamless engine mount.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/b7dd386d-8d62-4288-b214-c1dbb1df125f" />

## CAD Modeling

Here is the initial body drawing with the given lengths and such, technically there is an additional length to both pieces as a sort of additional space that holds the two pieces features together.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/1fc5b53f-0237-4f2e-a6a3-05fa015e7bec" />


<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/04f393ff-8f7c-40e6-85ae-e159b8a1699f" />

To aid in centering the M4 screw holes and the shaft, construction mode was utilized in order to set a clear boundary for each of the circles to be built on. This was used instead of the pattern feature as at this level and with specific non changing hole requirements, it’s faster than a pattern feature.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/c6f63b0a-f9a8-483b-80a7-0ade529001fa" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/3bcb27f1-a656-44d9-b6b6-27c0c8be9df6" />

This is the initial clearance to allow for the engine to be flush with the part and have a tight fit, it has a radius of 28mm and a depth of 2 mm mimicking the required clearance depth fo the base of the shaft.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/70f27623-dba0-44ef-a8c5-413da424a35d" />

This is the clearance for the base of the shaft, now to be clear the base of the shaft is not connected to the shaft but is rather just encompassing it and is 2 mm raised up compared to the rest of the motor face.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/17afc2e7-c400-4701-8038-b14c9bc5b23c" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/cefc79c9-ee2c-4772-b449-51e0fc7d17b4" />

These are the mounting screws holes, placed exactly 5 mm apart across a 15 mm surface, each hole has the clearance for a M3 screw. Hindsight says that the piece should have been made with a longer base but mathematically it still functions fine for holding the engine.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/48ca0591-b649-453b-b07c-ebb46eadcbdd" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/18ec6dce-d25f-4bc8-bf43-9f98470bd58e" />

Here is an isometric view, and front view of the Part fully completed

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/847efb01-8d07-4f93-a3ce-b1cc6246e48d" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/c7a414a3-449a-486f-ace3-532f2bb2ce61" />


## Topic: CAD DRAWING
As for the final part as specified in the post Topics section I created a drawing of the given part with a front, right, top, bottom, and isometric view with the given dimensions listed and descriptions for certain dimensions. It also includes a title box however this one was created inside of part instead of using a template as I could not find one 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/431ad182-6203-45c2-a1ce-ac855e352780" />

This assignment took around 10 hours to complete 

Here is a link to the CAD files and pdf cad drawing: [Mountfld.zip](https://github.com/user-attachments/files/32308633/Mountfld.zip)


Here is a link to the PDF:[A4.pdf](https://github.com/user-attachments/files/32312520/A4.pdf)


