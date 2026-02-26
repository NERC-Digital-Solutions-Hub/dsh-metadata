# Historic Droughts Inventory of drought references for Historic Standardised Precipitation Index time series for IHU hydrometric areas (1862-2015) - version 2

## Overview
- Time series of Standardised Precipitation Index (SPI) for IHU hydrometric areas (1862–2015), with SPI calculated for accumulation periods of 1, 3, 6, 9, 12, 18, and 24 months across all calendar months.
- Standard fitting period for the gamma distribution: 1961–2010; SPIs are normal scores with mean 0 and standard deviation 1, truncated at ±5 and stored in CSV format.
- Data supports multi-scale drought assessment: drought severity, duration, and timing across locations and time scales.

## Data Content and Structure
- Spatial-temporal coverage: IHU hydrometric areas (UK), 1862–2015; standardization period 1961–2010.
- Output format: CSV with 10 columns:
  - RID, POLYGONID, THEDATETIME, plus seven SPI aggregations (across the 7 accumulation periods for each month).
- SPI interpretation: higher values indicate wetter-than-average conditions; lower values indicate drier conditions.
- Data includes guidance on joining to spatial shapefiles via POLYGONID.

## Context and Purpose
- Part of two projects: DrIVER (Drought Impacts: Vulnerability thresholds in monitoring and Earlywarning Research) and Historic Droughts (UK-focused drought history; cross-disciplinary understanding of past droughts since the 19th century).
- Aims to advance drought monitoring, early warning, and policy-relevant understanding by aggregating SPI across IHUs and compiling drought references.
- Intended for incorporation into CEH droughts portal to enable users to study area-specific drought behavior.

## Data Sources and Methods
- Data sources:
  - IHU hydrometric areas (UK)
  - Met Office 5 km monthly rainfall grids (including UKCP09 data; various historical updates and rescues for 1862–1909)
- SPI calculation:
  - Based on McKee et al. (1993); cumulative precipitation over each accumulation period ends in a given month.
  - Gamma distribution fitted using L-moments (via modified SCI package) to transform to normal scores.
  - Data rescaled to a standard normal distribution (mean 0, sd 1); extreme values truncated at ±5.
- Accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; for each period, SPIs are computed for all 12 calendar months (84 time series per grid cell).
- Temporal dependencies noted:
  - For >12-month SPIs, overlapping data cause autocorrelation.
  - Monthly SPIs concatenated across months are also likely autocorrelated; users should account for serial correlation in trend analyses.
- Standard period for density fitting: 1961–2010.

## Data Quality, Limitations, and Considerations
- Distribution considerations: gamma distribution widely used but not perfect for UK data; alternatives like Pearson type 3 or Tweedie may be more suitable in some cases; current dataset uses gamma with justification and potential future updates.
- Data issues addressed: new monthly rainfall grids derived from daily data to replace earlier 1960–2000 grids due to localised issues.
- Data handling notes: No Data is coded as -9999; SPIs limited to -5 to +5.

## Usage and Applications
- Supports drought monitoring and historical drought research, enabling:
  - Multi-scale drought analysis over specific IHUs.
  - Cross-sector policy planning and resource management (water, agriculture, environment).
  - Integration with a drought portal for visualization and exploration by end users.
- Facilitates cross-reference with the Historic Droughts Inventory (hydrometeorological timelines and historical drought references).

## Acknowledgements and References
- Acknowledges DrIVER, Historic Droughts, and IMPETUS project contributions (NERC, Belmont Forum).
- Key references include: McKee et al. (1993); Stagge et al. (2015); Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); Kral et al. (2015); Tanguy et al. (2015, 2014).