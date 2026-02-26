# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023

- Overview
  - Long-term fortnightly monitoring dataset from Blelham Tarn, Cumbria, England.
  - Timeframe for this download: January 2023 to end of 2023.
  - Measured parameters: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, nutrients (NH4N, TON, PO4P, TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
  - Units: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), pH (unitless), NH4N and TON (µg N per L), PO4P and TOTP (µg P per L), SIO2 (µg per L), TOCA (µg per L).
  - Water samples are integrated from 0–5 m; when buoy sampling isn’t possible, shore sampling may be used.

- Sampling regime and collection details
  - Part of an ongoing long-term monitoring program with fortnightly sampling.
  - Sampling performed from a boat at a marked buoy location (deepest part of the lake); if not possible, samples collected from shore.
  - Data availability notes: some occasions with Flag 2 indicate non-integrated shore samples.
  - Data presented as raw (not yet quality controlled/calibrated in this release), though TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have undergone double-entry validation and visual checks by a database manager.
  - Missing data attributed to weather, equipment limits, or staffing.

- Data structure and file format
  - Delivered as comma-separated values (CSV).
  - Columns include:
    - sdate: measurement date
    - Description: variable name (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, TON, PO4P, TOTP, SIO2, TOCA)
    - value: measured value
    - sign(if<LOD): indicator for values below detection limit (a < sign if applicable)
    - flag: sampling location indicator (1 = buoy sample; 2 = shore sample)
  - Variables and units listed in the data description (as above).

- Measurement methods and quality control
  - Temperature and dissolved oxygen (TEMP and OXYG)
    - Instrument: YSI ProODO handheld (Xylem Analytics UK).
    - DO expressed in mg/L; saturation derived from Mortimer (1981).
    - DO % calibrated hourly; passes when 98–102% saturation.
    - Biweekly single-point DO% calibrations; bimonthly calibrations in air-saturated water.
  - Secchi depth (SECC)
    - Measured by lowering a Secchi disk on a marked rope.
  - Alkalinity (ALKA) and pH
    - Integrated water sample sealed to prevent atmospheric exchange.
    - Alkalinity and pH determined by Gran titration using a Radiometer GK2401C electrode (calibrated before each sampling).
  - Nitrogen species (NH4N, TON)
    - Measured colorimetrically with SEAL AQ2 after filtration (GF/C filter).
    - NH4N: blue-green indophenol reaction; range 0–2.0 mg/L; UKAS accredited.
    - TON: reduction of nitrate to nitrite; azo dye formation; range 0–2.0 mg/L; UKAS accredited.
  - Phosphorus and silicon (PO4P, TOTP, SIO2)
    - TOTP: digestion with potassium persulfate, followed by molybdenum blue colorimetric analysis; absorbance at 880 nm.
    - PO4P: colorimetric molybdenum blue after filtration.
    - SIO2: colorimetric method with ammonium molybdate, reduced to form silicomolybdenum blue; absorbance at 880 nm.
  - Phytoplankton chlorophyll a (TOCA)
    - Filtration of integrated sample; pigment extraction in boiling methanol; spectrophotometric analysis per Talling (1974).
  - Calibrations and quality controls
    - Calibrations and reference materials used for each analytical method.
    - Some analyses include routine controls (e.g., 1 mg/L NH3-N standards every 10 samples) and blanks.
  - Data quality status
    - Raw data in this release; not fully quality controlled or calibrated yet.
    - A subset has undergone double-entry validation and visual checks; ongoing validation implied.

- Data accessibility, traceability and metadata
  - Data are intended to be discoverable and usable, with metadata describing the sampling regime, methods, and units.
  - Missing data noted with weather/staff limitations; non-integrated samples flagged accordingly.
  - Methods and references linked for reproducibility and comparability (Mortimer 1981; Mackereth et al. 1978; Talling 1974; UKAS accreditation notes).

- Funding and references
  - Data collection funded by Natural Environment Research Council (NE/R016429/1) under UK-SCaPE National Capability.
  - Data validation supported by NERC via UKCEH National Capability (NE/Y006208/1).
  - Key references for methods include Mackereth et al. (1978), Mortimer (1981), Talling (1974).