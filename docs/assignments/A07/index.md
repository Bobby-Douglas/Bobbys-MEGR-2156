# A7 – FEA

## Topic: Bracket FEA

The objective the assignment known as A7 is to use the information and designs for the Bracket from the previous A6 and A5 assignments and alter them based on FEA models. While hand math was used in the sketch and eventual 3d dimensions of the bracket part, the Finite Element Analysis will be used to improve upon the design and fix any errors made previously. Not only refine the geometry but also reduce the mass while staying within the given max deflection, and other parameters.

A7 asks that each design iteration is ran 3 times or within a 7% error, using different meshes ranging from coarse to fine in order to improve accuracy. The Bracket is to be iterated a minimum of 3 times, making it as lightweight as possible.  If the bracket Tabulations don’t converge within 7 percent, then the finest mesh is to be used to fill in the chart. The mesh size for each iteration goes from 1 inch to 0.5 inches to 0.25 inches. The Charts measure max deflection and Stress and their location, mass, Safety factor, and the number of elements on the final mesh size. The material being used, like before, is Steel A36; the max stress is 36,000 psi, and the max deflection for any given part is 0.05 in 

<img width="974" height="1034" alt="image" src="https://github.com/user-attachments/assets/f96549e7-46eb-43af-bbec-14866f87daba" />


## Part 1: Bracket Redesign

As the project suggests, the first design is to act as the baseline and will be the original 3D CAD design from A6. First, the preprocessing steps come into place, first going to the Analysis tab and clicking on Simulate, where the displacement function is used to lock the internal measurements meant for the T beam in place. Then the load applied by the strap holding 1200 pounds of force is added to Feature 1 as stated in previous assignments. Then the mesh is added with a mesh of 1 inch to start off; after that, the analysis is run.

 This brings up an important point: for each design, only around 2 photos were taken; to an extent, each photo became repeatedly redundant, and after looking at the first one, the general theme of stress and deflection placement becomes clear. 

 <img width="975" height="578" alt="image" src="https://github.com/user-attachments/assets/abaeb58e-6271-4dd6-8156-b321e4e1ca41" />

Here is the Von Mises stress analysis of the Bracket, as shown for the first run of the design. The bracket faces an enormous amount of stress in the lengthy and skinny portion known as feature 2. The thought that some calculations during the initial geometric configuration in A5 had crossed my mind; however, this proves it and requires reconstruction. Running this design iteration 3 more times, while the displacement converged, the stress never did. The final result was a displacement of 0.922065 inches, a max stress of 2.22e^8 psi, a safety factor of 0.000162, and a mass of 1.264 pounds mass. This is far beyond what my bracket was designed to handle, so for the second design iteration, I adjusted the width of Feature 2.

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/1a6bdfd1-e5ca-4a77-a115-223bae46a684" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/a9d2cadb-7578-43ee-8025-3076e0ed1f37" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/3541139b-e1a6-4be9-b1e2-46663c536e61" />

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/6e758dfe-32b0-4299-b27e-7424c4e23e98" />

At design iteration 2, the width of feature 2 increased from 0.1157 inches to 0.5 inches to reduce the load due to the load, as seen in design one the majority of the deflection was in the very middle suggesting the feature was getting pulled apart. Adding material to try and combat this, the first attempt at changing the design added more material. After running the analysis, two important changes were noticed within the model. The displacement dropped to 0.0136 inches, which is well within range for the deflection; however, the stress was still way too high, using the fine mesh as the final results, as the model's stresses don’t converge. Although the location of the stress change was originally located in the middle of feature 2, it now resides at the connection between feature 1 and 2 at 2.827e^7psi. Its safety factor is 0.0013, its mass is 1.41 pounds mass, and the number of elements is 5985.

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/bddba010-d00f-4b32-bc10-906fdd39b9dd" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/89b52b22-9617-4b2c-94b7-bb956adc2b2a" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/26ea927a-9a61-4e2b-9a61-57f117512a5d" />

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/9f2d1f02-ece9-40e9-949e-4c0ed02fc03e" />

Using Google, I asked what to do if the beam was failing at the connection between two features, and the suggestion was to add a bend to increase the thickness of the part as we get to the connection. 

<img width="974" height="1157" alt="image" src="https://github.com/user-attachments/assets/55743210-499d-4d20-9fc2-5842d9e6fc6e" />

In the 3rd design iteration, 5 major changes were made to improve the strength of the part and reduce the stress. First, the diameter was changed to 2.5 inches of Feature 1, I adjusted the width from 0.5 inches to 1.25 inches on feature 2 and adjusted the width to the same length as the diameter. The height was reduced from 1.65 inches to 1.25 inches, and a 0.25 radius was added to the connection point between Feature 1 and 2. The width of the top portion as a whole was changed 
from about 2 inches to 3.2 inches, and the base thickness of Feature 3 was adjusted to 0.5 inches. 

The result was a displacement of   2.14e^-4, a stress of 5695.79 psi, a safety factor of 6.32, and 12255 elements. All well within the parameters given for the piece.  However, the mass is about 4 times greater at 4.974 pounds mass. As the goal was to improve stiffness, reduce stress, and reduce mass, one more iteration was required.

<img width="975" height="578" alt="image" src="https://github.com/user-attachments/assets/57d6a295-f86a-4721-9cdb-5b0fd9ad6024" />

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/4515a67d-02cf-48ec-acfa-fdd55e3e804b" />


