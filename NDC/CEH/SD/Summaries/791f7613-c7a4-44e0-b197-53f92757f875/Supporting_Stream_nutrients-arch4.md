# Supporting information

## Overview
- Dataset of nutrient concentrations (mg/L) for nitrate, silica, total nitrogen (TN), total phosphorus (TP), and soluble reactive phosphorus (SRP) from Blelham Tarn.
- Collected at the main buoy (1 m depth) and inflows/outflows: Wray Beck (inflow), Blelham Beck (outflow), Fish Pond Beck (inflow), and Ford Wood Beck (inflow).
- Sampling period: monthly June–December 2016 and January–December 2017.
- Analyses: SRP by Emma Gray; nitrate, silica, TN, TP by UK Centre for Ecology & Hydrology chemistry department (Lancaster).

## Data scope and structure
- Data columns: Date (dd/mm/yyyy), Site ( inflow/outflow/lake name), nitrate, silica, total nitrogen, total phosphorus, soluble reactive phosphorus (all in mg/L).
- Dataset description corresponds to Fig.1 map of Blelham Tarn inflows and outflows.

## Sampling design
- Sites include main buoy at 1 m depth and four inflow/outflow locations around Blelham Tarn.
- Frequency: monthly over two years (2016–2017).
- Scope supports assessment of spatial (sites) and temporal (monthly) nutrient dynamics in the lake system.

## Analytical procedures by parameter
- Soluble Reactive Phosphorus (SRP):
  - Field filtration, colorimetric analysis using ammonium molybdate and antimony potassium tartrate in acid, reduced with ascorbic acid.
  - Read at 880 nm; calibration curve with standards (50 µg/L, diluted to 10–100 µg/L); quality control with a 50 µg/L stock diluted to 10 µg/L.
- Total Phosphorus (TP):
  - Potassium persulphate digestion, colorimetric molybdenum blue method.
  - Unfiltered water digested, data corrected by blanks; measured with SEAL AQ2 discrete analyser.
- Total Nitrogen (TN):
  - Acidification with HCl, purge to remove inorganic carbon.
  - Measured with Shalar Formacs CA16 analyser (ND25 accessory).
- Nitrate:
  - Ion chromatography; samples filtered (Whatman cellulose acetate, 0.45 µm); Dionex ICS2100; QC samples every 10 runs.
- Silica:
  - Colorimetric method with ammonium molybdate; reduced with ascorbic acid to form silicomolybdenum blue.
  - Measured at 880 nm; background corrections applied.

## Quality control and data quality
- Calibration curves used for all colorimetric methods; regular QC procedures (AQC for SRP, blanks for TP, periodic QC samples for nitrate).
- Specific instruments and methods documented to support reproducibility and traceability.

## Data provenance and usage notes
- Data collected by Emma Gray; SRP analysis by Emma Gray; other analyses by UK Centre for Ecology & Hydrology chemistry department (Lancaster).
- Dataset accompanied by a map (Fig.1) of inflows and outflows, aiding spatial interpretation.
- Units are consistently mg/L across parameters; date format standardized as dd/mm/yyyy.

## Practical considerations for data leaders
- Data integration: two-year time span with multiple sites supports temporal and spatial nutrient trend analysis; ensure consistent site naming when merging with other datasets.
- Metadata and discoverability: file BLEL_Stream_nutrients.csv with clear provenance; consider exporting additional metadata (detection limits, QA metrics, instrument models) for enhanced interpretability.
- Potential limitations: method-specific biases and instrument differences; SRP measured separately from other nutrients may require harmonization checks when combined with external datasets.