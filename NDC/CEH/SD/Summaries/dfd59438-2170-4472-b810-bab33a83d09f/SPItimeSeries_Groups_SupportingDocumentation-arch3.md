# Standardised Precipitation Index time series for IHU Groups (1961-2012) dataset

## Overview
- Time series of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups.
- SPI calculated for six accumulation periods: 1, 3, 6, 12, 18, 24 months, each for every calendar month.
- Distribution fitting period: 1961-2010; dataset covers 1961-2012.
- Data stored in CSV format.

## Motivation and use
- Designed to be incorporated into a CEH droughts portal; enables aggregation of SPI over IHU groups to study drought within a defined area.
- SPI is a widely used drought index, suitable for assessing rarity of drought at various time scales and identifying anomalously wet periods.
- Different accumulation periods provide insights into short-, medium-, and long-term moisture patterns and their hydrological implications (soil moisture, crop stress, streamflows, reservoir levels, groundwater).

## Data sources
- Integrated Hydrological Units (IHU) Groups (Kral et al. 2015) as spatial units.
- CEH-Gridded Estimates of Areal Rainfall (CEH-GEAR) daily/monthly rainfall grids used to derive area-averaged rainfall for each IHU group.

## Methodology
- SPI defined as in McKee et al. (1993): based on the cumulative probability of precipitation for a given accumulation period; end month marks the accumulation period end.
- For each IHU group, SPI calculated for 6 durations (1, 3, 6, 12, 18, 24 months) across 12 calendar months, yielding 72 time series per group.
- Gamma distribution fitted to each time series using L-moments (to estimate parameters) instead of maximum likelihood.
- SPI transformation to a standard normal distribution (mean 0, SD 1); values are unitless; truncation applied at ±5 to limit extremes.
- R package SCI used (modified to apply L-moments for parameter estimation).
- Note on distributions: while gamma is widely used, some studies suggest alternatives (Pearson type 3, Tweedie) may be more suitable for the UK; gamma remains broadly accepted for now.
- Overlapping data for longer accumulation periods induces autocorrelation; SPIs for different months may not be independent, affecting frequency analysis and trend assessment.

## Dataset format and contents
- File format: CSV.
- Columns: 9 total.
  - RID: row identifier.
  - POLYGONID: IHU group ID (useful for joins with shapefiles).
  - THEDATETIME: date and time (month-end for the accumulation period).
  - Columns 4-9: SPI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months) across months as encoded in the rows.
- SPI values are normal scores from a standard normal distribution (mean 0, SD 1), unitsless; range typically within -5 to 5; -9999 denotes No Data.

## Temporal coverage and data quality notes
- Dataset period: 1961–2012.
- Baseline distribution fit uses 1961–2010; data prior to 1961 excluded due to sparse raingauge networks and higher uncertainty (CEH-GEAR context).
- Practical implications:
  - Longer accumulation periods (>12 months) involve overlapping data, increasing potential autocorrelation.
  - Monthly SPIs concatenated into longer series are likely autocorrelated; account for this in trend analyses.

## Data governance and access considerations
- Data provenance is explicit: SPI derivation relies on IHU group definitions and CEH-GEAR rainfall inputs.
- Methodological transparency (gamma/L-moments, SCI package) supports reproducibility, with notes on distribution choice and potential alternatives.
- Data sharing and openness considerations discussed in the broader monitoring framework context (ensuring metadata, data quality, and governance standards are upheld; public sharing of underlying datasets may present barriers in some cases). The dataset itself provides clear metadata within the description and references to source materials.

## Key references
- McKee, Doesken, Kleist (1993). The Relationship of Drought Frequency and Duration to Time Scales.
- Kral, Fry, Dixon (2015). Integrated Hydrological Units of the United Kingdom: Groups.
- Tanguy et al. (2014, 2015). CEH-GEAR; gridded rainfall data; methodological notes.
- Barker et al. (2015); Svensson et al. (2015); Stagge et al. (2015); Gudmundsson & Stagge (2014); Hayes et al. (2011). Drought indices, distributions, and interpretation guidelines.