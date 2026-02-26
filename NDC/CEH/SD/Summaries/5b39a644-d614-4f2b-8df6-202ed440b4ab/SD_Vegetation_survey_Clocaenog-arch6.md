# Details of data structure for 'Vegetation survey_Clocaenog.csv'

## Overview
- Supplement to the supporting documentation for data series (Clocaenog project).
- Single spreadsheet containing 22 columns.

## Data Structure and Content
- Columns 1-12: plot-level plant biomass data per unit area detailed for species over time.
  - Column 1: Year (1998–2012).
  - Column 2: Plant species.
  - Column 3: Biomass type indicator (total biomass vs. living biomass only).
  - Columns 4-12: Biomass measurements for experimental plots 1–9 corresponding to the species and year.
- Columns 13-22: plot-level total plant biomass data per unit area over time.
  - Column 13: Year (1998–2012).
  - Columns 14-22: Total biomass measurements for experimental plots 1–9 corresponding to the year.
- Empty cells indicate missing data for that year/plot.

## Column Mapping (summary)
- 1: Year (1998–2012) for species-level data
- 2: Species
- 3: Biomass type (total vs living)
- 4-12: Species-level biomass by plots 1–9
- 13: Year (1998–2012) for total biomass data
- 14-22: Total biomass by plots 1–9

## Data Quality Considerations
- Missing data represented by empty cells; handle as missing values during analysis.
- Time span covers 1998–2012; ensure consistency when merging with other data sources.

## Practical Use for Data Support
- Suitable for creating time-series dashboards or reports at both species-level (by living vs total biomass) and plot-level total biomass.
- Requires data shaping (wide to long or vice versa) depending on the analysis (per-species trends vs. per-plot totals).
- Annotation needed to distinguish living vs total biomass via column 3 when interpreting results.

## Related Documentation
- Supplement to: Clocaenog_supporting documentation_Data series.rtf