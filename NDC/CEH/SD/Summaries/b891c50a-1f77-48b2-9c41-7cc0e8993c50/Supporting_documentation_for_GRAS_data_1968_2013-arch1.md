# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

- Purpose and scope
  - Long-term monitoring dataset of multiple limnological variables from Grasmere, Cumbria, England.
  - Variables tracked: surface temperature, surface oxygen saturation, water clarity, water chemistry, and phytoplankton chlorophyll a.
  - Temporal coverage: June 1968 through end of 2013; sampling frequency ranges from weekly to fortnightly for some variables.
  - Initial collection by the Freshwater Biological Association; since 1989 collected by CEH and its predecessor Institute of Freshwater Ecology.

- Sampling regime and collection methods
  - Water samples collected from a boat at the lake’s deepest location (buoy).
  - When boat access to buoy was not possible, samples taken from the shore (Flag 2).
  - Integrated water samples collected from the 0–5 m depth layer.
  - Variables measured and reported: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), pH; NH4N, NO3N, PO4P, TOTP, SIO2, TOCA (all in µg per L, with TOCA in µg/L).

- Quality control and data cleaning
  - Data are raw and have not been quality controlled or calibrated (except for double entries from 2005 onward).
  - Visual checks have been performed.
  - Some measurements below detection limits are indicated with a < sign in sign_if_LT_LOD.

- Data structure and access
  - Data provided as a comma-separated values (CSV) file.
  - Columns include: sdate (measurement date), variable descriptions, value, sign_if_LT_LOD (indicates below detection limit), flag (1 = buoy location, 2 = shore visit).

- Variables, units, and data conventions
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation in % air-saturation.
  - SECC: Secchi depth in metres.
  - ALKA: alkalinity in µg CaCO3 per litre.
  - pH: pH.
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.

- Provenance and use in research
  - Documented in recent publications and datasets, including:
    - Maberly et al. (2013) on catchment productivity and lake CO2 emissions (Nature Climate Change).
    - Reynolds et al. (2012) on forty years of Grasmere water quality monitoring and effects of sewage enrichment vs hydraulic flushing (Freshwater Biology).
    - Wang et al. (2016) on coupling of carbon and silicon cycles in rivers and lakes (Scientific Reports).
    - Woolway et al. (2016) reference to Lake surface temperatures in state-of-the-climate summaries (Bulletin of the American Meteorological Society).
  - Demonstrates utility for long-term trend analysis, enrichment vs flushing effects, and biogeochemical coupling studies.

- Author and data stewardship
  - Large author team led by S.C. Maberly and colleagues.
  - Data historically curated by the Freshwater Biological Association and later by CEH; intact metadata and variable definitions provided for reuse.

- Considerations for analysts
  - Caution due to raw data lacking formal QC; account for potential measurement biases and detection-limit indicators.
  - Temporal and sampling-method consistency over decades should be assessed when analyzing trends.
  - Data gaps and possible changes in sampling location (buoy vs shore) may affect comparability.