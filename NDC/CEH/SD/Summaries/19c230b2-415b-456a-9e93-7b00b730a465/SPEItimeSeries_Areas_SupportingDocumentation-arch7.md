# Supporting Information

- This document describes the SPEI_IHU_HA dataset: time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas.
- SPEI is calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, with each period computed for all twelve calendar months.
- Data are stored as normal scores (mean 0, standard deviation 1) with no units; values are truncated to the range [-5, 5], and -9999 indicates No Data.
- Time frame: standardisation period 1961-2010; dataset covers 1961-2012 and is provided in CSV format.

## I. Brief Description of the dataset

- Time series of SPEI for each IHU hydrometric area (HA).
- Accumulation periods: 1, 3, 6, 12, 18, 24 months, each for all twelve months.
- Output is the SPEI end-of-period month (e.g., 6-month SPEI for July 1998 covers Feb–Jul 1998).
- 72 time series per location (6 durations × 12 months).

## II. Motivation

- Intended for integration into a CEH droughts portal to study drought over specific IHU areas.
- SPEI accounts for evapotranspiration (CWB = precipitation − evapotranspiration), improving drought relevance across hydrological and ecological analyses.
- Provides multi-scale drought information, with:
  - 1-month SPEI: short-term moisture/crop stress.
  - 3-month SPEI: short- to medium-term moisture, seasonal CWB estimates.
  - 6-month SPEI: medium-term moisture, potential links to flows and reservoirs.
  - 12-, 18-, 24-month SPEIs: long-term CWB patterns, groundwater considerations.
- Two spatial resolutions to support different GIS needs:
  - 1 km grids for fine-scale/local analyses.
  - 5 km grids for regional studies and smaller file sizes.

## III.1 Data Sources

- IHU hydrometric areas (UK) as the spatial framework.
- CEH-GEAR: gridded rainfall estimates (monthly and daily) for UK hydrological use.
- CHESS PET: potential evapotranspiration dataset.

## III.2 Method for deriving the SPEI grids

- SPEI follows Vicente-Serrano et al. (2010a): based on the cumulative CWB distribution for each location and accumulation period.
- For each location, compute SPEI for six durations and twelve months (72 series).
- Distribution fitting:
  - Primary: generalised logistic (log-logistic) distribution, estimated with maximum likelihood via the SCI R package.
  - If ML fails, use L-moments; if that fails, use method of moments.
- Transformation:
  - Convert the fitted distribution to normal scores (mean 0, sd 1).
  - Truncate extreme values to [-5, 5].
- Serial correlation considerations:
  - Overlapping data for longer durations leads to autocorrelation in the CWB time series and SPEI series.
  - Monthly SPEIs ending in each calendar month may also be autocorrelated due to overlapping data.
- Standard period used for fitting: 1961–2010.
- Data period available: 1961–2012 (due to data availability from CHESS PET and CEH-GEAR).

## IV. Format of the [SPEI_IHU_HA] dataset

- Stored in CSV format with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU HA ID (for joining with HA shapefile)
  - THEDATETIME: date and time
  - Columns 4–9: six temporal aggregations of SPEI (1, 3, 6, 12, 18, 24 months)
- SPEI values are normal scores (no units) in the range [-5, 5]; -9999 denotes No Data.

## V. Acknowledgments

- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.