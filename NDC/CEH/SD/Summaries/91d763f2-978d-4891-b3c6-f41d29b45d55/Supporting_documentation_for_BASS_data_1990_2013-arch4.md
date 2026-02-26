# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

- Purpose and scope
  - Long-term monitoring dataset from Bassenthwaite Lake, Cumbria, England.
  - Fortnightly sampling from August 1990 to the end of 2013.
  - Measurements cover physical, chemical, and biological water quality indicators.

- Data content and units
  - Variables available: 
    - Surface temperature (TEMP) in degrees Celsius
    - Surface oxygen saturation (OXYG) in % air-saturation
    - Secchi depth (SECC) in metres
    - Alkalinity (ALKA) in µg CaCO3 per litre
    - pH (PH)
    - Ammonium (NH4N) in µg N per litre
    - Nitrate (NO3N) in µg N per litre
    - Soluble reactive phosphate (PO4P) in µg P per litre
    - Total phosphorus (TOTP) in µg P per litre
    - Dissolved reactive silicon (SIO2) in µg per litre
    - Phytoplankton chlorophyll a (TOCA) in µg per litre
  - Water samples are integrated from 0 to 5 m; when not possible to visit the buoy, samples were taken from the shore.
  - Data provided in CSV format with columns:
    - sdate (date of measurement)
    - variable (descriptor of the measurement)
    - value (measurement value)
    - sign_if_LT_LOD (indicator if below detection limit, denoted by "<")
    - flag (1 = buoy location; 2 = shore)

- Sampling regime and data collection details
  - Measurements collected from a boat at a marked buoy at the lake’s deepest point; occasional shore sampling when access to buoy was not possible.
  - Data cover August 1990 through 2013.

- Quality control and data quality notes
  - Raw data that have not yet been quality controlled or calibrated (except for double entries from 2005 onwards).
  - Visual checks performed.
  - Data gaps: March–June 2001 missing due to foot-and-mouth outbreak restricting access.

- Metadata and data structure considerations
  - Data are stored as a comma-separated values file with descriptive headers for each column.
  - sign_if_LT_LOD provides detection-limit information per value.
  - flag indicates sampling location, aiding spatial context and potential comparability between buoy and shore samples.

- Usage and impact
  - The dataset is used in numerous publications to study phytoplankton dynamics, nutrient sources, climate-change impacts on lake ecosystems, and habitat assessments for local fish species.
  - Examples of cited work include studies published between 2008 and 2017 across freshwater biology, hydrobiologia, global change biology, and related fields.

- Data governance implications for Data Leaders
  - Actions to consider:
    - Implement formal quality control and calibration procedures prior to public release.
    - Maintain comprehensive metadata on methods, detection limits, and sampling locations to improve discoverability and reuse.
    - Track data gaps and plan for future data collection to address granularity and continuity needs.
    - Ensure clear data provenance and versioning; document any data corrections or reprocessing.
    - Facilitate data sharing and collaboration with wider science networks to enhance community of practice and reduce duplication of effort.
  - Opportunities for data products:
    - Create time-series dashboards for each variable (temperature, oxygen, nutrients, chlorophyll a).
    - Develop integrative analyses linking physical, chemical, and biological parameters to support policy and management decisions.