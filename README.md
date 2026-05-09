# Solar Dashboard

Interaktives Photovoltaik-Dashboard zur Analyse und Visualisierung von Solaranlagen-Daten im Browser — kein Build-Tool erforderlich.

## Features

- **7 Analyse-Tabs** — Stromerzeugung, Verbrauch, Einspeisung, Batterie, Vorteile, Zukunft, Klimawirkung
- **CSV-Upload** — eigene Datei laden per Schaltfläche oder Drag & Drop
- **Strompreisrechner** — Kauf-/Einspeisepreis und Anlagekosten live anpassbar
- **Eigenverbrauchsquote (EVQ)** — Erzeuger- und Verbraucherperspektive im Vergleich
- **Monatliche CSV-Granularität** — erkennt Monatsdaten automatisch, zeigt Jahr-Selektor
- **Netz-Unabhängigkeits-Score** — gewichteter Composite-Score aus 4 Komponenten (Autarkie, Netzfreiheit, Batterie-Resilienz, Entwicklungs-Bonus)
- **Amortisations-Rechner** — ROI-Fortschrittsanzeige mit konfigurierbaren Anlagekosten

## CSV-Format

```
Date time,Home (MWh),Vehicle (kWh),From Powerwall (MWh),Solar Energy (MWh),From Grid (MWh),To Grid (MWh)
2023-01-01T00:00:00+01:00,2.6,0.0,1.0,10.0,0.54,7.7
2023-02-01T00:00:00+01:00,0.4,0.0,0.1,0.8,0.09,0.5
```

- Trennzeichen: Komma **oder** Semikolon (automatisch erkannt)
- Datumsspalte: ISO-8601 oder beliebiges Format, das mit der Jahreszahl beginnt
- Monatliche **und** jährliche Datenreihen werden unterstützt

## Technologie

- Vanilla HTML/CSS/JavaScript (Single-File `index.html`)
- [Chart.js 4.4.0](https://www.chartjs.org/) via CDN

## Starten

```bash
# Einfach im Browser öffnen:
open index.html
```
