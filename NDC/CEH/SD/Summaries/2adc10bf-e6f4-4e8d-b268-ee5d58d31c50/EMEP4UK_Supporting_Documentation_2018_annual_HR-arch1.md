# High resolution European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

## Overview
- Provides the annual total surface resistance-based atmospheric deposition for the UK in 2018.
- Generated with EMEP4UK model rv4.36 (ACTM) and WRF model v4.1.1; UK results are extracted from a domain covering the EU at 27 × 27 km2 with a nested UK domain at 1 × 1 km2.

## Modelling framework and domain
- Atmospheric chemistry transport modelling chain:
  - EMEP MSC-W based model rv4.36 for deposition and concentrations.
  - 3D meteorology from WRF v4.1.1 with Newtonian nudging of NCEP/NCAR GFS reanalysis data (1° × 1° every 6 hours).
- Domain and resolution:
  - EU-wide grid at 27 × 27 km2 with nested UK domain at 1 × 1 km2; only UK model outputs are included.
- Emissions inputs:
  - UK emissions (NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOCs) based on the 2019 National Atmospheric Emission Inventory (NAEI) and rescaled to 2018 UK totals.
  - Non-UK emissions from CEIP at 0.1° × 0.1°; UK total used for 2018.

## Output data and contents
- Data format: NetCDF; annual totals for 2018.
- Measurements and variables (selected examples):
  - Area grid: area_Grid_km2 (km2).
  - Dry deposition components (example variants):
    - DDEP_SOX_m2Grid, DDEP_SOX_m2Conif, DDEP_SOX_m2Seminat, DDEP_SOX_m2Water_D, DDEP_SOX_m2Decid, DDEP_SOX_m2Crops (oxidised sulphur, various land covers).
    - DDEP_OXN_m2Grid, DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops (oxidised nitrogen, various land covers).
    - DDEP_RDN_m2Grid, DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops (reduced nitrogen, various land covers).
- Grid and coordinates:
  - Time dimension: time (unlimited; currently 1 entry for 2018).
  - Spatial grid: i = 765, j = 1254.
  - lon(j, i) and lat(j, i) coordinates provided.
- Units and projections:
  - Grid area: km2.
  - Deposition fluxes: mgS/m2 for sulphur species; mgN/m2 for nitrogen species.
  - Projection: polar stereographic; proj4 string provided for integration (includes k0 = 0.9330127019, lat_0 = 90, lon_0 = 0).
- Data access note:
  - NetCDF libraries required; compatible with R, Python, and FORTRAN.

## Data structure details
- Example 2018 output variable: DDEP_SOX_m2Grid.
- File structure includes:
  - Dimensions: time, i, j.
  - Variables: time, i, j, lon(j, i), lon/lat grids, and deposition fields by species and land cover.

## Quality assurance and limitations
- QA/QC performed for 2018:
  - Emissions validated against official inventories.
  - Model outputs evaluated visually (time series) and statistically with standard metrics.
- Documentation and QA reports available on request.
- Peer-reviewed models; used widely in the scientific community.
- Use of content is at the user’s risk; no warranty of error-free or fitness for a given purpose.

## Guidance for use
- Suitable for studies of atmospheric deposition impacts in the UK, including comparisons with observations or coupling with ecological/risk assessments.
- When integrating with other datasets, consider scale and land-cover mappings (since deposition is land-cover-specific in several variables).
- Ensure NetCDF compatibility and correct projection settings in analysis workflows.
- QA reports are available on request to support data credibility.

## References and provenance
- Primary model and technical references spanning EMEP MSC-W, WRF, and emissions inventories (NAEI 2022; CEIP).
- Related methodological and evaluation studies cited in the provided bibliography.