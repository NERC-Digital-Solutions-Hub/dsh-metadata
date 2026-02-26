# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013

- Purpose and scope
  - Long-term monitoring dataset for Blelham Tarn, Cumbria, England.
  - Variables include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH (PH), ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg SiO2/L), phytoplankton chlorophyll a (TOCA, µg/L).
  - Time span: data from April 1945 to end of 2013 (some variables 1945–2013).
  - Sampling regime: weekly to fortnightly; water samples integrated from 0 to 5 m.
  - Location and collection: samples taken from a boat at the deepest part of the lake (buoy); shore sampling when buoy access was not possible.
  - Collectors: Freshwater Biological Association initially; CEH and its predecessor Institute of Freshwater Ecology since 1989.

- Sampling regime and collection methods
  - Variables and units as listed above.
  - Data files are provided as a comma-separated values (CSV) dataset.
  - Flagging: Flag 1 = sample from the buoy location; Flag 2 = shore sample when buoy access was not possible.
  - Some samples may be non-integrated if shore sampling occurred; flagged accordingly.

- Data quality and limitations
  - Data are raw and have not been quality controlled or calibrated (except double entries from 2005 onwards); visually checked.
  - Gaps: March–July 2001 missing due to foot-and-mouth disease restrictions.
  - Values below detection limit are indicated with a < sign in sign_if_LT_LOD.

- Data structure and download format
  - CSV format with columns:
    - sdate (date of measurement)
    - variable (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
    - value (measurement value)
    - sign_if_LT_LOD (indicator for below detection limit)
    - flag (1 = buoy sample; 2 = shore sample)
  - Clear documentation of units for each variable (as listed above).

- Uses and example publications
  - The dataset has been used in multiple studies, including:
    - Bernhardt, Elliott, & Jones (2008) Modelling phytoplankton responses to changes in stratification and light conditions (Freshwater Biology).
    - Feuchtmayr et al. (2012) Spring phytoplankton phenology across lakes (Freshwater Biology).
    - Foley et al. (2012) Long-term oxygen depletion and drivers (Freshwater Biology).
    - Maberly et al. (2013) Catchment productivity and lake CO2 emissions (Nature Climate Change).
    - Wang et al. (2016) Carbon and silicon geochemical cycles in freshwater systems (Scientific Reports).
    - Woolway et al. (2016) Lake surface temperatures (Bulletin of the American Meteorological Society).
  - Demonstrates utility for long-term environmental health assessment and climate-related change analyses.

- Relevance for monitoring and policy analysis
  - Provides a standardized, long-running dataset suitable for trend analysis across multiple water quality and biological indicators.
  - Useful for assessing environmental health against standards over time and informing management decisions.
  - Highlights the importance of data provenance, raw-data considerations, and the need for quality control before policy-oriented analyses.
  - Supports data reuse and integration with other environmental datasets to enhance monitoring value.