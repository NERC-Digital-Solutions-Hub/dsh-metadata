# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023

## Summary
- Fortnightly monitoring dataset from the North Basin of Windermere, Cumbria, England, collected January–December 2023.
- Variables measured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH, ammoniacal nitrogen (NH4N, µg N L−1), total oxidised nitrogen (TON, µg N L−1), soluble reactive phosphate (PO4P, µg P L−1), total phosphorus (TOTP, µg P L−1), dissolved reactive silicon (SIO2, µg L−1), phytoplankton chlorophyll a (TOCA, µg L−1).
- Samples collected from a marked buoy location at the deepest part of the lake; if buoy access was not possible, samples taken from the shore (Flag 2).
- Data are raw (not fully quality controlled) but some fields have been double-entered and visually validated.

## Sampling regime and scope
- Study area: Windermere North Basin, UK.
- Sampling frequency: every two weeks (fortnightly).
- Depth integration: water samples integrated from 0 to 7 m when collected at buoy.
- Occasionally shore-based sampling when buoy access unavailable (Flag 2).

## Measured variables and units
- TEMP: surface temperature, °C
- OXYG: surface oxygen saturation, % air-saturation
- SECC: Secchi depth, m
- ALKA: alkalinity, µg CaCO3 per L
- pH: pH unit
- NH4N: total ammoniacal nitrogen, µg N per L
- TON: total oxidised nitrogen, µg N per L
- PO4P: soluble reactive phosphate, µg P per L
- TOTP: total phosphorus, µg P per L
- SIO2: dissolved reactive silicon (SiO2), µg per L
- TOCA: phytoplankton chlorophyll a, µg per L
- Sign(if<LOD): indicator for values below detection limit (a < sign)
- Flag: 1 = sample at buoy location; 2 = shore sampling

## Data structure and sampling details
- Data format: comma separated values (CSV).
- Columns include: sdate (measurement date), Variable/Description, Value/Description, Sign(if<LOD), Flag.
- Water samples integrated 0–7 m; sampling from buoy when possible, otherwise shore sampling.
- Missing data: due to weather, equipment limitations, or staff shortages.

## Quality control and validation
- Data are raw and not fully quality controlled or calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA have been double-entered by different people from field notebooks or lab records and visually validated by a database manager.
- Validation includes visual checks (graphs); calibration and QA details described for various instruments and methods.
- Missing data attributed to weather, equipment limitations, or staff shortages.

## Measurement methods (instruments and analyses)
- Temperature and dissolved oxygen: measured with YSI ProODO handheld instrument; DO% calibrated daily; regular biweekly and bimonthly calibrations.
- Secchi depth: measured with Secchi disk using marked rope.
- Alkalinity and pH: integrated water sample sealed to prevent atmospheric exchange; Gran titration with a combination electrode; electrode calibrated before each sampling.
- NH4N and TON: measured colorimetrically with SEAL AQ2 discrete analyser after filtration; standard colorimetric reactions with calibration curves; UKAS accredited methods; QA with control standards.
- TP: digestion with potassium persulphate (K2S2O8) and subsequent molybdenum blue colorimetric analysis; absorbance at 880 nm; standards and reference materials used for accuracy.
- SIO2: dissolved reactive silicon measured colorimetrically (silicomolybdenum blue) at 880 nm; QC samples included.
- TOCA: phytoplankton chlorophyll a measured after filtration and methanol extraction; analyzed spectrophotometrically.

## Data limitations and considerations for analysts
- Data are raw and not fully QC’d; results should be treated with caution for precise analyses without further validation.
- Some measurements below detection limits are flagged; interpret with the Sign(if<LOD) indicator.
- Sampling location variability (buoy vs shore) may introduce spatial heterogeneity.
- Temporal coverage is 2023 only; cross-year comparisons require alignment of methods and QA.

## Access, funding and references
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE National Capability); data validation supported by NERC through UKCEH (NE/Y006208/1).
- References for methods include:
  - Mackereth, J.F.H. et al. (1978) Water Analysis: Revised Methods for Limnologists
  - Mortimer, C.H. (1981) Oxygen content of air-saturated freshwater
  - Talling, J.F. (1974) In standing waters: Manual on Methods for Measuring Primary Production in Aquatic Ecosystems