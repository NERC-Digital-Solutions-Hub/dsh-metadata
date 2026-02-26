# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwa Water, UK, 2023

## Purpose and scope
- Part of a long-term monitoring dataset for Esthwa Tarn (Cumbria, England).
- Fortnightly sampling in 2023 (Jan–Dec) collecting surface temperature, surface oxygen, Secchi depth, alkalinity, pH, nutrients (NH4N, TON, PO4P, TOTP), dissolved silicon (SiO2), and phytoplankton chlorophyll a (TOCA).
- Samples taken from integrated 0–5 m water column; measurements made at a buoy at the lake’s deepest part (shore samples used when buoy access was not possible).

## Data collection regime
- Data provided as a CSV with columns for date (sdate), variable descriptions, values, detection flags (sign for below detection), and sampling location flag (flag: 1 buoy, 2 shore).
- Covered all measurements listed above for 2023.

## Measurements and methods
- Temperature and dissolved oxygen: measured with YSI ProODO; DO% calibrated to Mortimer (1981) standards; regular biweekly and bimonthly calibrations.
- Secchi depth: measured with a Secchi disk on a labeled rope.
- Alkalinity and pH: integrated water sample sealed to prevent exchange; Gran titration with a Radiometer electrode; electrode calibrated before each sampling.
- Nutrients:
  - NH4N and TON: colorimetric analysis on SEAL AQ2 after GF/C filtration; validated via calibration curves and UKAS accreditation.
  - PO4P: colorimetric molybdenum blue after filtration; calibration and blanks used.
  - TP (total phosphorus): digestion with potassium persulphate plus molybdenum blue colorimetric analysis; absorbance at 880 nm; calibration and reference checks.
- Phytoplankton chlorophyll a (TOCA): filtration, methanol extraction, spectrophotometric analysis.
- Dissolved reactive silicon (SIO2): colorimetric silicomolybdenum blue method; QC samples included.

## Quality control and data validation
- Data are raw and not yet quality controlled/calibrated.
- Double entry by different people from field notebooks/lab sheets; database manager performs visual checks (e.g., line graphs) for validation.
- Missing data attributed to weather, equipment limitations, or staff shortages.

## Data structure and accessibility
- Data stored as comma-separated values (CSV) with explicit fields for sdate, variable, value, sign, and flag.
- Designed for standardised reporting and long-term trend analysis, with ongoing quality assurance and potential portal upload.

## Funding and references
- Funding: Natural Environment Research Council (NE/R016429/1) under UK-SCaPE; data validation supported by UKCEH (NE/Y006208/1).
- References: Mackereth et al. (1978); Mortimer (1981); Talling (1974).