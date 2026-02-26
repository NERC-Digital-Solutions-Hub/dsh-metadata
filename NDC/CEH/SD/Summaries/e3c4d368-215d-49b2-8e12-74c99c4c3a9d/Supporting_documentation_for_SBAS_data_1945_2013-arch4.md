# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 1945 to 2013

## Overview
- Long-term monitoring dataset covering surface temperature, surface oxygen, Secchi depth, water chemistry, and phytoplankton chlorophyll a from the South Basin of Windermere, Cumbria, England.
- Time span: measurements from March 1945 to end of 2013; some variables began earlier than others.
- Collected on a weekly or fortnightly schedule; initial collection by the Freshwater Biological Association, then by the Centre for Ecology & Hydrology (CEH) and predecessors since 1989.
- Data intended to support analysis of lake conditions, nutrient dynamics, and phytoplankton responses over decades.

## Data collected
- Variables and units:
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - PH: pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Water sampling depths:
  - 0–5 m (1945–1962)
  - 0–10 m (1962–1964)
  - 0–7 m (1964 onwards)
- Sampling location and method:
  - Measurements taken from a boat at a marked location (buoy) in the deepest part of the lake.
- Data availability:
  - Data provided as comma-separated values (CSV) with columns for date, variable, value, and detection-limit indicator.

## Data quality and structure
- Quality control status:
  - Raw data are provided and have not been quality controlled or calibrated (except double entries from 2005 onwards); visual checks have been performed.
- Data structure:
  - Columns include sdate, variable (description), value, and sign_if_LT_LOD (indicating below-detection-limit values with a < sign).
  - Full variable descriptions accompany the data for clarity.

## Provenance and context
- Data origin and stewardship:
  - Initially collected by the Freshwater Biological Association; since 1989, managed by CEH and its predecessor Institute of Freshwater Ecology.
- Related publications and use cases:
  - Used in a range of ecological and climate-related studies, illustrating long-term ecological change and nutrient/phytoplankton dynamics (examples include assessments of early warning indicators in long-term data and windermere-specific phytoplankton/ecology research).

## Considerations for data leadership and reuse
- Completeness and granularity:
  - Long-running time series with some variables beginning earlier than others; sampling cadence averaged weekly to fortnightly.
- Metadata and discoverability:
  - Clear variable definitions, units, sampling depths, and time range aid discoverability and re-use; data are accompanied by descriptive notes on sample integration depth changes over time.
- Quality and reliability:
  - Raw data status requires careful QC/validation for analytical work; users should account for potential non-uniformities across the 0–5 m to 0–7 m depth transitions and varying detection limits.
- Access and governance:
  - Data stewardship by CEH/heritage institutions suggests clear provenance; suitable for integration into broader lake-monitoring or climate-change studies with attention to temporal continuity and methodological context.