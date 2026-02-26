# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 2014 to 2018

## Overview
- Ongoing long-term monitoring dataset from the North Basin of Windermere, Cumbria, England.
- Fortnightly sampling conducted from January 2014 to end of 2018.
- Measured variables include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples are integrated from 0 to 7 m and collected from a boat at the deepest part of the lake (buoy).

## Data and quality control
- The dataset comprises raw data that have not yet been quality controlled and calibrated.
- Data have been double entered and visually checked.
- Missing data are attributed to weather conditions or staff shortages.

## Data structure and content
- Data provided as comma separated values (CSV) with columns:
  - Date: measurement date.
  - Description: variable name (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value: measured value for each variable.
  - Sign (if<LOD): indicator for values below detection limit (a "<" sign).

## Metadata and interpretation
- Values below detection limit flagged with a sign "<" in the Sign (if<LOD) column.
- Measurements are standardised to the 0–7 m depth integration across the sampling regime.

## Data governance, access and limitations
- Data are raw and not yet quality controlled; users should apply QA/QC, calibration and metadata validation as needed for policy or decision-making.
- Metadata completeness may require additional verification with originators; data sharing is part of the dataset’s governance, but can present barriers if metadata are incomplete.
- Data transformation or harmonisation may be required to integrate with other datasets or monitoring frameworks.

## Funding and governance
- Data collection supported by Natural Environment Research Council, award NE/R016429/1, as part of the UK-SCaPE programme delivering National Capability.

## Usage and impact
- Dataset has been used in recent publications to inform climate and ecological research, including:
  - State of the Climate in 2018 (BAMS)
  - Studies on temporal and spatial variation in fish environmental DNA in Windermere
  - Investigations of early warning indicators in long-term ecological data
  - Research on pathogens, climate forcing, and ecosystem dynamics
  - Broader ecological and climate-change assessments across freshwater systems

## Related references
- Overview reference: Maberly et al. 2017 on long-term ecological informatics and knowledge generation from ecological data.