# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023

## Dataset purpose and scope
- Ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling during 2023 (January to December).
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammoniacal nitrogen (NH4N), total oxidised nitrogen (TON), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Sample collected from 0 to 5 m depth; primary location is a buoy at the deepest part of the lake; on some occasions, shore samples were taken when buoy access was not possible (Flag 2).

## Measured parameters and units
- TEMP: degrees Celsius
- OXYG: % air-saturation
- SECC: metres
- ALKA: µg CaCO3 per litre
- pH: unitless
- NH4N: µg N per litre
- TON: µg N per litre
- PO4P: µg P per litre
- TOTP: µg P per litre
- SIO2: µg per litre (as SiO2)
- TOCA: µg per litre

## Data collection methods
- Temperature and dissolved oxygen: measured with YSI ProODO handheld instrument.
- Secchi depth: measured with Secchi disk on measured rope.
- Alkalinity and pH: integrated sample sealed to prevent air exchange; measured by Gran titration with radiometer electrodes.
- NH4N: colorimetric measurement after filtration (SEAL AQ2) with calibration and quality checks; UKAS accredited.
- TON: colorimetric measurement after filtration (SEAL AQ2) with nitrate reduction and azo dye formation; UKAS accredited.
- TOTP: digestion with potassium persulphate followed by molybdenum blue colorimetric analysis; UV-Vis detection.
- SIO2: colorimetric silica determination after filtration; spectrophotometric measurement at 880 nm.
- TOCA: pigment extraction from filtered samples with boiling methanol; spectrophotometric analysis.
- PO4P: colorimetric measurement after filtration (molybdenum blue analysis).

## Data structure and format
- Data provided as CSV with columns:
  - sdate (date of measurement)
  - variable (name of measurement)
  - value (measured value)
  - sign(if<LOD) (indicator if below detection limit; shows a < symbol)
  - flag (sampling context: 1 = buoy location, 2 = shore visit)
- Water samples are integrated 0–5 m; non-integration occurs when buoy visit was not possible.

## Quality control and limitations
- Data are raw and not yet quality controlled or calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and validated visually by a database manager.
- Missing data attributed to weather conditions, equipment limitations, or staff shortage.
- Some measurements flagged (Flag 2) when shore sampling occurred instead of buoy sampling.
- Detection limit indicators present to denote values below analytical detection.

## Calibration and QA details
- DO % calibration conducted daily with single-point calibrations; requires 98–102% saturation for pass.
- Alkalinity and pH calibration performed with integrated sample and electrode calibration prior to each sampling occasion.
- NH4N and TON methods UKAS accredited; QA includes control standards and reference materials.
- Calibration ranges and accuracy described for each analytical method (e.g., NH4N 0–2.0 mg/L; TON 0–2.0 mg/L).

## Funding and references
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme) and NERC UKCEH National Capability NE/Y006208/1.
- References for methods: Mackereth et al. (1978), Mortimer (1981), Talling (1974).

## Practical implications for data analysts
- Rich, multi-parameter time series suitable for correlations and trend analyses, with explicit depth integration and measurement context.
- Be mindful of:
  - Data are raw; plan for QC/calibration before analysis.
  - Missing data due to logistics or weather; account for potential seasonal gaps.
  - Below-detection values indicated; handle appropriately in models.
  - Shore vs buoy samples flagged to account for spatial context.
  - Unit consistency across variables and potential need for standardisation when merging with other datasets.