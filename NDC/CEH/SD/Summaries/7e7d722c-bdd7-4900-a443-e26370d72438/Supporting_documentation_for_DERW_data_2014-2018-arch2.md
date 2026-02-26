# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., James, J.B., Keenan, P., Mackay, E.B., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term monitoring dataset for Derwent Water, Cumbria, England, collected from 2014 to 2018 with fortnightly sampling.
- Measured variables include:
  - Surface temperature (TEMP) in °C
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in m
  - Alkalinity (ALKA) in µg CaCO3 per L
  - pH
  - Ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP) in µg L^-1
  - Dissolved reactive silicon (SIO2) in µg L^-1
  - Phytoplankton chlorophyll a (TOCA) in µg L^-1
- Sampling depth: integrated from 0 to 5 m; boat-based at the deepest buoy location; occasional shore samples when buoy access was not possible.
- Data are provided in a CSV format with metadata indicating detection limits and sampling location.

## Sampling regime and collection methods
- Fortnightly sampling as part of an ongoing long-term monitoring program.
- Water samples collected from the deepest part of the lake at a marked buoy; when not possible, samples taken from the shore.
- Timeframe: January 2014 to end of 2018.
- End of long-term monitoring occurred in early 2019 due to funding shortages.

## Data quality and control
- Data presented are raw, not yet quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data primarily due to weather conditions or staff shortages.

## Data structure and content
- Data provided as a comma-separated values (CSV) file with columns:
  - Date: date of measurement
  - Variable, Description: names and units of each measured parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value, Description: measured values
  - Sign (if<LOD), Description: indicates if a value is below the detection limit (a “<” sign)
  - Flag, Description: 1 = sample taken at the buoy location; 2 = shore sample (buoy visit not possible)

## Data usage and key references
- Example publications using the dataset:
  - Winfield, I.J., Fletcher, J.M., & James, J.B. (2017). The 'reappearance' of vendace (Coregonus albula) in the face of multiple stressors in Bassenthwaite Lake, U.K. Fundamental and Applied Limnology, 189, 227-233.
  - Woolway, R.I. et al. (2016). Lake surface temperatures in State of the Climate in 2015. Bulletin of the American Meteorological Society, 97(8), S17-S18.
- Additional context:
  - Maberly, S.C. et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. In Ecological Informatics, pp. 455-482.

## Context for analysts
- This dataset supports trend analyses and assessments of environmental health indicators over time.
- Can be used for comparisons against standards, integration with other datasets, and exploration of phytoplankton dynamics, nutrient chemistry, and physical water quality changes.
- Raw data status highlights the need for subsequent quality control and calibration if used for policy performance monitoring or formal reporting.

## Context and limitations
- Monitoring ended in early 2019; dataset covers 2014–2018, with some 2019-related gaps due to funding.
- Data are raw and uncalibrated, requiring careful QC before formal analyses or reporting.
- Sampling methods and locations (buoy vs shore) are explicitly documented, enabling spatial/temporal sensitivity analyses.