# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018

## Overview
- Long-term monitoring dataset from Grasmere, Cumbria (England) with fortnightly sampling from January 2014 to March 2018.
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg SiO2 per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Sampling depth: integrated 0–5 m water column.
- Data are downloadable as CSV files and include metadata within the dataset description.

## Sampling regime and collection methods
- Sampling conducted from a boat at the lake’s marked deepest-location buoy; when inaccessible, sampling from the shore.
- Water samples are taken from 0–5 m; measurements include temperature, oxygen, and water chemistry variables.
- In some instances, visits to the buoy were not possible, and samples were taken from shore (Flag 2).
- End of long-term monitoring occurred in March 2018 due to funding shortages.

## Data quality and limitations
- The dataset provided is raw and has not yet undergone quality control or calibration.
- Data have been double-entered and visually checked; missing data primarily due to weather or staff shortages.
- Values below detection limits are indicated with a < sign in the corresponding “Sign (if<LOD)” column.

## Data structure and metadata
- Data delivered as comma-separated values (CSV) with the following columns:
  - Date: measurement date
  - Variable: name of the measured parameter (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value
  - Sign (if<LOD): indicates below detection limit with a < symbol
  - Flag: 1 = buoy at marked location; 2 = shore sampling when buoy visit was not possible
- Units and descriptions for each variable are provided (e.g., TEMP in °C, OXYG in % air-saturation, SECC in m, ALKA in µg CaCO3 per L, etc.).

## Data availability and end of monitoring
- The dataset is part of an ongoing long-term monitoring program but the Grasmere monitoring ended in March 2018 due to funding constraints.
- Data and publications have used this dataset to inform ecological and geochemical analyses and to illustrate long-term lake dynamics.

## Example publications and use
- Wang, B. et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
- Woolway, R.I. et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society.
- Maberly, S.C. et al. (2017). From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District. Ecological Informatics.

## Relevance for monitoring framework authors
- Demonstrates practical data types and units for lake monitoring across multiple environmental dimensions (physical, chemical, and biological).
- Illustrates sampling protocols and potential deviations (buoy vs shore) and depth-integrated sampling considerations.
- Highlights data governance aspects: raw data availability, metadata definitions, and the need for quality control before formal use.
- Emphasizes common challenges in monitoring frameworks: data gaps due to funding, the importance of clear data structure (variables, units, detection limits, and flags), and documentation to facilitate reuse and integration into policy-relevant assessments.