Ein Entscheidungsbaum ist ein grafisches und mathematisches Modell, das verwendet wird, um Entscheidungen zu treffen und Vorhersagen zu treffen. Das grundlegende Konzept eines Entscheidungsbaums kann wie folgt beschrieben werden:

### Aufbau eines Entscheidungsbaums

1. **Wurzelknoten (Root Node):**

   - Der Ausgangspunkt des Entscheidungsbaums. Hier beginnt der Entscheidungsprozess. Die Wurzel repräsentiert die gesamte Datenmenge und enthält die erste Frage oder Bedingung, anhand derer die Daten aufgeteilt werden.

2. **Interne Knoten (Internal Nodes):**

   - Diese Knoten repräsentieren die Fragen oder Bedingungen, die auf die Daten angewendet werden. Jeder interne Knoten teilt die Daten in zwei oder mehr Teilmengen basierend auf den Attributen der Daten.

3. **Zweige (Branches):**

   - Diese Verbindungen zeigen die Ergebnisse der Fragen oder Bedingungen an und führen zu weiteren internen Knoten oder Blattknoten.

4. **Blattknoten (Leaf Nodes):**
   - Die Endpunkte des Entscheidungsbaums. Jeder Blattknoten stellt eine Klassifikation oder eine Entscheidung dar. Bei Klassifikationsproblemen repräsentiert der Blattknoten die Klasse, bei Regressionsproblemen einen numerischen Wert.

### Funktionsweise

1. **Datenaufteilung:**

   - Der Entscheidungsbaum beginnt an der Wurzel und teilt die Daten iterativ auf, indem er an jedem internen Knoten Fragen oder Bedingungen zu den Attributen der Daten stellt. Die Bedingungen basieren auf den Attributen der Daten und werden so gewählt, dass sie die Daten optimal aufteilen.

2. **Bedingungen wählen:**

   - Die Auswahl der Bedingungen oder Fragen erfolgt anhand von Kriterien wie der Reduktion der Entropie (bei Klassifikationsproblemen) oder der Minimierung der Varianz (bei Regressionsproblemen). Beliebte Kriterien sind der Gini-Index, die Informationsgewinnrate oder die Varianzreduktion.

3. **Rekursive Aufteilung:**

   - Dieser Prozess der Aufteilung und Bedingungswahl wird rekursiv wiederholt, bis eine Stoppregel erfüllt ist. Diese Regeln können die maximale Tiefe des Baums, eine minimale Anzahl von Datenpunkten pro Knoten oder eine minimale Reduktion der Unsicherheit umfassen.

4. **Entscheidung treffen:**
   - Wenn die Stoppregel erreicht ist, werden die Blätter des Baums verwendet, um die endgültige Entscheidung oder Klassifikation zu treffen. Jeder Blattknoten enthält die Mehrheitsklasse (bei Klassifikationsproblemen) oder den Durchschnittswert (bei Regressionsproblemen) der in diesem Knoten befindlichen Datenpunkte.

### Vorteile

- **Einfach zu interpretieren:** Entscheidungsbäume sind intuitiv und leicht zu visualisieren.
- **Keine Skalierung der Daten erforderlich:** Sie benötigen keine Normierung oder Skalierung der Daten.
- **Umgang mit fehlenden Werten:** Entscheidungsbäume können leicht mit fehlenden Werten umgehen.

### Nachteile

- **Überanpassung (Overfitting):** Entscheidungsbäume neigen dazu, sehr tief zu werden und sich zu stark an die Trainingsdaten anzupassen, was ihre Generalisierungsfähigkeit auf neue Daten verschlechtert.
- **Instabilität:** Kleine Änderungen in den Daten können zu völlig unterschiedlichen Bäumen führen.

### Zusammenfassung

Ein Entscheidungsbaum teilt die Daten schrittweise basierend auf Bedingungen der Attribute auf und trifft Entscheidungen oder Klassifikationen anhand der resultierenden Teilmengen. Er ist ein leistungsfähiges Werkzeug zur Datenanalyse, das leicht zu interpretieren und zu visualisieren ist, jedoch vorsichtig verwendet werden muss, um Überanpassung zu vermeiden.
