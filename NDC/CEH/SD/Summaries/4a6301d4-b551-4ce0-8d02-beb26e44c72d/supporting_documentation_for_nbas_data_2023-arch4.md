# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023.

## Overview
- Part of an ongoing fortnightly monitoring dataset for Windermere North Basin (Cumbria, England) in 2023.
- Measurements encompass surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a.
- Sampling regime: every two weeks; water sampled from 0 to 7 m depth from a buoy at the deepest part of the lake; if buoy access was not possible, shore samples were collected.

## Data Available
- Variables and units (as downloadable data):
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - pH: (no unit specified)
  - NH4N: total ammoniacal nitrogen, µg N per L
  - TON: total oxidised nitrogen, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon (SiO2), µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
- Data structure: includes an indicator for values below detection (Sign column) and a sampling location flag (Flag: 1 for buoy, 2 for shore).

## Sampling Regime
- Fortnightly sampling throughout 2023.
- Samples based on an integrated water sample from 0–7 m depth; when buoy sampling was not possible, shore sampling was used.

## Data Quality and Uncertainty
- Data are raw and have not yet undergone full quality control and calibration.
- Selected variables (TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA) have been double-entered and visually validated by a database manager.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- Some UKAS accreditation is noted for particular chemical analyses (NH4N and TON).

## Data Structure and Access
- Data provided as a comma-separated values (CSV) file with:
  - sdate: measurement date
  - Variable, Description: the measured parameter and its description
  - Value: measured value
  - Sign(if<LOD): indicator if value is below detection limit
  - Flag: 1 = buoy sampling location; 2 = shore sampling
- Metadata covers sampling method, depth integration, and data processing status.

## Measurement Methods
- Temperature and dissolved oxygen: measured with YSI ProODO handheld instrument; DO% calibrated daily; oxygen saturation calculated from Mortimer (1981).
- Secchi depth: measured using a Secchi disk on a labelled rope.
- Alkalinity and pH: integrated water sample sealed to prevent exchange; Gran titration with a radiometer electrode; electrode calibration before each sampling.
- NH4N and TON: colorimetric analysis via SEAL AQ2 after filtration; calibration and QA procedures with control standards; UKAS accredited.
- TP: digestion with potassium persulphate, followed by molybdenum blue colorimetric analysis; UV-Vis spectrophotometry.
- SIO2: colorimetric silicon measurement after filtration; silicomolybdenum blue complex formation; calibrations at multiple concentrations.
- TOCA: filtration, methanol extraction, spectrophotometric analysis.
- QA/QC: routine calibrations, blanks, and reference materials used to ensure accuracy; selected analyses have UKAS accreditation.

## Limitations and Data Gaps
- 2023 dataset; potential gaps due to weather, access, or equipment constraints.
- Data provided as raw; users should plan for quality control and potential re-validation.

## Funding and Acknowledgments
- Data collection supported by Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE National Capability.
- Data validation supported by NERC through UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).

## References
- Mackereth, F.J.H. et al. (1978) Water Analysis: Some Revised Methods for Limnologists.
- Mortimer, C.H. (1981) Oxygen content of air-saturated fresh waters.
- Talling, J.F. (1974) In standing waters. Manual on Methods for Measuring Primary Production in Aquatic Ecosystems.