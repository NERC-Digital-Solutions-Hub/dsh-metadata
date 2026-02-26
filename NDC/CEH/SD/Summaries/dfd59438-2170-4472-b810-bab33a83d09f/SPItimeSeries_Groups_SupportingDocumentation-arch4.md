# I. Brief Description of the dataset

## Overview
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) groups.
- Derived to support inclusion in a CEH droughts portal; aggregated SPI across IHU groups enables region-specific drought analysis.
- SPI is a drought indicator based on precipitation probability; calculated for multiple accumulation periods (1, 3, 6, 12, 18, 24 months) and for each calendar month.
- Coverage: 1961–2012 (fitting period 1961–2010); data stored in CSV format.

## Data content and scope
- 72 time series per IHU group (6 durations × 12 calendar months).
- SPI values are “normal scores” (mean 0, SD 1; unitless), truncated to |SPI| ≤ 5; -9999 denotes No Data.
- Nine columns total in the CSV: RID, POLYGONID (IHU group ID), THEDATETIME, and six SPI aggregations (one per duration) for each month.

## Data sources and methodology
- Data sources:
  - IHU groups (Kral et al., 2015) from UK hydrological references.
  - CEH-GEAR gridded rainfall estimates (Tanguy et al., 2014; Keller et al., 2015) used to derive area-averaged rainfall for each IHU group.
- SPI calculation approach:
  - Based on cumulative precipitation for each accumulation period ending in a given month.
  - Gamma distribution fitted to historical accumulation series; parameters estimated with L-moments (preferred over maximum likelihood in some cases).
  - SPI transformed to a standard normal distribution (mean 0, SD 1).
  - Calculation uses a modified R SCI package; truncation applied for extreme values.
  - Acknowledges ongoing debate about using gamma vs. Pearson type 3 or Tweedie distributions; gamma used here for consistency with many drought datasets.
- Temporal considerations:
  - For >12-month SPI, overlapping data introduce autocorrelation; serial correlation acknowledged for trend analysis and other applications.

## Format and data structure
- Format: CSV.
- Columns:
  - RID (row identifier)
  - POLYGONID (IHU group ID; join key to shapefile)
  - THEDATETIME (date and time)
  - SPI1, SPI3, SPI6, SPI12, SPI18, SPI24 (six duration-based SPI values per month)
- SPI values: normal scores, range approximately -5 to 5; -9999 indicates no data.

## Data quality, limitations, and caveats
- Data only from 1961–2012 due to data density pre-1961; uncertainty increases prior to 1961.
- Gamma distribution limitations noted for UK data; alternative distributions may be explored in future updates.
- Autocorrelation due to overlapping accumulation periods; users performing frequency analysis or independent-event studies should account for this.
- Data provenance and processing steps (L-moments, GC package modifications) documented to support governance and reproducibility.

## Relevance for Data Leaders
- Aligns with data governance goals: clear data sources, lineage, and methodological transparency.
- Supports data discovery and metadata needs: explicit join key (POLYGONID), time stamps, and clear data definitions.
- Highlights data gaps and access considerations (data density, potential for paywalls/metadata complexity in broader contexts).
- Demonstrates an approach to multi-scale drought indicators and the importance of documenting limitations and rationale for distribution choices.

## References
- Barker et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011); Keller et al. (2015); Kral et al. (2015); McKee et al. (1993); National Drought Mitigation Center (2015); Stagge et al. (2015); Svensson et al. (2015); Tanguy et al. (2014).