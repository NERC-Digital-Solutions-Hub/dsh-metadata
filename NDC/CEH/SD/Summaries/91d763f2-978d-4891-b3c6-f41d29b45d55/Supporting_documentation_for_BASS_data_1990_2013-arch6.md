# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

- Purpose and scope
  - Long-term fortnightly monitoring dataset for Bassenthwaite Lake, Cumbria, England (1990–2013).
  - Provides a time-series of physical, chemical, and biological indicators to support analysis of lake dynamics and climate-related changes.

- Sampling regime and collection methods
  - Sampling frequency: fortnightly.
  - Depth of sampling: integrated from 0 to 5 m.
  - Location: measured from a boat at the deepest part of the lake (buoy); when unavailable, samples taken from the shore (not integrated) and flagged accordingly.
  - Data delivery format: downloadable CSV file.

- Variables and units (columns in the CSV)
  - sdate: Date of measurement
  - variable: Description of the measured parameter
  - value: Measured value
  - sign_if_LT_LOD: Indicates if a value is below detection limit (presence of a < sign)
  - flag: Data collection context
    - flag = 1: sample taken at buoy (integrated 0–5 m)
    - flag = 2: sample taken from shore (not integrated)
  - Variables included and units
    - TEMP: surface temperature, °C
    - OXYG: surface oxygen saturation, % air-saturation
    - SECC: Secchi depth, metres
    - ALKA: alkalinity, µg CaCO3 per litre
    - pH: pH
    - NH4N: ammonium, µg N per litre
    - NO3N: nitrate, µg N per litre
    - PO4P: soluble reactive phosphate, µg P per litre
    - TOTP: total phosphorus, µg P per litre
    - SIO2: dissolved reactive silicon (SiO2), µg per litre
    - TOCA: phytoplankton chlorophyll a, µg per litre

- Data quality and limitations
  - Raw data: not quality controlled or calibrated (except for double entries from 2005 onwards); visually checked.
  - Data gaps: March–June 2001 missing due to foot-and-mouth disease outbreak restricting lake access.
  - Detection limits: values below detection limit are flagged with sign_if_LT_LOD.

- Data structure and access
  - File format: comma-separated values (CSV).
  - Columns: sdate, variable, value, sign_if_LT_LOD, flag (plus descriptive metadata for each field).

- Data usage and potential products
  - Suitable for building self-serve data products (dashboards, pivot tables, time-series charts) and integrating with other lake datasets.
  - Can support trend analyses, seasonality studies, and climate-change impact assessments on phytoplankton and nutrient dynamics.
  - Can be combined with additional environmental datasets to enhance contextual analyses (e.g., hydrology, climate data).

- Notable publications and usage examples
  - Uses in modelling and analysis of phytoplankton and nutrient dynamics across English lakes.
  - Examples include studies on nutrient sources, retention times, climate-change impacts on vendace habitat, and long-term ecological responses.

- Provenance and timeframe
  - Data collected August 1990 through the end of 2013.
  - Dataset compiled and described by multiple authors (e.g., S.C. Maberly et al.).

- Practical notes for data support
  - When integrating into analyses, plan for QC steps to calibrate or validate raw measurements.
  - Be mindful of the shore-sampled entries (Flag 2) that are not integrated 0–5 m, which may affect comparability with buoy-derived samples.