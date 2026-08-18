# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
clear;
clc;

// 1. Define the discrete time sequence x[n]
// For example: x = [1, 2, 3, 4] at time n = [0, 1, 2, 3]
x = [1, 2, 3, 4];
n = 0:length(x)-1;

// 2. Define frequency range from -pi to pi (e.g., 500 points)
omega = linspace(-%pi, %pi, 500);

// 3. Compute DTFT using matrix multiplication
// X_dtft will store the complex Fourier values
X_dtft = x * exp(-%i * n' * omega);

// 4. Calculate Magnitude and Phase
mag = abs(X_dtft);
phase = atan(imag(X_dtft), real(X_dtft));

// 5. Plotting the results
scf(0); // Open new figure

// Plot Magnitude Spectrum
subplot(2, 1, 1);
plot2d(omega, mag, style=2); // style=2 plots in blue
xtitle("Magnitude Spectrum", "Frequency (\omega)", "|X(\omega)|");
xgrid();

// Plot Phase Spectrum
subplot(2, 1, 2);
plot2d(omega, phase, style=5); // style=5 plots in red
xtitle("Phase Spectrum", "Frequency (\omega)", "Phase (radians)");
xgrid();





<br>
### CALCULATIONS:
<img width="899" height="1599" alt="WhatsApp Image 2026-08-18 at 09 16 02" src="https://github.com/user-attachments/assets/dcefcfcd-b873-43b3-8f3d-a655de1f619a" />

### SAMPLE OUTPUT:
<img width="1600" height="888" alt="WhatsApp Image 2026-08-08 at 08 53 59" src="https://github.com/user-attachments/assets/69dfed57-5448-4f66-8de5-130749bd3ff9" />




## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

