# Supporting Information

## I. Brief Description of the dataset
- Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) groups.
- SPEI is a drought index based on the Climatic Water Balance (CWB = precipitation minus evapotranspiration) over a specified accumulation period.
- Calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; for each, values are produced for all 12 calendar months.
- Time series are likely autocorrelated due to overlapping accumulation periods.
- Standardisation period used to fit distributions: 1961–2010.
- Data coverage: 1961–2012.
- Data stored in CSV format.

## II. Motivation
- Derived to support CEH droughts portal by aggregating SPEI over IHU groups to study drought within specific areas.
- SPEI vs SPI: SPEI accounts for evapotranspiration (CWB), providing a drought measure that reflects water supply minus demand.
- SPEI can indicate drought rarity at multiple time scales, useful for short- to long-term moisture assessments.
- Applications across drought variability, reconstruction, atmospheric mechanisms, climate change impacts, and drought monitoring systems; many studies show SPEI correlates better with hydrological/ecological variables than other indices.
- Interpretation by time scale:
  - 1-month: short-term moisture, soil moisture/crop stress.
  - 3-month: short- to medium-term moisture, seasonal CWB.
  - 6-month: medium-term trends, potential link to streamflows/reservoirs.
  - 12-month: long-term CWB, related to streamflows/reservoirs.
  - 18–24-month: longer-term CWB, groundwater implications.
- Rationale for two resolutions (1km and 5km): fine local analysis (1km) and region-wide analysis with smaller, quicker-to-load files (5km).

## III.1 Data Sources
- Integrated Hydrological Units (IHU) groups (UK) as spatial reference units.
- CEH-Gridded Estimates of Areal Rainfall [CEH-GEAR] for monthly rainfall grids.
- CHESS PET dataset for potential evapotranspiration.

## III.2 Method for deriving the SPEI grids
- SPEI calculation follows Vicente-Serrano et al. (2010a): based on the cumulative probability of observed CWB amounts for each location and accumulation period.
- For each location and duration, SPEI values are assigned to the month in which the accumulation period ends (e.g., 6-month SPEI ending July 1998 covers Feb–Jul 1998).
- Distribution fitting:
  - Generalised logistic distribution (log-logistic) used to model CWB accumulations.
  - Debate on using Generalised Extreme Value (GEV); authors argue GL fits better for gridded data, avoids infinite SPEIs, and provides more reasonable tail behavior for a fixed standardisation period.
  - Parameter estimation via R SCI package: fitSCI uses maximum likelihood; falls back to L-moments, then method of moments if necessary.
  - SPEI transformed to normal scores (mean 0, sd 1) with no units.
  - Extreme values truncated at abs value 5.
- Temporal considerations:
  - Accumulations longer than 12 months involve overlapping data, introducing autocorrelation.
  - Monthly SPEIs concatenated across months are also likely autocorrelated; use in trend analysis requires accounting for serial correlation.
- Standard period: 1961–2010; dataset period 1961–2012 due to data availability (CHESS PET and CEH-GEAR).

## IV. Format of the [SPEI_IHU_groups] dataset
- CSV file with 9 columns:
  - RID: row identifier
  - POLYGONID: IHU group ID (for joins with shapefiles)
  - THEDATETIME: date and time
  - Columns 4–9: different temporal aggregations of SPEI (the six accumulation periods across 12 months)
- SPEI values are normal scores (mean 0, sd 1), no units, range limited to -5 to +5.
- -9999 indicates No Data.

## V. Acknowledgments
- Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
- Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.