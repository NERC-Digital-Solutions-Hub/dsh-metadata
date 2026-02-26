# CSAP_1.1_Peatland_transects.csv

## Overview
- Dataset of peat depth measurements from >250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
- Collected during field campaigns in 2019 and 2020.
- Used, with related CSAP data, to train a predictive peat distribution model (Hastie et al. 2022, Nature Geoscience).

## Data scope and purpose
- Primary variable: Peat_depth_cm (depth to base of peat).
- Additional site metadata to support analysis: Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Vegetation_type.
- Auxiliary disturbance indicators: Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting.
- Notes field for qualitative observations.
- Some sites have missing peat depth (NA in Peat_depth_cm).

## Methods and data collection
- Peat depth measured by coring with Russian-type or gouge augers.
- Location recorded with handheld GPS (Garmin).
- Qualitative notes on human impact captured when observed.
- Location data cross-checked against Landsat imagery in the field.

## Data structure
- Single UTF-8 encoded CSV.
- Columns: Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes.
- Date format: dd/mm/yyyy.
- Long/Lat in decimal degrees (WGS84); elevation in metres.

## Experimental design and sampling
- Peat depths sampled at regular intervals along transects.
- Transects chosen to cover areas of lowland Amazonia with previously limited data.
- Sampling spanned varied vegetation and hydroperiod types, guided by prior remote-sensing analyses and logistical constraints.

## Fieldwork and instrumentation
- GPS: Garmin eTrex10 or equivalent.
- Augers: Eijkelkamp-manufactured.

## Data quality and validation
- Quality control ensured by consistent field team participation, including local experts.
- Location validity checked against satellite imagery (LandSat).

## Data attributes and interpretation
- Type indicates data collection regime:
  - Type 1: extensive data on litter production/decay; automated dipwells and palaeo samples (over two years).
  - Type 2: automated dipwells installed.
  - Type 3: peat depth as mean of five measurements plus vegetation and disturbance data.
  - Type 4: single peat depth measurement.
- Peat_depth_cm is the primary quantitative measure; other fields provide contextual information for modeling.

## Geographic scope
- Latitude: approximately -0.8 to -5.88 degrees.
- Longitude: approximately -73.27 to -75.6 degrees.

## Related work and funding
- Related model and findings described in Hastie, A. et al. (2022) Nature Geoscience.
- Funded by UKRI-NERC, grant NE/R000751/1; Principal Investigator: Dr Ian Lawson.