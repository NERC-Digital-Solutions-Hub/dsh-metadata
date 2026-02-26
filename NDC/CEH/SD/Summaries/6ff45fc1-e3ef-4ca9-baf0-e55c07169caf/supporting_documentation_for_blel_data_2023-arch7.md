# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023

- This document describes a long-term monitoring dataset from Blelham Tarn, Cumbria, England, with fortnightly sampling in 2023.
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % AIR-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammoniacal nitrogen (NH4N, µg N per L), total oxidised nitrogen (TON, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg L−1), and phytoplankton chlorophyll a (TOCA, µg L−1).

- Sampling regime
  - Integrated water samples from 0 to 5 m depth, collected from a buoy at the deepest part of the lake; if buoy access was not possible, shore samples were taken (Flag 2).
  - Sampling period: January 2023 to end of 2023 (fortnightly).

- Data quality and QC
  - Reported data are raw and not fully quality controlled or calibrated yet.
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have undergone double-entry by different people and visual validation by a database manager.
  - Missing data noted due to weather, equipment limits, or staff shortages.

- Data structure and how to use
  - Delivered as a comma-separated values (CSV) file.
  - Core columns: sdate (measurement date), variable (name), value (measurement), sign(if<LOD) (indicator of below detection limit), flag (1 = buoy location; 2 = shore).
  - Variables and units summary (as described in the dataset).

- Measurement methods and instruments
  - Temperature and dissolved oxygen
    - Measured with YSI ProODO handheld instrument; DO in mg/L; oxygen saturation calculated relative to Mortimer (1981).
    - DO% calibrated daily; valid pass range 98–102%.
    - Biweekly DO% calibration in water-saturated air; bimonthly calibration in air-saturated water.
  - Secchi depth
    - Measured by lowering a Secchi disk with a measured rope.
  - Alkalinity and pH
    - Integrated water sample sealed to prevent atmospheric exchange; Gran titration with Radiometer GK2401C electrode (PHM64); electrode calibrated before each occasion.
  - Ammoniacal nitrogen (NH4N) and total oxidised nitrogen (TON)
    - Measured colorimetrically with SEAL AQ2 discrete analyzer after filtration (GF/C).
    - NH4N: blue-green indophenol reaction; range 0–2.0 mg/L; UKAS accredited; daily calibration and quality controls.
    - TON: hydrazine reduction of nitrate to nitrite; azo dye formation; range 0–2.0 mg/L; UKAS accredited; daily calibration and controls.
  - Total phosphorus (TP)
    - Digestion with potassium persulfate, followed by molybdenum blue colorimetric analysis (UV-150-02 spectrophotometer); range 0–0.2 mg/L P; blank corrected; precision/accuracy checks with reference materials.
  - Dissolved reactive silicon (SIO2)
    - Colorimetric method with ammonium molybdate and ascorbic acid, measured at 880 nm; range 0–5 mg/L SiO2; QC samples used.
  - Phytoplankton chlorophyll a (TOCA)
    - Filtration (GF/C) and methanol extraction; spectrophotometric analysis per Talling (1974).

- Data availability and limitations
  - Raw data are provided; users should account for the ongoing quality control/calibration process.
  - Data are time-series from a single lake, with spatial sampling restricted to buoy/deepest-point and occasional shore collections.

- Funding and references
  - Data collection funded by Natural Environment Research Council (NE/R016429/1) under UK-SCaPE.
  - Data validation supported by NERC (NE/Y006208/1).
  - Key references for methods: Mackereth et al. (1978), Mortimer (1981), Talling (1974).