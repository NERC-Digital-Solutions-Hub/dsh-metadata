# CSAP_1.1_Peatland_transects.csv

- Purpose and scope
  - Dataset of peat depth from over 250 locations in the Pastaza-Marañón Basin, Amazonian Peru.
  - Collected in field campaigns during 2019 and 2020.
  - Used, together with other project data, to train a predictive model of peat distribution (Hastie et al. 2022; Nature Geoscience).

- Data coverage and content
  - Locations include sites with peat depth measurements and a small number of sites with NA in Peat_depth_cm.
  - Geographic range: lat approximately -0.8 to -5.88; lon approximately -73.27 to -75.6.
  - Data structure: a single UTF-8 encoded CSV with fields for Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes.

- Data collection methods
  - Peat depth measured by coring with a Russian-type or gouge auger.
  - Location recorded with handheld GPS (Garmin eTrex10 or similar).
  - Qualitative observations of human impact recorded where present.

- Quality control and provenance
  - Consistency checks across field team members, including local experts.
  - Location data sense-checked against Landsat imagery in the field.

- Data structure and variable details
  - Type: 1–4, indicating different data collection schemes (e.g., Type 1 includes broad data on litter production/decay and palaeo data; Type 2 involves automated dipwells; Type 3 uses mean of five peat depth measurements plus additional data; Type 4 is a single peat depth measurement).
  - Campaign: field campaign during which data were collected.
  - Locality: village-nearest locality name.
  - Site_code: unique site identifier.
  - Date: format dd/mm/yyyy.
  - Long/Lat: decimal degrees (WGS84); typical horizontal accuracy better than ~10 m.
  - Elevation_m: elevation in metres.
  - Peat_depth_cm: depth to base of peat (in centimetres); NA if not recorded.
  - Vegetation_type: short qualitative vegetation description.
  - Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting: TRUE/FALSE indicators of human impact.
  - Notes: qualitative notes about the site.

- Experimental design and sampling
  - Peat depths sampled at regular intervals along transects designed to cover under-sampled areas in lowland Amazonia.
  - Transects span a variety of vegetation and hydroperiod types, guided by prior remote-sensing analyses.
  - Aimed to balance logistical constraints with broad geographic and ecological coverage.

- Instruments and calibration
  - Field instruments: Garmin GPS receivers; Eijkelkamp peat/soil augers.
  - Calibration steps: not applicable.

- Data usage, applications, and potential
  - Supports analyses of peat distribution and carbon storage risks in relation to land-use change.
  - Enables data-driven mapping and validation of peat thickness models.
  - Provides a basis for data products and dashboards to facilitate self-serve exploration by researchers and policymakers.

- Access, provenance, and funding
  - Funded by UKRI-NERC, grant NE/R000751/1; Principal Investigator: Dr Ian Lawson.
  - Data provenance includes field campaigns in 2019–2020 and linkage to broader CSAP data collections.