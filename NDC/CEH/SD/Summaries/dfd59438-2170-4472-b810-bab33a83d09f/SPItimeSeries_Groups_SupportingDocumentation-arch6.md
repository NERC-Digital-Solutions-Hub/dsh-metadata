# Standardised Precipitation Index time series for IHU Groups (1961-2012) dataset

## Overview
- Time series dataset of Standardised Precipitation Index (SPI) for Integrated Hydrological Units (IHU) Groups in the UK.
- Contains 72 SPI time series per IHU group (6 accumulation periods × 12 calendar months) covering 1961–2012.
- Stored in CSV format with 9 columns; SPI values are unitless normal scores (mean 0, SD 1) truncated at ±5 (No Data coded as -9999).

## What the dataset is for
- Designed to support drought monitoring and analysis across defined geographic areas (IHU Groups), complementary to a CEH drought portal.
- SPI at multiple time scales provides short- to long-term moisture context (1, 3, 6, 12, 18, 24 months) for each month.

## Data sources and derivation
- Data sources:
  - IHU Groups (Kral et al., 2015) – spatial hydrological reference units (~400 km² typical) in the UK.
  - CEH-GEAR – 1 km resolution daily and monthly areal rainfall estimates used to derive area-averaged rainfall for each IHU group.
- Derivation approach:
  - SPI calculated per McKee et al. (1993) and assigned to the month in which the accumulation period ends (e.g., 6-month SPI for July 1998 uses Feb–Jul 1998 data).
  - For each IHU group, SPI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months across all 12 calendar months (72 series per group).
  - Distribution fitting: gamma distribution estimated with L-moments (instead of MLE) due to data issues; parameters estimated using an R adaptation of the SCI package.
  - Transformation to standard normal scores (mean 0, SD 1); SPIs are unitless.
  - Extreme values truncated: abs(SPI) > 5 set to ±5.
- Important notes:
  - Although gamma is widely used, UK-specific tests (Shapiro–Wilk) suggest Pearson type 3 or Tweedie may be more adequate in some cases; gamma remains in use with potential future updates.
  - Accumulation periods >12 months use overlapping annual data, creating autocorrelation in the underlying series.
  - Serial correlation is present in concatenated monthly SPIs; treat for trend analyses accordingly.
- Temporal scope and justification:
  - Standard period to fit distribution: 1961–2010.
  - Dataset period: 1961–2012.
  - Start in 1961 due to sparse early raingauge data (pre-1961 uncertainty).

## Format and content of the dataset
- File format: CSV.
- Core columns (9 total):
  - RID: row identifier.
  - POLYGONID: IHU Group ID (useful for joining with IHU shapefiles).
  - THEDATETIME: date and time (month-end reference).
  - Columns 4–9: SPI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months) across the 12 calendar months (i.e., different temporal aggregations of SPI).
- Data characteristics:
  - SPI values are normal scores (no units), range limited to -5 to +5.
  - No Data indicator: -9999.
  - SPI values are designed for cross-group drought/moisture comparisons and temporal trend analyses.

## Usage considerations and caveats
- Time-scale interpretation:
  - 1-month SPI aligns with short-term moisture/soil moisture stress.
  - 3-month SPI supports seasonal moisture context.
  - 6-, 12-, 18-, 24-month SPIs reflect medium- to long-term moisture conditions, with links to streamflows and reservoir levels.
- Data quality and methodological caveats:
  - Gamma distribution assumption; future versions may use alternative distributions (e.g., Pearson type 3, Tweedie) if warranted.
  - Overlapping data in longer accumulation periods induces autocorrelation; adjust analyses accordingly.
  - Serial correlation when concatenating monthly SPIs for trend analyses; standard statistical tests assuming independence may be inappropriate.
- Practical notes:
  - Data linked to IHU Groups via POLYGONID for join operations with shapefiles.
  - Intended for integration into drought dashboards, analyses of spatial drought patterns, and historical trend exploration.

## References
- Barker, L.J., et al. 2015; Svensson, C., et al. 2015; Gudmundsson, L. & Stagge, J.H. 2014; Hayes, M. et al. 2011; Keller, V.D.J. et al. 2015; Kral, F. et al. 2015; McKee, T.B. et al. 1993; National Drought Mitigation Center 2015; Stagge, J.H. et al. 2015; Tanguy, M. et al. 2014.