# Standardised Precipitation Index time series for Integrated Hydrological Units Hydrometric Areas (1961-2012)

## Overview
- Time series of Standardised Precipitation Index (SPI) for IHU hydrometric areas, used to define and monitor drought and identify wet periods.
- SPI calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, each across all calendar months (72 series per location).
- Data intended for incorporation into CEH droughts portal to analyze drought at the level of specific hydrological units.
- SPI values are unitless “normal scores” with a mean of 0 and standard deviation of 1; values are truncated at ±5.

## Dataset scope and contents
- Time range: 1862 to 2015 (standard fitting period 1961–2010; historic data extend the series to 1862 thanks to digitised rainfall/temperature grids).
- Spatial units: Integrated Hydrological Units (IHU) hydrometric areas; coarsest spatial resolution within IHU.
- Format: CSV with 9 columns:
  - RID (row identifier)
  - POLYGONID (IHU hydrometric area ID)
  - THEDATETIME (date/time)
  - Columns 4–9: six SPI durations across 12 calendar months (72 time series per location)

## Data sources
- IHU hydrometric areas (UK-based IHU framework).
- Met Office 5-km monthly rainfall grids (UKCP09 data 1910–2011; updates 2012–2015; Historic Droughts digitised data for 1862–1909).

## Methodology
- SPI defined as per McKee et al. (1993): based on the cumulative precipitation probability for a given accumulation period.
- For each location and duration (1, 3, 6, 12, 18, 24 months) and for each calendar month, fit a gamma distribution to historical precipitation totals.
- Parameter estimation via L-moments (preferred over maximum likelihood in some cases) using a modified R package SCI.
- Transform precipitation totals to a normal distribution (mean 0, sd 1) to yield SPI values.
- Extreme value handling: SPI values beyond ±5 truncated to the limits.
- Serial correlation considerations:
  - Larger accumulation periods overlap in time, introducing autocorrelation.
  - SPIs for a given duration are not strictly independent; trend analyses should account for this.
- Notes on distribution choice:
  - Gamma distribution widely used and supported for Europe, but UK-specific studies suggest alternative distributions (Pearson type 3, Tweedie) may be more adequate in some cases.
- Standard fitting period: 1961–2010; data extend back to 1862 via historic gridded data, enabling long-term analysis.

## Data format and interpretation
- SPI values are unitless, representing anomalies relative to the historical distribution.
- Typical interpretation ranges align with conventional SPI usage (short-term to long-term moisture conditions and drought severity).
- Data caveats:
  - Autocorrelation present for longer-duration SPIs due to overlapping data.
  - Distribution choice may influence extremes; future versions may explore alternatives.

## Data governance, sharing, and metadata
- Dataset is produced for and supports the CEH droughts portal and related projects (Historic Droughts; DrIVER; IMPETUS).
- Metadata and data provenance are noted through project collaborations and digitisation efforts; explicit licensing is described within project documentation (open-data considerations referenced but not detailed here).
- Data quality is enhanced by sourcing from reputable gridded rainfall datasets and by applying standardized statistical approaches (L-moments, gamma distribution, SCIs).

## Usage considerations for monitoring frameworks
- Suitable for evaluating drought risk and moisture anomalies at the level of hydrometric areas, enabling policy-relevant monitoring across multiple time scales.
- Provides a consistent, reproducible method for generating comparative SPI time series across IHU units.
- Supports gap-filling and long-term trend assessment via extended historic data, while highlighting methodological limitations (distribution choice and autocorrelation) to be accounted for in decision-making.

## Acknowledgments and references
- Acknowledges support from DrIVER (NERC Belmont Forum), Historic Droughts (NERC), and IMPETUS projects.
- Key references include McKee et al. (1993) on SPI definition, Stagge et al. (2015) on candidate distributions, Barker et al. (2015), Gudmundsson & Stagge (2014) for the SCI package, Hayes et al. (2011) Lincoln Declaration, and Kral et al. (2015) on Integrated Hydrological Units.