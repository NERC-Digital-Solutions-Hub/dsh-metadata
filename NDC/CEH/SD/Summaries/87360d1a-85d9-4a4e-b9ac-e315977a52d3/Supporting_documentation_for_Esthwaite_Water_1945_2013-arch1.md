# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Overview
- Long-term monitoring dataset from Esthwaite Water, Cumbria, England, covering 1945–2013 (some variables back to 1945).
- Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH (PH), ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sampling frequency ranges from weekly to fortnightly; water samples are integrated from 0–5 m and collected at the deepest part of the lake from a buoy (or from shore if buoy visits were not possible).
- Data originally collected by the Freshwater Biological Association, later by CEH and its predecessor Institute of Freshwater Ecology.

## Sampling regime and collection methods
- Data delivered as a comma-separated values (CSV) file with columns:
  - sdate: measurement date
  - variable/Description: listed variables and their descriptions
  - value: measured values for each variable
  - sign_if_LT_LOD: indicates values below detection limit with a "<" sign
  - flag: 1 = sample taken at buoy location, 2 = sample taken from shore when buoy visit was not possible
- Water samples represent integrated measurements from the 0–5 m layer when possible.

## Data structure and variables
- Variables and units:
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - PH: pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Data note: values below detection limits are flagged; samples may come from shore if buoy access was not possible.

## Quality control and caveats
- Data are raw and not quality controlled or calibrated (except for double entries from 2005 onwards).
- Visual checks have been performed.
- Some samples are from shore rather than the buoy location.
- Users may need to perform quality control, calibration, and consistency checks before analysis or model development.

## Data usage and interpretation
- Suitable for long-term time-series analyses, multi-variable correlations, and ecological modelling (e.g., nutrient dynamics, phytoplankton responses, and water quality trends).
- Rich multi-parameter dataset enables exploration of interactions among temperature, oxygen, nutrients, chemistry, clarity, and chlorophyll over several decades.
- Be mindful of methodological shifts (buoy vs. shore sampling) and detection-limit indicators when interpreting trends.

## Related publications and usage
- Examples of studies utilizing this dataset include:
  - Nutrients exerting strong control on diatom communities in Esthwaite Water (Dong et al., Freshwater Biology, 2012)
  - Seasonal sensitivity of Cyanobacteria and phytoplankton to flushing rate and temperature (Elliott, Global Change Biology, 2010)
  - Spring phytoplankton phenology across lakes in the same region (Feuchtmayr et al., Freshwater Biology, 2012)
  - Catchment productivity controls CO2 emissions from lakes (Maberly et al., Nature Climate Change, 2013)
  - Coupling of carbon and silicon cycles in rivers and lakes (Wang et al., Scientific Reports, 2016)
  - Lake surface temperatures in State of the Climate 2015 (Woolway et al., Bulletin of the AMS, 2016)
- Demonstrates applicability for cross-study synthesis and climate-related aquatic ecosystem research.

## Access and provenance
- Dataset comprises raw measurements intended for download and subsequent analysis/quality assurance by investigators.
- Collected primarily at the deepest part of Esthwaite Water (buoy) with occasional shore samples when buoy sampling was not possible.
- Data span from 1945 to 2013, with multiple variables available in a single CSV structure for integrated analysis.