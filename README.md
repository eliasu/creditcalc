# Kreditrechner

A browser-based mortgage and shared housing cost calculator, built for planning communal living projects — e.g. buying a property with multiple people and splitting costs fairly.

## What it does

Enter a property purchase, configure one or more loan tranches, and instantly see the monthly rent per person for groups of 5 to 20 people.

### Inputs

**Purchase costs**
- Purchase price (Kaufpreis)
- Renovation / modernisation costs
- Acquisition costs: broker fee, notary & land registry, real estate transfer tax (pre-filled for Brandenburg: 6.5%)

**Loan tranches** — add as many as you need (e.g. bank loan + private subordinated loan)
- Each tranche has its own amount, interest rate, and term
- An allocation bar shows whether the tranches exactly cover the total loan amount

**Monthly running costs**
- Operating costs (Betriebskosten)
- Investment costs (Investitionskosten)
- Maintenance reserve (Instandhaltungsrücklage) — entered as € per m² per year

**Target rent** — used only to colour the table cells (green = at or below target, red = above)

### Output table

Rows: 5 to 20 people  
Columns: one per loan phase (e.g. "Year 1–10" while all tranches run, "Year 11–30" after the short-term loan is repaid)

Hover over any cell to see the full cost breakdown per person:
- Credit repayment
- Operating costs
- Investment costs
- Maintenance reserve

## Features

- **Multi-tranche loans** — model a bank loan alongside a private subordinated loan with different rates and terms
- **Phase columns** — the table automatically splits into time phases based on when each loan ends
- **Color coding** — green to red gradient based on a configurable target rent
- **Share link** — encodes all inputs into a URL for easy sharing
- **Reset button** — returns all fields to defaults
- **LocalStorage** — saves your inputs between sessions

## Usage

No build step. Open `index.html` in a browser.

```
creditcalc/
├── index.html       # Calculator
├── inflation.html   # German inflation data 1994–2024 (context for interest rate)
└── styles.css       # Shared styles
```

## Defaults (Brandenburg, Germany)

| Field | Default |
|---|---|
| Purchase price | 600,000 € |
| Renovation | 400,000 € |
| Broker fee | 0 % |
| Notary & land registry | 2 % |
| Real estate transfer tax | 6.5 % |
| Bank loan | 800,000 € · 4 % · 30 years |
| Subordinated loan | 200,000 € · 2 % · 10 years |
| Operating costs | 1,000 €/month |
| Investment costs | 500 €/month |
| Floor area | 336 m² |
| Maintenance reserve | 11.50 €/m²/year |
| Target rent | 650 €/person/month |
