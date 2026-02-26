# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023

## Purpose and scope
- Ongoing fortnightly monitoring dataset for Windermere North Basin (Cumbria, England) covering 2023.
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH, ammoniacal nitrogen (NH4N, µg N/L), total oxidised nitrogen (TON, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).

## Sampling regime
- Fortnightly sampling from Windermere North Basin; water samples integrated from 0 to 7 m.
- Measurements taken from a boat at the buoy (deepest lake location); when buoy access not possible, shore sampling used (not integrated; Flag 2).

## Data content and units
- Data available as CSV with columns: sdate (measurement date), Variable/Description (the parameter), Value/Description (measured value and unit), Sign(if<LOD) (below detection indicator), Flag (sample location: 1 buoy, 2 shore).
- Below detection values denoted with a < sign in Sign column.

## Data quality and QC
- Data presented are raw and not yet quality controlled or calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA have been double-entered by different people and validated by a database manager.
- Visual checks (line graphs) performed for QC; missing data attributed to weather, equipment, or staff constraints.
- Some outputs marked with flags (e.g., Flag 2 when shore sampling occurred).

## Methods and instrumentation (high-level)
- Temperature and dissolved oxygen: measured with YSI ProODO; DO% calibrated daily; regular DO % calibrations (biweekly air-saturated water, bimonthly water-saturated air).
- Secchi depth: measured with Secchi disk on a marked rope.
- Alkalinity and pH: integrated sample sealed to prevent atmospheric exchange; Gran titration with combination electrode; electrode calibrated prior to sampling.
- Ammoniacal nitrogen (NH4N) and total oxidised nitrogen (TON): colorimetric analysis with SEAL AQ2 after filtration; methods UKAS accredited; multiple calibration and control standards.
- Total phosphorus (TP): digestion with potassium persulphate followed by molybdenum blue colorimetric analysis; UV/visible spectrophotometer measurements; standards and blanks used for accuracy.
- Dissolved reactive silicon (SIO2): colorimetric method with silicomolybenum blue complex; calibrated across 0–5 mg/L; QC samples run periodically.
- Phytoplankton chlorophyll a (TOCA): methanol extraction after filtration; spectrophotometric analysis.
- Soluble reactive phosphate (PO4P): filtration and molybdenum blue colorimetric analysis; calibration and blanks used for each sampling occasion.

## Data structure details
- File format: CSV with clearly defined columns for date, variable description, measured value, detection flag, and sample location flag.
- Detection and sampling flags inform end users about data reliability and sampling context.

## Funding and acknowledgments
- Data collection funded by Natural Environment Research Council (award NE/R016429/1) as part of UK-SCaPE; data validation supported by UKCEH National Capability grant NE/Y006208/1.

## Practical notes for data users
- 2023 dataset (January–December); no quality control completed beyond the described QC steps.
- Use caution when analyzing borderline or undetected values; refer to Sign and Flag for interpretation.
- Data suitable for creating dashboards or self-serve analyses with clear provenance on methods and detection limits.