[![Shipping files](https://github.com/neuefische/ds-predictive-regression/actions/workflows/workflow-02.yml/badge.svg?branch=main&event=workflow_dispatch)](https://github.com/neuefische/ds-predictive-regression/actions/workflows/workflow-02.yml)

# Prädiktive Regression

In diesem Repository werfen wir einen Blick auf verschiedene Themen rund um das Arbeiten mit Daten beim Trainieren eines Modells zur **Vorhersage** (im Gegensatz zur reinen **Exploration**). Beim Arbeiten mit Daten müssen wir uns bewusst sein, dass wir in der Praxis nie wirklich **alle** Daten haben. Deshalb sollten unsere Experimente die Ergebnisse möglichst gut approximieren, die wir erhalten würden, wenn uns der vollständige Datensatz zur Verfügung stünde.

Unsere Modelle werden niemals perfekt sein, aber wir wollen eine gute **Balance zwischen Bias und Varianz** erreichen:

- Um zu verstehen, wie sich ein Modell auf neuen Daten verhält, ist ein **Train/Test-Split** vor dem Modellieren das Mindest-Setup. Später im Bootcamp lernen wir **Cross-Validation** kennen.
- Wenn wir feststellen, dass unser Modell **underfitted** (hoher Bias) ist, können wir prüfen, ob unterschiedliche **Kombinationen von Features** das Modell verbessern. Dafür betrachten wir die **Generierung polynomialer Features**.
- Wenn es eine große Lücke zwischen der Evaluationsmetrik auf dem Trainings- und dem Testdatensatz gibt, haben wir es möglicherweise mit **Overfitting** (hohe Varianz) zu tun. Das bedeutet, dass unser Modell schlecht auf neue Daten generalisiert. Eine Möglichkeit, dies zu reduzieren, ist **Regularisierung**.
- Schließlich gilt weiterhin: *Garbage in, garbage out*. Wir müssen sicherstellen, dass unsere Daten so korrekt wie möglich sind und zum jeweiligen Problem passen. Dazu gehört auch, **Ausreißer** zu untersuchen und zu entscheiden, ob es sich um fehlerhafte Daten (die korrigiert werden müssen) oder um extreme, aber valide Werte handelt (hier kann es eine fachliche bzw. geschäftliche Entscheidung sein, ob sie behalten oder entfernt werden – z. B. kann man es sich oft nicht leisten, 15 % des Datensatzes zu verwerfen).

In diesem Repository gibt es **3 Notebooks**, die diese Themen abdecken. Obwohl wir in den Notebooks **lineare Regression** als Beispielmodell verwenden, gilt dieses Framework grundsätzlich für jede **überwachte Modellierung**.

---

## Der Weg zum Erfolg

Bitte arbeitet **in Zweierteams** alle Notebooks in der folgenden Reihenfolge durch:

1. [Bias-Varianz-Trade-off & Polynomiale Features](1_Bias_Variance_Tradeoff.ipynb)
2. [Regularisierung](2_Regularization.ipynb)
3. [Erkennen von Ausreißern](3_Detecting_Outliers.ipynb)

Denkt daran: **Als Team seid ihr erfolgreicher.**  
Es gibt **keine dummen Fragen**! Wenn ihr euch mit den Konzepten bereits wohlfühlt, lernt ihr oft sogar noch mehr, indem ihr sie anderen erklärt.

---

## Umgebung einrichten

Bitte stellt sicher, dass ihr das Repository **geforkt** und eine neue **virtuelle Umgebung** eingerichtet habt. Dafür könnt ihr die folgenden Befehle verwenden:

Die hinzugefügte [requirements-Datei](requirements.txt) enthält alle Bibliotheken und Abhängigkeiten, die wir zum Ausführen der Notebooks zur prädiktiven Regression benötigen.

*Hinweis: Falls bei der Einrichtung der Umgebung Fehler auftreten, versucht, die Versionsangaben der problematischen Pakete aus der requirements-Datei zu entfernen.*

---

### **`macOS`**

Gebt die folgenden Befehle ein:

- Virtuelle Umgebung erstellen und benötigte Pakete installieren:

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### **`WindowsOS`** benutzen sie das folgende :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-Bash` CLI :
    ```
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:
    ```Bash
    python.exe -m pip install --upgrade pip
    ```
  
