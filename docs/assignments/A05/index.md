# A5 – Bracket Design

The T-beam below has the given parameters for which we are tasked with building a bracket around to hold a given load. The design for the bracket is below and is to be broken up into 5 separate features to be evaluated separately to find the cross-sectional area dimensions, with the length decided beforehand based on design needs. The load is a Polyester strap that is designed to hold a given load from 500 to 800 lb. force with a safety factor of 4; based on the diagram, the downward force experienced by the strap is 2 times the force. The given materials to choose from for the construction are Aluminum 6061-T6, Steel (ASTM A36), or Titanium (Ti 6Al – V4). The dimensions are calculated twice, given two different parameters: one is to not exceed the max stress of the given material, and the other is to not exceed a max deformation of 0.005 inches. The values of a, b and c are given below with their given tolerances

<img width="974" height="639" alt="image" src="https://github.com/user-attachments/assets/90462f35-01db-4176-b97b-39276e930621" />

This is the given model the bracket is based on; it is to be broken up into 5 features as shown. Instead of naming them feature A and so on, I chose to number them. Instead of A, B, C, D, and E, I have features 1,2, 3, 4, and 5, starting from feature A as feature 1

<img width="974" height="885" alt="image" src="https://github.com/user-attachments/assets/c93c76b2-e8e7-414f-91c3-dc0fd33c8edd" />

## Stress Analysis 

As Project A6 states, I begin by finding the dimensions based on the maximum stress the system can handle. Since I want to avoid writing repeated steps and assumptions, a general information page was created containing the initial knowns and unknowns, along with the assumptions needed for the equations being used to be accurate. A diagram of the bracket in it’s entirety, the T bar, and the polyester strap where also included. As for the material I went with steel A36 as it doesn’t require extreme wear resistance and is very affordable for it’s given strength. Looking  up the material on (name website) It has a max stress of 36 ksi and will be used as the basis for my equations. 
As you can see there is a portion that says part 1, originally bot the stress and deflection calculations for dimensions where going to be done using 1 model for both calculations, and the general assumptions page was going to be split accordingly. However to avoid overcrowding on each page that idea was scrapped, though you can still see the deflection under the knowns section, as I hadn’t erased it like I had thought. As for the Force on the polyester strap, it was decided to be 600 lb. force, based on the polyester strap's max strength. The straps given in the website were rated for 1475lb force, and as the load on the straps is two times the force, anything above 700 lb. of force would break the straps.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/73fb85e1-303b-4749-a4e6-1a28404c3b5c" />

While a starting feature wasn’t designated, it was suggested to begin with Feature 1, as its diameter will give the length dimensions in Feature 2, eliminating 1 dimension of the cross-sectional area. The length wasn’t given, so using the length of the strap, a slip buffer of 1 full strap length on either side of the strap was given. As the strap length is ¾ in, the beam length being 3 times that is 9/4 in or 2.25 inches. Using the given equation from the assignment and multiplying by a safety factor of 4, I’m able to solve for the radius, which was 0.576 in or a diameter of 1.152 in. And as for the Force, as there are only 2 forces acting in the z direction, the force which is named F1 is equal to the load, which is 1200lb force.

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/b162783b-dd43-4e8e-a8fc-681b2634cc1e" />

For Feature 2, using the diameter as the base dimension for the equation of cross-sectional area, A = b*h.  The length was decided to be 1.65 in to give a little over an inch of clearance between feature 1 and feature 3, although there was a lot of freedom, as the actual required clearance for the strap to fit is very small. After solving for the equation using the equation Sy = F/A and rearranging it to find h while multiplying by a safety factor of 4, we find h to be 0.1157 in. As the load is applied directly opposed by a force in the vertical direction, the force from Feature 1, or F1 is equal to the Force opposing it, or F2.

<img width="722" height="964" alt="image" src="https://github.com/user-attachments/assets/bf2cab18-442f-4910-9ca4-91fd355a2f22" />

## Analyze


## Decide


## Communicate

