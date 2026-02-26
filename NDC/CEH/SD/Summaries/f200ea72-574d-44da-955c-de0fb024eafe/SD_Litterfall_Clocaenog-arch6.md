# Details of data structure for 'Litterfall_Clocaenog.csv'

## Overview
- A single spreadsheet containing 48 columns.

## Column descriptions
- Columns 1–28: Litterfall data in grams per litter per sample quadrat.
  - Column 1: sampling date, spanning 10/11/1999 to 14/06/2011.
  - Columns 2–28: experimental details — Plot, Block, Treatment, and sampling quadrats.
- Columns 29–38: Plot-level mean litterfall data.
  - Column 29: date (same range as above).
  - Columns 30–38: mean litterfall mass per plot for plots 1–9.
- Columns 39–48: Plot-level mean litterfall data per unit area.
  - Column 39: date (same range as above).
  - Columns 40–48: mean litterfall mass per area.
- Note: Empty cells indicate no data available for that day.

## Timeframe
- Sampling dates range from 10/11/1999 to 14/06/2011.

## Data source reference
- Supplemental to the supporting documentation for data series described in: "Clocaenog_supporting documentation_Data series.rtf".

## Data quality considerations
- Data includes multiple formats and potential gaps; refer to Columns 1–28 for raw quadrat data and Columns 29–48 for aggregated plot-level metrics.
- Empty cells represent missing observations requiring handling during analyses.

## Practical use for end users
- Enables self-service analyses across:
  - Per-quadrat litterfall time series.
  - Per-plot mean litterfall over time.
  - Per-area mean litterfall over time.
- Suitable for building dashboards, reports, and data visualizations; supports cross-referencing with the experimental design (Plot, Block, Treatment).