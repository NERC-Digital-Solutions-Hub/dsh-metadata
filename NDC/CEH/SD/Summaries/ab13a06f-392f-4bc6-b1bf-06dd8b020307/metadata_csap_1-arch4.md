# CSAP_1.1_Peatland_transects.csv

## Overview
- Data on peat depth from more than 250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
- Collected during field campaigns in 2019 and 2020.
- Used, with related CSAP data, to train a predictive model of peat distribution (see Hastie et al. 2022, Nature Geoscience).

## Data collection scope and purpose
- Focused on filling gaps in peat-depth data across lowland Amazonia to support modeling of carbon storage risk from land-use change.
- Some sites include locations without peat depth measurements (NA in Peat_depth_cm), linked to data reported elsewhere in CSAP.

## Methods and instrumentation
- Peat depth measured by coring with a Russian-type or gouge auger.
- Location recorded with a handheld consumer-grade GPS (Garmin).
- Qualitative observations of human impact recorded when present.

## Data structure and content
- Single UTF-8 encoded CSV file with headers:
  - Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes
- Key data notes:
  - NA in Peat_depth_cm indicates no depth data recorded for that site.
  - Date is in text format dd/mm/yyyy.
  - Long/Lat are WGS84 decimal degrees; typical horizontal accuracy better than ~10 m.
  - Peat_depth_cm is the depth to the base of the peat (in cm).
  - Type indicates data collection level at each site (Type 1–4 with differing supplementary data).
- Geographical range:
  - Lat: approximately -0.8 to -5.88
  - Lon: approximately -73.27 to -75.6

## Field design and sampling
- Transects were laid out to cover areas of lowland Amazonia with limited prior data, spanning a variety of vegetation and hydroperiod types.
- Peat depths were sampled at regular intervals along transects; sampling adjusted for logistical constraints.
- For Type 3 sites, peat depth is the mean of five measurements; Type 1 and Type 2 include additional data on depth and other variables; Type 4 records a single peat depth.

## Quality control and data provenance
- Consistency across fieldwork teams maintained, with involvement of local experts.
- Location data sense-checked against Landsat imagery in the field.

## Field methods and data notes
- Instruments: Garmin GPS receivers (e.g., eTrex10); Eijkelkamp peat augers.
- Additional site notes capture vegetation type and signs of Hunting, NTFP harvesting, Fire, Agriculture, and Timber harvesting.

## Related data and usage
- The dataset contributes to a peat thickness map framework used to assess carbon storage risk; aligns with the broader CSAP data collection and the Hastie et al. (2022) study.
- Some sites connect to other CSAP datasets where peat depth data are not available in this file.

## Project funding and contact
- Funded by UKRI-NERC, grant NE/R000751/1.
- Principal Investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk).