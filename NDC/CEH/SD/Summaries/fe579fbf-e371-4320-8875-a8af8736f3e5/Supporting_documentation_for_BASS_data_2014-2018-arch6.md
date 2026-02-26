# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018

- Overview
  - Long-term, fortnightly monitoring dataset from Bassenthwaite Lake, Cumbria, England.
  - Timeframe: January 2014 through end of 2018; long-term monitoring ended early 2019 due to funding shortages.

- What is included
  - Measured variables and units:
    - TEMP: surface temperature (°C)
    - OXYG: surface oxygen saturation (% air-saturation)
    - SECC: Secchi depth (m)
    - ALKA: alkalinity (µg CaCO3 per litre)
    - pH
    - NH4N: ammonium (µg N per litre)
    - NO3N: nitrate (µg N per litre)
    - PO4P: soluble reactive phosphate (µg P per litre)
    - TOTP: total phosphorus (µg P per litre)
    - SIO2: dissolved reactive silicon (µg per litre)
    - TOCA: phytoplankton chlorophyll a (µg per litre)
  - Sampling regime:
    - Fortnightly samples from 0–5 m water depth.
    - Collected from a boat at a marked buoy location (deepest part of the lake).
    - If buoy access was not possible, samples collected from the shore (Flag 2).
  - Data scope:
    - All data cover 2014–2018.

- Data structure and access
  - Data format: comma-separated values (CSV).
  - Core columns:
    - Date: measurement date
    - Variable, Description: the parameter and its units
    - Value, Description: measured value
    - Sign (if<LOD), Description: indicates if value is below detection limit with a < sign
    - Flag, Description: 1 = buoy location; 2 = shore sampling
  - Examples of usage in literature include studies on carbon and silicon cycles, vendace reappearance, and long-term ecological knowledge.

- Quality control and limitations
  - Data are raw and not yet quality controlled or calibrated.
  - Double entered and visually checked; gaps due to weather or staff shortages.
  - Some values below detection limits are flagged (Sign <LOD).

- Practical considerations for data use
  - Consider QC/calibration needs before formal analyses.
  - Account for <LOD values via Sign indicators during analysis.
  - Distinguish buoy-based (Flag 1) from shore-based (Flag 2) samples to assess potential sampling biases.
  - Suitable for creating self-serve data products (dashboards, trend analyses) or informing related ecological research, with acknowledgment of funding-driven end date (2019).