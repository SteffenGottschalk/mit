Die Systemidentifikation ist ein Prozess, bei dem die dynamischen Eigenschaften eines Systems aus gemessenen Daten abgeleitet werden. Hier sind zwei experimentelle Methoden zur Durchführung der Systemidentifikation:

1. **Impulsantwort-Methode (Impulsantwortanalyse):**

   - **Beschreibung:** Bei dieser Methode wird eine kurze Impulsfunktion (wie ein Dirac-Impuls oder ein kurzer Rechteckimpuls) auf das System angewendet, und die Reaktion des Systems wird gemessen.
   - **Durchführung:** Ein Impuls wird typischerweise durch ein Schlaginstrument oder einen elektronischen Impulsgenerator erzeugt und auf das System angewendet. Die Antwort des Systems wird durch Sensoren (z.B. Beschleunigungsmesser, Drucksensoren) gemessen. Diese Antwort wird als Impulsantwort des Systems betrachtet.
   - **Analyse:** Die gemessene Impulsantwort wird dann analysiert, um die Übertragungsfunktion oder andere Systemparameter (wie Zeitkonstanten, Dämpfungsfaktoren) zu extrahieren. Dies kann durch Faltung mit der bekannten Impulsantwort oder durch Fourier-Analyse erfolgen.

2. **Frequenzgang-Methode (Frequenzantwortanalyse):**
   - **Beschreibung:** Diese Methode basiert auf der Anregung des Systems mit einer sinusförmigen Anregung unterschiedlicher Frequenzen und der Messung der Übertragungsfunktion oder des Frequenzgangs des Systems.
   - **Durchführung:** Das System wird mit sinusförmigen Signalen verschiedener Frequenzen angeregt, die durch einen Frequenzgenerator erzeugt werden. Die Antwort des Systems wird durch Sensoren gemessen, die die Amplitude und Phase der Ausgangssignale bei verschiedenen Frequenzen aufzeichnen.
   - **Analyse:** Durch Anwenden von Fourier-Transformationen auf die Eingabe- und Ausgabesignale kann der Frequenzgang des Systems bestimmt werden. Dieser Frequenzgang gibt Auskunft über die Amplituden- und Phasencharakteristik des Systems über einen Bereich von Frequenzen. Anhand des Frequenzgangs können Parameter wie Resonanzfrequenzen, Bandbreite und Dämpfung des Systems ermittelt werden.

Diese beiden Methoden sind grundlegend für die Systemidentifikation und werden je nach Systemtyp und den verfügbaren experimentellen Bedingungen angewendet. Andere Methoden wie die Zustandsraumdarstellung oder die Parameterschätzung durch Optimierungsalgorithmen können ebenfalls verwendet werden, um detailliertere Modelle zu erhalten, erfordern jedoch oft umfangreichere Daten und Analyseverfahren.
