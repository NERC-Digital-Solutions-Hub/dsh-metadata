# EMEP-WRF global model, version 4.45 – Seasonal mean surface ozone for the UK and USA, 2018

## Overview
- Dataset of daily mean surface ozone (6am–6pm) on a 1° × 1° global grid, focusing on the UK and USA for 2018.
- Seasonal mean ozone calculated for mid-April to mid-July per grid cell.
- Ozone values are reported in parts per billion (ppb) using the WGS 84 coordinate system.

## Model setup and data sources
- Based on the EMEP MSC-W chemical transport model, adapted into the EMEP-WRF framework (version 4.45; Vienna et al., 2016; Simpson et al., 2012).
- Meteorology driven by hourly 3D data from WRF version 4.2.2, itself initialized and nudged every six hours with GFS-FNL reanalysis data.
- Global domain with 1° × 1° horizontal resolution and 21 vertical layers (surface ~40 m to top ~16 km).
- Emissions for the run derived from IIASA GAINS model (v6a) for the year 2015.

## Temporal and geographic scope
- Time period: Year 2018.
- Outputs cover daily surface ozone (6am–6pm) and a seasonal mean for the UK and USA during the mid-April to mid-July window.

## Data content and structure
- Shapefile with gridded data (1° × 1°) and five attributes:
  - FID: Unique grid cell identifier
  - Lon: Longitude of grid cell center (decimal degrees)
  - Lat: Latitude of grid cell center (decimal degrees)
  - NAME: Country (USA or UK)
  - O3_ppb: Daily surface ozone concentration in ppb, and the seasonal mean for 2018 (mid-April to mid-July)
- Seasonal mean O3_ppb values range from 19.3 ppb to 50.9 ppb.

## Quality control and validation
- EMEP model outputs undergo QA/QC before use; validation described in Mills et al. (2018).
- Model performance assessed by comparing modelled and observed ozone from GAW sites during peak daily ozone periods.
- The model generally captures spatial and temporal ozone variations, including seasons with higher concentrations and longer ozone episodes.

## Use and interpretation
- Suitable for assessing spatial patterns and potential exposure of the UK and USA to surface ozone in 2018, and for exploring links to crop impact studies (e.g., ozone effects on wheat production as discussed in Mills et al. 2018).
- Important to note that the dataset is model-derived with 1° resolution; local-scale interpretation should consider resolution and emissions assumptions.
- Data provenance is documented (QA/QC, validation, and underlying modeling assumptions) and linked to the cited literature for context and methodological details.

## References
- Mills, G. et al. (2018). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology, 24, 3560–3574.
- Simpson, D. et al. (2012). The EMEP MSC-W chemical transport model technical description. Atmospheric Chemistry and Physics, 12, 7825–7865.
- Vieno, M. et al. (2016). The sensitivities of emissions reductions for the mitigation of UK PM2.5. Atmospheric Chemistry and Physics, 16, 265–276.