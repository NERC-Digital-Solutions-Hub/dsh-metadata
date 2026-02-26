# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2019 to 2020.

## Overview
- Fortnightly sampling in the South Basin of Windermere, Cumbria, England, from January 2019 to end of 2020.
- Variables collected: surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Data are provided for map- and analysis-ready visualization in GIS workflows.

## Data contents and schema
- Data format: comma-separated values (CSV).
- Columns:
  - Date: measurement date.
  - Variable, Description: name and unit context for each parameter (see below for units).
  - Value: measured value.
  - Sign (if<LOD): indicator when values are below detection limit.
- Variables and units:
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation in % air-saturation.
  - SECC: Secchi depth in metres.
  - ALKA: alkalinity in µg CaCO3 per litre.
  - pH: pH value.
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.
- Sampling specifics:
  - Water samples integrated from 0 to 7 m depth.
  - Measurements taken from a boat at a buoy located at the deepest part of the lake.

## Quality control and limitations
- Data are raw and have not yet been quality controlled or calibrated.
- Data have been double entered and visually checked.
- Missing data attributed to weather, COVID-19 restrictions, or staff shortages.
- Values below detection limit are flagged in the Sign (if<LOD) column.

## Data collection methods and provenance
- Funding: Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Collection site: South Basin of Windermere.
- Providers/authors: Feuchtmayr et al. (2024).

## Temporal and spatial coverage
- Temporal: January 2019 through December 2020.
- Spatial: measurements taken at a single buoy location in the deepest part of the South Basin, Windermere (no explicit coordinates provided in the dataset).

## GIS usage notes
- Ideal for creating time-series maps and basin-scale visuals by variable, using the Date and Variable fields.
- Since data are at a single sampling point (per date) but cover multiple variables, consider creating a multi-layer time series or joining variables by Date for composite maps.
- Pay attention to LOD flags when integrating values that are below detection limits.
- As raw data, apply appropriate quality control and calibration steps before formal analysis or decision-making.
- If needed, interpolate or integrate with other spatial datasets to generate basin-wide representations, while noting the single-sample-point limitation.

## Access, reproduction, and provenance
- Data format: CSV, with clear variable descriptions and units.
- Source and credits: Feuchtmayr et al. (2024); UK-SCaPE program; NERC funding.