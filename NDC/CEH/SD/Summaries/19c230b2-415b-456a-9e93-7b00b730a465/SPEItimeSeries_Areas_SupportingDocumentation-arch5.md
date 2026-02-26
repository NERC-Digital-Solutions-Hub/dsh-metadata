# Supporting Information

## Dataset Overview
- Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas (IHU HA). 
- Period: 1961–2012 (standardization 1961–2010). Data are stored in CSV format.
- SPEI calculated for six accumulation periods: 1, 3, 6, 12, 18, and 24 months, each across 12 calendar months (72 time series per location).
- Values are normal scores (mean 0, standard deviation 1), unitless, truncated to [-5, 5]; missing data flagged as -9999.
- Purpose: to support drought analysis and integration into a CEH droughts portal, enabling area-specific drought assessment across different timescales.

## Data Sources
- IHU hydrometric areas (UK) as the geographic basis.
- CEH-GEAR: gridded monthly rainfall estimates for UK hydrological use.
- CHESS PET dataset: potential evapotranspiration.

## Methodology
- SPEI computation follows Vicente-Serrano et al. (2010a): based on the cumulative Climatic Water Balance (CWB = precipitation − evapotranspiration) for each accumulation period and month-end.
- For each location and duration, a historic CWB time series is fitted with a statistical distribution.
- Preferred distribution: generalised logistic (log-logistic). Justification: robust fits for gridded data; GEV discouraged due to tail behavior and potential invalid parameter estimation in some cases.
- Fitting approach: SCI R package (fitSCI) using maximum likelihood; fallback to L-moments or method of moments if needed.
- Transformation: map fitted distribution to normal scores (mean 0, sd 1) with no units.
- Extreme value handling: SPEI magnitudes truncated at ±5.
- Autocorrelation considerations: longer durations (e.g., 18/24 months) involve overlapping data, introducing autocorrelation; monthly series also autocorrelated due to overlapping windows. Users should account for serial correlation in trend analyses.

## Dataset Format and Fields
- File format: CSV.
- Key columns (9 total):
  - RID: row identifier.
  - POLYGONID: IHU hydrometric area ID (use for joining with IHU shapefile).
  - THEDATETIME: date and time (end of the accumulation period).
  - Columns 4–9: SPEI values for the six accumulation periods (1, 3, 6, 12, 18, 24 months) for each month.
- Data characteristics: SPEI values are unitless normal scores; ranges approximately within [-5, 5], with most values between [-2, 2].
- NoData: -9999.

## Temporal Coverage and Standardization
- Standardization period: 1961–2010.
- Available data period: 1961–2012 (limited by CHESS PET and CEH-GEAR data).
- End-of-period alignment: SPEI for a given duration ends in a given month (e.g., 6-month SPEI for July 1998 corresponds to CWB from February–July 1998).

## Usage Context and Benefits
- Enables drought analysis over specific IHUs and supports aggregation at local (1 km) or regional (5 km) scales.
- Facilitates exploration of drought conditions across multiple timescales, informing hydrological and ecological studies.
- Supports incorporation into drought monitoring portals and data discovery through a standardized, well-documented SPEI dataset.

## Data Governance and Access Notes
- POLYGONID provides join capability to shapefiles representing IHU hydrometric areas for spatial analyses.
- Documentation indicates alignment with CEH-GEAR rainfall and CHESS PET datasets; users should reference these sources for provenance and potential updates.
- Acknowledgments: DrIVER project (NERC NE/L010038/1) under Belmont Forum initiative.

## Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (NERC).