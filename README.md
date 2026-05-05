# Kreditrechner

Ein browserbasierter Kredit- und Wohnkostenrechner, entwickelt für die Planung von Gemeinschaftsprojekten — z.B. den Kauf einer Immobilie mit mehreren Personen und die faire Aufteilung der Kosten.

## Was er kann

Kaufpreis und Kreditkonditionen eingeben, beliebig viele Kreditposten konfigurieren, und sofort die monatliche Miete pro Person für Gruppen von 5 bis 20 Personen ablesen.

### Eingaben

**Kaufpreis & Nebenkosten**
- Kaufpreis
- Modernisierungskosten
- Kaufnebenkosten: Maklerprovision, Notar & Grundbuch, Grunderwerbsteuer (voreingestellt für Brandenburg: 6,5 %)

**Kreditposten** — beliebig viele (z.B. Bankkredit + privates Nachrangsdarlehen)
- Pro Posten: Betrag, Zinssatz, Laufzeit
- Fortschrittsbalken zeigt ob die Posten den Kreditbetrag genau abdecken

**Monatliche Kosten**
- Betriebskosten
- Investitionskosten
- Instandhaltungsrücklage — eingegeben als € pro m² pro Jahr

**Idealvorstellung** — dient nur zur Einfärbung der Tabellenzellen (grün = am oder unter dem Zielwert, rot = darüber)

### Ergebnistabelle

Zeilen: 5 bis 20 Personen  
Spalten: eine pro Kreditphase (z.B. „Jahr 1–10" solange alle Posten laufen, „Jahr 11–30" nach Rückzahlung des kurzfristigen Darlehens)

Hover über eine Zelle zeigt die vollständige Kostenaufschlüsselung pro Person:
- Kreditrate
- Betriebskosten
- Investitionskosten
- Instandhaltungsrücklage

## Features

- **Mehrere Kreditposten** — Bankkredit und privates Nachrangsdarlehen mit unterschiedlichen Konditionen kombinieren
- **Phasenspalten** — Tabelle teilt sich automatisch nach Laufzeitenden auf
- **Farbcodierung** — Grün-Rot-Verlauf basierend auf der eingestellten Idealvorstellung
- **Link teilen** — alle Eingaben werden in die URL kodiert
- **Reset-Knopf** — setzt alle Felder auf Standardwerte zurück
- **LocalStorage** — Eingaben bleiben zwischen Sitzungen gespeichert

## Verwendung

Kein Build-Schritt nötig. `index.html` im Browser öffnen.

```
creditcalc/
├── index.html       # Rechner
├── inflation.html   # Deutsche Inflationsdaten 1994–2024 (Kontext für Zinssatz)
└── styles.css       # Gemeinsame Styles
```

## Standardwerte (Brandenburg)

| Feld | Standard |
|---|---|
| Kaufpreis | 600.000 € |
| Modernisierung | 400.000 € |
| Maklerprovision | 0 % |
| Notar & Grundbuch | 2 % |
| Grunderwerbsteuer | 6,5 % |
| Bankkredit | 800.000 € · 4 % · 30 Jahre |
| Nachrangsdarlehen | 200.000 € · 2 % · 10 Jahre |
| Betriebskosten | 1.000 €/Monat |
| Investitionskosten | 500 €/Monat |
| Wohnfläche | 336 m² |
| Instandhaltungsrücklage | 11,50 €/m²/Jahr |
| Idealvorstellung | 650 €/Person/Monat |
