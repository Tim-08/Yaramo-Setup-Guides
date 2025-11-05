
Der **PlanPro Importer** ermöglicht es, PlanPro-Dateien (`.ppxml`) in eine Python-Topologie zu importieren.  
Damit kannst du Planungsdaten in dein Yaramo-Projekt integrieren oder weiterverarbeiten.

---
## 🧩 Voraussetzungen

Bevor du startest, stelle sicher, dass du `Yaramo` erfolgreich installiert hast. Weitere Hilfe findest du dazu im [[🧭 Yaramo - Setup Guide]]

## 1️⃣ Installation

Installiere den PlanPro Importer direkt aus dem GitHub-Repository mit:

``` shell
poetry add git+https://github.com/simulate-digital-rail/planpro-importer
```

## 2️⃣ Import in dein Python-Projekt

Sobald das Paket installiert ist, kannst du es in deinem Python-Code verwenden.  
Importiere die benötigten Module:

``` python
from planpro_importer import PlanProVersion, import_planpro
```


## 3️⃣ PlanPro-Datei importieren

Mit der Funktion `import_planpro()` lässt sich eine `.ppxml`-Datei (PlanPro-Dateiformat) laden und in eine **Topologie-Struktur** überführen.

📘 Beispiel: PlanPro Version 1.9

``` python
topology = import_planpro("filename.ppxml", PlanProVersion.PlanPro19)`
```

📗 Beispiel: PlanPro Version 1.10

``` python
topology = import_planpro("filename.ppxml", PlanProVersion.PlanPro110)`
```

>[!TIPP]
Ersetze `filename.ppxml` durch den Pfad zu deiner eigenen PlanPro-Datei.  
Das zurückgegebene Objekt `topology` kann direkt mit anderen Yaramo-Komponenten weiterverarbeitet werden.




