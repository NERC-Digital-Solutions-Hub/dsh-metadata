# Supporting Document

## Overview
- Ongoing long-term monitoring dataset for Grasmere, Cumbria, England.
- Fortnightly sampling from January 2014 to end of March 2018.
- Variables measured: surface temperature (TEMP, °C); surface oxygen saturation (OXYG, % air-saturation); Secchi depth (SECC, m); alkalinity (ALKA, µg CaCO3 per L); pH; ammonium (NH4N, µg N per L); nitrate (NO3N, µg N per L); soluble reactive phosphate (PO4P, µg P per L); total phosphorus (TOTP, µg P per L); dissolved reactive silicon (SIO2, µg per L); phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples integrated from 0 to 5 m; collected from boat at the deepest part near a buoy, or from the shore if buoy visit was not possible.
- Data are raw and not quality controlled/calibrated; double-entered and visually checked.
- Long-term monitoring ended in March 2018 due to funding shortages.

## Sampling regime and collection methods
- Fortnightly sampling cadence.
- Water samples integrated for 0–5 m depth; collected from the buoyed location when possible.
- When buoy access wasn't possible, samples were taken from the shore alongside surface temperature and oxygen measurements.
- Timeframe: January 2014 – end of March 2018.

## Variables, units and data descriptions
- TEMP: surface temperature, °C.
- OXYG: surface oxygen saturation, % air-saturation.
- SECC: Secchi depth, m.
- ALKA: alkalinity, µg CaCO3 per L.
- pH: dimensionless pH value.
- NH4N: ammonium, µg N per L.
- NO3N: nitrate, µg N per L.
- PO4P: soluble reactive phosphate, µg P per L.
- TOTP: total phosphorus, µg P per L.
- SIO2: dissolved reactive silicon, µg per L.
- TOCA: phytoplankton chlorophyll a, µg per L.
- Note: water chemistry values below detection limit are marked with a "<" in the Sign field.

## Data structure and flags
- Data delivered as CSV with columns: Date, Variable (description of the measurement), Value, Sign (if < LOD), Flag.
- Sign indicates values below detection limit (uses "<" sign).
- Flag meanings: 1 = sample collected at the lake buoy location; 2 = sample collected from the shore because buoy visit was not possible.

## Data quality and limitations
- Data are raw and have not been quality controlled or calibrated.
- Visual double-entry checks performed; some data missing due to weather or staff shortages.

## Access and usage notes
- Dataset available for download as CSV; suitable for monitoring analyses and long-term trend assessment using standardised approaches.
- Provides a transparent basis for environmental health and policy performance assessments over time, with explicit metadata on sampling, units, and data flags.

## Example uses and references
- Example publications where this dataset has been used include:
  - Wang et al. (2016) Scientific Reports – Coupling of carbon and silicon geochemical cycles in rivers and lakes.
  - Woolway et al. (2016) Bulletin of the American Meteorological Society – Lake surface temperatures.
- Overview reference: Maberly et al. (2017) on long-term ecological research in the English Lake District.