# Supporting Information

- The document describes a time-series dataset of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Unit (IHU) groups, intended to support drought monitoring and environmental health assessment across defined hydrological areas.

## What the dataset contains

- Time series of SPEI for IHU groups (approximately 400 km2 per group) across accumulation periods of 1, 3, 6, 12, 18, and 24 months, calculated for each of the twelve calendar months.
- Data period: 1961–2012 (with standard distribution fitting performed on 1961–2010).
- Data stored as CSV with 9 columns; SPEI values are normal scores (mean 0, standard deviation 1), unitless, typically within -2 to +2 (extremes capped at ±5). No-data value is -9999.
- Each row includes:
  - RID (row identifier)
  - POLYGONID (IHU group ID)
  - THEDATETIME (date/time)
  - Six SPEI aggregations (one for each accumulation period) across months

## Purpose and use

- Designed to be incorporated into a CEH droughts portal and to allow drought analysis over specific IHU areas.
- Aggregating SPEI over IHU groups enables monitoring of drought conditions within user-defined regions and on multiple time scales.
- SPEI incorporates evapotranspiration (CWB = precipitation – evapotranspiration), providing a drought measure that can be more closely related to hydrological and ecological responses than precipitation alone.

## Data sources

- IHU groups (Integrated Hydrological Units of the UK)
- CEH-GEAR: gridded estimates of areal rainfall (monthly)
- CHESS PET dataset (potential evapotranspiration)

## Methodology

- SPEI calculation follows Vicente-Serrano et al. (2010a): based on the probability distribution of Climatic Water Balance (CWB) accumulations for each location.
- Accumulation periods (1, 3, 6, 12, 18, 24 months) are computed and assigned to the month in which the accumulation ends (e.g., 6-month SPEI for July 1998 uses Jan–Jul 1998 CWB).
- Distribution fitting:
  - Generalised logistic (log-logistic) distribution used to model historic CWB accumulations.
  - R package SCI employed; parameters estimated by maximum likelihood; failures fallback to L-moments or method of moments.
  - Transformation to normal scores to obtain unitless SPEI values.
  - Values truncated at ±5 due to distribution tail uncertainty.
- Autocorrelation considerations:
  - For accumulation periods > 12 months, overlapping data cause autocorrelation in the underlying CWB series.
  - Monthly SPEIs concatenated from consecutive months are also likely autocorrelated; informs users to account for serial correlation in trend analyses.
- Standard fitting period: 1961–2010; data availability limited to 1961–2012 due to CHESS PET and CEH-GEAR data ranges.

## Dataset format and GIS use

- CSV file with 9 columns; structure supports joining to IHU shapefiles via POLYGONID.
- Columns 4–9 contain the six temporal SPEI aggregations.
- SPEI values are unitless, normally distributed scores; use for mapping drought severity across space and time.

## Spatial resolutions and applicability

- Two gridded resolutions are provided (1 km and 5 km) to accommodate different research needs:
  - 1 km: finer, local area analysis
  - 5 km: smaller file sizes, suitable for regional drought assessments

## Acknowledgments and references

- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research)
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of Belmont Forum initiatives

## Practical considerations for analysts

- Use POLYGONID to join SPEI time series to IHU group polygons for regional monitoring.
- Consider autocorrelation when performing trend analyses, especially for longer accumulation periods (18–24 months).
- Compare SPEI across multiple accumulation periods to assess short-term vs. long-term drought signals.
- Leverage the two resolutions to balance detail (local insights) with computational efficiency (regional assessments).