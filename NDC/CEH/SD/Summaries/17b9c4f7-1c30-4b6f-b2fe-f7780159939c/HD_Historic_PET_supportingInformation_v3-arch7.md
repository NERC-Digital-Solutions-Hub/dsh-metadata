# Historic Gridded Potential Evapotranspiration (PET) based on temperature-based equation McGuinness-Bordne calibrated for the UK (1891-2015)

- What the dataset is
  - A 5 km gridded dataset of Potential Evapotranspiration (PET) for the UK, using a temperature-based McGuinness-Bordne equation calibrated for the UK.
  - Covers 1891–2015 with daily PET grids (mm/day) and monthly PET grids (mm/month).
  - Includes quality metrics grids to quantify spatial data quality.
  - Stored in NetCDF4 format following CEH gridded dataset conventions; projected on the British National Grid.

- Data content and structure
  - Daily PET grids: 5 km resolution, UK extent, one grid per day (365 or 366 per year).
  - Monthly PET grids: 5 km resolution, UK extent, 12 grids per year.
  - Four accompanying metric NetCDF files (two daily metric files and two monthly metric files) documenting data quality.
  - Data are provided in NetCDF4 with the British National Grid projection.

- Calibration, data sources, and methodology
  - Calibration: McGuinness-Bordne equation calibrated for the UK using a 1961–1990 period (UK-specific parameter tuning).
  - Data sources:
    - Met Office 5 km monthly mean temperature grids (1910–2011 from UKCP09, 2012–2015 updates, and 1891–1909 rescued data).
    - CHESS temperature data used to calibrate the equation (1961–1990) and CHESS PET data used for evaluation (1991–2012).
  - Process:
    - Daily temperatures derived by disaggregating monthly Met Office data using a pchip interpolation method.
    - PET grids computed from daily temperatures via the calibrated McGuinness-Bordne equation; monthly PET grids are sums of daily PET grids.
  - Alternative PET formulations were evaluated; the UK-calibrated McGuinness-Bordne provided the best performance for the UK.

- Quality assessment and metrics
  - Metrics used to evaluate PET accuracy against CHESS PET (Penman-Monteith reference) over 1991–2012:
    - Nash-Sutcliffe efficiency (NSE)
    - Mean absolute percentage error (MAPE)
    - Correlation coefficient
    - Bias ratio
    - Variability ratio (VR)
    - Kling-Gupta efficiency (KGE)
  - Metrics are provided for both daily and monthly datasets; MAPE is available as mean monthly values to inform uncertainty.

- Relevance for GIS and data use
  - Enables spatially explicit hydrological and drought analyses across long historical periods.
  - Suitable as input for hydrological models and drought forecasting assessments when combined with other GIS layers.
  - Useful for mapping spatial variability in PET across the UK and for regional analyses of evapotranspiration trends.
  - NetCDF4 format supports integration in GIS workflows and allows extraction of regional time series and cross-plot analyses.

- Provenance, context, and projects
  - Produced as part of two UK NERC-funded projects:
    - Historic Droughts (2014–2018; £1.5 million)
    - IMPETUS (2014–2018; £1 million)
  - Historic Droughts project involved multiple UK institutions and aimed to understand past droughts to improve future management.
  - IMPETUS aimed to improve drought forecasting by combining meteorological, hydrological, and demand data, including PET as a key input.

- References and acknowledgements
  - Key methodological and calibration references include:
    - Oudin et al. (2005) for the McGuinness-Bordne formulation
    - Perry and Hollis (2005) for UK gridded climatic datasets
    - Robinson et al. CHESS datasets for calibration and evaluation
    - Tanguy et al. (2018) historical gridded PET reconstruction for the UK
  - Acknowledges NERC grant support for Historic Droughts and IMPETUS.