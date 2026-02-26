# CSAP_1.1_Peatland_transects.csv

## Summary
- Dataset of peat depth measurements from over 250 locations in the Pastaza-Marañón Basin, Amazonian Peru, collected in 2019–2020.
- Data contributed to a predictive model of peat distribution (see Hastie et al. 2022, Nature Geoscience).
- Some sites are reported without peat depth measurements (NA) and relate to data reported elsewhere in CSAP data collections.
- Provided metadata describes collection methods, data structure, quality control, and project provenance.

## Data content and purpose
- Purpose: support understanding of peat thickness and distribution to assess carbon storage and land-use risks; facilitate discovery and reuse by others.
- Related work: used to train peat-distribution models; contributes to broader CSAP data collections.

## Collection and methods
- Peat depth measurement: coring using Russian-type or gouge auger.
- Site location: handheld consumer-grade GPS.
- Qualitative site observations: notes on human impact when observed.

## Quality control
- Consistency checks across fieldwork teams, with local experts contributing.
- Location data sense-checked against Landsat imagery in the field.

## Data structure and variables
- File format: a single UTF-8 encoded comma-separated-values file.
- Key fields (first row): Type, Campaign, Locality, Site_code, Date, Long, Lat, Elevation_m, Peat_depth_cm, Vegetation_type, Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting, Notes.
- Type: categorical code (1–4) describing data collection type with distinct datasets:
  - Type 1: broad data on litter production/decay; automated dipwells; cores for palaeoanalysis.
  - Type 2: automated dipwells installed.
  - Type 3: peat depth as mean of five measurements; additional vegetation and disturbance data.
  - Type 4: single peat depth measurement.
- Location and time: Locality (nearest village), Site_code (unique site identifier), Date (dd/mm/yyyy), Long/Lat (WGS84; typically precise <10 m), Elevation_m.
- Peat_depth_cm: depth to base of peat (cm); NA indicates missing measurement.
- Vegetation_type: short qualitative descriptor.
- Human-impact indicators (TRUE/FALSE): Hunting, NTFP_harvesting, Fire, Agriculture, Timber_harvesting.
- Notes: any qualitative observations.
- Geographical scope: latitude roughly -0.8 to -5.88 degrees; longitude roughly -73.27 to -75.6 degrees.

## Experimental design and data collection regime
- Transects sampled across lowland Amazonia to cover areas previously data-sparse, chosen with logistical constraints in mind.
- Transects span diverse vegetation and hydroperiod types based on prior remote sensing analysis.

## Instruments and calibration
- Field instruments: Garmin eTrex10 (GPS) and Eijkelkamp augers.
- Calibration: Not applicable for this dataset.

## Data provenance and access
- Location context: Pastaza-Marañón Basin, Peru.
- Project/funding: Funded by UKRI-NERC (grant NE/R000751/1); Principal Investigator Dr Ian Lawson.
- Contact: itil2@st-andrews.ac.uk.
- Related reference for model use: Hastie, A. et al. 2022 (Nature Geoscience) on peat thickness maps of Peru.

## Usage considerations and limitations
- Some sites include data from other CSAP reports or lack peat depth measurements (NA) but remain linked to broader CSAP data collections.
- Data quality relies on consistent field methods and cross-checking with satellite imagery; some data are missing (NA) for peat depth at certain sites.
- Scope is regional (Pastaza-M marañón Basin) and time-bounded to 2019–2020 field campaigns.

## Governance, stewardship implications
- Metadata alignment: ensure consistent naming, units, and code meanings (e.g., Type, boolean indicators) across CSAP datasets.
- Data integrity: maintain original field measurements and clearly document missing values (NA) and data type semantics.
- Interoperability: consider standardizing fields to facilitate integration with other peatland and carbon datasets (e.g., consistent coordinate reference system, date formats, and booleans).
- Data updating: establish a process for incorporating additional sites or updated measurements while preserving provenance (campaign, site_code, date).
- Accessibility and sharing: prepare data for upload to relevant portals in UTF-8 CSV format and link to related datasets; note any licensing or use restrictions from funding or partners.