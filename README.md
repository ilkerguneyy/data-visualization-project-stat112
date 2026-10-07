# Auto Sales vs. Country Indicators — Tableau Dashboards

Do country-level economic and social indicators line up with how many cars a company sells there?
This Tableau workbook blends an auto-sales order dataset with a 2023 country-indicators dataset and explores
five questions with one dashboard each.

*Coursework for STAT 112 (Introduction to Data Processing and Visualization), Department of Statistics,
METU — Fall 2024.*

## Data

- **Auto sales:** order-level sales records (order date, product line, quantity, price, MSRP, deal size, customer
  country). A widely used public sample dataset; customer names and contacts in it are fictional.
- **Country indicators (2023):** GDP, population, urban population, CO₂ emissions, unemployment rate, total tax
  rate, gasoline price and others.
- The two sources are blended on country.

## What I built

- **Data preparation in Tableau:** cleaned currency fields stored as text (`$` removed, converted to numbers) and
  derived per-capita and percentage measures — GDP per person, CO₂ per person, urban population share,
  unemployment and tax rates as percentages.
- **Five question dashboards:**
  1. Quantity ordered vs. CO₂ emissions per person
  2. Quantity ordered vs. gasoline price and total tax rate
  3. Unemployment rate vs. MSRP
  4. Urban population share vs. number of orders and deal size
  5. GDP per person vs. quantity ordered
- **Overview:** a world map of quantity ordered by country, and a Tableau story that walks through the dashboards.

## Files

| File | What it is |
|---|---|
| `proje112twbx.twbx` | Packaged workbook — includes both datasets. **Open this one.** |
| `proje112.twb.txt` | The same workbook as plain XML (renamed to `.txt` so it can be read on GitHub) |

Open the `.twbx` with [Tableau Public](https://public.tableau.com/) or Tableau Reader (both free).

## Limitations

Each dashboard compares country-level aggregates, so with a few dozen countries the patterns are descriptive only —
they do not show that an indicator drives sales.
