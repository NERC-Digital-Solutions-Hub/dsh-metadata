# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022

## Overview
- Long-term fortnightly monitoring at Esthwaite Tarn, Cumbria, England, covering surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a for 2021–2022.
- Data types included: TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA.

## Sampling regime
- Sampling frequency: fortnightly.
- Collection location and depth: water samples collected from a buoy at the deepest part of the lake; integrated 0–5 m water column.
- Alternative sampling: when buoy sampling was not possible, samples collected from the shore alongside surface temperature and oxygen measurements.
- Timeframe: January 2021 through the end of 2022.

## Data structure and content
- File format: comma separated values (CSV).
- Columns and meanings:
  - Date: Date of measurement.
  - Variable: The measured parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value: Measured value for each variable (units listed below).
  - Sign(if<LOD): Indicates values below the detection limit with a "<" sign.
  - Flag: Indicates sampling context (Flag = 1 = buoy sample; Flag = 2 = shore sample).
- Units:
  - TEMP: degrees Celsius (°C)
  - OXYG: percent air-saturation (%)
  - SECC: metres (m)
  - ALKA: micrograms per litre as CaCO3 (µg CaCO3 L−1)
  - pH: unitless
  - NH4N: micrograms per litre N (µg N L−1)
  - NO3N: micrograms per litre N (µg N L−1)
  - PO4P: micrograms per litre phosphorus (µg P L−1)
  - TOTP: micrograms per litre phosphorus (µg P L−1)
  - SIO2: micrograms per litre silicon (µg SiO2 L−1)
  - TOCA: micrograms per litre chlorophyll a (µg Chl a L−1)

## Quality control and data integrity
- Status: raw data not yet quality controlled or calibrated.
- Quality checks performed: double entry and visual verification.
- Common data gaps: weather conditions, lake access restrictions, COVID-19 restrictions, staff shortages.

## Data governance and accessibility
- Data are provided for download in CSV format.
- Metadata and data transformation needs are typical challenges prior to use in some monitoring frameworks (e.g., ensuring up-to-date metadata, data provenance, and consistent units).

## Funding and acknowledgments
- Data collection supported by Natural Environment Research Council (NERC) grant NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Data validation supported by NERC grant NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability.