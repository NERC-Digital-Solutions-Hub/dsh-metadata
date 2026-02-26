# Standardised Precipitation Index time series for IHU hydrometric areas (1961-2012)

## Overview
- Time series of Standardised Precipitation Index (SPI) calculated for IHU (Integrated Hydrological Units) hydrometric areas in the UK.
- SPI is a drought index based on precipitation probability for various accumulation periods, enabling drought monitoring and detection of anomalously wet periods.
- Dataset supports analysis across multiple time scales (short to long term) and is designed for integration into a drought portal.

## Data content and structure
- Accumulation periods: 1, 3, 6, 12, 18, 24 months; computed for each of the 12 calendar months.
- Per IHU Hydrometric Area, 72 time series are derived (6 durations × 12 months).
- Format: CSV with 9 columns:
  - RID (row identifier)
  - POLYGONID (IHU area ID for joins)
  - THEDATETIME (date/time)
  - Columns 4–9: SPI aggregations corresponding to the six durations
- SPI values are normal scores (mean 0, sd 1), unitless; range typically within -5 to +5; -9999 denotes No Data.

## Derivation and methodology
- SPI calculation follows McKee et al. (1993): SPI for a given accumulation period ends in the month that completes that period.
- Distribution fitting: gamma distribution estimated using L-moments (instead of MLE) due to some non-robust fits; implemented via a modified R SCI package.
- Note: gamma distribution is widely used and accepted in drought research, but UK-specific tests (Shapiro–Wilk) suggest other distributions (e.g., Pearson type 3, Tweedie) may be more adequate in some cases; future versions may use alternative distributions.
- Data overlap: accumulation periods >12 months involve overlapping annual data, introducing autocorrelation; this affects independence assumptions for frequency analyses.
- Serial correlation: resulting monthly series constructed from overlapping data will be autocorrelated; appropriate adjustments needed for trend analyses.

## Data sources and time frame
- Primary spatial reference: Integrated Hydrological Units of the UK (IHU) – Hydrometric Areas.
- Areal rainfall input: CEH-GEAR (1 km resolution daily/monthly rainfall estimates).
- Temporal scope: 1961–2012; gamma-fit period based on 1961–2010 standardization.
- Rationale for start year: CEH-GEAR data were sparser before 1961, increasing uncertainty.

## Format and metadata
- Data stored as CSV; key fields:
  - RID, POLYGONID, THEDATETIME, SPI1m, SPI3m, SPI6m, SPI12m, SPI18m, SPI24m
- SPI values are unitless “normal scores”; absolute values >5 are truncated; -9999 indicates missing data.

## Data quality, limitations and caveats
- Autocorrelation due to overlapping accumulation periods; caution for frequency analysis and independence assumptions.
- Potential model limitations: gamma distribution may not perfectly fit UK rainfall; consideration of alternative distributions for future versions.
- Data start at 1961 due to sparse pre-1961 rainfall networks, limiting early-period uncertainty.

## Usage and provenance
- Intended for incorporation into CEH droughts portal to study drought characteristics over specific IHUs.
- SPI interpretation varies by timescale (short-term vs long-term drought indicators; seasonal to groundwater implications).

## References
- McKee, Doesken, Kleist (1993); Hayes et al. (2011); Stagge et al. (2015); Svensson et al. (2015); Tanguy et al. (2015); Keller et al. (2015); Kral et al. (2015); Barker et al. (2015); Gudmundsson & Stagge (2014).