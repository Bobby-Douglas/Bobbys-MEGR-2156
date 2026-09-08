# A3 – Parametric and FEA

## Part 1

<img width="716" height="86" alt="image" src="https://github.com/user-attachments/assets/48258de8-7990-4ccf-96b3-6cfbff51d8a4" />

The objective of this project is to design a bar with a circular cross section where the values of the criteria are give for the material, maximum deflection and load. Determines the bars minimum length due to area and the load it faces under direct tension. The given Material was Aluminum without a specified mass, a Modulus of Elasticity (E) of 9.5 *10^6 psi, a load of 400 pound force, and a max axial deflection of 0.009 in. The cross sectional area was chosen after heavily analyzing the outline. Google was used to get a second opinion on how the initial cross sectional area was found, typing in part a of part 1 “ a. (5%) Choose the values for the cross sectional area of the bar. (width, height, and thickness)”. The beam in question was specified to be a circular beam as prompted by the instructions 

<img width="975" height="1300" alt="image" src="https://github.com/user-attachments/assets/74457f8c-f232-48bc-ab46-3b7394fe174f" />

The diameter was chosen by me to be 1 in, the cross-sectional area was determined to be 0.785 in^2.  Using the direct tension elongation equation δ = PL/AE and reconfiguring it, the length was found to be 167.8 inches or over 13 ft long. 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/f1b3ae4a-932d-48e0-8d2e-2dd37c7f413b" />


Heading over to the CAD software Creo Parametric, I inserted the cross-sectional area as chosen. Oddly the sketch was done before the extrude which nagged my mind the entire process, but not enough to change it. 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/d6a566aa-1d74-42f6-a234-483d4b81bf60" />

I originally inserted the exact length as derived, but instructions required that the CAD model generate the Length using the aforementioned constraints automatically. Using ChatGPT I put in the following prompts to learn how to automatically change the length in Creo parametric. “How to use Creo Software to find the Length of a circular beam using the direct tensions elongation equation” and “I’m using Creo Parametric 12.4, which Creo are you referencing”, the second prompt which was after I couldn’t find a button that Chatgpt kept referring to. 

<img width="974" height="959" alt="image" src="https://github.com/user-attachments/assets/13c16b14-18f9-40ce-8c74-ded8819d2f72" />

Going into Tools, then relations I typed in the given equations by Chatgpt, however there were 5 issues. I representing the area which didn’t make sense, the I equation was incorrect for the area of a circle. L which stood for length was incorrect, the correct equation was L = AEδ/P. d1 and d2 where invalid due to them referencing length parameters that were never determined. 

<img width="974" height="959" alt="image" src="https://github.com/user-attachments/assets/d6547747-b7b0-44fd-891e-be46ec58eda3" />

Revamping the Relations A = the circle area equation, L was derived from direct tension elongation equation, and d1I  placed equal to L; where d1I is the extrude distance.

<img width="975" height="784" alt="image" src="https://github.com/user-attachments/assets/178223e9-2390-44a4-af58-b266f2da95b3" />

Going tools, then in parameters, the parameters E for Modulus of Elasticity, DIAMETER, DEFMAX for the max deflection, A for Area. L is locked due to it being in Relation, it changes based on the changes of diameter.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/3c308171-2f9b-4511-ac42-ee51f91657a2" />

After setting the extrusion equal to L, Creo Parametric derives the length to be equal 167.8788574262 in. or around 1 inch larger then I calculated. 

<img width="566" height="1010" alt="image" src="https://github.com/user-attachments/assets/0c6d7851-f89a-403c-9286-5e2ff4a5773f" />

I then apply the given tension load by going to applications, then simulate and apply the load in the z direction to the surface edge at a load of 400 pounds force.

<img width="975" height="1159" alt="image" src="https://github.com/user-attachments/assets/edf15398-ad39-48bd-9f8e-99203a2cc030" />

<img width="316" height="629" alt="image" src="https://github.com/user-attachments/assets/cb8a9847-5f40-4b2b-95ec-218f8f3f18d5" />

I then set the constraints of the beam, going to Home then displacement under constraints. I add the material as aluminum for the material constraint.

