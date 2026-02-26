# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Overview
- Long-term monitoring dataset (1945–2013) from Esthwaite Water, Cumbria, England.
- Variables tracked: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Collected to support environmental health assessment and policy performance over time.

## Sampling regime and collection methods
- Sampling frequency: weekly to fortnightly, from April 1945 to 2013.
- Water samples integrated from 0–5 m depth.
- Collected from the deepest lake location at a buoy by boat; shore samples used when buoy access was not possible.
- Historical collection by Freshwater Biological Association; since 1989, CEH and its predecessors.

## Data structure and variables
- Data provided as a comma-separated values (CSV) file.
- Columns include:
  - sdate: measurement date
  - variable/Description: variable name and description (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: measured value
  - sign_if_LT_LOD: indicates values below detection limit with a "<"
  - flag: 1 = buoy location, 2 = shore sampling
- Units:
  - TEMP: °C
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 L−1
  - PH: pH
  - NH4N, NO3N, PO4P, TOTP, SIO2, TOCA: µg L−1 (phytoplankton chlorophyll a in TOCA)

## Quality control and data handling
- Data are raw and not quality controlled or calibrated (except double entries from 2005 onward); visually checked.
- Flag 2 denotes shore-sampling when buoy access was not possible.
- Below-detection-limit values marked with a "<" sign in sign_if_LT_LOD.
- Analysts can apply standardised QC/calibration steps before use in trend analyses.

## Data usage and publications
- Dataset has informed multiple studies on lake ecology and biogeochemistry, including:
  - 2012: Nutrients exert stronger control than climate on recent diatom communities in Esthwaite Water.
  - 2010: Seasonal sensitivity of cyanobacteria and other phytoplankton to flushing rate and temperature.
  - 2012: Spring phytoplankton phenology across lakes within the same climatological region.
  - 2013: Catchment productivity controls CO2 emissions from lakes.
  - 2016: Coupling of carbon and silicon geochemical cycles in rivers and lakes.
  - 2015/2016: Lake surface temperatures in state-of-climate reports.
- Demonstrates long-term data value for monitoring environmental health, nutrient dynamics, and climate-related responses.

## Considerations for monitoring and data stewardship
- The dataset exemplifies standard long-term monitoring with clear metadata on sampling methods and measurement units.
- Value lies in combining this time series with other datasets to enhance insights and policy relevance; underlying data accessibility is important for broader use.
- Caution advised due to absence of full quality control; users should perform calibration/QA appropriate to their analyses and account for sampling method changes (buoy vs shore) over time.