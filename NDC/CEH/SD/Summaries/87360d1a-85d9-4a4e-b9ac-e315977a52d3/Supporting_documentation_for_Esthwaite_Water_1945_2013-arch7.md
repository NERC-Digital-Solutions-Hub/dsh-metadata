# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Overview
- Long-term, lake-wide monitoring dataset from Esthwaite Water, Cumbria, England.
- Variables cover physical, chemical, and biological water properties: surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Time span: data from April 1945 to the end of 2013 (some variables start earlier than others).
- Originally collected by the Freshwater Biological Association; since 1989 managed by CEH and its predecessor.
- Useful for building map-based visualisations and time-series analyses in GIS, and for cross-referencing with other lake datasets.

## Content and variables
- Temperature (TEMP): degrees Celsius.
- Surface oxygen saturation (OXYG): % air-saturation.
- Secchi depth (SECC): metres.
- Alkalinity (ALKA): µg CaCO3 per litre.
- pH (PH): unitless.
- Ammonium (NH4N): µg N per litre.
- Nitrate (NO3N): µg N per litre.
- Soluble reactive phosphate (PO4P): µg P per litre.
- Total phosphorus (TOTP): µg P per litre.
- Dissolved reactive silicon (SIO2): µg SiO2 per litre.
- Phytoplankton chlorophyll a (TOCA): µg per litre.
- Water sampling: integrated 0–5 m depth; samples collected from a buoy at the deepest part of the lake when possible; shore samples used when buoy sampling was not possible (Flag 2).

## Sampling regime and collection methods (GIS considerations)
- Sampling frequency: weekly to fortnightly.
- Historical records from 1945 onward; dataset structure reflects multiple variables with consistent temporal coverage.
- Sampling location data implied (buoy at deepest lake point; some shore samples), enabling spatial mapping of sampling points and shoreline versus open-water samples.

## Data quality and structure
- Quality control: raw data; not yet quality controlled or calibrated (except for double entries from 2005 onward); visually checked.
- Data file format: comma-separated values (CSV).
- Key columns:
  - sdate: measurement date.
  - variable: the measured parameter (with description).
  - value: measurement value.
  - sign_if_LT_LOD: indicates if value is below detection limit (a "<" sign may appear).
  - flag: sampling context (1 = buoy at marked location; 2 = shore sampling when buoy sampling was not possible).

## GIS readiness and usage
- Structure supports time-series GIS visualisations and layered maps by variable and date.
- Ideal for linking to spatial features such as lake basins, sampling buoy locations, and shoreline samples.
- Handling below-detection values: use sign_if_LT_LOD to identify censored data; plan for imputation or exclusion in analyses as appropriate.
- Data are raw; users should apply their own quality-control/standardisation if integrating with other QC’ed datasets.

## Limitations and caveats
- Raw data with minimal QC; potential measurement inconsistencies across decades.
- Sampling context changes (buoy vs shore) may affect comparability across time and space.
- Some variables start earlier than others; not all parameters have identical temporal coverage.
- Calibration status unspecified beyond described checks; cross-dataset harmonisation may be necessary for broad-scale analyses.

## References and usage examples
- Recent publications using the dataset include studies on nutrient controls and phytoplankton dynamics in Esthwaite Water and related lake science (e.g., analyses of nutrient effects, seasonal phytoplankton responses, and links to carbon and silicon cycles).
- Specific cited works include: Dong et al. (2012), Elliott (2010), Feuchtmayr et al. (2012), Maberly et al. (2013), Wang et al. (2016), Woolway et al. (2016).