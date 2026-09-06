# Architecture

## Zielbild

Der POC bleibt eine bewusst schlanke, statische Website ohne Backend und ohne Build-Step. Die technische Struktur bildet die bestehende Exodus90.de-Seitenlogik nun als kleine Multi-Page-Site ab, statt alle Inhalte in eine Single Page zu pressen.

## Technologie

- HTML für Seitenstruktur und Inhalte
- gemeinsames CSS für Layout, Markenwirkung und Responsive Design
- Vanilla JavaScript nur für mobile Navigation und Demo-Formulare
- GitHub Pages als Hosting-Ziel

## High-Level-Aufbau

```text
Website
├── index.html
├── gruppen.html
├── erfahrungen.html
├── downloads.html
├── netzwerk.html
├── kontakt.html
├── impressum.html
├── datenschutz.html
├── css/
│   └── styles.css
├── js/
│   └── main.js
└── .github/workflows/
    └── pages.yml
```

## Seitenmodell

Die Startseite übernimmt Einstieg, Kernbotschaft, kurze Programminformation, Newsletter und Kontakt. Größere bzw. eigenständige Themen liegen auf Unterseiten:

- Gruppensuche
- Erfahrungsberichte
- Downloads
- Netzwerk Exodus
- Kontakt
- Impressum und Datenschutz

Die Gruppensuche enthält weiterhin nur einen Karten-Platzhalter; echte Standortlogik ist nicht Bestandteil des POC.

## UI-Struktur

Alle Seiten verwenden dieselben visuellen Muster über `css/styles.css`:

- Header und Hauptnavigation
- Exodus-Logo/Badge-Motiv
- orange Hero-/Akzentflächen
- große Headlines und direkte CTAs
- Inhaltsblöcke und Karten
- Formulare
- Footer

Die Wiederverwendung erfolgt bewusst über gemeinsame CSS-Klassen statt über ein Framework oder einen Build-Prozess.

## Interaktivität

JavaScript bleibt auf kleine UI-Funktionen begrenzt:

- mobile Navigation
- rein visuelle Formularbestätigung im POC

Es gibt keine clientseitige Anwendungsarchitektur, kein State-Management und keine API-Schicht.

## Daten und Backend

Der POC speichert keine produktiven Daten. Formulare werden nicht übertragen. Vorhandene Erfahrungsberichte werden als externe PDF-Dokumente verlinkt. Rechtstexte sind im POC nur Platzhalter und müssen vor produktiver Nutzung geprüft werden.

## Deployment

Die Website wird direkt aus dem Repository über GitHub Pages veröffentlicht. Es gibt keinen Build-Prozess; die auszuliefernden Dateien entsprechen dem Repository-Inhalt.

## Architekturprinzipien

- minimale technische Komplexität
- Multi-Page-Struktur nur dort, wo sie der bestehenden Informationsarchitektur entspricht
- statisch vor dynamisch
- JavaScript nur bei echtem Mehrwert
- gemeinsame Styles statt Framework-Komponenten
- responsive und zugängliche Basisstruktur
- Erweiterbarkeit ohne vorzeitige Infrastruktur