## Part 2

<img width="975" height="1159" alt="image" src="https://github.com/user-attachments/assets/c082e3a8-a79c-4c54-aef4-9e6beebc0cd1" />

Finally at the FEA Models, going to application then simulate, after running the simulation go to view results. From there pick a Displacement model and click ok, now that brings up the deflection curve. The deflection recorded verses the deflection originally given differ by 0.00138 in.

<img width="975" height="1159" alt="image" src="https://github.com/user-attachments/assets/cbf2cb76-0cf0-46fc-9bf6-0eb330be8473" />

Following the same process as before except when picking the model, click stress and in the box to the right click von Mises. This brings up the Von Mises Stress Curve FEA, and before hitting ok hit contour and deformation to add the contour lines like this. 

## Part 3

<img width="732" height="975" alt="image" src="https://github.com/user-attachments/assets/fa5c23c5-dadd-46da-a952-c87325746d2e" />

The axial deflection based on my hand calculations were given as 0.009 in vs the simulated axial deflection which was 0.01038. A difference of 0.00138 in, the percent difference as solved by hand was calculated to 15.33 percent. The most likely reason was the due to minor rounding errors throughout and material property, as I used a pre-loaded aluminum material which might have had a slightly different Modulus of Elasticity as the one used for my calculations was chosen out of a range from 8.5 to 11.5 *10^6. While 15 percent is higher than expected I would trust my hand calculations more. The modulus of elasticity is in a range and I am unaware of the preloaded modulus for aluminum on the simulation, so I would rather run through the calculation by hand than rely on the computer who has a currently unknown input in the range. As I have ran out of time I am unable to complete part b of part 3 but I can say for certainty that with an additional pinhole this would not pass the safety factor as the beam itself didn’t pass the safety factor to begin with.

## Part 4

Through this I have learned valuable Creo Parametric simulation skills that will benefit me in the future. My biggest challenge throughout this process was proper documentation and saving my progress. I constantly had to go back to screenshot different sections of my work which in hindsight wasted a lot of time. I spent a total of 10 hours on this, with mostly wasted on remaking cad models and having to go back record different steps. 

## Section 2: Modifying Parameters 

Modifying Design Parameters, changing the width as according to directions while maintaining the same material, E value, Load value, and DEFMAX to see how the length of the beam changes accordingly.

<img width="975" height="784" alt="image" src="https://github.com/user-attachments/assets/b391a842-b857-4a6d-b6e6-d4f245dc6529" />

<img width="975" height="784" alt="image" src="https://github.com/user-attachments/assets/ec96fdb2-d74e-48ef-a5ac-10432da07bdb" />

I duplicated the first model and after saving the copy, go to the top menu, go to tools then parameters and switch the Diameter from 1 inch to 5 inches. My initial assumption based on the restructured direct tension elongation equation L = δAE/P,  is that the beam size will grow. As the cross sectional area grows bigger the Length will too as they are directly proportional to each other.

<img width="975" height="784" alt="image" src="https://github.com/user-attachments/assets/99983126-2e14-40ee-80da-459e1b2684e5" />

After Resetting the model as predicted the Length increases in a directly proportional relationship to the cross sectional area. However It increased in a exponential way which wasn’t something I had initially guessed; though thinking about it now makes logical sense due to the nature of the Area of a circle equation.

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/527585dd-1784-4b10-91ba-e10c5d0a73aa" />

The beam after the increase of extrusion showing that the formula put in works as expected. 

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/3cd26df5-c6b2-449d-8c51-6ffa6406419b" />

<img width="975" height="579" alt="image" src="https://github.com/user-attachments/assets/185b0995-08cf-45fc-81fb-0c98e0847a70" />

Just like before I ran both a simulation on the new beam, using said simulation made both a deflection and Von Mises graph without contour lines. The deflection throughout the beam is much smaller than previously despite being tens of times larger, and the physical stress is more than a thousand times smaller than the first model.

### Here are the CAD files for this project: [A3 files.zip](https://github.com/user-attachments/files/31956372/A3.files.zip)

### Here is the PDF file of this document


