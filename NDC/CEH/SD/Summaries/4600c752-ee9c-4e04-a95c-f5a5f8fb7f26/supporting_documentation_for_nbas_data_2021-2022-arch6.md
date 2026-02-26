# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2021 -2022.

## Overview
- Part of an ongoing fortnightly monitoring dataset for Windermere North Basin (Cumbria, England).
- Variables include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Timeframe: January 2021 to end-2022.
- Data available to download as a CSV, with raw measurements that are not yet quality controlled or calibrated.

## What is included (variables and units)
- Temperature (TEMP): °C
- Surface oxygen saturation (OXYG): % air-saturation
- Secchi depth (SECC): metres
- Alkalinity (ALKA): µg CaCO3 per litre
- pH: unitless
- Ammonium (NH4N): µg N per litre
- Nitrate (NO3N): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg SiO2 per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre

Note: Water samples are integrated from 0 to 7 m; measurements taken from a boat at the deepest part of the lake.

## Sampling regime and collection methods
- Sampling frequency: Fortnightly.
- Location and method: North Basin windermere; measurements collected from a buoy at the deepest lake location, using a boat.
- Data collection supported by NERC programmatic funding as part of UK-SCaPE and ACCESS-UK national capability initiatives.

## Data structure and access
- Format: Comma separated values (CSV) file.
- Columns (described): Date (measurement date); Variable (with a Description summarizing the parameter, e.g., TEMP); Value (numerical measurement); Sign(if<LOD) (indicates if below detection limit, using a "<" sign); each field accompanied by a Description clarifying its meaning.

## Data quality, limitations, and provenance
- Quality status: Raw data not yet quality controlled or calibrated.
- Quality checks: Data have been double entered and visually checked.
- Gaps: Missing data due to weather conditions, COVID-19 restrictions, or staff shortages.
- Data validation: Supported by NERC awards NE/Y006208/1 as part of ACCESS-UK.

## How this supports data users (Data Support perspective)
- Provides a well-documented, self-serve dataset enabling time-series analysis of multiple water quality and phytoplankton indicators.
- Clear unit definitions and measurement details aid cross-dataset integration and methodological transparency.
- Availability of raw data with detection-limit indicators supports careful quality assessment and future calibration workflows.