Um den Mittelwert und die Standardabweichung einer Zeitreihe in Python zu berechnen, kannst du die Bibliothek `numpy` verwenden, da sie effiziente Funktionen für numerische Berechnungen bietet. Hier ist ein Beispiel, wie du den Mittelwert und die Standardabweichung einer Liste von Zahlen berechnen kannst:

```python
import numpy as np

# Beispiel-Zeitreihe (Liste von Zahlen)
zeitreihe = [3, 5, 8, 12, 15, 18, 20]

# Mittelwert berechnen
mittelwert = np.mean(zeitreihe)
print(f"Mittelwert: {mittelwert}")

# Standardabweichung berechnen (Stichprobe)
std_abweichung = np.std(zeitreihe, ddof=1)
print(f"Standardabweichung: {std_abweichung}")
```

### Erklärung des Codes:

1. **Import der Bibliothek**: `import numpy as np` importiert die Bibliothek `numpy` und ermöglicht den Zugriff auf ihre Funktionen über das Kürzel `np`.

2. **Zeitreihe**: `zeitreihe` ist eine Beispiel-Liste von Zahlen, die deine Zeitreihe darstellt. Du kannst diese Liste entsprechend deiner eigenen Daten anpassen.

3. **Mittelwert berechnen**: `np.mean(zeitreihe)` ruft die Funktion `mean` aus `numpy` auf, um den Mittelwert der Zeitreihe zu berechnen und weist ihn der Variable `mittelwert` zu.

4. **Standardabweichung berechnen**: `np.std(zeitreihe, ddof=1)` verwendet die Funktion `std` aus `numpy`, um die Stichproben-Standardabweichung der Zeitreihe zu berechnen. Der Parameter `ddof=1` steht für "delta degrees of freedom" und korrigiert die Berechnung für eine Stichprobe (d.h., es wird durch \( n-1 \) statt \( n \) geteilt).

5. **Ausgabe**: Die berechneten Werte werden dann mit `print` ausgegeben.

Dieses Beispiel zeigt, wie einfach es ist, den Mittelwert und die Standardabweichung einer Zeitreihe mit Python und `numpy` zu berechnen.
