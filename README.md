# NeTEx Visualizer CH

Interaktives Visualisierungstool für NeTEx-Snippets, entwickelt im Rahmen der **NeTEx Realisierungsvorgabe Schweiz 2.0**.

🔗 **Live:** [aschmid-code.github.io/netex-viz](https://aschmid-code.github.io/netex-viz)

---

## Features

- **Karte** — Haltestellen und Linienverläufe auf Leaflet-Karte (OpenStreetMap / CARTO dark)
- **Fahrplan** — Marey-Diagramm (Weg-Zeit) mit D3.js
- **Details** — Alle PassingTimes, Stop-Referenzen, Linien-Metadaten
- **Drag & Drop** — XML-Datei direkt ins Browserfenster ziehen
- **Beispieldaten** — Zwei CH-Snippets direkt auswählbar

## Verwendung

Keine Installation. Einfach öffnen:

👉 [aschmid-code.github.io/netex-viz](https://aschmid-code.github.io/netex-viz)

**Eigene NeTEx-Datei laden:**
1. XML-Datei per Drag & Drop ins Fenster ziehen, oder
2. «Eigene XML» Button klicken

Die Datei bleibt lokal im Browser — es werden keine Daten hochgeladen.

## Lokale Entwicklung

Kein Build-Step nötig. Einfach einen lokalen Webserver starten:

```bash
# Python
python3 -m http.server 3000

# Node.js
npx serve .
```

Dann: [http://localhost:3000](http://localhost:3000)

## Deployment

Bei jedem `git push` auf `main` wird das Tool automatisch via GitHub Actions deployed.

Der Status ist unter **Actions** im Repo sichtbar. Nach ca. 30 Sekunden ist die neue Version live.

## Unterstützte NeTEx-Elemente

| Element | Visualisierung |
|---|---|
| `StopPlace` | Koordinaten → Karte |
| `ScheduledStopPoint` | Name → Labels |
| `Line` | Metadaten → Detail |
| `ServiceJourney` | → Fahrplan + Liste |
| `TimetabledPassingTime` | → Marey + Detail |
| `StopPointInJourneyPattern` | Reihenfolge → Sequenz |

## Verwandte Projekte

- [NeTEx Realisierungsvorgabe Schweiz](https://github.com/openTdataCH/netexRealisationGuideSwitzerland)

## Lizenz

[MIT](LICENSE) © 2026 aschmid-code
