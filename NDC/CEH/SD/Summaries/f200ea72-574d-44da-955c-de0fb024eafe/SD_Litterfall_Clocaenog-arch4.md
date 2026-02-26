# Details of data structure for 'Litterfall_Clocaenog.csv'

## Overview
- Supplement to the supporting documentation for data series. 
- Dataset consists of one spreadsheet with 48 columns describing litterfall measurements.

## Dataset structure
- Columns 1–28: litterfall data in g litter per sample quadrat; Column 1 is the sampling date (10/11/1999 to 14/06/2011); Columns 2–28 contain experimental details (Plot, Block, Treatment, and sampling quadrats).
- Columns 29–38: plot-level mean litterfall data; Column 29 is the date (10/11/1999 to 14/06/2011); Columns 30–38 contain mean litterfall mass per plot for plots 1–9.
- Columns 39–48: plot-level mean litterfall data per unit area; Column 39 is the date (10/11/1999 to 14/06/2011); Columns 40–48 contain mean litterfall mass per area.
- Empty cells indicate no data available for that day.

## Temporal coverage and data availability
- Date range covered: 10/11/1999 to 14/06/2011.
- Missing data represented by empty cells.

## Provenance and related documentation
- Related to Clocaenog supporting documentation for data series (referenced as 'Clocaenog_supporting documentation_Data series.rtf').
- Specifically documents the data structure for Litterfall_Clocaenog.csv.

## Data governance and usage notes
- Contains both raw (per-sample quadrat) and aggregated metrics (per-plot and per-area).
- Units:
  - Raw: g litter per sample quadrat.
  - Aggregated: mean litterfall mass per plot and per unit area.
- Metadata captured in columns 2–28 (Plot, Block, Treatment, sampling quadrats); essential for correct data mapping and analysis.
- Data quality considerations:
  - Missing values are represented as empty cells; plan handling during analysis.
  - Ensure consistent interpretation of dates and units when integrating raw and aggregated data.