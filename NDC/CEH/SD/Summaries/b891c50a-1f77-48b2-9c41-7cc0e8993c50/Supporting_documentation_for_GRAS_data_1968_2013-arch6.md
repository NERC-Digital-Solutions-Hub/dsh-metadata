# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

## Overview
- Long-term monitoring dataset for Grasmere, Cumbria, England, covering 1968–2013.
- Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Originated with the Freshwater Biological Association; since 1989 collected by CEH and predecessors.

## Sampling regime and collection methods
- Sampling frequency: weekly to fortnightly.
- Depth integration: samples gathered from 0–5 m depth.
- Measurement location: taken from a boat at the deepest part of the lake (buoy). If the buoy was inaccessible, samples were taken from the shore (flagged as visit to buoy not possible).
- Timeframe: June 1968 to end of 2013.

## Data scope and variables
- Variables and units:
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - PH: pH
  - NH4N: ammonium, µg N per L
  - NO3N: nitrate, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon, µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
- Data are provided as a CSV with columns: sdate (measurement date), variable (with description), value, sign_if_LT_LOD (below detection limit indicator), flag (sampling location indicator: 1 buoy, 2 shore).

## Data quality and limitations
- Data status: raw data not quality controlled or calibrated; some double entries exist from 2005 onward.
- Visual checks performed; no formal QC applied to the entire dataset.
- Detection limits indicated where applicable (values below LOD shown with a < sign).
- Occasional non-integrated samples (Flag 2) when buoy sampling was not possible.

## Data structure and access
- File format: comma separated values (CSV).
- Key fields to align when merging with other datasets: date alignment, unit consistency, handling of <LOD values, and Flag indicators for sampling location.

## Documentation and usage context
- Cited in recent publications:
  - Maberly et al. (2013) Nature Climate Change: catchment productivity controls CO2 emissions from lakes.
  - Reynolds et al. (2012) Freshwater Biology: long-term water quality trends and phytoplankton ecology.
  - Wang et al. (2016) Scientific Reports: carbon and silicon geochemical cycles.
  - Woolway et al. (2016) Bulletin of the AMS: lake surface temperatures.
- Suitable for long-term trend analysis, multi-variable relationships, and cross-variable insights related to lake water chemistry and phytoplankton dynamics.

## Practical considerations for data support and analysis
- Prepare for blending across variables with potential missing values and non-uniform sampling intervals.
- Consider separate handling for samples from buoy (Flag 1) versus shore (Flag 2).
- Apply appropriate QC/ calibration steps if integrating with other calibrated datasets.
- When communicating findings, clearly note raw data status and any limitations due to sampling or detection limits.