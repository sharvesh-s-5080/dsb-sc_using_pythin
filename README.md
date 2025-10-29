# DSB-SC USING PYTHON
# Aim

To implement and analyze Double Sideband Suppressed Carrier (DSB-SC) modulation using Python’s NumPy and Matplotlib libraries.

# Apparatus Required

Software: Python with NumPy and Matplotlib libraries Hardware: Personal Computer

# Theory

Double Sideband Suppressed Carrier (DSB-SC) is a type of amplitude modulation where the carrier signal is suppressed, and only the sidebands (which contain the information) are transmitted.

<img width="864" height="538" alt="505732129-38453f40-70c0-4697-b347-10cc10c0db6c" src="https://github.com/user-attachments/assets/103174f4-474b-45e5-b11d-271f08072f89" />

<img width="815" height="471" alt="505732196-47223c8c-4587-402f-8703-3dccd7d8c4e8" src="https://github.com/user-attachments/assets/280ffb09-3177-4ec4-915a-bf50948ae07e" />


# PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
Am = 5.4
Ac = 10.8
fm = 434
fc = 4340
fs = 43400
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.figure(figsize=(10, 6))
plt.subplot(3,1,1)
plt.plot(t, m)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.subplot(3,1,2)
plt.plot(t, c)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.subplot(3,1,3)
plt.plot(t, s)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.tight_layout()
plt.show()
```
# OUTPUT WAVEFORM:

<img width="989" height="590" alt="download" src="https://github.com/user-attachments/assets/d7e2eade-010d-438a-9ede-686245592b96" />


# TABULATION:


# RESULT:

Thus, Double Sideband Suppressed Carrier (DSB-SC) modulation was successfully implemented using Python’s NumPy and Matplotlib libraries, and the message, carrier, and modulated waveforms were plotted and analyzed.
