# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 1990 to 2013

## Overview
- Long-term monitoring dataset from Bassenthwaite Lake, Cumbria, England.
- Fortnightly sampling conducted from August 1990 to end of 2013.
- Data intended for discovery and reuse by researchers, with context on collection methods and limitations.

## Data Content
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
- Data are provided as raw measurements (not quality controlled/calibrated) with some double entries from 2005 onward.
- Values below detection limits are indicated with sign_if_LT_LOD.
- Data are described as integrated water samples from 0–5 m depth; where buoy sampling was not possible, shore samples were taken (Flag 2).

## Sampling regime and collection methods
- Measurements taken from a boat at the deepest part of the lake near a marked buoy; when not possible, samples collected from the shore.
- Sampling regime is long-term and designed to support assessments of lake chemistry, temperature, and phytoplankton indicators.

## Quality Control & Limitations
- Raw data only; no formal quality control or calibration applied (except for duplication checks from 2005 onward).
- Visual checks conducted.
- Notable data gap: March–June 2001 due to foot-and-mouth disease restricting access to the lake.

## Data Structure & File Format
- File format: comma-separated values (CSV).
- Columns include:
  - sdate: date of measurement
  - variable/Description: name and description of the measured variable (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - value: measured value
  - sign_if_LT_LOD: indicator if value is below detection limit (e.g., "<")
  - flag: 1 if sample taken at buoy location; 2 if sample taken from shore
- Data range: August 1990 through 2013.

## Provenance, Gaps & References
- Recent example publications where the dataset has been used include:
  - Bernhardt, Elliott, & Jones (2008)
  - Elliott, Jones, & Page (2009)
  - Elliott & Bell (2011)
  - Jones, Page, Elliott, Thackeray & Heathwaite (2011)
  - Maberly et al. (2013)
  - Meis, Thackeray & Jones (2009)
  - Thackeray, Maberly & Winfield (2006)
  - Winfield et al. (various publications 2006–2017)
  - Woolway et al. (2016)
- Dataset is downloadable and accompanied by metadata describing measurement protocols and units.

## Data Stewardship Considerations
- Maintain consistent metadata standards (variable codes, units, and detection limit indicators).
- Validate and, where possible, quality-check raw data against calibration records; document any calibration or QC steps added.
- Preserve sampling context (buoy vs shore, depth integration) to support correct interpretation and reuse.
- Track and document data gaps (e.g., 2001 interruption) and any future updates or corrections.
- Ensure access to the dataset remains stable and clearly linked to referenced publications for traceability.