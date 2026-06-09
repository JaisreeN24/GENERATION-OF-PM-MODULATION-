# Phase-Modulation

# EXP NO: 7	GENERATION AND DETECTION OF PM

## AIM:

To write a program for Phase Modulation and Demodulation using SCILAB.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY:

## PHASE MODULATION (PM):

Phase modulation is a type of modulation in which the phase of the high frequency (carrier) signal is varied in accordance with the instantaneous value of the modulating signal.

### PHASE DEVIATION (Δθ) AND MODULATION INDEX (mp):

The phase deviation Δθ represents the maximum change in phase of the carrier signal caused by the modulating signal.

We define the modulation index mp as the ratio of phase deviation to the amplitude of the modulating signal.

mp = Δθ

(Phase modulation index is measured in radians.)

### Note:
Keep all the switch faults in OFF position.

## PHASE MODULATION GENERATION:

The circuits used to generate phase modulation must vary the phase of a high frequency signal (carrier) as a function of the amplitude of a low frequency signal (modulating signal). In practice, different methods are used to generate PM signals.

## Algorithm:1. Define Parameters:

· Fs: Sampling frequency.

· T: Duration of the signal.

· Fc: Carrier frequency.

· Fm: Frequency of the modulating signal.

· Mp: Phase modulation index, which controls the extent of phase deviation.

2. Generate Signals:

· modulating_signal: Sinusoidal signal used for modulation.

· carrier_signal: The high-frequency carrier signal.

· modulated_signal: PM modulated signal calculated by varying the phase of the carrier signal according to the modulating signal.

3. Phase Modulation:

· modulated_signal is obtained by phase modulating the carrier signal with the modulating signal.

4. Phase Demodulation:

· Phase Detection: Extracts the phase variations from the PM signal.

· Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.

· Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the signal and recover the original modulating signal.

5. Visualization:

· Plots the modulating signal, carrier signal, PM modulated signal, and demodulated signal for analysis.

## Program
```
Am=14.6;
fm=1578;
fs=157800;
t=0:1/fs:2/fm;
Ac=21.9;
fc=15780;
B=5.1;
em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);
efm=Ac*cos((2*3.14*fc*t)+B*sin(2*3.14*fm*t)); 
subplot(4,1,3);
plot(t,efm);
epm=Ac*cos((2*3.14*fc*t)+B*cos(2*3.14*fm*t));
subplot(4,1,4);
plot(t,epm);

```


## Output Waveform:
<img width="1919" height="1121" alt="image" src="https://github.com/user-attachments/assets/cfa6a977-4d96-4ef9-bbd0-9992170408ad" />




## RESULT:
Thus the frequency modulation and demodulation is successfully done and the output is experimentally verified.
