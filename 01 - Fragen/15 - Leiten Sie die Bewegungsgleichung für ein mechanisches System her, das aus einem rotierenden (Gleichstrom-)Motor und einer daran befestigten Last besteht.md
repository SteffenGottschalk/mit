Um die Bewegungsgleichung für das mechanische System, bestehend aus einem Gleichstrommotor und einer daran befestigten Last, herzuleiten, gehen wir wie folgt vor:

1. **Systembeschreibung**:

   - Der Gleichstrommotor hat eine Drehachse.
   - Eine Last ist direkt an der Motorwelle befestigt und dreht sich mit dieser.

2. **Kräfte und Momente**:

   - **Motor-Drehmoment**: Sei \( T_m \) das von der Motorwelle auf die Last ausgeübte Drehmoment.
   - **Trägheitsmoment der Last**: Sei \( J \) das Trägheitsmoment der Last um die Drehachse.
   - **Reibungsmoment**: Falls vorhanden, sei \( T_f \) das Reibungsmoment.

3. **Bewegungsgleichung**:
   Die Bewegungsgleichung beschreibt das dynamische Verhalten des Systems und lautet für den rotierenden Fall:
   \[ J \frac{d\omega}{dt} = T\_{\text{gesamt}} \]

   Dabei ist \( \omega \) die Winkelgeschwindigkeit der Last und \( T\_{\text{gesamt}} \) das Gesamtdrehmoment, das auf die Last wirkt.

4. **Gesamtdrehmoment \( T\_{\text{gesamt}} \)**:
   Das Gesamtdrehmoment setzt sich aus dem Motor-Drehmoment \( T*m \) und dem Reibungsmoment \( T_f \) zusammen:
   \[ T*{\text{gesamt}} = T_m - T_f \]

5. **Motor-Drehmoment \( T_m \)**:
   Das Motor-Drehmoment \( T_m \) hängt von der Motorspannung \( V \), dem Motorstrom \( I \), und der Drehzahl \( \omega \) ab. Für einen Gleichstrommotor gilt oft die vereinfachte lineare Beziehung:
   \[ T_m = k_m I \]
   wobei \( k_m \) eine Konstante ist, die das Drehmoment in Abhängigkeit vom Strom angibt.

6. **Gleichgewichtsbedingung**:
   Im stationären Zustand, wenn sich die Geschwindigkeit nicht ändert (\( \frac{d\omega}{dt} = 0 \)), gilt:
   \[ T_m = T_f \]

7. **Zusammenfassung der Bewegungsgleichung**:
   Unter Berücksichtigung aller obigen Punkte ergibt sich die Bewegungsgleichung für das System zu:
   \[ J \frac{d\omega}{dt} = k_m I - T_f \]

   Diese Gleichung beschreibt die Dynamik des mechanischen Systems, das aus einem Gleichstrommotor und einer daran befestigten Last besteht.
