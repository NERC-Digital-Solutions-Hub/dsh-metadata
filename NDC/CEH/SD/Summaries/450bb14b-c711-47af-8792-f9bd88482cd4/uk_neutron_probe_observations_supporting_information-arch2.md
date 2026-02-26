# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

## Overview of the dataset
- Long-term archive of neutron probe soil moisture observations for hundreds of UK locations (UKSMD).
- Covers 1966–2013 with data from 428 locations (tubes) across 45 study areas; data quality controlled and standardized.
- Data types include neutron probe counts (R), volumetric soil moisture (θ), and depth-integrated profile moisture content (PMC).
- Metadata includes tube location (British National Grid and coordinates), site details, vegetation, soil type, geology, and publication references.
- No neutron probe observations for Northern Ireland to date.

## Dataset structure (four files)
- Volumetric_soil_moisture_UKSMD.csv: Time-series of NP count rate R and volumetric soil moisture θ at multiple depths.
- Profile_moisture_content_UKSMD.csv: Time-series of depth-integrated profile moisture content (PMC) to specified depths, provided as PMC1 (mm water stored) and PMC2 (m3 water/m3 soil).
- Tube_metdata_UKSMD.csv: Tube-level metadata (location, dates, depths, vegetation, land-use, soil type, geology, coordinates, start/end dates, depth availability, etc.).
- Site_publications_UKSMD.csv: Publications and reports linked to each area/site with URLs when available.

## Data production methods
- Data recovery from historic sources: The Soil Moisture Databank (SMDB, Gardner 1981) plus additional archived NP data (1966–2013) recovered from tapes and spreadsheets.
- Consolidation: NP counts (R), volumetric moisture (θ), and PMC values were produced to maximize consistency over the full period (1966–2013).
- Coverage: 441 tube locations in 45 study areas (across England, Wales, Scotland); no data for Northern Ireland.

## How the data were derived
- Neutron probe readings (3.2.1): In-situ measurements via NP tubes; readings apply to surrounding soil within a defined radius; repeat measurements possible at the same location.
- Volumetric soil moisture (3.2.2): θ derived from NP readings using calibration equations; field calibration possible; notes on shallow-depth underestimation and site-specific calibration uncertainties.
- Depth-integrated PMC (3.2.3): PMC calculated by integrating θ over depth using layer factors; missing PMC values derived where possible using established methods.

## Dataset format and contents
- Four CSV files (data and metadata) designed for easy import into spreadsheet or code (R, Python, Fortran).
- Metadata includes:
  - Tube_ID, Tube_Name, AREA_ID, AREA_NAME, SITE_ID, SITE_NAME
  - Coordinates: EASTING/NORTHING, LATITUDE/LONGITUDE
  - Dates: TUBE_START_DATE, TUBE_END_DATE
  - Depth and data availability: DEPTH_SPECIFIC, DEPTH_INTEGRATED, MAX_DEPTH
  - Land-use/Land cover and VEGETATION (categorized into six broad types)
  - CALIBRATION_COMMENT and TUBE_COMMENT
- Data files include:
  - DATE_TIME, TUBE_ID, AREA_ID, RW (water count), DEPTH, COUNT, VOLUMETRIC_SOIL_MOISTURE (θ), COMMENT, QUALITY1, QUALITY2
  - PMC1 and PMC2 with corresponding date/time and depth information

## Data availability and geographic coverage
- Data available for 45 geographic areas, 112 sites, and 428 NP tubes (as of the compilation).
- Spatial map (Figure 1) highlights NP tube locations and data availability by area.
- Notable long-duration datasets include Hodnet Heath (HODHE) and Lincolnshire (LINCS); some areas have 10+ years of data.
- Northern Ireland has no NP observations in the UKSMD to date.

## Quality control, uncertainty, and data flags
- Missing data marked as -1; some derived values labelled with a 'c' to indicate calculated during data recovery.
- Quality flags:
  - QUALITY1 (q1): set to 1 when θ values exceed 1.0 or show high uncertainty; indicates suspect absolute moisture values.
  - QUALITY2 (q2): set to 1 for jumps/spikes in time-series that are otherwise consistent with other data.
- Negative θ values removed; in a few areas θ > 1.0 due to peat-rich soils and high rainfall; interpret absolute values with caution.
- NP-derived moisture is reliable for detecting changes, but absolute θ values have higher uncertainty without site-specific calibration.
- Where original θ values were unavailable, θ was estimated using calibration relations; such values are flagged as 'c' and carry greater uncertainty.

## How to use the UKSMD data
- Acknowledgement: credit original studies and references via Site_publications_UKSMD.csv.
- Data forms:
  - For depth-specific moisture: Volumetric_soil_moisture_UKSMD.csv (R, θ by depth)
  - For depth-averaged comparisons: Profile_moisture_content_UKSMD.csv (PMC1 and PMC2)
- Data quality: consider performing analyses with and without suspect data (q1/q2) to assess sensitivity.
- Applications:
  - Hydrological, agricultural, and land-surface model testing and data assimilation.
  - Historical drought analysis and soil moisture dynamics (1966–2013; includes 1976 drought).
  - Cross-validation with remotely-sensed soil moisture products (noting topsoil limitations of NP vs satellite).
  - Contributions to regional and international soil moisture studies alongside ISMN, COSMOS-UK, and related datasets.
  - Historical emissions assessments where soil moisture is a relevant driver (e.g., nitrous oxide emissions).
- Limitations to consider:
  - Top 10 cm soil moisture is less reliable for NP data when compared to satellite/cosmic-ray sensors.
  - Absolute θ values have calibration-related uncertainties; focus on relative changes and temporal trends.
  - Some sites require cautious interpretation due to missing calibration details or data recovery limitations.

## Data usage notes and references
- Data linked to numerous publications; users should consult Site_publications_UKSMD.csv for references and DOIs/URLs.
- The dataset integrates legacy SMDB data with newer recoveries to enable long-term analyses of UK soil moisture variability.
- Acknowledgment of LOCAR and related meteorological data is encouraged where applicable.

## Acknowledgements
- Funded by NERC-CEH Water Programme and FP7 MELODIES project; dataset preparation supported by NERC ASSIST program.
- Thanks to individuals and teams who aided site identification and data recovery.