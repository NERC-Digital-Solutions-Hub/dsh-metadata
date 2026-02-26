# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2014 to 2018. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Fletcher, J.M., Guyatt, H., Hunt, A.G., James, J.B., Mackay, E.B., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2021)

## Overview
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England (2014–2018).
- Fortnightly sampling of surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data are provided as raw measurements with specific units described below.

## Sampling regime and collection methods
- Water samples collected from a boat at the deepest part of the lake, from a marked buoy location.
- When buoy access wasn't possible, samples taken from the shore along with surface measurements.
- Water samples are integrated from 0 to 5 meters.
- Measurement period spans January 2014 through end of 2018.
- Fortnightly sampling frequency.

## Data columns and units
- Date: Date of measurement.
- Variable, Description: Each parameter and its unit:
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - pH: pH
  - NH4N: ammonium (µg N per L)
  - NO3N: nitrate (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon (µg SiO2 per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)
- Value, Description: numerical measurements for each variable.
- Sign (if<LOD), Description: indicates if a value is below the detection limit (<).
- Flag, Description:
  - Flag = 1: sample taken at the marked buoy location.
  - Flag = 2: sample taken from the shore (buoy visit not possible).

## Quality control and data availability
- Data presented are raw and not yet quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data arise from weather conditions or staff shortages.

## Data structure and accessibility
- Data provided as a comma-separated values (CSV) file.
- Clear schema with Date, Variable/Description, Value/Description, Sign (LOD), and Flag fields.
- Documentation notes handling of detections below limits and sampling locations.

## Funding and related work
- Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.

## Example publications and usage
- 2019: Modelling lake cyanobacterial blooms; climate-driven impacts studied using this dataset.
- 2016: Coupling of carbon and silicon geochemical cycles in rivers and lakes.
- 2016–2017: Lake surface temperatures referenced in broader climate context.
- Overview reference: From Ecological Informatics to the Generation of Ecological Knowledge: Long-Term Research in the English Lake District.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle considerations for a long-term environmental dataset:
  - Comprehensive description of collected variables, units, and measurement methods.
  - Clear data structure with metadata on detection limits and sampling locations.
  - Emphasis on data provenance, including sampling regime and field conditions.
  - Acknowledgement of data quality status and ongoing calibration needs.
  - Documentation of funding sources and links to related research, aiding discoverability and reuse.
- Highlights practical challenges for data systems:
  - Raw data requiring quality control and calibration.
  - Handling of below-detection-limit values and sampling gaps.
  - Need for consistent metadata and standardized data formats to support reuse across studies.