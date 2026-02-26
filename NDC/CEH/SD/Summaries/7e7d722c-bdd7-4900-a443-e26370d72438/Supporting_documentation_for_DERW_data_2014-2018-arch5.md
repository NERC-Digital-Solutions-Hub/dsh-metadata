# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P., Mackay, E.B., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Ongoing long-term monitoring dataset from fortnightly sampling at Derwent Water, Cumbria, England.
- Data available to download include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH; ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples integrated from 0 to 5 m; measurements from a boat at the deepest part of the lake; shore sampling used when buoy access wasn’t possible.
- Timeframe: January 2014 to end of 2018; long-term monitoring ended early 2019 due to funding shortages.

## Data, variables and format
- Variables and units:
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - pH: pH
  - NH4N: ammonium, µg N per L
  - NO3N: nitrate, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon, µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
- Data file format: comma separated values (CSV) with columns:
  - Date (date of measurement)
  - Variable, Description (name and units)
  - Value (measurement value)
  - Sign (if values are below detection limit, a < sign)
  - Flag (1 = sample taken at buoy; 2 = shore sample when buoy visit not possible)

## Sampling regime and collection methods
- Fortnightly sampling regime as part of a long-term program.
- Sampling locations: buoy at deepest part of Derwent Water; if buoy visit not possible, shore sampling used.
- Water samples integrated from 0–5 m depth.

## Quality control and data handling
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double entered and visually checked.
- Missing data attributed to weather conditions or staff shortages.

## Data structure and metadata
- Data organized in CSV with clear variable definitions and units.
- Flags indicate sampling conditions (Flag 1 buoy, Flag 2 shore).

## Usage, provenance and publications
- Example publications citing the dataset:
  - Winfield, I.J., Fletcher, J.M., & James, J.B. (2017). Reappearance of vendace in Bassenthwaite Lake. Fundamental and Applied Limnology.
  - Woolway et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society.
- Overview context: long-term ecological data contributing to ecological informatics and knowledge generation from English Lake District datasets.

## Data accessibility and governance notes
- Dataset represents long-term monitoring with funding-driven cessation in 2019; data end at 2018.
- Data are intended for download and reuse, with raw data and explicit notes on lack of QC at this stage.
- For Data Stewards: ensure metadata captures sampling methods, depth integration, detection-limit handling, and flag meanings; plan for ongoing QC, calibration, and interoperability with similar lake datasets; document provenance and data lineage to support discoverability and reuse.