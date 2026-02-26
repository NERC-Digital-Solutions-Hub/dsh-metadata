# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 2014 to 2018.

## Overview
- Long-term fortnightly monitoring dataset from Esthwaite Water, Cumbria, England (2014–2018).
- Measured variables:
  - Surface temperature (TEMP) in °C
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in metres
  - Alkalinity (ALKA) in µg CaCO3 per L
  - pH
  - Ammonium (NH4N) in µg N per L
  - Nitrate (NO3N) in µg N per L
  - Soluble reactive phosphate (PO4P) in µg P per L
  - Total phosphorus (TOTP) in µg P per L
  - Dissolved reactive silicon (SIO2) in µg per L
  - Phytoplankton chlorophyll a (TOCA) in µg per L
- Water samples integrated from 0 to 5 m; measurements collected from a boat at the deepest part of the lake (buoy). If buoy sampling wasn’t possible, near-shore sampling was performed.
- Data provided in CSV format with columns for Date, Variable, Value, Sign (for values below detection limit), and Flag.

## Sampling Regime and Collection Methods
- Fortnightly sampling as part of an ongoing long-term monitoring effort.
- Sampling regime:
  - Primary: integrated 0–5 m water column at the marked buoy location.
  - Alternative when buoy access is unavailable: samples taken close to shore.
- Timeframe: January 2014 through the end of 2018.
- Data describe surface and near-surface measurements collected from a boat.

## Data Structure and Content
- File format: comma separated values (CSV).
- Key columns:
  - Date: date of measurement
  - Variable: measured parameter (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value for each variable
  - Sign (if<LOD): indicates if the value is below the detection limit (a “<” sign)
  - Flag: sampling location indicator
    - Flag = 1: sample collected at the buoy (marked location)
    - Flag = 2: sample collected near shore (buoy sampling not possible)

## Quality Control and Limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Double entered and visually checked.
- Missing data attributed to weather conditions or staff shortages.

## GIS Relevance and Considerations
- Suitable for map-based visualisations and time-series GIS analyses when combined with other spatial data.
- Must consider data heterogeneity (mix of buoy and near-shore samples) and detection-limit signs.
- Spatial representation:
  - Primary sampling point associated with the buoy location (deepest part of the lake); near-shore samples require explicit location handling.
- Data cleaning required prior to mapping (e.g., handling <LOD values, QA/QC calibration).

## Data Access and Funding
- Funding: Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.

## Notable Published Uses
- Pilotto F et al. (2020). Meta-analysis of multidecadal biodiversity trends in Europe. Nature Communications.
- Wang, B. et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
- Woolway, R.I. et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society.
- Maberly et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. Ecological Informatics.