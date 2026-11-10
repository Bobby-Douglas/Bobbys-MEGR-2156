# A9 – Pulleys

## Objective

In Project A9 we are tasked with designing a pullly system due a situation combining different concepts, like friction, static analysis, and dynamic analysis. We are told that the Pullly system is to have 2 equal size pulleys with a diameter of 3 inches each, and a distance appart of 4 to 6 inches. The Rotational speed is given to be between 1000 and 2000 rpm, the belt tension is between 4 to 6 lbf in stationary conditions, and the material fo the pullys is between Alluminum, ABS and Steel. And the shaft is to include a grove, with a safety factor for the entire structure to be 3, and the given belt has a yield strength of 471 psi.
 

<img width="800" height="331" alt="image" src="https://github.com/user-attachments/assets/c944547c-5971-4081-b239-6afaf53f2df9" />



## Analyze and Decide




After initial set up of knowns and unknowns, Ai was used to assist in the design of the FBD, in my mind I struggle with how the diagram should be oriented and that had halted further progression. Google generated an image that was copied with slight adjustments to match my needs for an FBD needed to Find a suitable belt from Resource 1.

 
<img width="975" height="1158" alt="image" src="https://github.com/user-attachments/assets/c57d68dc-9362-4dfe-97e8-5529bacbb0a2" />


 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/8240598b-32db-4bd2-8355-d9da851549f4" />












For the given calculations, it was decided that the distance between the pulleys would be 5 inches, the Torque would be 5 lbf *in, the RPM would be 1500 rpm, the material of the pulleys would be aluminum, with a max safety factor of 40 ksi.The Coefficient of Friction for Aluminum wasn’t given so I found an article online stating the coefficients of friction for different given materials, the link to the website will be at the bottom. We are tasked to solve for the force given on the tight and loose side of the pulley along with the necessary diameter for the pulley. Deriving the Given tight side force was 4.503 lbf while the loose side was 0.720 lbf, and the diameter was 0.1831 inches, however in the screen shot below I had put inches squared, a small unit error.  

<img width="975" height="1134" alt="image" src="https://github.com/user-attachments/assets/343666a5-b7af-44e3-81a2-9546b8eabdda" />

 <img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/efe170b9-6ccf-4069-ad5e-1cccc3906c1f" />

 

Using the provided resources to locate a belt, every belt diameter was measured in mm, so the belt diameter was converted. It’s diameter in mm was 4.6054 mm, which was also wrote as mm squared which was a unit error. Looking down at the diagram the belt that matched the needed specification was belt 8112K52, and it was promptly selected.

<img width="975" height="1158" alt="image" src="https://github.com/user-attachments/assets/b1c362a3-31bb-43a8-a6df-3b0e3e9d10a1" />

 
For the Shaft section we are tasked to find the diameter of the shaft, the material was predetermined as steel 1060 from the assignment guidelines, using the shear stress equation  the diameter was determined to be 0.03954 inches.      


<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/29824223-cfdf-4129-9335-72ba8972f462" />





To reduce friction between the Frame supporting the gears and shaft, we are tasked with finding an appropriate Journal bearing base off the Pressure – Velocity Rating derived. For this instance we are converting from rpm to rad/s, changing 1500 rpm to 157.08 rad/s. using the total force value as the load we solve for pressure using the equation given in the book in the plain bearing section. To solve for L we are told to use the ration L/d where L is the length of the bearing and d is the diameter, as the diameter is 0.3954 in the length is totaled to about 0.5931 inches. Solving for the PV rating using a safety factor of 3, we get a PV rating of 9502.83, the closest Journal bearing material that would suffice would be dry graphite, which has a PV rating of 15,000.

 
<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/ee1827ce-d936-4aef-8272-7c2826bbdd7a" />

	

The frame was described to hold both gears in place, using the previously found values we are able to derive the Cross sectional area of the frame which was 1.2 by 0.1 inches, as that’s much too small to support the  shafts, we use a square shaft part with a height as large as the length of the Journal bearing for convenience. The length is 10 inches, as the distance between the two pulley’s is 5 inches, and the total distance from end to end of the pulley’s is 8 inches, the final Length was decided as 10 inches, giving 1 inch of clearance on either side.  The width just had to be large enough to support the gears and journal bearing, and 4 inches is more than enough for that task.
	
<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/9182103b-b31f-470c-bcf9-f46b351cd1ce" />


# Communicate 

 


As for Lessons Learned from this project, I had learned about the differences in Journal bearing materials. Before I was unaware what Journal bearings are, and through this assignment I learned not only how their used but how solid materials are able to absorb oils and such.

Link to the external website used:https://www.gates.com/content/dam/documents-library/catalogs/polyurethane-belt-program-catalogue-K1012-en.pdf



PDF of A9:



