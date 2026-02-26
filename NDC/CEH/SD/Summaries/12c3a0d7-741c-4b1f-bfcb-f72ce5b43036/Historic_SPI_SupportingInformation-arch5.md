# Historic Gridded Standardised Precipitation Index (SPI) using gamma distribution with standard period 1961-2010 for the United Kingdom (1862-2015) - version 3

## Overview
- 5 km gridded Standardised Precipitation Index (SPI) data for the United Kingdom, a drought index based on precipitation probabilities.
- Calculated for accumulation periods: 1, 3, 6, 9, 12, 18, 24 months; for each of the 12 calendar months.
- Time span: 1862–2015; standard gamma distribution fit uses 1961–2010.
- Data format: NetCDF4, two-dimensional UK grids with twelve monthly grids per year file; one file per accumulation period.
- Projection: British National Grid; SPI values are normal scores (mean 0, stdev 1) with no units; range limited to -5 to +5.

## Data Provenance and Version History
- Data sources:
  - Met Office 5 km monthly rainfall gridded data (comprising UKCP09 data for 1910–1959 and 2001–2011, 1960–2000 monthly grids from daily grids, 2012–2015 updates, and historic droughts rescue data 1862–1909).
- Project context:
  - Historic droughts project (NE/L01016X/1); DrIVER and IMPETUS initiatives support development for drought understanding and management.
- Version history:
  - Version 3 updates underlying rainfall data (now Met Office grids) and adds a 9-month accumulation; standardization period remains 1961–2010.
  - Version 2 identical to Version 3 except for a data-transfer error that caused SPI18 files to be missing/substituted; Version 3 supersedes Version 2.
- Methodology note:
  - SPI calculation follows McKee et al. (1993); gamma distribution fitted via L-moments (using modified R SCI package) to obtain parameters; data transformed to standard normal scores.
  - Some literature suggests alternative distributions (e.g., Pearson Type III, Tweedie) may fit UK data better, but gamma remains the adopted standard for this dataset.

## Data Structure, Format, and Content
- Format: NetCDF4 adhering to CEH gridded dataset conventions.
- Structure: UK-wide 2D grids with 12 monthly grids per year; one file per accumulation period.
- Coverage: 1862–2015; standard period 1961–2010 for distribution fitting.
- Example of data interpretation: the 6-month SPI for July 1998 corresponds to precipitation from January–July 1998, with monthly SPIs derived for all accumulation periods.

## Data Quality, Limitations, and Uncertainties
- Autocorrelation considerations:
  - For accumulation periods >12 months, overlapping data introduce autocorrelation in the underlying time series.
  - Monthly SPIs may be autocorrelated when concatenated across months; use such series for trend analysis with appropriate adjustments.
- Data limitations:
  - 1960–2000 rainfall grids had localised issues; new monthly grids were derived from daily data (1960–2000) to improve reliability.
  - Serial dependence and potential under/over-representation at distribution tails due to gamma fit limitations; truncation at +/-5 mitigates extreme values.
- Future work:
  - Potential production of new SPI datasets using different distributions if justified by methodological advances.

## Access, Use, and Governance Guidance for Data Stewards
- Purpose and utility:
  - Enables spatial analysis of drought propagation, identification of severely affected areas, and assessment of short- to long-term precipitation anomalies across the UK.
- Metadata and provenance:
  - Include data sources (Met Office grids, UKCP09, historic droughts rescue data), version history (v3 supersedes v2), standard period used for fitting (1961–2010), and calculation methodology (gamma with L-moments, SCI package adaptation).
- Data management and updating:
  - Maintain clear lineage and versioning; document changes to underlying rainfall data and accumulation periods.
  Ensure compatibility with NetCDF4 and CEH conventions; track any future methodological changes (e.g., new distributions) and corresponding impacts on data products.
- Usage considerations:
  - Be mindful of serial correlation in long accumulation periods when performing trend analyses; consider adjusting statistical methods accordingly.
  - Attribute appropriate references for the SPI methodology and data provenance in any downstream usage.

## Acknowledgments and References
- Acknowledges support from DrIVER (NE/L010038/1), Historic Droughts (NE/L01016X/1), and IMPETUS (NE/L010267/1) projects.
- Key references cited for methodology and data sources include McKee et al. (1993), Barker et al. (2015), Svensson et al. (2017), Gudmundsson & Stagge (2014), and related CEH-GEAR and SPI literature.