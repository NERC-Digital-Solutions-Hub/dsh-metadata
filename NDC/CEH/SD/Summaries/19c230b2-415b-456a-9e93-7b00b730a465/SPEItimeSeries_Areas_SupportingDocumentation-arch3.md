# Supporting Information

- I. Brief Description of the dataset
  - Time series of Standardised Precipitation-Evapotranspiration Index (SPEI) for Integrated Hydrological Units (IHU) hydrometric areas.
  - SPEI calculated for accumulation periods: 1, 3, 6, 12, 18, 24 months; each for 12 calendar months.
  - Data are autocorrelated due to accumulation and time series structure.
  - Standard fitting period: 1961-2010; dataset spans 1961-2012; stored in CSV format.

- II. Motivation
  - Derived to support a CEH droughts portal; enables drought analysis over specific IHUs by aggregating SPEI.
  - SPEI accounts for evapotranspiration (CWB) and is used to monitor drought across short- to long-term scales.
  - Widely used in drought-related studies and monitoring systems; facilitates understanding of drought rarity at chosen time scales.

- III.1 Data Sources
  - IHU hydrometric areas (UK) as spatial units.
  - CEH-GEAR: gridded monthly areal rainfall estimates for the UK.
  - CHESS PET dataset: potential evapotranspiration data.

- III.2 Method for deriving the SPEI grids
  - SPEI follows the original Vicente-Serrano et al. (2010a) definition: based on cumulative CWB distribution.
  - For each location and duration, 72 time series (6 durations × 12 months) are produced.
  - Distribution fitting: generalised logistic (log-logistic) distribution; SCI R package used for fitting (maximum likelihood; fallback to L-moments or method of moments if needed).
  - SPEI values are transformed to normal scores (mean 0, SD 1); unitless; truncated at ±5.
  - Note: overlapping data in longer durations creates autocorrelation; monthly series constructed from SPEIs ending in consecutive months are also likely autocorrelated.
  - Standardisation period: 1961-2010; data available for 1961-2012 due to data source limits.

- IV. Format of the [SPEI_IHU_HA] dataset
  - CSV file with 9 columns:
    - RID: row identifier
    - POLYGONID: IHU hydrometric area ID (joins with shapefile)
    - THEDATETIME: date and time
    - Columns 4-9: six temporal aggregations of SPEI (1, 3, 6, 12, 18, 24 months)
  - SPEI values are normal scores (unitsless); range limited to -5 to +5; -9999 indicates No Data.

- V. Acknowledgments
  - Project: DrIVER (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research).
  - Funded by the Natural Environment Research Council (award NE/L010038/1) under the Belmont Forum initiative.

- References
  - Tool and methodology references for SPEI calculation, distribution fitting, and datasets (e.g., Vicente-Serrano et al., Stagge et al., CEH-GEAR, CHESS PET, SCI package).