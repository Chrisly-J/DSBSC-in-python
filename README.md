# DSBSC-in-Python

## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries. 

## EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer


## Algorithm:


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program
```
import  numpy as np
import matplotlib.pyplot as plt
Am=6.3
fm=503
Ac=12.6
fc=5030
fs=50300
t=np.arange(0, 2/fm, 1/fs)
m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*3.14*fc*t)
s2=(Ac-m)*np.cos(2*3.14*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
```

## Output Graph

<img width="710" height="546" alt="image" src="https://github.com/user-attachments/assets/594e4cd4-8682-4973-bf57-509b41c3916c" />

## Tablular Column

<img width="625" height="442" alt="Screenshot 2025-11-04 230940" src="https://github.com/user-attachments/assets/e16da9d6-a22f-46e2-aa73-e0846c33d7ce" />

## Result

Thus the DSB-SC-AM Modulation is generated using python.

