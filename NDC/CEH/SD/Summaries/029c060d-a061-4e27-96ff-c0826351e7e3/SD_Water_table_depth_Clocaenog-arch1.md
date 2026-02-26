# Details of data structure for 'Water table depth_Clocaenog.csv'

- This document is a supplement to the supporting documentation for data series described in: 'Clocaenog_supporting documentation_Data series.rtf'.
- It describes the structure of the dataset named 'Water table depth_Clocaenog.csv'.

## Dataset structure
- The dataset consists of a single spreadsheet with 10 columns.
- Column 1 contains dates spanning from 13/05/1999 to 30/06/2015.
- Columns 2 to 10 contain water table depth measurements (in centimetres, cm) from the soil surface for experimental plots 1 through 9.
- Values indicating water below the water table are recorded as 'below detectable limit'.

## Key data characteristics to consider
- Data types: numeric depth values (cm) with occasional non-numeric placeholder text ('below detectable limit') for undetectable depths.
- Temporal coverage: over 16 years (1999–2015), with potential gaps implied by data recording or detection limits.
- Spatial coverage: 9 experimental plots, enabling cross-plot comparisons of water table depth over time.

## Implications for analysis
- Pre-processing needed to handle 'below detectable limit' entries (e.g., censoring or imputation strategies).
- Ensure consistent date parsing and alignment across all plots.
- Potential for correlations and temporal trends across plots, requiring careful handling of mixed data types and any missing values.

## Metadata and provenance
- Part of the broader supporting documentation package for Clocaenog data series.
- The dataset is intended to be used in analyses of water table depth across time and plots, with accompanying documentation providing context.