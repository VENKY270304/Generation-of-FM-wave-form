## Aim
To generte Frequency modulated wave for given specification
## Tools Required
Python or MATLAB
## Procedure
1.Initialize the amplitude and frequency of carrier wave

2.Initialize the amplitude and frequency of Message signal

3.Initialize the frequency deviation delta.

4.Initialize the time duration

5.Plot the FM wave

## Code
```python
import numpy as np
import matplotlib.pyplot as plt
A_c = 1  # Carrier amplitude
f_c = 100  # Carrier frequency (Hz)
f_m = 10  # Message frequency (Hz)
delta_f = 50  # Frequency deviation (Hz)
T = 1  # Duration of the signal (in seconds)
fs = 1000  # Sampling frequency
t = np.linspace(0, T, int(fs * T), endpoint=False)
m_t = np.sin(2 * np.pi * f_m * t)
s_t = A_c * np.cos(2 * np.pi * f_c * t + delta_f * m_t)
plt.figure(figsize=(10, 6))
plt.subplot(2, 1, 1)
plt.plot(t, m_t)
plt.title("Message Signal (m(t))")
plt.xlabel("Time [s]")
plt.ylabel("Amplitude")
plt.subplot(2, 1, 2)
plt.plot(t, s_t)
plt.title("FM Modulated Signal (s(t))")
plt.xlabel("Time [s]")
plt.ylabel("Amplitude")

plt.tight_layout()
plt.show()
```

##  Waveform
![image](https://github.com/user-attachments/assets/7a425bda-94e0-44ac-9009-d048304aab19)

## Result
The program executed sucessfully