For the 4th and final design iteration to reduce weight, a principle from Solid Mechanics was Utilized. As the material at the core of a beam hardly participates in taking the stress load, hollowing out Feature 1 and 2 would not only greatly reduce weight but even possibly improve the moment of inertia, which therefore reduces the stress on the beam according to the equation I = (pi/64)(d2^2-d1^2). For Feature 1, a hole with a diameter of 1.8 inches was punched through the middle, and for Feature 2, a triangular gap with a width of 2 inches, and a thickness of 0.75 inches was.
After analysis, running meshes from coarse to fine, the finest mesh was used, as the runs didn’t converge. The displacement was 9.374e^-4 inches; the Stress was 10711.3 psi, the safety factor was 3.36, and the number of elements was 11,575. While not an ideal Safety factor, the mass was cut down to 2.9 pounds mass, a 2-pound difference, which is worth the slight underperformance of the parameter. 

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/054042dc-c834-47e7-a590-0eda28fbf777" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/b26b5c1a-845e-4a27-836c-ee59bd5fb4b6" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/6cea35df-9e63-4d8e-adbe-45caf38a3cf0" />

<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/77ae001d-eb44-4454-8c74-2d6f5d7ee74c" />

Here is a quick table with the Stress, deflection, Locations of both, mass, Safety factor, and number of elements.

<img width="893" height="414" alt="Screenshot 2026-10-27 121630" src="https://github.com/user-attachments/assets/1c05c3ab-8b5b-4c9e-8a5f-d761e2070aa7" />

### Reflection

From these Design iterations, many important lessons were learned in perfecting the 3D model Bracket. When dealing with a perpendicular connection between 2 connecting features, a method to reduce the stress at the connection is to create a bend to slowly increase the size of a feature at that bend and decrease the likelihood of failure. Sometimes, when creating certain design specifications, your initial geometry can be off by a mile; whether that was a reflection of poor use of equations or not, it still shows that double-checking in the sketch phase is important to save time later down the line. A hollow beam, to an extent, reduces stress the same amount as a solid beam; therefore, to save material, hollow beams are preferable. These are some of the lessons learned while designing the Bracket. This assignment took 15 hours to complete, 5 of which were wasted figuring out the requirements to simulate features and procrastination. 

## Topic: Linkage FEA

To complete the topic section of A7, the same process applied to the bracket is to be repeated on the Linkage portion from previous A sections. The material is to stay the same, a minimum of 3 design iterations are necessary with a minimum of 3 mesh fields from coarse to fine. 


<img width="974" height="569" alt="image" src="https://github.com/user-attachments/assets/68e6dd32-6f3f-4db8-af5d-aeceb2f031a6" />


Starting with the Original design, first an initial load of 1200 pounds-force is applied, and the set immovable displacement points are set. Then the Meshes are set; the sizing for the meshes, as the bracket model was unable to converge using the previous mesh sizes, they are dropped to the range of  0.5 inches,  0.25 inches, and finally 0.1 inches. After analyzing and running each individual mesh, convergence between runs weren’t within 7 % so the fine mesh results were taken as the final result.
Its displacement was 3.960e^-6 in, its stress was 1198.40 psi, its safety factor was 30.04, and the number of elements was 20,118 with a mass of just 3.156e^-1. The design itself wasn’t particularly bad; however, as 3 design iterations are required, some changes are to be made.


<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/4729a971-f501-486a-9711-459ec66f83c6" />


<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/1fdffb7d-b6d9-4a73-aceb-a71bc4c8859c" />

For the second 2nd design iteration, the width of the part was decreased to just 0.05  in, nothing else was changed of the model. Running the meshes and analyzing, the Displacement was 1.303e^-5; its stress was 1324.36 psi, its safety factor was 27.183, its mass was 1.498e^-1, and the number of elements was 10613. With the mass cut down, this is a successful model; however, 1 more iteration is required. Also, 1 calculation wasn’t included, and the stress was multiplied by e^-5; that was an error and is safe to ignore.


<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/3ce02466-d263-423e-828e-c0790d927a8d" />


<img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/b0a65ecd-173b-4e4c-93c0-8b832e53ae7f" />

The final change made to the design came in lowering the radius from 1.5 inches to 1.5 inches. Initial concerns for the structural integrity of the part where prevalent however it was still ran. After analyzing the deflection for this third iteration was 8.31e^-6 in, it’s stress was 1565.69 psi , it’s safety factor was 23, it’s mass was 6.566e^-2 pounds mass, and it’s number of elements was 4850. This piece perform much better than attended, and as  it’s stiffness, max stress, and weight efficiency are well within the limits, this is the final iteration.


<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/c8d86170-108d-4f6c-a969-59f3ad4c5cb4" />


<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/3b487350-cf00-459b-9c6d-f8527a43ab9d" />

<img width="974" height="579" alt="image" src="https://github.com/user-attachments/assets/5d1c853f-6da3-4c13-aa6d-f604d54069e5" />


  <img width="731" height="975" alt="image" src="https://github.com/user-attachments/assets/c209fd07-7792-464e-ab83-d452b3093ee8" />

These are the results and their corresponding locations and such.

<img width="689" height="421" alt="Screenshot 2026-10-27 122357" src="https://github.com/user-attachments/assets/c4c73931-4781-44af-b063-480f09869169" />

Here are the links to all the models and Analysis's used in Calculations 

### Models Folder: [A7hw.zip](https://github.com/user-attachments/files/34030852/A7hw.zip)

### PDF of document 
