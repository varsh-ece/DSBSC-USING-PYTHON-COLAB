# DSBSC-USING-PYTHON-COLAB

# AIM:
o implement and analyze DOUBLE SIDE BAND SUPPRESSED CARRIER (DSBSC) using Python's NumPy and Matplotlib libraries.

# EQUIPMENTS REQUIRED
•personal computer
. software: python with numpy and mathplotlib libraries

# THEORY:
Double Sideband Suppressed Carrier (DSB-SC) is an amplitude modulation technique where the carrier signal is completely suppressed, and only the sidebands containing the message information are transmitted. It is more power-efficient than standard AM but requires a synchronized carrier at the receiver for proper demodulation.

# PROCEDURE

Initialize Parameters: Set the values for message amplitude, carrier amplitude, message frequency, carrier frequency, and sampling frequency.

Generate Time Axis: Create a time vector for the duration of the signal.

Generate Message Signal: Define the message signal as a cosine wave.

Generate Carrier Signal: Define the carrier signal as a cosine wave with a higher frequency.

Generate DSB-SC Signal: Multiply the message signal and carrier signal to produce the Double Sideband Suppressed Carrier (DSB-SC) modulated signal.

Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and the DSB-SC modulated signal.

# Program:

```
import numpy as np
import matplotlib.pyplot as plt

Am=3.6
Fm=151
Ac=7.2
Fs=15100
Fc=1510

t=np.arange(0,2/Fm,1/Fs)

m=Am*np.cos(2*np.pi*Fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*Fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1 = (Ac + m) * np.cos(2 * np.pi * Fc * t)
s2=(Ac-m)*np.cos(2*np.pi*Fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
```

# Output Waveform
<img width="1062" height="603" alt="image" src="https://github.com/user-attachments/assets/0d6ae95b-8ebc-4eb5-b7af-0a8b366f430c" />


Tabulation :

<img width="705" height="439" alt="image" src="https://github.com/user-attachments/assets/8941f3dd-697d-420a-a323-612b596c442b" />




RESULT:

The DSB-SC modulated signal was successfully generated. The output shows suppression of the carrier, with only the sidebands carrying the message information clearly visible in the waveform.
