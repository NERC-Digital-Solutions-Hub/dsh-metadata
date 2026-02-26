# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023

## Overview
- Ongoing fortnightly monitoring in 2023 of Windermere South Basin (Cumbria, England) focusing on surface temperature, surface oxygen, Secchi depth, water chemistry, and phytoplankton chlorophyll a.
- Variables available for download: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3/L), pH, NH4N (µg N/L), TON (µg N/L), PO4P (µg P/L), TOTP (µg P/L), SIO2 (µg/L as SiO2), TOCA (µg/L).
- Timeframe: January 2023 through December 2023.
- Samples are integrated from 0–7 m and collected from a boat at a marked buoy location at the deepest part of the lake.

## Sampling regime and data coverage
- Fortnightly sampling regime as part of an ongoing monitoring dataset.
- Water samples collected as integrated 0–7 m vertical profile.
- Data cover January–December 2023; includes multiple chemical and biological indicators.

## Variables and units
- Surface temperature (TEMP): degrees Celsius.
- Surface oxygen saturation (OXYG): percent air-saturation.
- Secchi depth (SECC): metres.
- Alkalinity (ALKA): µg CaCO3 per L.
- pH: unitless (pH value).
- Total ammoniacal nitrogen (NH4N): µg N per L.
- Total oxidised nitrogen (TON): µg N per L.
- Soluble reactive phosphate (PO4P): µg P per L.
- Total phosphorus (TOTP): µg P per L.
- Dissolved reactive silicon (SIO2): µg/L as SiO2.
- Phytoplankton chlorophyll a (TOCA): µg/L.

## Quality control and data quality
- Data shown are raw and not yet quality controlled or calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, TOCA: double-entered by different people and qualitatively validated; database manager checked visually (line graphs).
- NH4N and TON methods are UKAS-accredited; validation includes calibration curves and control standards.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- Sign(if<LOD) column indicates values below detection limit with a < symbol.

## Data structure
- Format: comma-separated values (CSV).
- Columns:
  - sdate: date of measurement.
  - Variable, Description: variable name (e.g., TEMP) and its description.
  - Value, Description: measured value for each variable.
  - Sign(if<LOD), Description: indicator if value is below detection limit (<).

## Analytical methods
- Temperature and dissolved oxygen:
  - Instrument: YSI ProODO handheld (Xylem).
  - DO% calibration and biweekly/bi-monthly calibrations; Mortimer (1981) referenced for saturation calculations.
- Secchi depth:
  - Measured by lowering a Secchi disk on a marked rope.
- Alkalinity and pH:
  - Integrated water sample sealed to prevent exchange; Gran titration with Radiometer GK2401C electrode; electrode calibration prior to sampling.
- Nitrogen species:
  - NH4N: SEAL AQ2 discrete analyser after filtration; colorimetric indophenol blue method; UKAS accredited; calibration and quality control standards described.
  - TON: SEAL AQ2 discrete analyser after filtration; reduction of nitrate to nitrite with hydrazine; colorimetric detection at 546 nm; UKAS accredited; calibration and QC described.
- Phosphorus and silica:
  - TP: K2S2O8 digestion with molybdenum blue colorimetry; UV-150-02 spectrophotometer; digestion and calibration details provided; blank-corrected.
  - PO4P: molybdenum blue colorimetric analysis after filtration.
  - SIO2: colorimetric with ammonium molybdate; silicomolybdenum blue complex measured at 880 nm; QC samples included.
- Phytoplankton chlorophyll a (TOCA):
  - Extraction: filtered sample extracted with boiling methanol; analyzed spectrophotometrically (Talling 1974 methodology).

## Limitations and GIS considerations
- Raw data, not fully quality controlled; be cautious about accuracy without validation steps.
- Single-station time series: sampling from one buoy at the deepest lake location; spatial coverage limited to that site.
- Depth integration (0–7 m) may limit depth-resolved GIS analyses.
- Some measurements below detection limits are flagged; conversion or imputation may be needed for certain analyses.
- No explicit georeferenced coordinates included in the dataset description; GIS work may require linking to the buoy’s spatial location.

## Access, provenance and funding
- Data collection supported by Natural Environment Research Council (NE/NERC) award NE/R016429/1 as part of UK-SCaPE.
- Data validation supported by NERC via UKCEH National Capability (NE/Y006208/1).

## References
- Mackereth F.J.H., Heron J., Talling J.F. (1978) Water Analysis: Some Revised Methods for Limnologists. Freshwater Biological Association.
- Mortimer C.H. (1981) The oxygen content of air-saturated fresh waters. Istituzioni limnologiche.
- Talling J.F. (1974) In standing waters. In Vollenweider (Ed.), Manual on Methods for Measuring Primary Production in Aquatic Ecosystems. Blackwell.