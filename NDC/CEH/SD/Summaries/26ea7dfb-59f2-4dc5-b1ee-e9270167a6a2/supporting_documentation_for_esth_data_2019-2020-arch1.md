# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019 2020

## Overview
- Part of an ongoing long-term monitoring dataset at Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling from January 2019 to the end of 2020.

## Data included
- Variables and units:
  - TEMP: surface temperature, in degrees Celsius
  - OXYG: surface oxygen saturation, in % air-saturation
  - SECC: Secchi depth, in metres
  - ALKA: alkalinity, in µg per litre as CaCO3
  - pH: acidity/basicity
  - NH4N: ammonium, in µg N per litre
  - NO3N: nitrate, in µg N per litre
  - PO4P: soluble reactive phosphate, in µg P per litre
  - TOTP: total phosphorus, in µg P per litre
  - SIO2: dissolved reactive silicon, in µg SiO2 per litre
  - TOCA: phytoplankton chlorophyll a, in µg per litre
- Sample integration and location:
  - Integrated from 0 to 5 m; measurements from a boat at a buoy location (Latitude 54.364, Longitude -2.988), at the deepest part of the lake.
  - If buoy visit not possible, samples taken from the shore along with surface measurements (Flag 2).

## Sampling regime
- Measurements collected fortnightly at Esthwaite Water from January 2019 through 2020.
- All data downloaded as a CSV with structured columns.

## Data structure
- Columns include: Date, Variable, Value, Sign (if <LOD), Flag.
- Variables listed per row (e.g., TEMP, OXYG, SECC, ALKA, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
- Sign indicates below detection limit with a "<" sign where applicable.
- Flag: 1 = sample taken at buoy on the lake; 2 = shore sample (buoy visit not possible).

## Data quality and limitations
- Data are raw and not yet quality controlled or calibrated.
- Double-entered and visually checked; missing data due to weather, lake access restrictions, Covid-19, or staff shortages.

## Geographic and methodological notes
- Sampling location and depth details provided; water samples collected from 0–5 m when possible.
- When access to buoy was blocked, shore samples were used instead.

## Data availability and access
- Data are available to download as a CSV in the described format.
- Quality control and calibration planned as part of ongoing validation.

## Funding and support
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE, delivering National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK, delivering National Capability).