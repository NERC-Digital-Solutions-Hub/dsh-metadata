# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023.

## Overview
- Part of an ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling in 2023; measured variables: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, NH4N, TON, PO4P, TOTP, SIO2, and phytoplankton chlorophyll a (TOCA).
- Units: TEMP °C; OXYG % air-saturation; SECC m; ALKA µg CaCO3/L; pH (dimensionless); NH4N, TON, PO4P, TOTP, SIO2, TOCA in µg/L.
- Water sampled from 0–5 m; from a buoy at deepest lake location; shore sampling if buoy inaccessible.
- Data are raw and not yet fully quality-controlled/calibrated.

## Data Content and Structure
- Data downloadable as CSV with columns:
  - sdate (measurement date), variable (description of each parameter), value (measurement), sign(if<LOD) (indicates below detection limit), flag (sampling location: 1 buoy, 2 shore).
- 2023 data cover January 2023 through December 2023.
- Variables include TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA.
- Metadata describe measurement context (0–5 m integrated sample; location details).

## Quality Control and Uncertainty
- Raw data presented; not yet quality-controlled/calibrated.
- Some values double-entered by different people and visually validated by a database manager.
- Missing data attributable to weather, equipment limitations, or staff shortages.
- Quality checks include calibration notes for instruments and reference material usage where applicable.

## Measurement Methods (highlights)
- Temperature and DO: measured with YSI ProODO; DO% calibrated daily; biweekly DO% calibration; DO sat calculated from Mortimer (1981).
- Secchi depth: measured with Secchi disk on labeled rope.
- Alkalinity and pH: integrated water sample sealed to prevent exchange; Gran titration with Radiometer GK2401C electrode; electrode calibrated before sampling.
- NH4N and TON: SEAL AQ2 discrete analyser after filtration; colorimetric reactions; UKAS accredited methods; ranges 0–2.0 mg/L for NH4N and TON.
- Total Phosphorus (TP): digestion with K2S2O8 and molybdenum blue colorimetry; UV-Vis measurement; calibration with standards.
- Dissolved reactive silicon (SIO2): colorimetric method (molybdate/ascorbic acid) with measurement at 880 nm; QC samples included.
- Phytoplankton chlorophyll a (TOCA): methanol extraction from filtered sample; spectrophotometric analysis.
- Soluble reactive phosphate (PO4P): filtration and colorimetric molybdenum blue method; blanks and accuracy checks included.

## Data Governance and Context
- Part of UK-SCaPE program; funded by Natural Environment Research Council (NERC) awards NE/R016429/1 and NE/Y006208/1 for validation.
- Methods reference standard limnology sources (Mackereth et al. 1978; Mortimer 1981; Talling 1974).
- Data intended for long-term trend analysis and broader ecosystem understanding.

## Practical Considerations for Data Leaders
- The dataset provides a foundation for monitoring water quality and phytoplankton dynamics but requires calibration and formal QC in future releases.
- Metadata should emphasize detection limits (sign field) and sampling-location flags for clear provenance.
- To enable system-wide data strategy, integrate this dataset with other lake monitoring data, ensure consistent metadata standards, and plan for ongoing data validation workflows.

## Funding and References
- Data collection supported by NERC award NE/R016429/1 (UK-SCaPE).
- Data validation supported by NERC/UKCEH National Capability (NE/Y006208/1).
- Key references: Mackereth et al. (1978); Mortimer (1981); Talling (1974).