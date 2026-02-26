# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Bassenthwaite Lake 2014 to 2018

## Overview
- Long-term, fortnightly monitoring dataset from Bassenthwaite Lake (Cumbria, England) covering 2014–2018.
- Focuses on surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.

## Variables and units
- Temperature (TEMP): degree Celsius
- Surface oxygen saturation (OXYG): % air-saturation
- Secchi depth (SECC): metres
- Alkalinity (ALKA): µg CaCO3 per litre
- pH: unitless
- Ammonium (NH4N): µg N per litre
- Nitrate (NO3N): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre

## Sampling regime and collection methods
- Sampling regime: fortnightly, 0–5 m integrated water samples.
- Location: at a marked buoy at the deepest part of the lake; when visiting the buoy was not possible, samples were taken from the shore.
- Sampling notes: water samples sometimes collected from shore (Flag 2); when at buoy, Flag 1 indicates buoy sampling.
- Timeframe: data from January 2014 to end of 2018; long-term monitoring ended early 2019 due to funding.

## Data structure and labeling
- Data format: comma-separated values (CSV).
- Columns:
  - Date: date of measurement
  - Variable, Description: the measured parameter (as listed above)
  - Value, Description: measured value
  - Sign (if<LOD), Description: whether the value is below the detection limit (a < sign)
  - Flag, Description: 1 = sample taken at buoy location; 2 = shore sample

## Quality control and limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Double entered and visually checked; some missing data due to weather or staff shortages.
- Below-detection values indicated with a < sign; interpretation requires attention to Sign and Flag.

## Time span, access and provenance
- Coverage: January 2014 through December 2018.
- Access: data available for download as CSV.
- Provenance: part of ongoing lake monitoring; referenced in multiple publications.

## GIS considerations and usage
- Suitable for map-based visualization of temporal and spatial trends (buoy vs. shore samples).
- Handle raw data carefully: account for LOD signals and flags to distinguish sampling location.
- Unit consistency and data cleaning recommended before integration with other datasets.

## Publications and references
- Wang, B. et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports 6:35832.
- Winfield, I.J., Fletcher, J.M. & James, J.B. (2017). The 'reappearance' of vendace in Bassenthwaite Lake. Fundamental and Applied Limnology 189:227–233.
- Woolway, R.I. et al. (2016). Lake surface temperatures. Bulletin of the American Meteorological Society, 97(8), S17–S18.
- Maberly, S.C. et al. (2017). From Ecological Informatics to Ecological Knowledge: Long-Term Research in the English Lake District. Ecological Informatics,  pp. 455–482.