# Supporting Information for Gridded estimates of daily and monthly areal rainfall for the United Kingdom (1890-2015) [CEH-GEAR]

- Purpose and scope
  - CEH-GEAR provides 1-km gridded estimates of daily and monthly rainfall for Great Britain (GB) and Northern Ireland (NI) plus ~3000 km2 of catchment in the Republic of Ireland (ROI), covering 1890 onward with annual updates as new raingauge data become available.
  - Rainfall estimates are derived from the Met Office national precipitation database; daily and monthly totals are produced with a natural neighbour interpolation approach and normalisation by SAAR (Standard Average Anomaly Rainfall).
  - Daily estimates refer to rainfall accumulated over 24 hours from 09:00 on day t to 09:00 GTM on day t+1.
  - Dataset development adheres to BS7843-4:2012 guidance; detailed methodology described in Keller et al. (2014).

- Data sources
  - Met Office MIDAS: definitive national dataset of daily and monthly rainfall, provided to CEH under license; CEH maintains a synchronized copy in its Oracle database with a QC procedure to discard unrealistic extremes.
  - Met Office SAAR grids (1961-1990) for GB (Spackman, 1993) and for NI (Walsh, 2012).
  - Met Office and Met Éireann historical observations feeding the gridding process.

- Method for deriving daily and monthly grids
  - Interpolation: natural neighbour interpolation with normalisation by SAAR.
  - Daily grids (two-stage process):
    - Stage 1: provisional daily grids using all available daily raingauges.
    - Stage 2: adjust provisional daily grids with a monthly correction factor so that the sum of daily grids matches the derived monthly grid.
  - Monthly grids:
    - Generated from the monthly raingauge network; for months with a complete daily dataset, daily values are summed to obtain the monthly total.
    - If a daily gauge shares coordinates with a monthly gauge, the monthly gauge is used in interpolation to reduce error.
  - Units: rainfall depth in millimetres (mm).
  - Coverage: separate storage for GB/NI with distinct monthly and daily grid folders.

- Minimum distance grids and data gaps
  - A 100 km minimum distance threshold is applied; grids are not produced beyond this threshold to preserve representativeness.
  - Early versions (pre-1961) have more gaps due to sparser networks, notably in Scotland, Wales, and SW England.
  - Ancillary information provided for modellers:
    - Year of the first missing data for each grid point.
    - Year of the last missing data for each grid point.
    - Total number of days with missing data for each grid point for the entire period.
  - These three ancillary grids are produced for both monthly and daily data and are updated annually.

- Quality control (QC)
  - A four-step QC is applied to identify and reject unrealistically high rainfall values using a 200-year return-period reference rainfall model (FHB/Stewart et al. framework).
  - Steps:
    - (1) Flag days/gauges where reference rainfall is exceeded.
    - (2) Cross-check remaining high values against major UK rainfall events database.
    - (3) Use daily rainfall maps (post-1961 GB maps) to visually assess whether the event is genuine.
    - (4) For remaining cases, compare time series with the 10 nearest gauges (extended to 7 if needed) using Time-Series Plotter; identify issues such as multiday accumulations or reporting gaps.
  - Common issues identified and addressed:
    - Multiday accumulations and incorrect data flags leading to false highs.
    - Rejection of multiday accumulation cases and inconsistent daily records.
    - Exclusion of data with severe inconsistencies from the rainfall database used to generate grids.

- Data format and storage
  - Data stored in NetCDF4 format following CEH gridded dataset conventions.
  - Structure: yearly files; GB and NI datasets stored in separate folders; daily and monthly grids stored separately.
  - Core variables: rainfall amount (mm) and minimum distance (distance to the closest gauge used for estimation).
  - Ancillary NetCDF4 files:
    - Yearly missing data records for spatial and temporal extent.
    - Three ancillary grids (monthly and daily) detailing first missing year, last missing year, and total days missing per grid point.

- Governance, provenance, and reuse
  - Data are derived from licensed Met Office data and are kept in sync with MIDAS; CEH copies maintained to ensure reproducibility.
  - Methodology and QC procedures are documented to support data integrity, transparency, and potential audit.
  - Dataset designed for hydrological and modelling use; clear documentation of gaps and representativeness (e.g., 100 km threshold) aids appropriate reuse and interpretation.
  - References and methodological foundations provided to support reproducibility and validation (e.g., Collier et al., Keller et al., Spackman, Stewart et al., Svensson et al., Walsh).