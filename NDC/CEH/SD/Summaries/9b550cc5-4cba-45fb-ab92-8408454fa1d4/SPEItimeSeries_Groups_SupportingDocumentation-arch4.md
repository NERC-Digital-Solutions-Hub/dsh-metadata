# Supporting Information

- ## I. Brief Description of the dataset:
  - Contains time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) groups.
  - SPEI is a drought index based on Climatic Water Balance (CWB = precipitation minus evapotranspiration) for various accumulation periods (1, 3, 6, 12, 18, 24 months), each for the 12 calendar months.
  - Values are autocorrelated due to accumulation periods and calendar-month alignment.
  - Standard distribution fitting uses 1961–2010; dataset covers 1961–2012.
  - Data are stored in CSV format.

- ## II. Motivation
  - Aimed to support incorporation into a CEH droughts portal; aggregating SPEI over IHU groups enables area-specific drought analysis.
  - SPEI accounts for evapotranspiration, unlike SPI, providing a comprehensive drought perspective.
  - Different accumulation periods yield information at various time scales:
    - 1-month: short-term soil moisture/crop stress
    - 3-month: short- to mid-term moisture and seasonal CWB
    - 6-month: medium-term CWB trends, potential links to streamflow/reservoirs
    - 12-month: long-term CWB patterns, linked to streamflow/reservoirs
    - 18/24-month: longer-term CWB, potentially groundwater signals
  - Two spatial resolutions (1 km and 5 km) address local-detail needs and faster regional analyses.

- ## III. Data Sources
  - IHU groups (Integrated Hydrological Units of the UK) as spatial reference units.
  - CEH-GEAR: gridded estimates of daily/monthly areal rainfall for UK hydrological use.
  - CHESS PET: potential evapotranspiration dataset.

- ## III.2 Method for deriving the SPEI grids
  - SPEI computation follows Vicente-Serrano et al. (2010a): based on the cumulative probability of CWB amounts; SPEI for a given accumulation period ends in the corresponding end month.
  - For each location, SPEI is computed for 6 durations and 12 months (72 time series per location).
  - A statistical distribution is fitted to each historic CWB accumulation time series; default is the generalised logistic (log-logistic) distribution. Considerations:
    - GEV was considered but found to be less suitable for gridded data and tails; generalised logistic provides more stable, realistic return periods with fixed standardisation.
    - Parameter estimation via the SCI R package (maximum likelihood; fallbacks to L-moments or method of moments if needed).
  - SPEI is transformed to standard normal scores (mean 0, sd 1) with no units; values truncated at ±5.
  - Note on autocorrelation:
    - For durations >12 months, overlapping data cause autocorrelation in the underlying CWB series.
    - Concatenated monthly SPEI series may also be autocorrelated; relevant for trend analyses.
  - Standard fitting period: 1961–2010; data period: 1961–2012 (due to CHESS PET and CEH-GEAR data availability).

- ## IV. Format of the [SPEI_IHU_groups] dataset:
  - CSV with 9 columns:
    - RID (row identifier)
    - POLYGONID (IHU group ID; use for joins with shapefiles)
    - THEDATETIME (date/time)
    - Columns 4–9: six SPEI aggregations (one for each accumulation period across months)
  - SPEI values are normal scores (mean 0, sd 1), range -5 to 5; -9999 denotes No Data.

- ## V. Acknowledgments:
  - Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research)
  - Funding: Natural Environment Research Council (award NE/L010038/1) as part of the Belmont Forum initiative.

- ## References
  - The dataset relies on a broad literature base for SPEI methodology, distribution fitting, and drought indices, including Vicente-Serrano et al. (2010a, 2010b), Stagge et al. (2015), and related hydrological data sources (CEH-GEAR, CHESS PET).