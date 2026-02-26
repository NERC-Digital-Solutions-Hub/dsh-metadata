# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

## Overview
- Long-term monitoring dataset from Grasmere, Cumbria, England (1968–2013) collecting:
  - Surface temperature (TEMP, °C)
  - Surface oxygen saturation (OXYG, % air-saturation)
  - Secchi depth (SECC, m)
  - Alkalinity (ALKA, µg CaCO3 per L)
  - pH (PH)
  - Ammonium (NH4N, µg N per L)
  - Nitrate (NO3N, µg N per L)
  - Soluble reactive phosphate (PO4P, µg P per L)
  - Total phosphorus (TOTP, µg P per L)
  - Dissolved reactive silicon (SIO2, µg per L)
  - Phytoplankton chlorophyll a (TOCA, µg per L)
- Data collected weekly to fortnightly; initial collection by Freshwater Biological Association, later by CEH and predecessors.
- Water samples are integrated from 0–5 m; collected from a buoy at the deepest part of the lake or from shore when buoy sampling wasn’t possible.

## Sampling regime and collection methods
- Sampling period: June 1968 – end of 2013.
- Sampling locations:
  - Primary: boat at buoy at deepest part of Grasmere.
  - Alternative: shore sampling when buoy sampling wasn’t possible (Flag 2).
- Measurements cover multiple water quality and phytoplankton variables using standard lake-water sampling practices.
- Data include a field flag indicating sampling site (Flag 1 = buoy, Flag 2 = shore).

## Data quality and limitations
- Raw data not yet quality controlled or calibrated (except for double entries from 2005 onward); visually checked.
- Detection limits are indicated via sign_if_LT_LOD (< sign when below detection limit).
- Values below detection limit and sampling location flags are explicitly recorded, which affects downstream cleaning/QA for GIS use.

## Data structure and access
- Format: comma-separated values (CSV).
- Key columns:
  - sdate: date of measurement
  - variable/Description: variable type (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value/Description: measured value
  - sign_if_LT_LOD/Description: indicates below detection limit with a "<" sign
  - flag/Description: sampling location flag (1 = buoy, 2 = shore)
- Each row corresponds to a single measurement for a given variable at a given date.

## GIS considerations and guidance
- Spatial scope: single lake with temporal sampling; use for time-series analysis and lake-wide condition mapping rather than multi-site spatial comparisons.
- Preferred use:
  - Combine multiple variables to create lake health or water-quality maps over time.
  - Use the flag field to separate buoy-based samples from shore samples in spatial analyses or quality assessments.
  - Account for 0–5 m integrated sampling when modeling depth-related variability; consider additional depth-specific datasets if available.
- Data preparation:
  - Calibrate or QC raw data if a higher assurance dataset is required (noted as raw here).
  - Handle <LOD values using sign_if_LT_LOD metadata during analysis.
  - Ensure consistent units across variables (e.g., µg N/L for nitrogen species, µg P/L for phosphorus, °C for temperature, m for depth-related measures).
- Potential enhancements:
  - Integrate with other Grasmere datasets or lake basins to enable comparative GIS analyses.
  - Create time-enabled layers/maps to visualize trends and anomalies across 1968–2013.

## Notable publications and usage
- Maberly et al. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change.
- Reynolds et al. (2012). Forty years of monitoring water quality in Grasmere: enrichment and hydrological effects on phytoplankton ecology. Freshwater Biology.
- Wang et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
- Woolway et al. (2016). Lake surface temperatures (State of the Climate in 2015). Bulletin of the American Meteorological Society.