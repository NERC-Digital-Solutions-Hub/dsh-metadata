# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

## Overview
- A dataset (UK-SCAPE_Y6_Flux_Dataset) of time series for land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil physics data, collected from six eddy covariance (EC) flux towers across England and Wales during 2023–2024.
- Sites encompass diverse ecosystems including croplands (peat and mineral soils), grassland on peat, lowland fen under conservation management, and an intact upland raised bog; elevation ranges from -2 to 565 m, with mean annual temperatures about 5–10°C and annual precipitation between 534 and 1815 mm.

## Study sites
- Six flux monitoring sites described in UK-SCAPE_Y6_Site_Metadata.csv, covering land uses such as:
  - Croplands (two on peat soils, one on mineral soil)
  - Grassland on peat
  - Lowland fen under conservation management
  - Upland raised bog
- Sites span a wide elevational gradient and have varying measurement heights (Zm) and instrumentation details summarized in the metadata file.

## Data collected
- Flux data
  - Turbulent flux densities of sensible heat (H) and latent heat (LE) measured above the canopy using open-path eddy covariance systems (sonic anemometer, LI-7500 IRGA) at ~20 Hz, logged to a CR3000 logger and telemetered.
  - Measurements logged as 30-minute flux averages; measurement heights vary by site.
- Ancillary data
  - Air temperature (TA), relative humidity (RH) at 2.0 m; barometric pressure (PA) from IRGA; net radiation (NETRAD) and its components (SW_IN/OUT, LW_IN/OUT); soil heat flux (G); soil water content (SWC) and soil temperature (TS); precipitation (P).
  - Peatlands: water table depth (WATER_TABLE_DEPTH) where possible.
  - Vegetation measurements: canopy height, LAI, biomass; destructive sampling for carbon export.
- Observation cadence
  - Micrometeorological and soil observations at 0.1 Hz, summarized as 30-minute means; precipitation totaled for the period.

## Data processing
- Flux calculations
  - EddyPro software (v7.0.6) used to compute H and LE from raw EC data, with corrections for angle of attack, tilt, coordinate rotation, spectral attenuation, density effects, and other instrumental biases.
- Quality control
  - Sensor repairs/replacements as needed; calibrations following manufacturer specs.
  - QC includes removal of statistical outliers (median absolute deviation), stationarity and turbulent condition tests, and friction velocity (USTAR) thresholds.
  - Footprint analysis (FFP) to ensure flux representativeness; fluxes retained if >80% originated within the target ecosystem.
  - Visual review of all flux and ancillary data to remove clearly erroneous values.
  
## Data gap-filling and flux partitioning
- Gap-filling
  - Gaps in EC fluxes (NEE, LE, H) and ancillary data filled using the Marginal Distribution Sampling approach.
- Flux partitioning
  - Net ecosystem exchange (NEE) partitioned into gross primary production (GPP) and ecosystem respiration (Reco) using day/night methods from Reichstein et al. (2005) and Lasslop et al. (2010).
  - Implemented with the REddyProc package in R; where possible, ancillary data gaps filled using collocated COSMOS-UK sites.

## Data structure
- Time series files
  - Data are provided as separate CSV files for each of the six EC sites.
  - Each file follows the structure described in UK-SCAPE_Data_Dictionary.csv and covers the START_DATE to END_DATE from UK-SCAPE_Y6_Site_Metadata.csv.
  - Missing records are encoded as -9999; TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software (e.g., Excel).
- Vegetation data
  - Non-continuous time series in CSV format when available, with variables described in UK-SCAPE_Data_Dictionary.csv.

## Nature and units of recorded values
- Flux, micrometeorological, and soil physics variables and their units are detailed in the UK-SCAPE_Data_Dictionary.csv.

## Acknowledgments
- Thanks to landowners and organisations enabling flux tower installations and access (Natural Resources Wales, RSPB, Natural England, Great Fen Project, G's Cambs. Growers Ltd., T. C Darby & Sons Ltd.).
- Data collection funded by the NERC UK-SCAPE programme delivering National Capability; specific thanks for capital support for Grange Farm flux tower.

## References
- Key methodological references underpinning data processing and gap-filling, including Reichstein et al. (2005, 2016), Lasslop et al. (2010), Mauder et al. (2006, 2013), Papale et al. (2006), Moncrieff et al. (1997, 2004), and related supporting literature.