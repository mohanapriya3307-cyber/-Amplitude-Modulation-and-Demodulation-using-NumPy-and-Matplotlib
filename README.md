# -Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib

__Aim__: 

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

__Apparatus Required__: 

Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 

__Theory__: 

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 


__Algorithm__:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Program__:
```
import numpy as np
import matplotlib.pyplot as plt
Am = 8
fm = 460
Ac = 16
fc = 4600
fs = 47400
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
````
__Tabulation__:

<img width="1082" height="714" alt="image" src="https://github.com/user-attachments/assets/01ede976-1514-4625-9497-a9c1594a7089" />

 __Output__:

<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/bbef5335-0300-4062-b263-e6d163eeefe7" />


 __Result__:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus, AM is implemented using numPy and Matplotlib.

