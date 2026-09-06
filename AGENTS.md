# Agent Instructions

Vor jeder Änderung am Projekt müssen `CONCEPT.md` und `ARCHITECTURE.md` gelesen werden.

Nach jeder Änderung muss geprüft werden, ob sich fachlicher Umfang, Features, Seitenstruktur, technische Architektur oder zentrale Entscheidungen verändert haben. Falls ja, müssen `CONCEPT.md` und/oder `ARCHITECTURE.md` im selben Arbeitsgang aktualisiert werden.

`CONCEPT.md` ist die fachliche Quelle für Ziel, Umfang und Features.

`ARCHITECTURE.md` ist die technische High-Level-Quelle für Aufbau, Technologien und zentrale Architekturentscheidungen.

Beide Dateien müssen jederzeit den aktuellen Projektstand widerspiegeln. Keine kleintechnischen Implementierungsdetails aufnehmen, sofern sie nicht architekturrelevant sind.

## Git-Workflow

- Niemals direkt auf `main` arbeiten.
- Für jedes zusammenhängende Arbeitspaket einen temporären Branch von `main` erstellen.
- Alle Änderungen dieses Arbeitspakets ausschließlich auf diesem Branch durchführen.
- Nach Abschluss einen Pull Request gegen `main` erstellen.
- Den Pull Request per **Squash Merge** nach `main` mergen.
- Der Squash-Commit soll einen klaren Titel und eine kompakte Beschreibung der relevanten Änderungen enthalten.
- Ziel ist genau ein sauberer Commit auf `main` pro abgeschlossenem Arbeitspaket.
