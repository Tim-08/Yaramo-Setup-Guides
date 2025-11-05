Der **SUMO Converter** dient dazu, Daten aus dem Yaramo-Projekt in das SUMO-Format zu exportieren.  
Diese Anleitung führt dich Schritt für Schritt durch die Installation und Konfiguration.

---
## 🧩 Voraussetzungen

Bevor du startest, stelle sicher, dass du `Yaramo` erfolgreich installiert hast. Weitere Hilfe findest du dazu im [[🧭 Yaramo - Setup Guide]]


## 1️⃣ SUMO Converter installieren

Füge den SUMO Converter direkt aus dem GitHub-Repository hinzu:

``` shell
poetry add git+https://github.com/simulate-digital-rail/sumo-exporter/
```

## 2️⃣ SUMO installieren

Der Exporter benötigt SUMO (insbesondere das Tool **netconvert**).  

Um SUMO direkt in deiner virtuellen Umgebung zu installieren, verwende:

``` shell
pip install eclipse-sumo
```


>[!INFO] Installationsoptionen
>Weitere Informationen und Installationsoptionen findest du auf der offiziellen Seite:  
👉 [SUMO Downloads](https://sumo.dlr.de/docs/Downloads.php)

## 3️⃣ libnsl installieren (für Linux)

SUMO benötigt zusätzlich die Bibliothek [**libnsl**](https://www.linuxfromscratch.org/blfs/view/svn/basicnet/libnsl.html). 

Unter Fedora:
``` shell
sudo dnf install libnsl
```

Unter Ubuntu/Debian:
``` Shell
sudo apt install libnsl
```

## 4️⃣ Exportierte Dateien finden und importieren
Nach erfolgreichem Export findest du die erzeugten SUMO-Dateien unter:

```
/yaramo_project/sumo-config/
```

Diese Dateien kannst du direkt in die **SUMO GUI** importieren, um deine Simulation zu starten.

## 5️⃣ SUMO GUI installieren (optional)
Die grafische Oberfläche von SUMO (GUI) kann auf zwei Wegen installiert werden:

- 🔗 [Offizielle Webseite](https://eclipse.dev/sumo/)
- 🧱 [Flathub](https://flathub.org/en/apps/org.eclipse.sumo)

Mit der GUI kannst du anschließend deine exportierten Netzwerke visuell inspizieren und simulieren.