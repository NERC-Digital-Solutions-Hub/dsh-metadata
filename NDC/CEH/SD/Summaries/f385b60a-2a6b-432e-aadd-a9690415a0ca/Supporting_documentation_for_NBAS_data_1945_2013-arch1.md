# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013

## Overview
- Long-term monitoring dataset from the North Basin of Windermere, Cumbria, England, covering 1945–2013 for multiple surface lake metrics.
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), and phytoplankton chlorophyll a (TOCA, µg/L).
- Sampling regime: weekly or fortnightly measurements; surface water samples are integrated from the surface down to a specified depth.
- Depth integration changes over time: 0–5 m (1945–1962), 0–10 m (1962–1964), and 0–7 m (1964 onwards).
- Data origin: originally collected by the Freshwater Biological Association; since 1989 by the CEH and its predecessors.
- Data availability: provided as CSV with clearly defined columns and units; end date of the dataset is 2013.
- Quality control: raw data are not quality controlled (except for double entries from 2005 onwards); visually checked.
- Location and sampling method: measurements taken from a boat at the deepest part of the lake (buoy location).

## Data structure and contents
- CSV format with columns:
  - sdate: date of measurement
  - variable, Description: variable name and description (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value, Description: measured value for each variable
  - sign_if_LT_LOD, Description: indicates values below detection limit with a "<" sign
- Units specified for each variable (as listed above).
- Data cover February 1945 through 2013-12 (end of 2013).

## Access, provenance, and context
- Data provenance: Freshwater Biological Association (initial collection); CEH and predecessors since 1989.
- Dataset end date: 2013.
- Purpose: enables analysis of long-term trends and relationships among temperature, oxygen, nutrients, water chemistry, Secchi depth, and phytoplankton chlorophyll a in Windermere.
- Examples of usage in recent publications are provided in the dataset documentation.

## Quality, limitations, and considerations for analysts
- Data are raw and not yet quality controlled; users may need to apply calibration/quality control procedures for formal analyses.
- Detection limits are indicated with sign_if_LT_LOD for values below detection.
- Depth-integrated sampling means that depth-homogenized water properties reflect integrated conditions over the specified depths, which may affect interpretation for stratified periods.
- Data gaps exist in the 1945–2013 record due to historical collection practices and methodological changes.

## Notable uses and publications (selection)
- Do early warning indicators consistently predict non-linear change in long-term ecological data? (Journal of Applied Ecology, 2016)
- Insights into perch population and community biology from a 70-year Windermere study (Couture & Pyle, 2015)
- Pathogens trigger top-down climate forcing on ecosystem dynamics. Oecologia (2016)
- Predicting the impact of changing nutrient load and temperature on the phytoplankton of England's largest lake, Windermere. Freshwater Biology (2012)
- Various works on phytoplankton phenology, climate change effects, and lake ecosystem dynamics (examples listed in the dataset documentation)