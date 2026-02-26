# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2019 to 2020

## Overview
- Long-term monitoring dataset comprising surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a.
- Fortnightly sampling at Blelham Tarn, Cumbria, England.
- Timeframe: January 2019 to end of 2020.
- Parameters collected include temperature, oxygen saturation, Secchi depth, alkalinity, pH, nutrients (ammonium, nitrate, phosphate, total phosphorus, dissolved silica) and phytoplankton chlorophyll a.
- Data are prepared for downstream analyses and reporting, with raw data intended for subsequent quality control and calibration.

## Sampling regime and collection methods
- Sampling frequency: fortnightly.
- Location and method: measurements collected from a boat at a marked buoy at the deepest part of the lake; if the buoy could not be accessed, samples collected from the shore.
- Integrated water sample: collected from 0 to 5 m.
- Measured parameters and units:
  - Surface temperature (TEMP) in degrees Celsius
  - Surface oxygen saturation (OXYG) in % air-saturation
  - Secchi depth (SECC) in metres
  - Alkalinity (ALKA) in µg CaCO3 per litre
  - pH
  - Ammonium (NH4N) in µg N per litre
  - Nitrate (NO3N) in µg N per litre
  - Soluble reactive phosphate (PO4P) in µg P per litre
  - Total phosphorus (TOTP) in µg P per litre
  - Dissolved reactive silicon (SIO2) in µg per litre
  - Phytoplankton chlorophyll a (TOCA) in µg per litre

## Quality control and data handling
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double entered and visually checked.
- Missing data are attributed to weather, COVID-19 restrictions, or staff shortages.

## Data structure (CSV)
- Date, Description = Date of measurement
- Variable, Description = Variable name and description (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA with their units)
- Value, Description = Values for each variable
- Sign (if<LOD), Description = Indicates if values are below detection limit with a "<" sign
- Flag, Description = 
  - Flag = 1: sample taken at the lake buoy location
  - Flag = 2: sample taken from shore because buoy visit was not possible

## Data availability and limitations
- Data cover January 2019 to end of 2020 and are available as a CSV with the specified structure.
- Raw data status means users should apply quality control and calibration before formal analysis.
- Some entries may be flagged due to sampling deviations (shore vs buoy) or detection limits.

## Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.