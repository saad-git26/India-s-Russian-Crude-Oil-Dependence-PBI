# India-s-Russian-Crude-Oil-Dependence-PBI
  Interactive Power BI dashboard on India's Russian crude oil imports (2021 to 2026). Tracks monthly import volume (mbpd), yearly import value (USD bn) and Russia's share of India's supply, with slicers, KPI cards and a custom dark navy and amber theme. Built with Power BI, Power Query and Excel, no DAX.


# India's Russian Crude Oil Dependence (2021 to 2026) | Power BI Dashboard

  An interactive Power BI dashboard that tracks how much crude oil India imports from Russia, how much it costs, and how big Russia's share of India's oil supply has become between 2021 and 2026.


## Project Objective

  After 2022, Russia went from a minor supplier to one of India's largest crude oil sources. This project answers simple questions with data:

- How much Russian crude did India import each month (in million barrels per day)?
- How did the import value (USD billion) change year by year?
- How big is Russia's share in India's total crude imports?
- How did events like sanctions affect imports?

## Key Insights

- **Peak import:** 2.70 mbpd in June 2026 (a record month).
- **Lowest import:** 1.05 mbpd in February 2026, after sanctions on Rosneft and Lukoil (Nov 2025) pulled imports down.
- **Average import:** 1.83 mbpd across the months with verified data.
- **Import value:** grew from USD 1.1 bn (2021-22) to USD 54 bn (2023-24), then eased to USD 50.2 bn (2024-25).
- **Russia's share:** rose from about 2% (2021-22) to about 35% (2024-25).

## Dashboard Features

- **4 KPI cards:** Peak Import, Lowest Import, Average Import, Peak Russia Share
- **Line chart:** monthly Russian crude import (mbpd)
- **Column chart:** import value by financial year (USD bn)
- **Bar chart:** Russia's share by financial year (%)
- **Detail table:** month, import volume (mbpd) and notes
- **Interactive slicers:** month range slider and financial year filter; every visual updates together
- **Custom design:** dark navy and amber theme, custom background and a Power BI theme file (`Russian_Crude_Navy_Amber_theme.json`)

## Data Model

  The Excel file `india_russia_crude_oil_powerbi_v2.xlsx` has 4 sheets:

| Sheet | Purpose | Key columns |
|---|---|---|
| Monthly_Data | Monthly import volume | Month, Financial_year, Russian_crude_mbpd, Source_ID, Note |
| Annual_Data | Yearly value and share | Financial_year, Import_value_usd_bn, Russia_share_pct, Source_ID, Note |
| Sources | Reference list of data sources | Source_ID, Source_Name, Website_Link |
| Quick_Summary | Simple Excel formulas (SUM, MAX, MIN, AVERAGE) | Measure, Value |

**Relationships (One-to-Many, single direction):**
- `Annual_Data[Financial_year]` to `Monthly_Data[Financial_year]`
- `Sources[Source_ID]` to `Monthly_Data[Source_ID]`

  No DAX is used. All KPIs come from simple built-in aggregations (Maximum, Minimum, Average).

## Tools Used

- **Power BI Desktop:** data modelling, visuals, theme
- **Power Query:** data cleaning (removed empty months, set data types)
- **Microsoft Excel:** data entry and simple formulas

## Data Sources

  Figures are collected from public reports, including Kpler (via Business Today and TASS), Swarajya, Himal Press, ThePrint, Carnegie and Hiru News. Full details are in the `Sources` sheet.

## Limitations

- Monthly data is available only for months where a reliable figure was found; other months are left blank, not estimated.
- Different sources give slightly different numbers (for example, 2024-25 import value is USD 50.2 bn in one source and about USD 56 bn in another). The dashboard uses the figure noted in the `Sources` sheet.
- Some monthly values are tracker estimates and may be revised later.
- 2025-26 and 2026-27 annual values are not yet available.

## How to Use

1. Download the repository.
2. Open `Russia_Oil_Dependence.pbix` in Power BI Desktop.
3. If the data path breaks: Home, Transform data, Data source settings, then point to `india_russia_crude_oil_powerbi_v2.xlsx`.
4. To apply the theme: Design, Themes, Browse for themes, then pick `Russian_Crude_Navy_Amber_theme.json`.
5. Use the slicers and click any visual to explore.

## Repository Contents

- `Russia_Oil_Dependence.pbix` : Power BI report
- `india_russia_crude_oil_powerbi_v2.xlsx` : dataset
- `Russian_Crude_Navy_Amber_theme.json` : custom theme
- `images/` : dashboard screenshots

## Author
**SAAD SHAIKH**
www.linkedin.com/in/saad-s-062baa286 | saad.shaikh1551@gmail.com

If you found this useful, please give the repo a star.
## README IS Generated with CLAUDE HELP
