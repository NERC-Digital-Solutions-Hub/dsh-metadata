# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 2014 to 2018

## Overview
- Long-term monitoring dataset with fortnightly sampling at Grasmere, Cumbria, England.
- Variables include surface temperature, oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.
- Time period covered: January 2014 to end of March 2018 (monitoring ended due to funding shortages).

## Sampling regime and collection methods
- Measurements taken from a boat at the marked buoy located at the deepest part of the lake; when unavailable, samples collected from the shore (Flag 2).
- Water samples integrated from 0 to 5 meters.
- If buoy visits were not possible, shore sampling occurred along with surface temperature and oxygen measurements.

## Variables, units and data structure
- TEMP: surface temperature, °C
- OXYG: surface oxygen saturation, % air-saturation
- SECC: Secchi depth, metres
- ALKA: alkalinity, µg CaCO3 per litre
- pH: pH
- NH4N: ammonium, µg N per litre
- NO3N: nitrate, µg N per litre
- PO4P: soluble reactive phosphate, µg P per litre
- TOTP: total phosphorus, µg P per litre
- SIO2: dissolved reactive silicon, µg per litre
- TOCA: phytoplankton chlorophyll a, µg per litre
- Data are provided in CSV format with columns: Date, Variable, Value, Sign (if <LOD), Flag (1 = buoy site, 2 = shore)
- Some values below detection limit are marked with a "<" sign in the Sign column.

## Quality control and data status
- Data are raw and have not been quality controlled or calibrated.
- Double-entered and visually checked.
- Missing data primarily due to weather conditions or staff shortages.

## Temporal scope and data limitations
- Fortnightly sampling cadence with occasional gaps.
- End of long-term monitoring occurred in March 2018 due to funding constraints.
- Some measurements are flagged as shore samples when buoy sampling was not possible.

## Usage notes for GIS specialists
- Suitable for time-enabled map layers by variable (e.g., TEMP, OXYG, SECC, ALKA, pH, nutrients, TOCA).
- Consider metadata that records sampling location (buoy vs shore) and 0–5 m water column integration.
- Account for raw data status: plan for quality control/calibration before formal mapping or analysis.
- Pay attention to detection limits (Sign <LOD) and the presence of any missing data due to external factors.

## References and context
- Example publications list where this dataset has been used.
- Overview reference: Maberly et al. (2017) on long-term ecological information and knowledge generation.