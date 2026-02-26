# SPEI_IHU_groups dataset

- Purpose and use
  - Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Unit (IHU) groups.
  - Intended to support drought monitoring and analysis within a CEH droughts portal; aggregates SPEI over IHU groups to study drought over areas of interest.
  - Enables end-user self-service analyses through ready-made SPEI values by duration and month, with guidance for interpretation.

- What the dataset contains
  - SPEI values calculated for accumulation periods of 1, 3, 6, 12, 18, and 24 months, for each of the 12 calendar months.
  - Values are normal scores (mean 0, standard deviation 1), unitless, truncated to [-5, 5].
  - Data cover 1961–2012 (standard period used for distribution fitting: 1961–2010).
  - Stored in CSV format with 9 columns:
    - RID (row identifier)
    - POLYGONID (IHU group ID)
    - THEDATETIME (date and time)
    - SPEI_1, SPEI_3, SPEI_6, SPEI_12, SPEI_18, SPEI_24 (six temporal aggregations)
  - NoData value coded as -9999.
  - Spatial resolutions available: 1 km and 5 km grid datasets (to support both local and regional analyses).

- Data sources and inputs
  - Integrated Hydrological Units (IHU) groups (UK) as the spatial framework.
  - CEH-Gridded Estimates of Areal Rainfall (CEH-GEAR) for monthly rainfall grids.
  - CHESS PET dataset for potential evapotranspiration (PET).

- Methodology for deriving SPEI
  - SPEI is based on the cumulative Climatic Water Balance (CWB = precipitation − evapotranspiration).
  - For each location, SPEI is calculated for six durations (1, 3, 6, 12, 18, 24 months) and assigned to the month in which the accumulation ends.
  - Distribution fitting:
    - Primary fit using the generalised logistic (log-logistic) distribution via the SCI R package (maximum likelihood; fallback to L-moments, then method of moments if needed).
    - SPEI values are transformed to standard normal scores (mean 0, sd 1).
    - Extreme values truncated at ±5.
  - Note on data structure and autocorrelation:
    - For durations > 12 months, the underlying CWB series uses overlapping data, introducing autocorrelation.
    - Monthly SPEI series may also be autocorrelated when concatenating across months, which affects certain analyses (e.g., trend tests) and should be accounted for.

- Format and data interpretation
  - Dataset name reference: [SPEI_IHU_groups].
  - Temporal alignment: SPEI values correspond to the end of the accumulation period (e.g., 6-month SPEI for July 1998 covers Feb–Jul 1998).
  - The 9-column CSV structure facilitates joining to IHU shapefiles via POLYGONID.

- Data quality and limitations
  - Autocorrelation inherent due to overlapping accumulation periods.
  - Extreme values are truncated to maintain stable statistics.
  - Fitting period for the distribution is 1961–2010; dataset spans 1961–2012 (utilizes CHESS PET and CEH-GEAR data availability).

- Acknowledgments and references
  - Part of the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research); funded by NERC (award NE/L010038/1) as part of the Belmont Forum initiative.
  - Key methodological references include Vicente-Serrano et al. (2010a, 2010b, 2011, 2012, 2013), Stagge et al. (2015), and related SPEI literature.