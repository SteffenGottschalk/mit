Erstellen Sie in Matlab oder Python ein Histogramm.
Okay, gerne zeige ich Ihnen, wie man ein Histogramm sowohl in Matlab als auch in Python erstellt.

### Matlab

In Matlab können Sie ein Histogramm mit der Funktion `histogram` erstellen. Hier ist ein einfaches Beispiel:

```matlab
% Erzeugung von zufälligen Daten
data = randn(1000, 1);  % 1000 zufällige Datenpunkte aus einer Normalverteilung

% Histogramm erstellen
histogram(data, 'BinWidth', 0.5);  % BinWidth bestimmt die Breite der Bins im Histogramm
xlabel('Datenwerte');
ylabel('Häufigkeit');
title('Histogramm der zufälligen Daten');
```

### Python (mit Matplotlib)

In Python verwenden wir Matplotlib, um ein Histogramm zu erstellen. Hier ist ein ähnliches Beispiel:

```python
import matplotlib.pyplot as plt
import numpy as np

# Erzeugung von zufälligen Daten
data = np.random.randn(1000)  # 1000 zufällige Datenpunkte aus einer Normalverteilung

# Histogramm erstellen
plt.hist(data, bins=30, edgecolor='black')  # bins gibt die Anzahl der Bins im Histogramm an
plt.xlabel('Datenwerte')
plt.ylabel('Häufigkeit')
plt.title('Histogramm der zufälligen Daten')
plt.grid(True)
plt.show()
```

### Erklärung

- **Matlab**: Die Funktion `histogram` erstellt das Histogramm direkt. Sie können die Anzahl der Bins oder die Bin-Breite mit Parametern wie `NumBins` oder `BinWidth` steuern.
- **Python**: Die Funktion `plt.hist` aus Matplotlib erstellt das Histogramm. Sie können die Anzahl der Bins mit dem Parameter `bins` festlegen.

Beide Beispiele erzeugen ein Histogramm der zufälligen Daten und beschriften die Achsen sowie den Titel des Diagramms. Sie können die Parameter und Optionen je nach Bedarf anpassen, um das Aussehen und Verhalten des Histogramms zu ändern.
