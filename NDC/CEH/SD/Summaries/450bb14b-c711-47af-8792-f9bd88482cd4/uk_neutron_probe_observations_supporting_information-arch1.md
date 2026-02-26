# Collated neutron probe measurements and derived soil moisture data, UK, 1966-2013: Supporting Information

- Overview
  - An archive of neutron probe soil moisture data collated for hundreds of UK locations, now in the UK Soil Moisture Databank (UKSMD).
  - Coverage: observations from 1966 to 2013, across 428 locations (with data for 45 study areas and 112 sites; ~441 neutron probe tube locations reported in the dataset narrative).
  - Data types provided: raw neutron probe counts, volumetric soil moisture content, and depth-integrated profile moisture content, plus rich metadata and links to publications.

- Dataset structure
  - Four CSV files (two data, two metadata):
    - Volumetric_soil_moisture_UKSMD.csv: time-series of neutron probe count rate R and volumetric soil moisture θ at various depths.
    - Profile_moisture_content_UKSMD.csv: time-series of depth-integrated profile moisture content (PMC1 in mm water, PMC2 in m3 water/m3 soil).
    - Tube_metadata_UKSMD.csv: tube ID, location, dates, depths, vegetation, land-use, soil type, geology, coordinates, etc.
    - Site_publications_UKSMD.csv: references to papers/reports related to each area/site with URLs/DOIs.
  - Data units and formats are provided; metadata tables include AREA_ID, AREA_NAME, SITE_ID, TUBE_ID, coordinates, dates, depths, vegetation, land-use, soil type, and calibration information.

- Data production and recovery
  - Data consolidation: old SMDB data (1960s–1980s) recovered from magnetic tapes; newer NP data (1970s–2013) retrieved from spreadsheets/databases and quality controlled.
  - Purpose: create a consistent, long-term UK NP soil moisture dataset spanning 1966–2013, linking raw NP counts to moisture values.
  - Coverage notes: older data (SMDB) recovered for 99 locations; broader LOCAR-era data added (329 locations); compiled to yield in-situ soil moisture data from 441 tube locations in 45 study areas (England, Wales, Scotland).

- Neutron probe readings (3.2.1)
  - Measurements done by lowering a neutron probe into access tubes; count rate R relates to soil moisture through calibration.
  - Each reading applies to a surrounding soil sphere (approx. 0.2–0.3 m radius).

- Volumetric soil moisture (3.2.2)
  - θ (m3 water/m3 soil) derived from R via calibration: θ = a(R/Rw) + b, where Rw is the water count and a, b are calibration parameters.
  - Field calibration possible; if unavailable, use standard calibration (Wallingford method).
  - Topsoil correction: readings within about 15–20 cm of surface often excluded due to neutron leakage; when not available, the next depth’s reading is assumed to apply to the upper zone.
  - Recovery rates: θ recovered for ~73% of observations; θ values recovered for ~78% of observations. When θ missing, values imputed using site- and soil-type assumptions, increasing uncertainty.

- Depth-integrated profile moisture content (3.2.3)
  - PMC values computed from θ at multiple depths, using layer factors to obtain water content per soil layer and summing to depth zn.
  - PMC provided in two formats: PMC1 (mm water stored to depth zn) and PMC2 (m3 water/m3 soil to depth zn).
  - If PMC depths vary by site, authors derived PMC down to maximum measurement depth using the stated method.

- Data availability and format details
  - Data are available for 45 geographic areas, 112 sites, and 428 NP tube locations (no observations yet for Northern Ireland).
  - The dataset provides three forms of soil moisture data: raw NP readings (R, Rw), θ, and PMC.
  - Tables and figures (including a UK map) illustrate area coverage and data availability by site/tube.

- Missing data and quality control (QC)
  - Missing data are indicated as -1; where possible, missing values are estimated and flagged with COMMENT codes (e.g., 'c' for recently calculated estimates).
  - Missing metadata (elevation, etc.) sourced from other datasets and noted in tube metadata.
  - Negative θ values removed; QC flags applied to θ values:
    - QUALITY1 (q1): values > 1.0 flagged due to potential overestimation in high-rainfall/peat soils; treat with caution.
    - QUALITY2 (q2): jumps/spikes flagged after time-series inspection; may be retained if consistent with other data and observer records.
  - Calibration uncertainty: converting NP counts to θ depends on soil category calibrations; typical uncertainty can exceed 20% in very wet soils; when calibration is uncertain, newer estimates marked with 'c' (higher absolute-value uncertainty).

- Important usage notes
  - NP-derived soil moisture is generally more reliable for detecting changes over time than for precise absolute moisture values.
  - Top 10 cm of soil moisture is less reliable for validation against satellite or cosmic-ray sensors; use UKSMD for deeper soil moisture analyses or temporal trends.
  - Data are valuable for hydrological, agricultural, and land-surface model validation and data assimilation; can be combined with datasets like ISMN, COSMOS-UK, and the Global Soil Moisture Databank for broader context.
  - The dataset supports historical drought analysis (e.g., 1976 drought) and long-term soil-water balance studies.

- How to use and acknowledge
  - Acknowledge original studies via Site_publications_UKSMD.csv and Table A.1 in the Appendix when citing data sources.
  - Use Volumetric_soil_moisture_UKSMD.csv for depth-specific, time-resolved θ; use Profile_moisture_content_UKSMD.csv for depth-integrated PMC values to compare across soils with different maximum measurement depths.
  - Consider using QC flags (q1, q2) to assess sensitivity analyses by including/excluding suspect data.

- Applications and potential
  - Model validation and data assimilation for hydrological and land-surface models.
  - Cross-validation with remotely sensed soil moisture products, with caveats about topsoil reliability.
  - Historical climate and drought research; linking soil moisture to groundwater recharge and vegetation effects.
  - Historical emission studies (e.g., nitrous oxide) where soil moisture is a key driver.

- Acknowledgments
  - Supported by NERC-CEH Water Programme and FP7 MELODIES; dataset preparation supported by NERC ASSIST program.
  - Gratitude extended to individuals who assisted in site identification and referencing.

- References and further material
  - Comprehensive references and data sources are provided in the document and linked metadata; Site_publications_UKSMD.csv contains DOIs/URLs for related publications.