# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2014 to 2018

## Overview
- Long-term fortnightly monitoring dataset spanning January 2014 to end of 2018.
- Location: Blelham Tarn, Cumbria, England.
- Variables included: 
  - Temperature (TEMP, °C)
  - Surface oxygen saturation (OXYG, % air-saturation)
  - Secchi depth (SECC, m)
  - Alkalinity (ALKA, µg CaCO3 per L)
  - pH
  - Ammonium (NH4N, µg N per L)
  - Nitrate (NO3N, µg N per L)
  - Soluble reactive phosphate (PO4P, µg P per L)
  - Total phosphorus (TOTP, µg P per L)
  - Dissolved reactive silicon (SIO2, µg per L)
  - Phytoplankton chlorophyll a (TOCA, µg per L)

## Sampling regime and collection methods
- Water samples integrated from 0 to 5 m depth.
- Measurements taken from a boat at a marked buoy; when not possible, samples collected from shore (Flag 2).
- Fortnightly sampling frequency.
- Data provided as raw measurements (not yet quality controlled/calibrated).

## Data structure and format
- Data delivered as a comma-separated values (CSV) file with columns:
  - Date: measurement date
  - Variable: measurement type (e.g., TEMP, OXYG, SECC, etc.)
  - Value: measured value
  - Sign: indicates if value is below detection limit (<LOD)
  - Flag: 1 = buoy location; 2 = shore sampling

## Quality control and limitations
- Raw data have not been quality controlled or calibrated yet.
- Data double entered and visually checked.
- Missing data due to weather conditions or staff shortages.
- Some samples collected on shore when buoy access was not possible (Flag 2).

## Access and usage notes
- Dataset is downloadable as a CSV file.
- designed for integration with other data and for building self-serve data products (dashboards, reports).
- Time series continuity is part of an ongoing long-term monitoring program.

## Funding and example uses
- Funding: Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme.
- Example publications utilizing the dataset:
  - Gray et al. (2019) Modelling lake cyanobacterial blooms: Freshwater Biology
  - Wang et al. (2016) Scientific Reports
  - Woolway et al. (2016) Bulletin of the American Meteorological Society
- Overview reference: Maberly et al. (2017) Ecological Informatics (long-term ecological data in English Lake District).