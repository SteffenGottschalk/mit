Um eine gemessene Spannung auf einer grafischen Benutzeroberfläche (GUI) in C++ anzuzeigen, verwenden wir üblicherweise eine Bibliothek wie Qt, wxWidgets oder GTK+. Hier ist ein einfaches Beispiel mit Qt, das eine GUI-Anwendung erstellt, um eine gemessene Spannung darzustellen:

```cpp
#include <QApplication>
#include <QWidget>
#include <QLabel>
#include <QSlider>
#include <QVBoxLayout>
#include <QString>

// Erstelle eine einfache GUI-Anwendung mit Qt
class VoltageDisplay : public QWidget {
public:
    VoltageDisplay(QWidget *parent = nullptr)
        : QWidget(parent)
    {
        // GUI-Elemente erstellen
        QVBoxLayout *layout = new QVBoxLayout(this);
        QLabel *label = new QLabel("Gemessene Spannung:", this);
        voltageLabel = new QLabel("0.0 V", this);
        voltageLabel->setAlignment(Qt::AlignCenter);

        // Slider für die Spannungssimulation (optional)
        QSlider *slider = new QSlider(Qt::Horizontal, this);
        slider->setRange(0, 100);
        connect(slider, &QSlider::valueChanged, this, &VoltageDisplay::onSliderValueChanged);

        // Layout erstellen
        layout->addWidget(label);
        layout->addWidget(voltageLabel);
        layout->addWidget(slider);
        setLayout(layout);

        setWindowTitle("Spannungsmessung");
    }

private slots:
    // Slot für die Aktualisierung der Spannungsanzeige
    void onSliderValueChanged(int value) {
        double voltage = value / 10.0; // Beispiel für eine Spannungssimulation
        QString voltageStr = QString::number(voltage, 'f', 1) + " V";
        voltageLabel->setText(voltageStr);
    }

private:
    QLabel *voltageLabel;
};

int main(int argc, char *argv[]) {
    QApplication app(argc, argv);

    VoltageDisplay window;
    window.resize(300, 150);
    window.show();

    return app.exec();
}
```

### Erläuterung des Codes:

1. **Header-Dateien einbinden**: Die notwendigen Qt-Header-Dateien werden eingebunden, um die Qt-Funktionalitäten nutzen zu können.

2. **Klasse `VoltageDisplay`**: Diese Klasse erbt von `QWidget` und stellt das Hauptfenster der Anwendung dar.

3. **Konstruktor `VoltageDisplay`**: Hier werden die GUI-Elemente erstellt:

   - Ein vertikales Layout (`QVBoxLayout`).
   - Ein `QLabel` für die Überschrift "Gemessene Spannung:".
   - Ein weiteres `QLabel` (`voltageLabel`) für die Anzeige der Spannung.
   - Ein `QSlider` zur Simulation einer gemessenen Spannung (kann optional sein).

4. **`onSliderValueChanged` Slot**: Dieser Slot wird aufgerufen, wenn sich der Wert des Sliders ändert. Hier wird eine simuliert gemessene Spannung berechnet und im `voltageLabel` angezeigt.

5. **`main` Funktion**: Die `main` Funktion erstellt eine `QApplication`, erstellt ein Objekt der Klasse `VoltageDisplay`, zeigt es an und startet die Qt-Event-Schleife (`app.exec()`).

### Hinweise:

- Dieses Beispiel verwendet Qt für die GUI-Entwicklung. Stellen Sie sicher, dass Sie die Qt-Bibliothek installiert und konfiguriert haben, um mit Ihrem C++-Compiler zu arbeiten.
- Die Spannung wird hier durch den Slider simuliert. In einer tatsächlichen Anwendung würde die Spannungswerte von einem Messgerät oder einer ähnlichen Quelle kommen.
- Dies ist ein grundlegendes Beispiel. Je nach Anforderungen können weitere Funktionen und Komponenten hinzugefügt werden, z.B. eine Echtzeitdatenaktualisierung, Grafiken oder mehr komplexe Benutzeroberflächenelemente.

Dieses Beispiel gibt Ihnen einen Einstiegspunkt für die Entwicklung einer C++-basierten GUI-Anwendung zur Anzeige einer gemessenen Spannung.
