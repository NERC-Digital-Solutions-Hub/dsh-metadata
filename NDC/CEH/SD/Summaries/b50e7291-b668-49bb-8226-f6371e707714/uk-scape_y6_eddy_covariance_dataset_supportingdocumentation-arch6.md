# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

- The UK-SCAPE_Y6_Flux_Dataset provides time series observations of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), along with supporting meteorological and soil physics data from six eddy covariance (EC) flux towers across England and Wales.
- Accompanied by site metadata (UK-SCAPE_Y6_Site_Metadata.csv) and a data dictionary (UK-SCAPE_Data_Dictionary.csv) to describe variables, units, and data structure.
- Designed to enable data exploration and self-serve analyses of ecosystem energy and carbon fluxes.

## Study sites and contents

- Six EC flux towers representing diverse land uses:
  - Three croplands (two on peat, one on mineral soils)
  - One grassland on peat
  - One lowland fen under conservation management
  - One upland raised bog
- Elevation range: -2 m to 565 m above sea level.
- Climate context: mean annual temperature 5–10 °C; mean annual precipitation 534–1815 mm.
- Site metadata file includes: site name, file name, measurement interval, land use, soil type, temperatures, precipitation, location, elevation, exposure, slope, crop years (for croplands), instrument models, measurement heights, and other site characteristics.

## Data collection and instrumentation

- Flux data (H and LE) collected above the canopy with open-path EC systems:
  - Sonic anemometer, LI-7500 IRGA for CO2 and H2O
  - Sampling rate: 20 Hz, logged to CR3000 Micrologger and telemetered
  - Measurement heights (Zm) varied by site; croplands had Zm raised during maize production
- Ancillary meteorological and soil data collected:
  - Air temperature (TA) and relative humidity (RH) at 2.0 m
  - Barometric pressure (PA)
  - Net radiation (NETRAD) and components (SW_IN, SW_OUT, LW_IN, LW_OUT)
  - Soil heat flux (G) at 0.03 m depth
  - Soil volumetric water content (SWC) and soil temperature (TS)
  - Precipitation (P)
  - Water table depth (peatlands)
- Vegetation data: canopy height, LAI (LAI-2000/LAI-2200C), biomass samples for carbon export; destructively sampled and processed in lab

## Data processing and quality control

- Flux calculation: EddyPro software (v7.0.6) to derive 30-minute flux averages (H, LE, NEE) and ancillary variables; includes standard corrections (coordinate rotation, angle-of-attack, high/low-frequency attenuation, density corrections, etc.)
- Quality control (QC):
  - Sensor maintenance with repairs/replacements as needed
  - Calibration of gas analyzers per manufacturer specs
  - Statistical QC: outliers removed via median absolute deviation; stationarity and turbulence tests; turbulence thresholds
  - Footprint analysis: fluxes considered representative if >80% originate within target ecosystem (FFP footprint model)
  - Visual inspection and manual removal of clearly erroneous values
- Data gaps and processing:
  - Gaps in EC data (NEE, LE, H) and ancillary data filled using Marginal Distribution Sampling (Reichstein et al., 2005)
  - Partitioning of NEE into Gross Primary Production (GPP) and Reco using Reichstein et al. and Lasslop et al methods
  - Gap-filling and partitioning performed with REddyProc (R)
  - Ancillary gaps filled where possible using collocated COSMOS-UK data

## Data structure and accessibility

- Time series provided as separate CSV files for each of the six sites
- Each file follows the structure described in UK-SCAPE_Data_Dictionary.csv
- Time series cover the intervals defined in UK-SCAPE_Y6_Site_Metadata.csv
- Missing records indicated by -9999
- TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software (e.g., Excel)

## Nature of recorded values and documentation

- Flux, micrometeorological, and soil physics variables and units are detailed in UK-SCAPE_Data_Dictionary.csv
- Vegetation data are non-continuous time series with metadata described in the same dictionary

## Data quality, usage notes, and limitations

- Comprehensive QC and continuity checks underpin data reliability
- Data gaps exist due to instrument downtime or QC pruning; gap-filled data are provided with standard methods
- Site-specific details (e.g., measurement heights, vegetation status) influence interpretation and require careful consideration when cross-site comparisons are made

## Acknowledgments and funding

- Data collected with the cooperation of landowners and organizations (e.g., Natural Resources Wales, RSPB, Natural England, Great Fen Project)
- Funded by the NERC UK-SCAPE programme (delivering National Capability)
- Grange Farm flux tower funded by a donor