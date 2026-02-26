# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2014 to 2018

## Overview
- A long-term, fortnightly monitoring dataset from the South Basin of Windermere, Cumbria, England, covering 2014–2018.
- Variables include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg L−1), phytoplankton chlorophyll a (TOCA, µg L−1).
- Sampled from 0–7 m depth at a marked buoy location in the deepest part of the lake; measurements taken from a boat.
- Data available as raw, uncalibrated values with a note that some values are below detection limits.

## Sampling regime and methods
- Fortnightly sampling regime as part of an ongoing monitoring effort.
- Measurements collected from a boat at a fixed buoy in the deepest part of South Basin Windermere.
- Timeframe for available data: January 2014 – end of 2018.
- Detection limit handling indicated by a "<" sign in the data where applicable.

## Data structure and content
- Data delivered as comma-separated values (CSV).
- Columns:
  - Date: measurement date.
  - Description (Variable): the variable name (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA) with a description.
  - Value: measured value for each variable.
  - Sign (if<LOD): indicator for values below detection limit (<).
- Variables and units clearly specified in the data description.

## Data quality and limitations
- The dataset comprises raw data that have not yet been quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data are attributed to weather conditions or staff shortages.
- Users should apply appropriate quality control and calibration steps if integrating with other datasets or for trend analyses.

## Access, usage, and potential outputs
- Data are suitable for time-series analysis, trend detection, and exploratory data products (e.g., dashboards, pivot-like summaries).
- Potential to create self-serve data explorations and visualizations for end users, with guidance on interpretation and tool usage.

## Funding and provenance
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1, part of the UK-SCaPE programme delivering National Capability.
- Dataset has supported or been used in recent publications (examples cited include climate state reporting and lake ecology studies).

## Practical notes for data support
- Consider implementing a formal quality-control pipeline (calibration, QA/QC checks, documentation of LODs, and units).
- Develop metadata and data provenance records to accompany the CSV (sampling date, location specifics, equipment, and methods).
- Create data products (e.g., time-series dashboards, summary statistics by year/season, and anomaly detection) to facilitate wider reuse and knowledge transfer.