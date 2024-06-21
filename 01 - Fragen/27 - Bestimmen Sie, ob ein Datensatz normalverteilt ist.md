In Python gibt es verschiedene Bibliotheken und Funktionen, die Ihnen helfen können, zu bestimmen, ob ein Datensatz normalverteilt ist. Hier zeige ich Ihnen einige praktische Beispiele mit den Bibliotheken `numpy`, `scipy.stats` und `matplotlib`.

### Beispiel mit Histogramm und Q-Q Plot

```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.stats as stats

# Beispiel-Datensatz generieren (normalverteilt)
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=1000)

# Histogramm mit Normalverteilungskurve
plt.figure(figsize=(12, 4))

plt.subplot(1, 2, 1)
plt.hist(data, bins=30, density=True, alpha=0.6, color='g')

# Normale Verteilungskurve
xmin, xmax = plt.xlim()
x = np.linspace(xmin, xmax, 100)
p = stats.norm.pdf(x, np.mean(data), np.std(data))
plt.plot(x, p, 'k', linewidth=2)
plt.title('Histogramm und Normalverteilungskurve')
plt.xlabel('Datenwerte')
plt.ylabel('Dichte')

# Q-Q Plot
plt.subplot(1, 2, 2)
stats.probplot(data, dist="norm", plot=plt)
plt.title('Q-Q Plot')

plt.tight_layout()
plt.show()
```

### Shapiro-Wilk Test

Der Shapiro-Wilk Test kann verwendet werden, um die Normalverteilung eines Datensatzes zu prüfen.

```python
import scipy.stats as stats

# Beispiel-Datensatz generieren (normalverteilt)
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=1000)

# Shapiro-Wilk Test
statistic, p_value = stats.shapiro(data)

print(f"Shapiro-Wilk Testergebnisse:")
print(f"Teststatistik: {statistic}")
print(f"P-Wert: {p_value}")

alpha = 0.05
if p_value > alpha:
    print("Die Daten könnten normalverteilt sein (nicht ablehnend)")
else:
    print("Die Daten sind nicht normalverteilt (ablehnend)")
```

### Kolmogorov-Smirnov Test

Der Kolmogorov-Smirnov Test kann ebenfalls verwendet werden, um die Normalverteilung eines Datensatzes zu überprüfen.

```python
import scipy.stats as stats

# Beispiel-Datensatz generieren (normalverteilt)
np.random.seed(0)
data = np.random.normal(loc=0, scale=1, size=1000)

# Kolmogorov-Smirnov Test
statistic, p_value = stats.kstest(data, 'norm')

print(f"Kolmogorov-Smirnov Testergebnisse:")
print(f"Teststatistik: {statistic}")
print(f"P-Wert: {p_value}")

alpha = 0.05
if p_value > alpha:
    print("Die Daten könnten normalverteilt sein (nicht ablehnend)")
else:
    print("Die Daten sind nicht normalverteilt (ablehnend)")
```

### Hinweise:

- Stellen Sie sicher, dass Sie die Daten entsprechend Ihres spezifischen Falls anpassen (z.B. durch Laden realer Daten oder Anpassen der Parameter für die Verteilung).
- Grafische Methoden wie Histogramme und Q-Q Plots sind oft hilfreich, um eine schnelle visuelle Inspektion der Normalität durchzuführen.
- Statistische Tests wie Shapiro-Wilk oder Kolmogorov-Smirnov bieten eine formale Möglichkeit, die Normalverteilung zu überprüfen, und liefern Ihnen einen P-Wert zur Entscheidung.

Diese Beispiele sollten Ihnen einen guten Ausgangspunkt bieten, um die Normalverteilung von Daten in Python zu untersuchen.
