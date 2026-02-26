# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P., Mackay, E.B., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Part of an ongoing long-term monitoring dataset for Derwent Water, Cumbria, England.
- Fortnightly sampling from 2014 through 2018; data cover January 2014 to end of 2018.
- End of long-term monitoring occurred early 2019 due to funding shortages.
- Variables collected: surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.

## Sampling regime and collection methods
- Water samples collected from integrated 0–5 m depth; measurements based on a marked buoy location at the deepest part of the lake.
- When buoy access was not possible, samples were taken from the shore, alongside surface temperature and oxygen.
- All data are captured in a CSV format with a consistent column structure.

## Data structure and fields
- CSV file with columns:
  - Date: date of measurement
  - Variable/Description: specific variable measured (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA) and a description
  - Value: measured value for each variable
  - Sign (if<LOD): indicates if the value is below the detection limit (a < sign)
  - Flag: indicates sampling location (Flag = 1 = buoy sample; Flag = 2 = shore sample)

## Variables and units
- TEMP: surface temperature, °C
- OXYG: surface oxygen saturation, % air-saturation
- SECC: Secchi depth, metres
- ALKA: alkalinity, µg CaCO3 per litre
- pH: acidity/alkalinity measure (unitless in this context)
- NH4N: ammonium, µg N per litre
- NO3N: nitrate, µg N per litre
- PO4P: soluble reactive phosphate, µg P per litre
- TOTP: total phosphorus, µg P per litre
- SIO2: dissolved reactive silicon, µg per litre
- TOCA: phytoplankton chlorophyll a, µg per litre

## Data quality and status
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data largely attributable to weather conditions or staff shortages.

## Data details and interpretation
- Water samples were taken as a single integrated sample from 0–5 m whenever possible.
- If samples could not be taken at the buoy, shore samples were collected with concurrent surface temperature and oxygen measurements.
- Values below detection limits are annotated with a < sign in the Sign (if<LOD) column.
- Sampling accuracy and comparability may be affected by periods without buoy access or by logistical constraints.

## Data usage and references
- The dataset has been used in various publications, including:
  - Winfield, I.J., Fletcher, J.M., & James, J.B. (2017). The 'reappearance' of vendace (Coregonus albula) in Bassenthwaite Lake under multiple stressors. Fundamental and Applied Limnology, 189, 227-233.
  - Woolway, R.I. et al. (2016). Lake surface temperatures in State of the Climate in 2015. Bulletin of the American Meteorological Society, 97(8), S17-S18.
- An overview reference: Maberly, S.C. et al. (2017). Long-Term Research in the English Lake District. In Ecological Informatics, 455-482.