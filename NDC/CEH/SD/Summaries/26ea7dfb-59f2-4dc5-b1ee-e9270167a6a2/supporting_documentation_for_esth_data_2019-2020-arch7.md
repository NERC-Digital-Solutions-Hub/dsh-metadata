# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019  2020

## Overview
- Ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling conducted from January 2019 to the end of 2020.
- Measures cover physical, chemical, and biological water quality indicators.

## What is included
- Surface temperature (TEMP) in degrees Celsius.
- Surface oxygen saturation (OXYG) in % air-saturation.
- Secchi depth (SECC) in metres (water clarity).
- Alkalinity (ALKA) in µg per litre as CaCO3.
- pH.
- Ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2) in µg per litre.
- Phytoplankton chlorophyll a (TOCA) in µg per litre.

## Sampling regime and location
- Fortnightly sampling from a boat at the buoy location (Latitude 54.364, Longitude -2.988) at the lake’s deepest point.
- When buoy access was not possible, samples collected from the shore; water samples were not integrated in these cases.
- 0–5 m integrated water samples where possible.
- All data cover January 2019 through end of 2020.

## Data collection and quality control
- Data provided as raw (not yet quality controlled or calibrated).
- Double entered and visually checked.
- Missing data attributed to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.

## Data structure and format
- Data delivered in a comma-separated values (CSV) file.
- Columns include:
  - Date (measurement date) and Description.
  - Variable descriptors for TEMP, OXYG, SECC, ALKA, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA.
  - Value for each variable.
  - Sign (if below detection limit, indicated with a "<" sign).
  - Flag indicating sampling location (Flag = 1 for buoy, Flag = 2 for shore).

## Temporal and spatial coverage
- Temporal: January 2019 – December 2020.
- Spatial: Esthwaite Water (buoy location with occasional shore sampling when buoy access was unavailable).

## Access, usage, and limitations
- Data available for download as a CSV file.
- Note: values are raw; users should account for lack of QA/calibration before GIS integration or analyses.
- Sampling is at a single primary site (buoy) with occasional shore samples; may affect spatial representativeness for lake-wide analyses.

## Funding and acknowledgments
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE, National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK, National Capability).