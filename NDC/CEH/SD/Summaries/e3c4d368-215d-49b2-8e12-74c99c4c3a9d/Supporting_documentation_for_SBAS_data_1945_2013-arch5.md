# Supporting Document  
Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013. Maberly, S.C., Brierley, B., Carter, H.T., Clarke, M.A., De Ville, M.M., Fletcher, J.M., James, J.B., Keenan, P., Kelly, J.L., Mackay, E.B., Parker, J.E., Patel, M., Pereira, M.G., Rhodes, G., Tanna, B., Thackeray, S.J., Vincent, C., Feuchtmayr, H. (2017)

- Overview
  - Long-term, weekly to fortnightly monitoring dataset from the South Basin of Windermere, Cumbria, England.
  - Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
  - Time period covered: March 1945 to end of 2013 for all variables (some began earlier for certain variables).

- Sampling regime and collection methods
  - Sampling frequency: weekly or fortnightly.
  - Sample location and method: collected from a boat at the deepest part of the lake (marked buoy).
  - Depth integration for water chemistry: initially 0–5 m (1945–1962), 0–10 m (1962–1964), and 0–7 m (1964 onwards) for water chemistry.
  - Data origin: initially by the Freshwater Biological Association; since 1989, collected by CEH and its predecessor Institute of Freshwater Ecology.
  - Temporal scope for data: March 1945 to end of 2013.

- Data available and content
  - Variables and units:
    - TEMP: surface temperature in degrees Celsius.
    - OXYG: surface oxygen saturation in % air-saturation.
    - SECC: Secchi depth in metres.
    - ALKA: alkalinity in µg CaCO3 per litre.
    - PH: pH.
    - NH4N: ammonium in µg N per litre.
    - NO3N: nitrate in µg N per litre.
    - PO4P: soluble reactive phosphate in µg P per litre.
    - TOTP: total phosphorus in µg P per litre.
    - SIO2: dissolved reactive silicon in µg per litre.
    - TOCA: phytoplankton chlorophyll a in µg per litre.
  - Data format: comma separated values (CSV) with columns including sdate (measurement date), variable, value, and sign_if_LT_LOD (indicator if below detection limit with a < sign).
  - Depth integration metadata: exact depth range used for water chemistry varies by time as noted above.
  - Detection limits: values below detection limit are flagged by sign_if_LT_LOD (<).

- Quality control and data quality
  - Status: raw data, not yet quality controlled or calibrated.
  - Exceptions: double entries exist from 2005 onwards.
  - Validation: data have been visually checked.

- Data structure and documentation
  - Primary data file structure: columns for date, variable description, value, and quality/detection indicators.
  - Measurement context: measurements are taken from the deepest lake point at a marked buoy.

- Data availability and usage
  - The dataset is available for download (hosted by CEH/associated data portals).
  - Recent publications using the dataset demonstrate its applicability to long-term ecological and climate-related analyses, including early warning indicators of non-linear change, perch population studies, pathogen-driven ecosystem forcing, phytoplankton phenology, and climate sensitivity across taxa.
  - Example references (selected):
    - Burthe et al. 2016, Journal of Applied Ecology. Do early warning indicators consistently predict non-linear change in long-term ecological data?
    - Craig et al. 2015, Biology of Perch (Windermere 70-year study).
    - Edeline et al. 2016, Oecologia. Pathogens trigger top-down climate forcing on ecosystem dynamics.
    - Elliott 2012, Freshwater Biology. Predicting impacts of changing nutrient load and temperature.
    - Thackeray et al. 2013/2016, various on phenology, climate sensitivity, and ecosystem responses.
  - Additional citations cover related lake biogeochemistry and climate-related studies.

- Governance, provenance, and stewardship notes
  - Custodianship: data originated with the Freshwater Biological Association and has been maintained by CEH and its predecessors since 1989.
  - Metadata and transparency: clear documentation of sampling regime, depth integration changes over time, and variable units.
  - Key stewardship considerations for data stewards:
    - The data are raw and require QC/calibration before use in comparative analyses.
    - Metadata should be preserved and enhanced to reflect depth integration changes and detection-limit handling.
    - Ensure consistent interpretation of the sign_if_LT_LOD flag for below-detection values.
    - Maintain linkage to the temporal context (1945–2013) and the evolving measurement methods.
    - Provide clear data access pathways and versioning to support discoverability and re-use by data users.