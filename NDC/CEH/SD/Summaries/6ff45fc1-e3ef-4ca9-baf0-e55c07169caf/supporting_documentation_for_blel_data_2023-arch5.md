# Supporting Document Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023

- Overview
  - Part of a long-term monitoring dataset for Blelham Tarn, Cumbria, England.
  - Fortnightly sampling throughout 2023.
  - Measured variables: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH, ammoniacal nitrogen (NH4N, µg N/L), total oxidised nitrogen (TON, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).
  - Water samples integrated from 0–5 m; sampling from a boat at a buoy location when possible; shore samples used when buoy sampling was not possible.
  - Documented data range: January 2023 – end of 2023.

- Data contents and structure
  - Delivered as a comma-separated values (CSV) file.
  - Core columns include:
    - sdate: measurement date.
    - variable/Description: the measured parameter (name and unit described).
    - value: measured value for each variable.
    - sign(if<LOD): indicates if value is below detection limit (uses a “<” sign).
    - flag: indicates sampling location (1 = buoy, 2 = shore).
  - Clear specification of units for each variable and handling of measurements below detection limits.

- Sampling regime and measurement methods
  - Measurement regime: fortnightly sampling at the deepest part of the lake; integrated 0–5 m water samples; alternative shore sampling when buoy access was not possible.
  - Temperature and dissolved oxygen:
    - Measured with YSI ProODO handheld instrument.
    - DO% calibrated daily; saturation checks with biweekly and bimonthly calibrations.
  - Secchi depth: measured using a Secchi disk with a labeled rope.
  - Alkalinity and pH: integrated sample sealed to minimize atmospheric exchange; Gran titration with a specified electrode; calibration performed beforehand.
  - Nutrients and chlorophyll:
    - NH4N and TON: colorimetric analyses using SEAL AQ2 discrete analyser after filtration; methodology includes calibration, repeats, and UKAS accreditation.
    - TP: digestion using potassium persulphate with subsequent molybdenum blue colorimetric analysis; UV/Vis spectrophotometer measurement.
    - SIO2: colorimetric silica determination with ammonium molybdate and ascorbic acid, read at 880 nm; QC samples run at defined intervals.
    - TOCA: chlorophyll a extraction and spectrophotometric analysis after filtration.

- Quality control and data quality
  - Data presented are raw and not yet quality controlled or calibrated.
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered from field notebooks/lab sheets and validated by a database manager through visual checks (line graphs).
  - Missing data explained by weather, equipment limitations, or staff shortages.
  - Some measurements have ongoing QC steps (e.g., calibration and control standards described for several analyses).

- Purpose, governance, and provenance
  - Data collection supported by the Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE; data validation supported by UKCEH under NE/Y006208/1.
  - Documentation provides extensive methodological references and standard procedures (e.g., Mackereth et al. 1978; Mortimer 1981; Talling 1974) to support reproducibility and comparability.
  - Metadata includes method details, calibration procedures, detection limits, and QC practices to support data discovery, governance, and reuse.

- Data availability and update considerations for stewardship
  - The document details a fixed-year dataset (2023) with explicit sampling dates and procedures.
  - Emphasizes that datasets should respect sharing limitations and that systems are in place to support updates; current data cover Jan–Dec 2023 and may be expanded in future iterations following the described protocols.
  - Clear indication of units, detection indicators, and location flags to aid interoperability with other datasets.

- Limitations and caveats for users
  - Raw data require quality control and calibration before formal analysis or integration into broader data systems.
  - Incomplete sampling scenarios (shore vs buoy) are captured via flag indicators, which users must account for in analyses.
  - Data quality varies by component (e.g., some analyses include UKAS accreditation and QC steps, others are raw with planned validation).

- Documentation and references
  - Methodological references provided for underlying analytical techniques and calibration.
  - Documentation includes process flows for data capture, entry, validation, and QC planning, supporting traceability and data lineage.