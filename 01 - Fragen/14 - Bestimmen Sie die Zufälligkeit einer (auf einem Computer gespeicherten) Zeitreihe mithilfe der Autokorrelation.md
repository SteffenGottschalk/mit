Um die Autokorrelation einer Zeitreihe in Python zu berechnen und die Zufälligkeit zu bestimmen, können wir die folgenden Schritte durchführen. Ich werde ein einfaches Beispiel mit Python und den Bibliotheken `numpy` und `matplotlib` zeigen.

Zuerst müssen wir die erforderlichen Bibliotheken importieren:

```python
import numpy as np
import matplotlib.pyplot as plt
```

Angenommen, wir haben eine Zeitreihe `X`, die wir betrachten möchten. Hier ist ein Beispiel, wie Sie die Autokorrelationsfunktion berechnen und grafisch darstellen können:

```python
# Beispielzeitreihe X (hier als zufällige Normalverteilung generiert)
np.random.seed(0)
X = np.random.randn(100)  # 100 zufällige Werte

# Berechnung der Autokorrelationsfunktion (ACF)
def autocorr(x, lag):
    return np.corrcoef(np.array([x[:-lag], x[lag:]]))

lags = range(1, 21)  # Bereich der Verzögerungen, z.B. von 1 bis 20

autocorr_values = [autocorr(X, lag)[0, 1] for lag in lags]

# Plot der Autokorrelationsfunktion
plt.figure(figsize=(10, 5))
plt.stem(lags, autocorr_values, use_line_collection=True)
plt.xlabel('Lag')
plt.ylabel('Autocorrelation')
plt.title('Autocorrelation Function')
plt.grid(True)
plt.show()
```

### Interpretation:

- In diesem Beispiel wird eine Zeitreihe `X` erzeugt, die aus 100 zufälligen Normalverteilungen besteht.
- Die Funktion `autocorr` berechnet die Autokorrelationskoeffizienten für verschiedene Verzögerungen `lag`.
- Der Bereich der Verzögerungen `lags` ist von 1 bis 20 gewählt (kann je nach Bedarf angepasst werden).
- Die Autokorrelationsfunktion wird dann mit `plt.stem` grafisch dargestellt.

### Zufälligkeit bestimmen:

Um die Zufälligkeit der Zeitreihe zu bestimmen, sollten Sie die Autokorrelationsfunktion analysieren:

- **Zufällige Zeitreihe**: Wenn die Zeitreihe zufällig ist, sollten die Autokorrelationswerte für alle Verzögerungen nahe bei null liegen.
- **Nicht zufällige Zeitreihe**: Falls die Zeitreihe nicht zufällig ist, können signifikante Autokorrelationswerte bei bestimmten Verzögerungen auftreten, was auf strukturelle Muster oder Abhängigkeiten hinweist.

Zusätzlich können Sie statistische Tests wie den Ljung-Box-Test verwenden, um die Signifikanz der Autokorrelationswerte zu prüfen.

Die gezeigte Python-Implementierung bietet eine grundlegende Möglichkeit, die Autokorrelation zu berechnen und zu visualisieren, was Ihnen helfen kann, die Zufälligkeit einer Zeitreihe zu beurteilen.
