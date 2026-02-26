# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013

- Purpose and scope
  - Long-term monitoring dataset for the South Basin of Windermere (Cumbria, England) covering 1945–2013 for multiple water quality and phytoplankton variables.
  - Variables include physical, chemical, and biological measurements to support analysis of lake dynamics and ecological change.

- Sampling regime and collection methods
  - Sampling frequency: weekly or fortnightly.
  - Timeframe: March 1945 through end of 2013 (some variables began earlier; others follow later).
  - Providers: Freshwater Biological Association initially; Centre for Ecology & Hydrology (CEH) and predecessors since 1989.
  - Depth and location: water samples collected from a boat at a buoy at the deepest part of the lake.
  - Depth integration: historical shifts in depth integration (0–5 m, 0–10 m, then 0–7 m from 1964 onwards).

- Variables and units (as downloadable data)
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation as % air-saturation.
  - SECC: Secchi depth in metres (water clarity).
  - ALKA: alkalinity in µg CaCO3 per litre.
  - PH: pH.
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.
  - Note: data include a sign_if_LT_LOD column indicating values below detection limits.

- Data quality and limitations
  - Data are raw (not yet quality controlled or calibrated); only visual checks have been performed.
  - Some entries are known to be double entries from 2005 onward.
  - Below-detection-limit values are indicated (sign_if_LT_LOD).
  - Metadata about sampling methods and depth integration changes are included to aid interpretation.

- Data structure and access
  - Provided as a comma-separated values (CSV) file.
  - Columns include: sdate (measurement date), variable (description of the variable), value (measurement value), sign_if_LT_LOD (indicator for below detection limit).
  - Additional descriptive context lists the measurement regime, depths, and units for each variable.

- Examples of use in the literature
  - Long-term ecological indicators and non-linear change in ecological data.
  - Insights into fish population and community biology from a multi-decade study.
  - Climate and nutrient–phytoplankton interactions; phenology and ecosystem responses in a large, temperate lake.
  - Broader references include publications in Journal of Applied Ecology, Freshwater Biology, Ecology of Freshwater Fish, Nature Climate Change, and other prominent journals.

- Practical implications for analysts
  - Provides a rich, multi-decadal baseline for hydrology, water chemistry, and phytoplankton dynamics to study trends and responses to climate and nutrient changes.
  - Useful for developing and testing predictive models of lake state, phenology, and trophic interactions.
  - Requires careful handling of raw data, detection-limit indicators, and depth-integration changes; results should be contextualized with the provided metadata and any quality-control status.