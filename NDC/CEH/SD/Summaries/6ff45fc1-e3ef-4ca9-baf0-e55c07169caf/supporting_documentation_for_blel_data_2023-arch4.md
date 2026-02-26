# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023. Feuchtmayr, H., Dodd, B.A., Guyatt, H., Hunt, A.G., Le Quesne, K., McShane, G., Moorhouse, H., Rankin, G., Rhodes, G., Thackeray, S.J. (2025)

## Overview and purpose
- Long-term, fortnightly monitoring dataset from Blelham Tarn, Cumbria, England.
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH; nutrients and pigments: NH4N, TON, PO4P, TOTP, SIO2, and phytoplankton chlorophyll a (TOCA, µg L−1).
- Samples are integrated from 0–5 m; when buoy sampling wasn’t possible, shore samples were taken (Flag 2).
- Data cover January 2023 to December 2023 and are available for download as CSV.

## Sampling regime and collection details
- Fortnightly sampling schedule as part of ongoing monitoring.
- Water samples taken from boat at the deepest lake location (buoy); shore samples used if buoy access was not possible.
- Depth-integrated sampling (0–5 m) for water chemistry; temperature and oxygen measured in situ.

## Data and variables
- Variables and units (as reported): TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 L−1), pH, NH4N (µg N L−1), TON (µg N L−1), PO4P (µg P L−1), TOTP (µg P L−1), SIO2 (µg SiO2 L−1), TOCA (µg L−1).
- Data values provided in a CSV with columns:
  - sdate: measurement date
  - variable/Description: variable name and description
  - value/Description: measured value
  - sign(if<LOD): indicates below detection limit with a < sign
  - flag: 1 if buoy site, 2 if shore sample
- Missing data attributed to weather, equipment limitations, or staff shortages.

## Data structure and format
- File format: comma-separated values (CSV).
- Columns include: sdate, Description (variable), value (measurement), sign(if<LOD), flag (sample location).
- Clear indication of below-detection values and sampling location to support data discovery and reuse.

## Quality control and data processing
- Data are raw and have not yet undergone formal quality control or calibration for all variables.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people from field notebooks or lab records and validated by a database manager.
- Visual checks performed by the database manager (e.g., line graphs).
- Data gaps explained by weather, equipment limitations, or staff shortages.

## Measurement methods and QA/QC specifics
- Temperature and dissolved oxygen: measured with YSI ProODO; DO% calibrated daily; biweekly DO% calibration in water-saturated air; bimonthly calibration in air-saturated water.
- Secchi depth: measured with Secchi disk on labeled rope.
- Alkalinity and pH: integrated sample sealed to prevent exchange; Gran titration with Radiometer GK2401C electrode; electrode calibration before each sampling.
- NH4N and TON: measured colorimetrically with SEAL AQ2; filtration through Whatman GF/C; alkaline conditions for NH4N; calibration with stock solutions; UKAS accredited method for both.
- TP: digested with K2S2O8 and measured via molybdenum blue colorimetry (absorbance at 880 nm) using UV-150-02 spectrophotometer; standards and reference materials used for accuracy.
- SIO2: dissolved reactive silicon measured colorimetrically (silicomolybenum blue) at 880 nm with standard QC samples.
- TOCA: chlorophyll a extracted from filtered samples with boiling methanol and analyzed spectrophotometrically.
- Methods referenced include established protocols and are underpinned by UKAS-accredited practices for certain nutrients (NH4N, TON).

## Data provenance, funding, and references
- Funding: Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE; data validation supported by UKCEH National Capability (NE/Y006208/1).
- Key references for methodology: Mackereth et al. (1978), Mortimer (1981), Talling (1974).

## Practical implications for Data Leaders
- The dataset provides a robust, long-term baseline of multiple aquatic parameters suitable for trend analyses and data system planning.
- Clear provenance, sampling consistency, and detailed methodological notes support data discoverability, reuse, and governance.
- Highlights the need for ongoing quality control and metadata enrichment to improve data trustworthiness and cross-project interoperability.