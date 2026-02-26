# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013.

## Overview of the dataset
- Long-term monitoring dataset from the North Basin of Windermere, Cumbria, England, covering 1945–2013 (some variables starting later).
- Weekly or fortnightly measurements for multiple variables: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH (PH), ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Measurements collected from a boat at the deepest part of the lake; sampling depth varies over time: 0–5 m (1945–1962), 0–10 m (1962–1964), and 0–7 m (from 1964 onwards).
- Data managed by the Freshwater Biological Association (FBA) until 1989, then by the Centre for Ecology & Hydrology (CEH) and its predecessor institutes.
- Available as a comma separated values (CSV) file with specific columns.

## Data quality and processing
- The dataset comprises raw data that have not yet been quality controlled or calibrated (except for double entries from 2005 onwards); visual checks have been performed.
- Values below detection limits are indicated with a “<” sign in the sign_if_LT_LOD field.

## Data structure and access
- CSV columns include:
  - sdate, Description (date of measurement)
  - variable, Description (the variable name, e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value, Description (the measured value)
  - sign_if_LT_LOD, Description (indicator of below-detection-limit)
- The dataset is used in recent publications, illustrating its utility for long-term environmental analysis.

## Temporal scope and sampling regime
- Time span: 1945 through 2013.
- Sampling regime: weekly or fortnightly monitoring.
- Depth-integrated sampling from surface to varying depths as noted above.

## Potential uses for environmental monitoring
- Assess long-term trends and health of Windermere’s surface conditions, including temperature, oxygen saturation, water clarity, and nutrient/chemical status.
- Explore relationships between physical/chemical variables and phytoplankton chlorophyll a dynamics.
- Support cross-study comparisons and historical baseline assessments for lake management and climate change research.
- Serve as a data source for methodological studies, such as early-warning indicators for ecological change and climate-related ecological responses.

## Provisions for data integration and accessibility
- The dataset has been employed in multiple environmental research publications, highlighting its value when combined with other datasets.
- An ongoing challenge and opportunity for analysts: increase dataset value by integrating with additional datasets and ensure underlying data accessibility through appropriate portals and data governance practices.