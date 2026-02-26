# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023.

## Overview
- Fortnightly monitoring dataset from Windermere North Basin (Cumbria, England) covering surface temperature, surface oxygen, Secchi depth, water chemistry, and phytoplankton chlorophyll a for 2023 (January–December).
- Data available as raw measurements collected from a buoy location (deepest lake point) or, when inaccessible, from shore.
- Key variables and units: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 L⁻¹), pH, NH4N (µg N L⁻¹), TON (µg N L⁻¹), PO4P (µg P L⁻¹), TOTP (µg P L⁻¹), SIO2 (µg SiO₂ L⁻¹), TOCA (µg L⁻¹).

## Data Included and Structure
- Data columns in CSV: sdate (measurement date), Variable/Description, Value, Sign(if<LOD), Flag.
- Flags: Flag = 1 indicates sample taken at buoy location; Flag = 2 indicates shore sampling (no buoy access).
- Detection limits indicated by a < sign in the Sign(if<LOD) column.
- Measurements cover integrated water samples from 0 to 7 m depth (with occasional non-integrated shore samples).

## Measurement Methods
- Temperature and dissolved oxygen: measured with YSI ProODO; DO in mg/L, saturation derived from Mortimer (1981). Calibration includes daily DO% checks and biweekly and bimonthly calibrations.
- Secchi depth: measured using Secchi disk on a labeled rope.
- Alkalinity and pH: integrated sample sealed to prevent exchange; Gran titration with Radiometer GK2401C electrode; electrode calibration prior to sampling.
- Ammoniacal nitrogen (NH4N) and Total oxidised nitrogen (TON): colorimetric analysis with SEAL AQ2 after filtration (GF/C); UKAS accredited methods; detailed calibration and quality control.
- Total phosphorus (TP): digestion with potassium persulphate, molybdenum blue colorimetry; UV-150-02 spectrophotometer; blanks and reference materials used for accuracy.
- Dissolved reactive silicon (SIO2): colorimetric assay with ammonium molybdate and reduction to form silicomolybenum blue; measured at 880 nm; QC samples included.
- Phytoplankton chlorophyll a (TOCA): filtration, methanol extraction, spectrophotometric analysis.
- Soluble reactive phosphate (PO4P): filtration and molybdenum blue colorimetric analysis; calibration and blanks used for accuracy.

## Quality Control and Data Integrity
- Data presented are raw (not yet quality controlled/calibrated). Some variables have had double-entry verification (TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA) and visual validation by a database manager.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- UKAS accreditation applies to specific analytical methods; calibration and control standards employed throughout.

## Data Availability and Access
- Data supplied as comma-separated values (CSV) with clearly labeled variables and units; data below detection limits flagged accordingly.
- Documentation includes method details, detection limits, and QC notes to support reproducibility and transparent monitoring.

## Coverage and Timeframe
- Geographic scope: Windermere North Basin, Cumbria, England.
- Temporal scope: January 2023 through December 2023, with fortnightly sampling cadence.

## Funding and References
- Funding: Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme, National Capability); data validation supported by NERC (NE/Y006208/1).
- References for methods: Mackereth et al. (1978), Mortimer (1981), Talling (1974).