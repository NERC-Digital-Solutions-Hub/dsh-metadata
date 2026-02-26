# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023. Feuchtmayr, H., Carter, H.T., Dodd, B.A., Keenan, P.O., Le Quesne, K., McShane, G., Moorhouse, H., Rankin, G., Rhodes, G., Thackeray, S.J. (2025)

## Overview and scope
- Part of an ongoing fortnightly monitoring dataset for Windermere South Basin, Cumbria, England, covering January–December 2023.
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammoniacal nitrogen (NH4N), total oxidised nitrogen (TON), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data types and units prepared for download as CSV (see data structure below).

## Data variables and units
- TEMP: degree Celsius (°C)
- OXYG: percent air-saturation (%)
- SECC: metres (m)
- ALKA: micrograms per litre as CaCO3 (µg CaCO3 L⁻¹)
- pH: unitless
- NH4N: micrograms per litre (µg N L⁻¹)
- TON: micrograms per litre (µg N L⁻¹)
- PO4P: micrograms per litre (µg P L⁻¹)
- TOTP: micrograms per litre (µg P L⁻¹)
- SIO2: micrograms per litre (µg L⁻¹)
- TOCA: micrograms per litre (µg L⁻¹)
- Sign(if<LOD): indicates values below detection limit with a < sign

## Sampling regime
- Fortnightly sampling from the South Basin of Windermere.
- Water samples are integrated from surface to 7 m depth (0–7 m).
- Measurements taken from a boat at a marked buoy located at the lake’s deepest point.
- Timeframe for data: January 2023 to December 2023.

## Quality control and data quality
- Data are raw and have not yet been quality controlled or fully calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA data have been double entered into Excel from field notebooks/lab records and visually validated by a database manager.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- Partial QA applied: some validation through duplicate analyses and visual review; UKAS accreditation mentioned for specific methods (NH4N, TON).

## Data structure and metadata (data dictionary)
- Data provided as a comma-separated values (CSV) file with columns:
  - sdate: date of measurement
  - Description: variable name and description (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value for each variable
  - Sign(if<LOD): indicator for values below detection limit (a “<” sign if applicable)

## Measurement methods (highlights)
- Temperature and dissolved oxygen: measured with YSI ProODO handheld instrument; DO% calibrated daily; calibration targets 98–102% DO in water-saturated air; biweekly DO% calibrations and bimonthly calibrations in air-saturated water.
- Secchi depth: measured by lowering a Secchi disk on a labeled rope.
- Alkalinity and pH: integrated water sample sealed to prevent gas exchange; Gran titration with a combination electrode; electrode calibrated prior to each sampling.
- NH4N and TON: measured colorimetrically with SEAL AQ2 after filtration; NH4N involves indophenol-blue chemistry with calibration and quality controls; TON involves reduction of nitrate by hydrazine and colorimetric detection; methods UKAS accredited.
- Total phosphorus (TP): digestion with potassium persulphate, followed by molybdenum blue colorimetric analysis; UV/visible spectrophotometry used for detection; standards and reference materials used for accuracy.
- Dissolved reactive silicon (SiO2): colorimetric measurement with ammonium molybdate and ascorbic acid reduction to form silicomolybenum blue; calibration range 0–5 mg/L; QC samples run periodically.
- Phytoplankton chlorophyll a (TOCA): extraction and spectrophotometric analysis after filtration and methanol extraction.
- Phosphate (PO4P): colorimetric molybdenum blue analysis after filtration; calibration and blanks included for each sampling occasion.
- References for methods: Mackereth et al. (1978), Mortimer (1981), Talling (1974).

## Data governance, availability, and supporting information
- Funding and validation support:
  - Data collection funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE National Capability.
  - Data validation supported by NERC through UKCEH National Capability (NE/Y006208/1).
- References provided for methods to support traceability and methodological transparency.
- Documented status implies readiness for further quality control, calibration, and potential dissemination through appropriate data portals; notes on data provenance and validation steps aid dataset discoverability and reuse.
- No explicit embargo or access restrictions stated; imprint of ongoing data quality work and calibration needs.

## Practical considerations for data stewards
- Ensure downstream users understand the current QA status (raw data; partial validation completed).
- Record and communicate data provenance, sampling regime, and measurement methods to maintain reproducibility and interoperability.
- Monitor and document updates as QA/calibration proceeds; maintain linkage to the original measurement dates and methods.
- Preserve metadata about detection limits (Sign(if<LOD)) and units to enable proper interpretation and filtering.
- Facilitate integration with other datasets by aligning variable definitions, units, and depth-integrated sampling approach.