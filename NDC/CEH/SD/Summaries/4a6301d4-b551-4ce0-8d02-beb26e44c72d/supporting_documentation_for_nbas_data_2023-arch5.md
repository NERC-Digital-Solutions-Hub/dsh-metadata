# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023.

## Overview
- Part of an ongoing fortnightly monitoring program in the North Basin of Windermere, Cumbria, England.
- Variables included: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, total ammoniacal nitrogen (NH4N), total oxidised nitrogen (TON), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Water samples integrate from 0 to 7 meters; measured from a buoy at the lake’s deepest part. When buoy access is not possible, shore samples are taken (Flag 2).
- Timeframe for the data: January 2023 to end of 2023.

## Data Content and Scope
- Data downloaded as CSV with the following variables and units:
  - TEMP: degrees Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - ALKA: µg CaCO3 per litre
  - pH: (pH units)
  - NH4N: µg N per litre
  - TON: µg N per litre
  - PO4P: µg P per litre
  - TOTP: µg P per litre
  - SIO2: µg per litre (as SiO2)
  - TOCA: µg per litre
- Data structure includes:
  - sdate: measurement date
  - Variable/Description: the variable measured
  - Value/Description: the measured value
  - Sign(if<LOD): indicates values below detection limit with a "<" symbol
  - Flag: 1 = buoy location, 2 = shore sampling

## Quality Assurance and Limitations
- These are raw data and have not yet been quality controlled or calibrated.
- Some QA performed:
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and visually validated by a database manager.
  - Missing data attributable to weather, equipment limitations, or staff shortages.
- Identified limitations:
  - Raw data status means users should apply their own calibration/ QC where required before analysis or sharing as final datasets.

## Methods and Instrumentation (Summary)
- Temperature and dissolved oxygen:
  - Measured with a YSI ProODO handheld instrument; DO% calibrated daily; Biweekly DO% calibration in water-saturated air and bimonthly in air-saturated water.
- Secchi depth:
  - Measured by lowering a Secchi disk with a measured rope.
- Alkalinity and pH:
  - Integrated water sample sealed to prevent atmospheric exchange; Gran titration with a Radiometer GK2401C electrode; electrode calibrated before each sampling.
- Nitrogen and phosphorus analyses:
  - NH4N: colorimetric analysis with SEAL AQ2 after filtration; calibration and QA checks including reference materials; UKAS-accredited method.
  - TON: colorimetric analysis after reduction of nitrate to nitrite; UKAS-accredited method.
  - TOTP: digestion with potassium persulfate and molybdenum blue colorimetric analysis; UV-Visible spectrophotometry.
  - PO4P: colorimetric analysis (molybdenum blue) after filtration.
- Silicon (SIO2) and Chlorophyll a (TOCA):
  - SIO2: colorimetric with ammonium molybdate and reduction to silicomolybenum blue; calibrated with QC samples.
  - TOCA: pigment extraction from filtered water with methanol, analyzed spectrophotometrically.

## Data Governance and Sharing Considerations for Data Stewards
- The dataset provides a transparent description of variables, units, sampling regime, and data structure, aiding discoverability and reuse.
- Clear indication of raw data status and QA steps helps users assess suitability for their analyses and whether re-calibration or further QC is required.
- Documented methods and calibration regimes support reproducibility and provenance; UKAS-accredited methods noted for select analyses (NH4N, TON).
- Embargo and update mechanisms are not explicitly described; intake, update cadence, and data availability should be clarified if data are to be shared more broadly or across platforms.

## Funding and References
- Data collection supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme.
- Data validation supported by UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).
- Method references include Mackereth et al. (1978), Mortimer (1981), and Talling (1974).