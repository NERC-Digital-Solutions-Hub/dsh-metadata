# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

## Overview
- UK-SCAPE Eddy Covariance dataset provides time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), alongside supporting meteorological, soil physics, and vegetation data.
- Global structure includes site metadata, flux and ancillary data (one file per site), vegetation data, and a data dictionary.
- Data cover ten eddy covariance (EC) flux tower sites across England and Wales, with measurements spanning multiple years (2018–2023).

## Dataset contents
- Site metadata file: UK-SCAPE_Site_Metadata.csv
- Flux and ancillary data: one per site (file format <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv)
- Vegetation data files: UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv
- Data dictionary: UK-SCAPE_Data_Dictionary.csv
- Missing data indicated by -9999; inapplicable metadata fields marked NA.

## Study sites and sampling regime
- Site types include:
  - Two croplands on drained lowland peat
  - Four managed grasslands (three on drained lowland peat, one on mineral soil)
  - One cropland converted during measurement from managed grassland (mineral soil)
  - Two lowland fens under conservation management
  - One relatively intact upland blanket bog
- Elevation range: from 2 m below sea level to 565 m above
- Mean annual temperature: 5–10 °C; annual precipitation: 534–1815 mm
- Flux measurement periods defined by START_DATE and END_DATE in metadata; vegetation data collected where possible
- Data structure: time series per site; vegetation data as non-continuous series when available

## Data acquisition and instrumentation
- Flux data:
  - Open-path eddy covariance (EC) systems measuring turbulent fluxes of H and LE above the canopy
  - Instruments: sonic anemometer, LI-7500 IRGA; sampling at 20 Hz; data logged on CR3000 Micrologger and telemetered
  - Measurement heights varied by site; Zm fixed at most sites (raised to ~5 m during maize in croplands)
  - Spatial arrangement of sensors with specific horizontal offsets
- Ancillary data:
  - Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure from IRGA
  - Net radiation (NETRAD) and components (SW_IN, SW_OUT, LW_IN, LW_OUT)
  - Soil heat flux (G) at 0.03 m depth; soil water content (SWC) and soil temperature (TS) at various depths
  - Precipitation (P); water table depth (peatlands)
  - Data scanned at 0.1 Hz; logged as 15- or 30-minute means
- Vegetation data:
  - Biomass file and canopy height/LAI file
  - Biomass: destructive sampling when possible; moisture content and dry biomass; carbon export (C_EXPORT)
  - Canopy height and LAI measured with field instruments (LAI-2000/LAI-2200)

## Data processing, quality control, gap filling
- Flux processing:
  - EddyPro software (v7.0.6) used to compute fluxes; 30-minute block averages
  - QC procedures include outlier removal, stationarity, turbulence tests, and corrections for instrument tilt and density effects
  - Footprint analysis (Kljun et al. 2015) ensures representativeness; fluxes considered representative if >80% originates within target ecosystem
- Gap filling and partitioning:
  - Gaps in fluxes and ancillary/derived data filled using Marginal Distribution Sampling (Reichstein et al. 2005)
  - NEE partitioned into GPP and RECO using methods from Reichstein et al. (2005) and Lasslop et al. (2010)
  - Gap-filling/partitioning performed with REddyProc (R)
  - When possible, ancillary data gap-filled with COSMOS-UK site data
- Data quality checks:
  - Visual inspection of all flux and ancillary data
  - Manual removal of clearly erroneous values after QC

## Data structure and metadata
- Time series are provided as separate CSV files per site; vegetation data as non-continuous time series
- File naming convention for flux data: <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv
- Metadata for sites included in UK-SCAPE_Site_Metadata.csv
- Data dictionary (UK-SCAPE_Data_Dictionary.csv) describes data types, column names, descriptions, sensor depths, and units

## Data access and management
- Data acquisition supported by COSMOS-UK and UK-NERC programs; funding from NERC (NE/R016429/1) and Defra SP1219
- Acknowledgments extend to landowners and site managers for access and permissions
- Author contributions span conceptualization, data collection, processing, management, and publishing
- References to standard processing, QC, and footprint methodologies cited in accompanying literature

## Implications for Data Leaders
- Demonstrates the value of a well-structured, multi-site data asset with consistent naming, metadata, and a central data dictionary to facilitate discoverability and reuse
- Highlights the importance of standardized, auditable processing pipelines (EddyPro, REddyProc) for cross-site comparability
- Emphasizes rigorous QA/QC, footprint assessment, and transparent gap-filling/flux-partitioning to ensure data reliability and usability
- Shows benefits of cross-network collaboration (COSMOS-UK) for data gap-filling and enrichment, strengthening the broader data ecosystem
- Underlines need for clear documentation of instruments, measurement heights, and calibration practices to support data provenance and reproducibility