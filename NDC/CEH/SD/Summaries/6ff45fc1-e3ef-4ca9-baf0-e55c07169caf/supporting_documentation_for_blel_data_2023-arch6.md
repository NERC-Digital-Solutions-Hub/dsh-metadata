# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023

- Overview
  - Part of an ongoing long-term monitoring dataset collected fortnightly at Blelham Tarn, Cumbria, England.
  - Timeframe: January 2023 to the end of 2023.
  - Variables provided: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH; ammoniacal nitrogen (NH4N, µg N/L), total oxidised nitrogen (TON, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).
  - Sampling location: integrated 0–5 m water column; measured from a buoy at the deepest part of the lake; if the buoy was inaccessible, samples collected from the shore.
  - Data coverage: all data are from 2023; some shore samples marked with Flag 2 when buoy access was not possible.

- Data content and formats
  - Delivered as comma separated values (CSV) with the following columns:
    - sdate: measurement date
    - Description: variable name (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA)
    - value: measured value for each variable
    - sign(if<LOD): indicates if the value is below the detection limit (a < sign)
    - flag: 1 if sample was taken at the buoy location; 2 if sample was taken from shore due to buoy inaccessibility

- Quality control and data quality
  - The data are raw and not yet quality controlled or calibrated.
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and validated by a database manager; visual checks against line graphs performed.
  - Missing data are attributed to weather, equipment limitations, or staff shortages.

- Methods and instrumentation
  - Temperature and oxygen: measured with YSI ProODO; DO% calibrated daily; biweekly and bimonthly calibrations conducted.
  - Secchi depth: measured with a Secchi disk on a labeled rope.
  - Alkalinity and pH: integrated sample sealed to prevent atmospheric exchange; measured by Gran titration and a combination electrode.
  - NH4N and TON: measured colorimetrically with SEAL AQ2 after filtration; UKAS-accredited methods; calibration and control standards used.
  - Total phosphorus (TP): digestion with potassium persulphate, followed by molybdenum blue colorimetric analysis using a UV/visible spectrophotometer; calibration and reference materials used.
  - Dissolved reactive silicon (SIO2): colorimetric method using ammonium molybdate and reduction to form silicomolybenum blue; measured at 880 nm.
  - Phytoplankton chlorophyll a (TOCA): filtered sample with boiling methanol extraction; quantified spectrophotometrically.
  - General QA: calibration and standard references referenced in methods; UKAS accreditation for relevant measurements.

- Data structure details
  - Variables are organized in a single CSV with explicit sdate and value fields.
  - sign(if<LOD) indicates below-detection-limit values; flag indicates sampling location (buoy vs shore).

- Usage notes and caveats
  - Treat as raw data until quality control and calibration are completed.
  - Be aware of potential incomplete records due to weather or access issues; some measurements marked with flags for sampling conditions.
  - Units and detection-limit indicators provided to aid proper interpretation and potential data integration with other datasets.

- Data provenance and funding
  - Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme.
  - Data validation supported by NERC via UKCEH National Capability for UK Challenges Programme NE/Y006208/1.

- References for methods
  - Mackereth et al. 1978; Mortimer 1981; Talling 1974 (standard methods cited for water analysis techniques).