# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

- Presents an archive of neutron probe soil moisture data collated for hundreds of UK locations.
- UK Soil Moisture Databank (UKSMD) currently provides observations for 428 locations.
- Coverage spans 1966–2013, with records from 1 to 20 years per site.
- Data types available: neutron probe readings (R), volumetric soil moisture (θ, m3 water/m3 soil), and depth-integrated profile moisture content (PMC).
- Metadata included, with tube locations linked to British National Grid coordinates and lat/long.
- Dataset designed for open access and reuse, with explicit metadata and publication links.

## Dataset structure

- Volumetric_soil_moisture_UKSMD.csv: Time-series of neutron probe count rate R and volumetric soil moisture θ across various depths.
- Profile_moisture_content_UKSMD.csv: Time-series of depth-integrated profile moisture content (PMC) provided as depth-specific and depth-integrated values.
- Tube_metdata_UKSMD.csv: Tube-level metadata including location, dates, depths, vegetation, land-use, soil type, geology, coordinates, and calibration notes.
- Site_publications_UKSMD.csv: Links to publications and reports related to each site (with URLs/DOIs).

- All files are CSVs for easy import into spreadsheet or analysis tools (R, Python, Fortran).
- Metadata includes AREA_ID, AREA_NAME, SITE_ID, TUBE_ID, coordinates, depths, vegetation, land-use, soil type, geology, and calibration information.
- Data fields include DATE_TIME, DEPTH, RW (water count), COUNT (raw counts), VOLUMETRIC SOIL MOISTURE θ, PMC1 (depth-integrated from surface to depth), PMC2 (same as PMC1 but in different units), and quality flags.

## Data production methods

- UKSMD consolidates NP observations from 1966–2013, recovered from fragile magnetic tapes and disparate spreadsheets/databases.
- Older data from The Soil Moisture Databank (SMDB, Gardner 1981) recovered from historical tapes; newer data (up to 2013) retrieved from local records across UKCEH.
- All data and associated data (raw NP counts to θ to PMC) have been quality controlled and converted to SI units.
- Data integration approach:
  - NP counts (R) and water counts (Rw) preserved where possible.
  - θ derived from R using calibration equations; field calibrations or Wallingford calibration equations used when site-specific calibrations unavailable.
  - To address atmospheric/leakage issues, readings at shallow depths (<15–20 cm) often omitted unless site-specific corrections applied.
  - When θ missing but NP data exist, θ is recalculated using calibration equations; some sites use original θ values if recovered.
- Final UKSMD covers 441 tube locations in 45 study areas across England, Wales, and Scotland.

## Data availability and formats

- Data are available in three forms:
  - Raw count data: NP readings (R) and water counts (Rw) at multiple depths.
  - Volumetric soil moisture: θ values at various depths (0 ≤ θ ≤ 1).
  - Depth-integrated profile moisture content (PMC): water stored from surface to a depth zn (in mm) or as m3 water/m3 soil.
- Geographic coverage: 45 areas, 112 sites, 428 NP tubes; no observations from Northern Ireland.
- Notable long-term datasets include Hodnet Heath (HODHE) and Lincolnshire sites (LINCS); some areas provide up to 13+ years of data.
- Data availability visuals (e.g., maps) accompany the dataset to show location and data duration.

## Missing data, quality control and uncertainty

- Missing data are flagged as -1; where possible, missing values are estimated from related data (marked with COMMENT 'c' to indicate derived values).
- Metadata gaps filled from alternative contemporary datasets; location corrections noted in TUBE_COMMENT.
- Quality flags:
  - QUALITY1 (q1): θ values > 1.0 flagged as q1 due to potential overestimation in some peat/very wet soils.
  - QUALITY2 (q2): jumps/spikes in time series flagged for potential anomalies.
- θ values are constrained to 0–1; a few observations exceed 1.0 in peat-rich rainfall zones, warranting caution.
- Uncertainty considerations:
  - NP-derived soil moisture is reliable for detecting changes but less certain for absolute values due to calibration variability.
  - Calibration uncertainty can exceed 20% in very wet soils; site-specific calibrations improve accuracy.
  - Where θ is not available or calibration is uncertain, historically derived PMC values may carry higher uncertainty and are flagged accordingly.
- When θ or PMC values are reconstructed recently, they are flagged with 'c' to indicate greater absolute-value uncertainty.

## How to use the data

- Acknowledge original research and link to publications, using the Site_publications_UKSMD.csv file and Table A1 references.
- Suitable for:
  - Analyzing long-term soil moisture variability and drought responses (1966–2013; e.g., drought of 1976 era).
  - Model validation and data assimilation for hydrological, agricultural, or land-surface models; can be combined with ISMN, COSMOS-UK, and global soil moisture databanks for broader studies.
  - Assessing relationships between soil moisture and vegetation, soil types, and land use.
  - Calibration and validation of remotely-sensed soil moisture products, with caveats about the top 10 cm being less reliable for in-situ-to-EO comparisons.
- Data can be used to study water balance variability, recharge processes (e.g., in chalk upland areas), and long-term soil moisture trends across diverse UK environments.
- Users should consider quality flags (q1, q2) and calibration uncertainties when conducting analyses; it may be prudent to compare results with and without flagged data.
- The dataset supports historical analyses of emissions-related hydrology (e.g., nitrous oxide studies) and can contribute to revisiting LOCAR-related site studies when combined with meteorological datasets.

## Acknowledgements

- Recovery and analysis supported by NERC-CEH Water Programme and FP7 MELODIES project.
- Dataset preparation for deposition supported by NERC under ASSIST program.
- Acknowledgement of individuals who aided in site identification and data recovery.

## References and data sources

- Contains calibration studies, soil moisture methodology papers, and LOCAR-related references (as cited in the dataset documentation and accompanying references).
- Site-level historical studies linked in Site_publications_UKSMD.csv.