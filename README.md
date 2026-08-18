# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM

// Clear environment and console

clear;

clc;

// 1. Define the discrete time sequence x[n]

fs = 1000; // Sampling frequency (Hz)

t = (0:fs-1)/fs; // 1 second duration

x = sin(2*%pi*50*t) + sin(2*%pi*120*t); // Example signal with 50Hz & 120Hz



// 2. Compute FFT

N = length(x);
X_fft = fft(x, -1); // -1 for forward FFT

// 3. Frequency axis

freqs = (0:N-1) * (fs/N);


// 4. Magnitude Spectrum (only first half due to symmetry)

mag = abs(X_fft(1:N/2));


// 5. Plotting the results

scf(0);


// Plot Magnitude Spectrum

plot2d(freqs(1:N/2), mag, style=2);

xtitle("Spectral Analysis using FFT", "Frequency (Hz)", "|X(f)|");

xgrid();


### CALCULATIONS:
<img width="331" height="573" alt="image" src="https://github.com/user-attachments/assets/952096b6-713a-46bf-b26f-abba931cdbbd" />
<img width="315" height="474" alt="image" src="https://github.com/user-attachments/assets/99ec515e-f1ed-436b-a64c-1430f0c237c8" />




### SAMPLE OUTPUT:
<img width="998" height="772" alt="image" src="https://github.com/user-attachments/assets/49aaeea9-71db-4ba5-897d-f3d9d34fa405" />




## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.

