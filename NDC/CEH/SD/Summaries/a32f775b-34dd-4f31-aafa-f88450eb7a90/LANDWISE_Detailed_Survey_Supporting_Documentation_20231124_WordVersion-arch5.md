# LANDWISE Detailed Survey Supporting Documentation (Version 1.4)

- Purpose and scope
  - Documents a detailed LANDWISE survey dataset of surface and sub-surface hydraulic and hydrological soil properties across Thames catchment.
  - Part of the LANDWISE project under the Natural Flood Management Research Programme, supported by NERC grant NE/R004668/1.
  - Related to the LANDWISE Broad-scale survey and broader LANDWISE data collection (soil near-surface properties, vegetation observations, land use/management) across Thames catchment (2018–2021).

- Dataset contents and structure
  - Single CSV file: LANDWISE_detailed_survey_soil_data_2021_updated_v2.
  - Structure: 70 columns and 380 rows.
  - Data type conventions: missing values represented as "NA"; column definitions provided in the documentation (Table 5).
  - Includes identifiers (site, field, location), geolocation (OS grid, Easting/Northing), sampling dates and times, depths, and a wide set of measured properties.

- Sampling design and field locations
  - Seven fields selected from the LANDWISE Broad-scale survey, organized into three sites by geology: mudstone, carbonate (chalk), and limestone.
  - Sampling across land-use and management contrasts within each site.
  - Within-field sampling along transects at three location types: TR (trafficked), IN (infield), UN (untrafficked margins); 15 locations per field (TR1–TR5, IN1–IN5, UN1–UN5).
  - Field locations shown in accompanying figures; approximate site coordinates provided for anonymity.

- Measurements and methods (field and lab)
  - Bulk density and inferred porosity (with depth)
    - Method: volumetric soil cores and oven drying (105°C).
    - Sites/types: Arable (bulk density/porosity by depth).
    - Sampling: 50 samples per field; 5 fields across Spring 2021; post-harvest not explicitly listed for these measurements.
  - Soil moisture retention (pF 0–2)
    - Method: Sandbox lab analysis (volumetric suction).
    - Sites: Arable fields (limestone sites) in Spring/Autumn campaigns.
  - Saturated hydraulic conductivity (Ksat, Kfs)
    - Method: Guelph Permeameter (Mariotte principle).
    - Depths: 25 cm and 45 cm.
    - Field locations offset to avoid interference; 12 samples per field; 5 arable fields; multiple campaigns in Spring/Autumn 2021.
  - Infiltration (unsaturated hydraulic conductivity, Kunsat)
    - Method: Mini Disk Infiltrometers.
    - Location types: Arable, Grassland, and Woodland; multiple fields.
    - Spring and post-harvest campaigns with separate measurements (pre-harvest, post-harvest).
  - Soil and vegetation root depth
    - Method: Auger and tape measure.
    - Sites: Arable, Grassland, and Woodland; multiple fields.
  - Timing and campaigns
    - Spring sampling: April 2021 for some measurements.
    - Autumn sampling: October 2021 for others.
  - Data capture and processing
    - Field and lab data recorded in Excel; subsequent QC and flagging applied.

- Data quality control and flags
  - Data entry QC: dual-entry verification to catch typos.
  - Infiltration QC flags (Infiltration_1_QC_Flag, Infiltration_2_QC_Flag)
    - Good: no issues.
    - Invalid: physically implausible values; removed.
    - A: notably unsteady infiltration rate.
    - B: less than 15 ml infiltrated (minimum for accurate calculation).
    - C: unusually high K values (within +3 SD of Carsel & Parrish distribution)—may reflect novel soil state.
  - Guelph permeameter QC flags (Guelph_Permeameter_QC_Flag)
    - Good: no issues.
    - Invalid: physically implausible values (e.g., negative values, alpha outside 0.01–0.5 cm−1); removed.
  - Documentation notes
    - Guelph double-head vs single-head measurements: preference given to double-head; if invalid, single-head measurements used and averaged.
  - Data structure for QC
    - QC flags and notes embedded in dataset columns; missing values denoted as NA where measurements were invalid or not taken.

- Units, variables, and data organization
  - The dataset includes 70 columns with a defined schema (IDs, location codes, geospatial coordinates, sample timing, depths, and measured soil properties).
  - Columns cover site/field/location identifiers, sampling geography, dates/times, depths, and derived properties (e.g., porosity, VWC, Kfs, Kunsat).
  - Location and sample metadata include OS grid squares and British National Grid coordinates (Easting/Northing).

- Fieldwork and instrumentation
  - Soil sampling: Eijkelkamp 07.53.SC kit with closed ring holder; Edelman and Stony augers.
  - Laboratory analyses: oven drying (105°C) for bulk density and moisture content; Sandbox for soil moisture retention.
  - Infiltration: Mini Disk Infiltrometers (Decagon Devices).
  - Saturated hydraulic conductivity: Guelph Permeameter (Soilmoisture Equipment Corp.).
  - Validation and calibration: balances and ovens calibrated and validated; equipment details and serials provided for traceability.

- Related datasets and references
  - Related to LANDWISE Broad-scale survey: Soil near-surface properties, vegetation observations, land use and land management for 1800 Thames catchment locations (2018–2021).
  - Key methodological references: Carsel & Parrish (1988) for soil water retention characteristics; Zhang (1997) for disk infiltrometry-based hydraulic parameters; METER and Soilmoisture Equipment Corp. operating manuals for equipment procedures.

- Data access and reuse
  - The dataset is provided as a single CSV with a defined structure and accompanying metadata to support reuse, interpretation, and integration with related LANDWISE datasets.
  - Missing values and QC flags should be consulted to assess data suitability for specific analyses and to document data provenance in any downstream use.