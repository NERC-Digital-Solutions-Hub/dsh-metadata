# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

## Overview of dataset
- UK-SCAPE Eddy Covariance dataset provides time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), with supporting meteorological, soil physics, and vegetation data.
- Data components: site metadata, flux and ancillary data (one file per site), vegetation data (biomass; canopy height and LAI), and a dictionary of data variables.
- Ten eddy covariance (EC) flux tower sites across England and Wales, spanning diverse land uses and ecosystems.
- Time period: 2018–2023.

## Study sites and scope
- Site types include:
  - Two croplands on drained lowland peat
  - Four managed grasslands (three on drained lowland peat, one on mineral soil)
  - One cropland converted from managed grassland (on mineral soil)
  - Two lowland fens under conservation management
  - One relatively intact upland blanket bog
- Elevation range: from 2 meters below sea level to 565 meters above sea level.
- Climate range: mean annual temperature 5–10 °C; mean annual precipitation 534–1815 mm.
- Site metadata file: UK-SCAPE_Site_Metadata.csv summarizes characteristics (land use, soil type, measurement heights, instrumentation, dates, etc.).

## Data structure and file organization
- Time-series files: one per site with flux and ancillary data.
- File naming convention for flux data: <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv.
- Vegetation data files (when available): UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv.
- Data dictionary: UK-SCAPE_Data_Dictionary.csv describes variables, data types, units, and sensor depths.
- Data gaps: missing records marked as -9999; inapplicable metadata as NA.

## Measurements and instrumentation
- Flux measurements:
  - Open-path eddy covariance systems measuring turbulent fluxes of sensible heat (H) and latent heat (LE) above canopy.
  - Instruments: sonic anemometer, LI-7500 IRGA; sampling at 20 Hz.
  - Data logged and transmitted to a secure server; measurement heights (Zm) vary by site.
- Ancillary measurements:
  - Air temperature (TA) and relative humidity (RH) at 2.0 m height.
  - Barometric pressure (PA) from IRGA internal barometer.
  - Net radiation (NETRAD) and components (SW_IN, SW_OUT, LW_IN, LW_OUT) via four-component radiometers.
  - Soil heat flux (G) at 0.03 m depth using flux plates.
  - Volumetric soil water content (SWC) and soil temperature (TS) at various depths.
  - Precipitation (P) via tipping bucket or digital weighing rain gauge.
  - Water table depth (WATER_TABLE_DEPTH) for peatlands where possible.
- Vegetation measurements:
  - Biomass (destructive sampling where possible) and canopy height/LAI.
  - Dry biomass used to estimate carbon export (C_EXPORT); crop yields and dates from farm records when available.

## Data processing and quality control
- Flux calculation:
  - Turbulent fluxes computed with EddyPro software (v7.0.6) using 30-minute averaging.
  - QC steps include: 20 Hz data quality checks, angle-of-attack corrections, rotation to local terrain, corrections for spectral attenuation, humidity-density effects, and density corrections for LE.
  - EddyPro also derives wind speed and direction at measurement height.
- Quality control (QC) and representativeness:
  - Outliers removed using median absolute deviation; stationarity and turbulence tests applied (Mauder & Foken 2006).
  - Periods of low turbulence filtered using USTAR thresholds.
  - Flux footprint assessed with Kljun et al. 2015 footprint model (FFP); fluxes considered representative if >80% originate within target ecosystem.
  - Visual QC: all flux and ancillary data plotted; clearly erroneous values removed.
- Gap filling and flux partitioning:
  - Gaps in EC fluxes and ancillary/derived data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
  - Net ecosystem exchange (NEE) partitioned into gross primary production (GPP) and ecosystem respiration (RECO) using nighttime/daytime methods (Reichstein et al., 2005; Lasslop et al., 2010).
  - Gap-filling and partitioning performed with REddyProc (R package).
  - Where possible, ancillary data gap-filled using co-located COSMOS-UK sites.
- Data structure details:
  - Time-series data provided as separate CSVs per site; vegetation data provided as non-continuous time series when available.
  - Missing data indicated by -9999; site metadata NA where not applicable.

## Data accessibility and documentation
- Comprehensive documentation included:
  - UK-SCAPE_Site_Metadata.csv (site-level metadata)
  - UK-SCAPE_Data_Dictionary.csv (variable descriptions and units)
  - UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv (vegetation data)
- Data management and publication handled by UK Centre for Ecology & Hydrology staff; acknowledgments to funding bodies and site managers.
- References provided for data processing methods and quality control standards.

## Reuse and collaboration considerations for environmental monitoring
- Standardized data products enable cross-site comparisons and long-term monitoring assessments.
- Rigorous QC, gap-filling, and flux partitioning support robust estimates of GPP and RECO across diverse ecosystems.
- Metadata completeness and clear data dictionaries facilitate data discovery and reuse by analysts.
- Dataset interoperability with COSMOS-UK and other national programs enhances value beyond single-use applications.

## Key takeaways for monitoring aims
- Provides high-quality, standardized observations of land–atmosphere exchanges (H, LE, NEE) across ten sites in England and Wales over five years.
- Combines flux data with extensive ancillary measurements and vegetation data to support ecosystem energy, water, and carbon balance analyses.
- Employs established processing, QC, footprint assessment, and gap-filling methodologies to ensure data reliability and comparability.
- Emphasizes data accessibility and interoperability, with thorough metadata and documentation to enable reuse for policy performance monitoring and environmental health evaluations.