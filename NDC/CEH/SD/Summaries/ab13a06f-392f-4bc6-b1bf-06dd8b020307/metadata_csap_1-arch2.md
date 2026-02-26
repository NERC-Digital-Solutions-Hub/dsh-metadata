# CSAP_1.1_Peatland_transects.csv

## Overview
- Dataset documenting peat depth from more than 250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
- Collected during field campaigns in 2019 and 2020.
- Used, alongside other projects’ data, to train a predictive model of peat distribution (Hastie et al. 2022, Nature Geoscience).
- Some sites have missing peat depth measurements (NA), but are related to data reported elsewhere in CSAP.

## Data Collection and Methods
- Peat depth measured by coring with a Russian-type or gouge auger.
- Location recorded with a handheld GPS (consumer-grade).
- Qualitative observations of human impacts noted when present.
- Location data sense-checked against Landsat imagery in the field.
- Calibration and analytical steps are not applicable for this dataset.

## Data Structure and Variables
- Single UTF-8 encoded CSV with header row of variables:
  - Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes
- NA indicates missing data.
- Key variables:
  - Type: 1–4, indicating differing data collection regimes (e.g., litter data, dipwells, peat depth by site, etc.).
  - Peat_depth_cm: depth to base of peat.
  - Spatial: Long, Lat (WGS84), Elevation_m.
  - Qualitative context: Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes.

## Experimental Design
- Regular transects designed to cover areas of lowland Amazonia where data were previously lacking.
- Transects span diverse vegetation and hydroperiod types (informed by prior remote-sensing analysis).
- Logistics constrained sampling scope.

## Data Quality and Limitations
- Quality control ensured by cross-team consistency, including involvement of local experts.
- Location validation against satellite imagery in the field.
- Some sites include only qualitative notes or may lack peat depth measurements (NA in Peat_depth_cm).

## Geographical and Temporal Scope
- Location range: lat -0.8 to -5.88 degrees; long -73.27 to -75.6 degrees.
- Campaign period: 2019–2020.
- Region: Pastaza-Marañón Basin, Amazonian Peru.

## Data Use, Provenance, and Linking Context
- Contributes to peat-thickness mapping and carbon-storage risk assessments when combined with additional CSAP datasets (as in related Nature Geoscience work).
- Some sites link to data reported elsewhere in CSAP, providing broader context for peat-related analyses.

## Funding and Contact
- Funded by UKRI-NERC, grant NE/R000751/1.
- Principal Investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk).