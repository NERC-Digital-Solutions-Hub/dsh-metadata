# Supporting Document
Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013. Maberly, S.C., Brierley, B., Carter, H.T., Clarke, M.A., De Ville, M.M., Fletcher, J.M., James, J.B., Keenan, P., Kelly, J.L., Mackay, E.B., Parker, J.E., Patel, M., Pereira, M.G., Rhodes, G., Tanna, B., Thackeray, S.J., Vincent, C., Feuchtmayr, H. (2017)

- Overview of the dataset
  - Long-term monitoring dataset covering 1945 to 2013 for North Basin Windermere, Cumbria, England.
  - Variables include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved silica, and phytoplankton chlorophyll a.
  - Sampling frequency: weekly or fortnightly, depending on variable and period.
  - Origin: initially collected by the Freshwater Biological Association; since 1989 managed by the Centre for Ecology & Hydrology (CEH) and its predecessor.

- Data scope and variables
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation (% air-saturation).
  - SECC: Secchi depth in metres (water clarity).
  - ALKA: alkalinity in µg CaCO3 per litre.
  - PH: pH.
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.
  - Note: some samples are below detection limit, indicated by a < in sign_if_LT_LOD.

- Sampling regime and depth integration
  - Water samples are integrated from the 0–5 m layer (1945–1962), 0–10 m (1962–1964), and 0–7 m (1964 onward).
  - Measurements collected from a boat at the deepest part of the lake, at a fixed buoy location.

- Data quality and structure
  - These are raw data and have not been quality controlled or calibrated (except for double entries from 2005 onward).
  - Visual checks have been performed for data plausibility.
  - Data are organized in a comma-separated values (CSV) file with columns:
    - sdate (measurement date)
    - variable, Description (the variable name and description)
    - value, Description (the measurement value)
    - sign_if_LT_LOD, Description (indicator if below detection limit)

- Access, metadata, and format
  - Data provided as downloadable CSV with clear variable descriptions and units.
  - Includes a flag for detections below the limit of detection to aid interpretation.

- Usage and example citations
  - The dataset has been used in multiple recent publications, including:
    - Early warning indicators and non-linear change in long-term ecological data.
    - Long-term perch biology and ecology in Windermere.
    - Climate forcing, pathogen effects on ecosystem dynamics, and phenological change in freshwater systems.
    - Phytoplankton phenology, nutrient load and temperature impacts on Windermere phytoplankton.
  - These examples illustrate the dataset’s applicability for climate-related ecological studies, nutrient dynamics, and long-term phenological analyses.

- Implications for data leadership and stewardship
  - Demonstrates the value of long-running, multi-parameter lake datasets for monitoring environmental change.
  - Highlights the need for ongoing quality control, calibration, and metadata to maximize utility.
  - Underlines importance of data provenance (origin, method changes, sampling depth) and clarity on measurement units and detection limits.
  - Shows potential for data sharing across networks and integration with broader lake, climate, or ecological data communities.