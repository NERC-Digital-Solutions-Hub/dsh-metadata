# Supporting Information

## Overview
- Time series dataset of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPEI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with each accumulation period computed for all 12 calendar months.
- Standard period used to fit the distribution: 1961–2010; data cover 1961–2012.
- Data stored in CSV format and designed for incorporation into a drought portal (CEH droughts portal).

## Data Purpose and Context
- Enables study of drought over specific IHU hydrometric areas by aggregating SPEI across areas.
- SPEI accounts for evapotranspiration (CWB = precipitation minus evapotranspiration), providing a drought metric that reflects water balance.
- SPEI supports multi-temporal analysis (short to long-term droughts) and can be linked to hydrological and ecological variables.

## Data Sources
- IHU hydrometric areas (UK) as the spatial reference units.
- CEH-GEAR: 1 km monthly rainfall grids used to derive gridded SPEI.
- CHESS PET dataset: potential evapotranspiration data.

## Method for Deriving SPEI
- SPEI computation follows Vicente-Serrano et al. (2010a): based on the cumulative probability of CWB amounts for a given accumulation period.
- For each location and month, SPEI is assigned to the end month of the accumulation period (e.g., 6-month SPEI for July 1998 covers Feb–Jul 1998).
- Six accumulation periods (1, 3, 6, 12, 18, 24 months) across 12 months yield 72 time-series per location; in the dataset, each row includes end-month SPEI values for the six durations.
- Distribution fitting: generalised logistic (log-logistic) distribution used to model historic CWB accumulations. GEV was considered but found less appropriate for gridded SPEI data.
- Fitting performed with the R SCI package (fitSCI) using maximum likelihood; fallback to L-moments or method of moments if needed.
- SPEI values are transformed to standard normal scores (mean 0, sd 1), with units removed; values truncated at ±5 to handle extremes.
- Serial correlation considerations:
  - For accumulation periods > 12 months, overlapping data cause autocorrelation in the underlying annual CWB series.
  - Monthly SPEI series constructed by concatenating monthly SPEIs are also likely autocorrelated, which should be accounted for in trend analyses.

## Data Format and Structure
- File format: CSV.
- Key columns:
  - RID: row identifier.
  - POLYGONID: IHU hydrometric area ID (use for joins with shapefiles).
  - THEDATETIME: date and time (end of the accumulation period).
  - Columns 4–9: SPEI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months) at the end month; these are the normal scores with no units.
- Data value range: SPEI values approximately between -5 and +5; No Data = -9999.

## Spatial and Temporal Coverage
- Spatial: IHU hydrometric areas (coarsest spatial unit within IHU framework) with two grid resolutions provided (1 km and 5 km).
- Temporal: 1961–2012 (standard fitting period 1961–2010; dataset extends to 2012 due to data availability overlap).

## Data Quality, Limitations, and Considerations
- Autocorrelation: accumulation periods introduce overlapping data; impacts the assumption of independence in frequency analyses.
- Extreme values: truncation at ±5 mitigates instability at distribution tails.
- Data gaps and No Data values: -9999 indicates missing observations.
- Differences between distribution choices (generalised logistic vs. GEV) based on fit quality and tail behavior; rationale provided for choosing the generalized logistic distribution.
- Data provenance and reproducibility: dataset produced as part of the DrIVER project; funding via NERC and Belmont Forum; detailed references to data sources and methods.

## Provenance and Access
- Derived from IHU, CEH-GEAR, and CHESS PET datasets.
- Methods and software details (R package SCI) documented to enable replication.
- Acknowledgments indicate project support and funding sources.

## Practical Use for Analysts
- Suitable for identifying correlations between SPEI at different time scales and hydrological/ecological variables.
- Enables predictive modelling of drought likelihood and severity across UK hydrometric areas at multiple time scales.
- Can support drought monitoring and early warning within the CEH droughts portal or similar decision-support systems.
- Important to account for serial correlation and overlapping data when conducting trend or frequency analyses.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of Belmont Forum initiative.

## References (selected)
- Vicente-Serrano et al. (2010a, 2010b); Stagge et al. (2015); Beguería et al. (2014); Kral et al. (2015); Tanguy et al. (2014, 2015); Robinson et al. (2015); SO on.