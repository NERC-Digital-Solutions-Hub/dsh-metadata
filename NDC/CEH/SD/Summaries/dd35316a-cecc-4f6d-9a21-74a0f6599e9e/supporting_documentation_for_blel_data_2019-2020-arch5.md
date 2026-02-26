# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2019 to 2020

## Overview
- Part of an ongoing long-term monitoring dataset for Blelham Tarn, Cumbria, England.
- Fortnightly sampling conducted from Jan 2019 to end of 2020.
- Variables included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), phytoplankton chlorophyll a (TOCA).
- Data are provided with specified units (see below) and accompany notes on detection limits.

## Sampling regime and collection methods
- Measurements taken from a boat at a marked location (buoy) at the deepest part of the lake; when unavailable, samples taken from the shore.
- Integrated water samples from 0 to 5 m when possible.
- Data include a flag to indicate whether sampling was at the buoy (Flag = 1) or from the shore due to buoy inaccessibility (Flag = 2).
- Water chemistry values below detection limit are marked with < in the Sign (if<LOD) column.
- Sampling regime intended as consistent, but occasional deviations are noted.

## Quality control and data status
- Data presented are raw and have not yet been quality controlled or calibrated.
- Double entered and visually checked; any missing data attributed to weather, COVID-19 restrictions, or staff shortages.

## Data structure and format
- Data delivered as a comma-separated values (CSV) file.
- Core columns:
  - Date: Date of measurement.
  - Variable/Description: Name and description of each parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value/Description: Numerical values for each variable.
  - Sign (if<LOD)/Description: Indicates if a value is below detection limit.
  - Flag/Description: Indicates sampling location (Flag = 1 buoy; Flag = 2 shore).

## Temporal and geographic coverage
- Temporal coverage: January 2019 through December 2020.
- Geographic scope: Blelham Tarn, Cumbria, England.

## Variables, units, and notes
- TEMP: surface temperature in degrees Celsius.
- OXYG: surface oxygen saturation in % air-saturation.
- SECC: Secchi depth in metres.
- ALKA: alkalinity in µg CaCO3 per litre.
- pH: unitless measure of acidity/alkalinity.
- NH4N: ammonium in µg N per litre.
- NO3N: nitrate in µg N per litre.
- PO4P: soluble reactive phosphate in µg P per litre.
- TOTP: total phosphorus in µg P per litre.
- SIO2: dissolved reactive silicon in µg per litre.
- TOCA: phytoplankton chlorophyll a in µg per litre.

## Data access and governance considerations
- Data are available to download (location and portal unspecified in the document).
- Data are raw and require quality control and calibration before broader dissemination.
- Documentation includes definitions, units, detection-limit handling, and sampling conditions to support reuse.

## Funding and support
- Data collection supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.