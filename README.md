# RADAR-RANGE-EQUATION
## Aim
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Scilab programming.

## Theory
The Radar Range Equation is a key relationship used in radar system design to determine the maximum distance (range) at which a radar can detect a target.

It is expressed as:

<img width="965" height="329" alt="image" src="https://github.com/user-attachments/assets/c6210d9d-a821-4f47-9716-864db1cc157e" />

## Algorithm
Initialize constants:

λ (wavelength) = 0.03 m
σ (radar cross section) = 1 m²
Vary each parameter while keeping the others constant:

Pt: 0.1 → 10
Gt: 1 → 50
Pm: 1e⁻¹⁵ → 1e⁻¹⁰
Compute maximum range using: R_max = ((Pt * Gt² * λ² * σ) / ((4π)³ * Pm))¼

Plot the following:

Pt vs Rmax
Gt vs Rmax
Pm vs Rmax
## Procedure
Refer to the Algorithm and write the Scilab code for the experiment.
Open Scilab on your system.
Create a New Editor File:
Go to File → New → Script.
Type Your Code in the editor window.
Save the File with a suitable name (e.g., radar_range.sce).
Execute the Code:
Press F5 or click Execute → File with echo.
If Any Errors Occur:
Review and correct the code.
Save and run it again until it executes successfully.
## Code
Gr = 30;
l = 0.03;
sigma = 1;  
pmin = 1e-10;
Gt = 30;
Pt = 0.5:0.5:100;   
Rmax1 = (((Pt .* Gt .* Gr .* (l.^2).* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,1);
plot(Pt, Rmax1);
Pt = 16;
Gt = 0.1:0.1:9;     
Rmax2 = (((Pt .* Gt .* Gr .* (l.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,2);
plot(Gt, Rmax2);
Gt = 14;
pmin = 1e-14:1e-13:1e-9;  
Rmax3 = (((Pt .* Gt .* Gr .* (l.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,3);
plot(pmin,Rmax3);




## Output
<img width="1706" height="1005" alt="image" src="https://github.com/user-attachments/assets/65c4d83b-fe13-4ea7-a31b-05a863606742" />

Manual Calculation
![WhatsApp Image 2025-12-03 at 13 33 40_9e70f08b](https://github.com/user-attachments/assets/ff8bd330-3a3d-4d39-b4c7-4a10f870a763)

![exp 10](https://github.com/user-attachments/assets/fab7b2ca-f676-4f2f-9013-3331a5f43717)

Result
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
