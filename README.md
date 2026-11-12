# Location – TradingView Indikatoren

## Smart Key Levels (`SmartKeyLevels.pine`)

Pine Script v6, `overlay=true`.

**Einbauen:** TradingView → Pine-Editor → Inhalt von `SmartKeyLevels.pine` einfügen → „Zum Chart hinzufügen".

**Funktionen**
- Volumenprofil (POC, VAH/VAL, Volumen-Berge mit Ober-/Unterkante, optional Balken am rechten Rand)
- Tageshoch/-tief und Vortageshoch/-tief
- Magic Numbers (automatische oder eigene Schrittweite + eigene Liste)
- Lern-Gedächtnis: Swing-Level werden gespeichert; halten sie, steigt ihre Stärke, werden sie durchbrochen, sinkt sie
- Eigene Zonen per Einstellungen (`von-bis; von-bis; Preis`) → werden gezeichnet und geben Level Bonus-Score
- Scoring (Volumen, Reaktionen, Konfluenz, Magic, Zone) → nur die besten N Level, ★ = Qualität, Tabelle oben rechts

**Grenzen von Pine Script:** Ein Indikator kann deine mit dem Zeichentool gezeichneten Linien/Boxen nicht auslesen und nichts dauerhaft speichern. Eigene Bereiche werden deshalb in den Einstellungen eingetragen. Das „Lernen" funktioniert über die Chart-Historie (Swing-Gedächtnis), nicht über ein trainiertes Modell.

### NQ / MNQ / ES / MES
Werden automatisch erkannt: Magic Numbers im 25/50/100-Punkte-Raster.

### Alerts
Alert anlegen → Bedingung „Smart Key Levels" → „Beliebiger alert()-Funktionsaufruf". Meldet Berührung von Key-Levels (ab wählbarer ★-Zahl) und den Bruch von Vortag-H/L, einmal pro Bar-Schluss.
