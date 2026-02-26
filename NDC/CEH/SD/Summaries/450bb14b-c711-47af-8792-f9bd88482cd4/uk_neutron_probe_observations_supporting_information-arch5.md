# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

- Overview of the dataset
  - An archive of neutron probe soil moisture data collated for hundreds of UK locations; UKSMD currently provides observations for 428 locations across 45 study areas, spanning 1966–2013 (1–20 years per site).
  - Three data forms are provided: neutron probe counts (R) and derived volumetric soil moisture (θ); depth-integrated profile moisture content (PMC); plus comprehensive metadata and publications references.
  - Linkages to British National Grid coordinates and latitude/longitude for tube locations.

- Dataset contents and structure
  - Four CSV files in the UKSMD package:
    - Volumetric_soil_moisture_UKSMD.csv: time-series of NP count rate R and volumetric soil moisture θ at multiple depths.
    - Profile_moisture_content_UKSMD.csv: time-series of depth-integrated profile moisture content (PMC) in two formats (PMC1 in mm water, PMC2 in m3 water/m3 soil).
    - Tube_metadata_UKSMD.csv: tube identifiers, locations, dates, depths, vegetation, land-use, soil type, geology, coordinates, start/end dates, depth coverage, altitude, and quality notes.
    - Site_publications_UKSMD.csv: references to publications and online URLs for sites/areas.
  - Metadata and data files use SI units and CSV format for easy import into common analysis environments (R, Python, Fortran, etc.).
  - Derived descriptions and field mappings summarized in accompanying Tables 2 and 3.

- Data production, provenance, and processing
  - UKSMD combines older SMDB data (1960s–1980s) and more recent NP data (up to 2013), recovered from magnetic tapes and dispersed spreadsheets/databases, into a single consistent dataset.
  - Recovered data include NP counts (R) and, where possible, derived θ; PMC values are derived where needed to provide depth-integrated moisture.
  - Core processing approaches:
    - NP readings (3.2.1): measurements taken with neutron probes in access tubes to specific depths; each reading corresponds to an associated soil volume around the probe.
    - Volumetric moisture (3.2.2): θ derived from NP readings using calibration equations (θ = a(R/Rw) + b), with field calibration preferred; site-specific calibrations or Wallingford standard calibrations used when unavailable; top-layer readings below ~15–20 cm often omitted due to neutron leakage.
    - Depth-integrated PMC (3.2.3): PMC is the vertical integral of θ over depth, computed using layer factors; missing PMC values are derived where possible.
  - Coverage: in total, 441 tube locations in 45 study areas are represented; 428 tubes have related data; no observations from Northern Ireland.
  - Data accuracy and consistency efforts include quality control and a comprehensive audit of original data holdings.

- Data quality, uncertainty, and flags
  - Quality control:
    - Negative θ values removed and marked as missing (-1).
    - Some θ values (>1.0) flagged as suspect in BALQU, CRINA, and PLYNL due to peat/very moist conditions; QUALITY1 indicates potential issues (1 if >1.0, else 0).
    - PMC values with unrealistic jumps inspected; corrections documented or values removed if unverifiable.
    - NP-derived estimates are reliable for detecting changes over time, but absolute θ values carry calibration-related uncertainties; typical θ could vary significantly depending on calibration equation used.
  - Flags:
    - QUALITY1: values >1.0 or other anomalies in θ/PMC.
    - QUALITY2: jumps/spikes in time-series data.
    - Some recalculated values are labelled with a ‘c’ to indicate derived/calculated values due to missing original data.
  - Guidance for users:
    - Emphasize temporal variability over absolute values due to calibration uncertainty.
    - Consider analyses with and without flagged data to assess sensitivity.

- Metadata and documentation
  - Tube_metadata_UKSMD.csv provides rich site-level context: tube IDs, area IDs/names, coordinates (GB grid and lat/long), start/end measurement dates, depth coverage, altitude, vegetation, land use, soil type, geology, calibration notes, and comments.
  - Site_publications_UKSMD.csv links data to published references and online URLs to aid attribution and traceability of original observations.
  - Post-processing includes categorization of vegetation into broad LAND_USE types to aid data discovery.

- Data availability, geographic coverage, and usage
  - Data are available for 45 geographic areas with 112 sites and 428 NP tubes; no NI data.
  - Names and area codes provided (e.g., BALQU, SMDBE; LINCS, SMDBT; etc.) with site counts and tube counts per area.
  - Data can support:
    - Historical drought analysis (1966–2013) and water balance studies.
    - Hydrological and land-surface model evaluation and data assimilation (in combination with ISMN, COSMOS-UK, and the Global Soil Moisture Databank).
    - Assessments of soil moisture variability and long-term trends across UK soil types and land covers.
  - Practical considerations:
    - NP measurements are generally less reliable for absolute soil moisture in the top ~10 cm when compared with satellite observations; better for detecting changes over time.
    - Useful for validating remotely-sensed soil moisture products when used with appropriate caveats.

- How data can be used and cited
  - Acknowledge original studies using Site_publications_UKSMD.csv; Table A.1 provides an overview of data sources and contributing studies.
  - UKSMD data can complement other soil moisture datasets (ISMN, COSMOS-UK, Global Soil Moisture Databank) for regional to national-scale analyses.
  - The dataset spans a 47-year period (1966–2013), capturing events such as the 1976 drought.

- Access, licensing, and acknowledgements
  - The dataset has been prepared for deposit in European Open Data initiatives (EIDC) and supported by NERC-CEH and related projects (MELODIES, ASSIST).
  - Acknowledgements and references accompany the dataset, detailing calibration work, data recovery efforts, and historical data sources.

- Notable limitations and considerations for governance
  - Some metadata gaps exist due to historical data recording practices; location precision and site linking may be limited in a few cases.
  - Calibration-related uncertainties are inherent; users should incorporate calibration method information (Tube_metadata) and consider data quality flags in analyses.
  - Northern Ireland observations are not represented; users focusing on UK-wide assessments should exclude NI gaps or seek supplementary sources.