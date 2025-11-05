Dieser Setup-Guide hilft dir dabei, ein neues Python-Projekt mit **Poetry** aufzusetzen und das **Yaramo**-Paket direkt aus dem GitHub-Repository zu installieren.  
Die folgenden Schritte bleiben gleich, sind aber mit zusätzlichen Erklärungen versehen, damit du genau verstehst, was passiert.

---

## 1️⃣ Virtuelle Umgebung erstellen *(optional)*

Eine **virtuelle Umgebung** stellt sicher, dass deine Projektabhängigkeiten von global installierten Python-Paketen getrennt sind.  
So vermeidest du Versionskonflikte und kannst saubere Entwicklungsumgebungen pflegen.

```bash
python -m venv venv
```

Anschließend musst du die virtuelle Umgebung **aktivieren**:

macOS / Linux:

```bash
source venv/bin/activate
```

Windows (PowerShell):

```PowerShell
venv\Scripts\activate
```


## 2️⃣ Poetry installieren

[Poetry](https://python-poetry.org/) ist ein modernes Tool zur **Paketverwaltung und Projektverwaltung** in Python.  
Es ersetzt `pip` und `virtualenv` teilweise, indem es Abhängigkeiten sauber verwaltet und reproduzierbare Builds ermöglicht.

Installiere Poetry mit:

```bash
pip install poetry
```

Überprüfe anschließend die Installation:

```bash
poetry --version
```

Wenn du eine Versionsnummer siehst, ist alles korrekt installiert.


## 3️⃣ Neues Poetry-Projekt erstellen

Mit diesem Befehl erzeugst du ein neues Projektverzeichnis inklusive `pyproject.toml` (der zentralen Konfigurationsdatei):

```bash
poetry new yaramo_project
```

>[!Warning] **Wichtig:**  
Das Projekt darf **nicht denselben Namen** wie die zu installierenden Pakete haben (also z.B. **nicht `yaramo`**), sonst kann es zu Konflikten kommen.

Wechsle danach in das neu erstellte Projektverzeichnis:

```bash
cd yaramo_project
```


## 4️⃣ Yaramo-Paket hinzufügen
Jetzt fügst du das **Yaramo-Paket** direkt aus dem GitHub-Repository hinzu.  
Poetry lädt dabei automatisch die neueste Version aus dem Repository und trägt sie in `pyproject.toml` ein.

```bash
poetry add git+https://github.com/simulate-digital-rail/yaramo
```

Nach der Installation kannst du mit folgendem Befehl prüfen, ob alles korrekt eingebunden wurde:

```bash
poetry show
```

Du solltest nun `yaramo` in der Liste der installierten Pakete sehen.