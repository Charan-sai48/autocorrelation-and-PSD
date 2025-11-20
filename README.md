# autocorrelation-and-PSD
## AIM:
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor<BR>
•	SCI LAB

## THEORY:
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.

<img width="582" height="91" alt="image" src="https://github.com/user-attachments/assets/1f831c6a-7227-4886-93c5-96afe7f80d9b" />

## Algorithm
1.	Load or Define the Signal: Input your time-domain signal.
2.	Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3.	Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4.	Plot Results: Visualize the autocorrelation function and PSD.

## PROGRAM
```
t=0:0.01:6.28;
x=sin(1.7*t)+cos(4.1*t);
subplot(3,2,1);
plot(x);
au=xcorr(x,x);
subplot(3,2,2);
plot(au);
psd=fft(au);
subplot(3,2,3);
plot(abs(psd));
fw=fft(x);
subplot(3,2,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
```

## OUTPUT
<img width="755" height="620" alt="AC-6 SS" src="https://github.com/user-attachments/assets/d709b289-f70c-47ef-be32-f5480d8249ee" />


## RESULT
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
 
