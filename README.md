# Helios Core

A lightweight photovoltaic analytics dashboard for solar production, consumption, battery storage, grid exchange, economics and climate impact.

## Overview

Helios Core is a single, dependency-free HTML file. It works offline, loads in one request and renders all charts as inline SVG — no framework, no chart library, no build step.

---

## Features

* ☀️ **Erzeugung** – annual yield, use of production (self-consumption vs. feed-in), monthly profile
* 🏠 **Verbrauch** – coverage by solar, Powerwall and grid; autarky and self-consumption rate; grid-independence score
* 🔋 **Speicher & Netz** – Powerwall discharge, grid exchange and net balance
* 💶 **Finanzen** – annual savings, amortisation path against system cost, further benefits
* 🌱 **Klima** – avoided CO₂ with equivalents, cumulative impact including forecast
* 📈 **Trends & Prognose** – forecast to 2030, year-over-year change, full annual table

Across all views:

* Partial years (commissioning year, running year) are detected and marked; they are excluded from records, averages, year-over-year deltas and the forecast base
* Every figure and every analysis text is computed from the data — nothing is hard-coded
* Adjustable assumptions (electricity price, feed-in tariff, system cost), stored locally
* CSV upload via button or drag & drop, persisted locally, with one-click reset to sample data
* Deep links per view (`#finanzen`), keyboard-navigable tabs and charts, accessible chart descriptions
* Mobile-first layout with sticky navigation and no horizontal scrolling

---

## CSV format

Use the Tesla app export or any CSV with these columns (see [`data.csv`](data.csv)):

| Column contains | Meaning |
|---|---|
| first column | date (`2025-01-01T…` or `01.01.2025`) |
| `Home` | household consumption |
| `Powerwall` | energy from battery |
| `Solar` | solar production |
| `From Grid` | grid import |
| `To Grid` | grid feed-in |

Rows can be annual or monthly. Units are read from the header (`kWh` or `MWh`). Comma- and semicolon-separated files are supported, including German decimal commas.

---

## Tech Stack

* HTML5, CSS3 (custom properties, CSS Grid)
* Vanilla JavaScript (ES2022)
* Inline SVG charts and icon sprite
* GitHub Pages

---

## Live Demo

🔗 [https://looped83.github.io/helios-core/](https://looped83.github.io/helios-core/)

---

## Roadmap

* [ ] Smart home integrations
* [ ] Weather forecasting
* [ ] AI-powered energy optimization
* [ ] Push notifications
* [ ] Mobile app integration
* [ ] Advanced battery analytics

---

## Disclaimer

This project is intended for educational and informational purposes only.

Actual solar production values may vary depending on weather conditions, hardware configuration, and data source accuracy. Economic figures are estimates without subsidies or taxes.

---

## Author

Created by looped83

GitHub: [https://github.com/looped83](https://github.com/looped83)
