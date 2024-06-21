Um ein Signal in MATLAB oder Python zu filtern und die Energie bei 5 Hz zu reduzieren, kann ein Hochpass- oder Bandsperrfilter verwendet werden. Hier zeige ich Ihnen beide Methoden in MATLAB und Python.

### MATLAB

```matlab
% Beispiel-Signal erzeugen
Fs = 100;                % Abtastrate in Hz
t = 0:1/Fs:10-1/Fs;      % Zeitvektor
f1 = 5;                  % Störfrequenz
f2 = 15;                 % Nutzfrequenz
signal = sin(2*pi*f1*t) + sin(2*pi*f2*t);  % Signal mit 5 Hz und 15 Hz Komponenten

% Hochpassfilter entwerfen
fc = 5;  % Grenzfrequenz in Hz
[b, a] = butter(4, fc/(Fs/2), 'high');  % 4. Ordnung Butterworth Hochpassfilter

% Signal filtern
filtered_signal = filtfilt(b, a, signal);

% Signale plotten
figure;
subplot(2, 1, 1);
plot(t, signal);
title('Originales Signal');
xlabel('Zeit (s)');
ylabel('Amplitude');

subplot(2, 1, 2);
plot(t, filtered_signal);
title('Gefiltertes Signal');
xlabel('Zeit (s)');
ylabel('Amplitude');
```

### Python

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import butter, filtfilt

# Beispiel-Signal erzeugen
Fs = 100  # Abtastrate in Hz
t = np.arange(0, 10, 1/Fs)  # Zeitvektor
f1 = 5  # Störfrequenz
f2 = 15  # Nutzfrequenz
signal = np.sin(2 * np.pi * f1 * t) + np.sin(2 * np.pi * f2 * t)  # Signal mit 5 Hz und 15 Hz Komponenten

# Hochpassfilter entwerfen
fc = 5  # Grenzfrequenz in Hz
b, a = butter(4, fc / (Fs / 2), btype='high')  # 4. Ordnung Butterworth Hochpassfilter

# Signal filtern
filtered_signal = filtfilt(b, a, signal)

# Signale plotten
plt.figure(figsize=(12, 6))
plt.subplot(2, 1, 1)
plt.plot(t, signal)
plt.title('Originales Signal')
plt.xlabel('Zeit (s)')
plt.ylabel('Amplitude')

plt.subplot(2, 1, 2)
plt.plot(t, filtered_signal)
plt.title('Gefiltertes Signal')
plt.xlabel('Zeit (s)')
plt.ylabel('Amplitude')

plt.tight_layout()
plt.show()
```

Diese Skripte erzeugen ein Beispiel-Signal mit einer Störfrequenz von 5 Hz und einer Nutzfrequenz von 15 Hz. Sie entwerfen und wenden einen Hochpassfilter an, um die Energie bei 5 Hz zu reduzieren, und stellen das gefilterte Signal im Zeitverlauf dar.
