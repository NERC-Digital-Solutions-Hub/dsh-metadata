# CSAP_1.1_Peatland_transects.csv

## Overview
- Dataset of peat depth measurements from more than 250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
- Collected during field campaigns in 2019 and 2020 and used to train a predictive model of peat distribution (see Hastie et al., 2022, Nature Geoscience).
- Some sites have location data but no peat depth measurements (NA in Peat_depth_cm); these sites relate to data reported elsewhere in CSAP.

## Data collection and methods
- Peat depth measured by coring with a Russian-type or gouge auger.
- Location recorded with a handheld consumer-grade GPS.
- Qualitative observations of human impact recorded when present.
- Consistency ensured by field teams including local experts; location data sense-checked against Landsat imagery.

## Data structure
- A single UTF-8 encoded CSV with these columns:
  - Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes
- NA indicates no data recorded.

## Experimental design and sampling
- Peat depths sampled at regular intervals along transects designed to cover areas with previously lacking data.
- Transects spanned a variety of vegetation and hydroperiod types, considering logistical constraints.

## Fieldwork and instrumentation
- GPS: Garmin eTrex10 or similar.
- Augers: Eijkelkamp brand.
- Calibration steps: Not applicable.
- Analytical methods: Not applicable.

## Data interpretation and site-level details
- Type categories:
  - Type 1: Broad data on litter production/decay over two years; automated dipwells installed; cores for palaeoenvironmental analysis.
  - Type 2: Automated dipwells installed.
  - Type 3: Peat depth recorded as the mean of five measurements; additional data on vegetation and human disturbance.
  - Type 4: Single peat depth measurement.
- Date format: dd/mm/yyyy.
- Location details: Locality (village name); Site_code (unique site identifier); Long/Lat (WGS84, typically better than 10 m).
- Elevation_m: Elevation in metres.
- Notes: Qualitative site notes.

## Geographic coverage
- Lat: approximately -0.8 to -5.88 degrees.
- Long: approximately -73.27 to -75.6 degrees.

## Funding and contact
- Funded by UKRI-NERC, grant NE/R000751/1.
- Principal Investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk).