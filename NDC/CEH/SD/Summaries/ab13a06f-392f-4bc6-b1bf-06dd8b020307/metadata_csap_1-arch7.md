# CSAP_1.1_Peatland_transects.csv

## Overview
- Dataset of peat depth measurements from >250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
- Collected during field campaigns in 2019 and 2020.
- Used (alongside other CSAP data) to train a predictive model of peat distribution (see Hastie et al. 2022, Nature Geoscience).
- A small number of sites are listed with NA in Peat_depth_cm and relate to data reported elsewhere.

## Data content and structure
- Single UTF-8 encoded CSV with a header row listing variables.
- Variables include: Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes.
- NA values indicate no data recorded for a field.
- Units and formats:
  - Date: dd/mm/yyyy
  - Long/Lat: decimal degrees (WGS84)
  - Elevation_m: metres
  - Peat_depth_cm: centimetres
  - Boolean indicators (Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting): TRUE/FALSE

## Methods and quality assurance
- Peat depth measured by coring with a Russian-type or gouge auger.
- Location recorded with handheld GPS (Garmin eTrex10 or similar).
- Qualitative observations of human impact recorded when present.
- Quality control included consistency checks within the field team (local experts present) and sense-checking locations against Landsat imagery in the field.

## Experimental design and sampling
- Peat depths sampled at regular intervals along transects designed to cover areas of lowland Amazonia where data were previously lacking.
- Transects spanned a range of vegetation types and hydroperiod conditions, chosen with regard to prior remote-sensing analyses and logistical constraints.
- Typically, transects cover diverse sites to capture spatial variability in peat depth and associated conditions.

## Geographical and temporal coverage
- Spatial extent: lat -0.8 to -5.88 degrees; long -73.27 to -75.6 degrees.
- Temporal extent: field campaigns conducted in 2019 and 2020.
- Localities are named (Locality) with unique Site_code identifiers.

## Variables and data types (key fields)
- Type: 1, 2, 3, or 4 (site classification with differing data collection schemes)
- Campaign: field campaign identifier
- Locality: place name near the site
- Site_code: unique site identifier
- Date: date of data collection
- Long / Lat: GPS-derived coordinates
- Elevation_m: elevation in metres
- Peat_depth_cm: peat depth to base of peat (cm)
- Vegetation_type: qualitative vegetation description
- Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting: TRUE/FALSE indicators of disturbances or land-use signals
- Notes: qualitative site notes

## Data provenance and usage
- The dataset supports map-based visualization and spatial analysis of peat depth distribution.
- Closely tied to the CSAP program and data collection efforts; referenced in the training of peat-distribution models (Hastie et al., 2022).
- Data can be integrated with other datasets to enhance GIS-based understanding of peatlands and associated risks.

## Access, references, and contact
- Project funding: UKRI-NERC, grant NE/R000751/1
- Principal investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Related publication for context: Hastie, A. et al. (2022) Nature Geoscience, "Risks to carbon storage from land-use change revealed by peat thickness maps of Peru" (doi provided in abstract)