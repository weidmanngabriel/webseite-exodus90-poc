# Architecture

## Zielbild

Der POC ist eine bewusst schlanke, statische Website ohne Backend und ohne Build-Step. Die technische Struktur soll leicht verständlich, direkt auslieferbar und einfach erweiterbar bleiben.

## Technologie

- HTML für Seitenstruktur und Inhalte
- CSS für Layout, Designsystem und Responsive Design
- Vanilla JavaScript nur für kleine UI-Interaktionen
- GitHub Pages als Hosting-Ziel

## High-Level-Aufbau

```text
Website
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── assets/
└── .github/workflows/
    └── pages.yml
```

## Seitenmodell

Der POC wird zunächst als kompakte Single-Page umgesetzt. Die bestehende Informationslogik wird über klar getrennte Inhaltssektionen abgebildet:

- Header / Navigation
- Hero
- Programminformation
- Gruppenbereich
- Karten-Platzhalter
- Erfahrungen
- Downloads
- FAQ
- Newsletter
- Kontakt
- Footer

Falls der Relaunch später wieder mehrere eigenständige Seiten benötigt, können dieselben visuellen und inhaltlichen Bausteine ohne grundlegenden Architekturwechsel auf mehrere HTML-Dateien verteilt werden.

## UI-Struktur

Wiederkehrende Muster werden als konsistente CSS-Komponenten gedacht, nicht als Framework-Komponenten. Dazu gehören insbesondere:

- Buttons
- Inhaltssektionen
- Karten
- CTA-Bereiche
- Formulare
- Accordion
- Navigation und Footer

## Interaktivität

JavaScript bleibt auf klar begrenzte UI-Funktionen beschränkt, insbesondere:

- mobile Navigation
- FAQ-Accordion
- rein visuelle Formularbestätigung im POC

Es gibt keine clientseitige Anwendungsarchitektur, kein State-Management und keine API-Schicht.

## Daten und Backend

Der POC speichert keine produktiven Daten. Formulare werden nicht übertragen. Die spätere Gruppenkarte ist ausdrücklich nicht Bestandteil der ersten technischen Umsetzung und wird durch einen sichtbaren Platzhalter repräsentiert.

## Deployment

Die Website wird direkt aus dem Repository über GitHub Pages veröffentlicht. Es gibt keinen Build-Prozess; die auszuliefernden Dateien entsprechen dem Repository-Inhalt.

## Architekturprinzipien

- minimale technische Komplexität
- statisch vor dynamisch
- JavaScript nur bei echtem Mehrwert
- responsive und zugängliche Basisstruktur
- klare Trennung von Inhalt, Styling und Verhalten
- Erweiterbarkeit ohne vorzeitige Infrastruktur
