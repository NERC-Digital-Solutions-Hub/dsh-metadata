# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023.

- Context and scope
  - Ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
  - Fortnightly sampling throughout 2023 (January to December).
  - Data downloadable as raw measurements across multiple physicochemical and biological parameters.

- Variables and units included
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - pH: pH
  - NH4N: total ammoniacal nitrogen, µg N per L
  - TON: total oxidised nitrogen, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon (SiO2), µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
  - Sample depth: integrated 0–5 m; shore samples if buoy visit not possible

- Data structure and access
  - Data provided as CSV with columns:
    - sdate (measurement date)
    - Description (variable name)
    - value (measurement)
    - sign(if<LOD) (below detection limit indicator)
    - flag (sampling location: 1 = buoy, 2 = shore)
  - Missing data explained by weather, equipment limitations, or staff constraints
  - Below-detection-limit values indicated with a < sign in sign field

- Sampling and measurement methods
  - Temperature and dissolved oxygen measured with YSI ProODO
    - Dissolved oxygen calibration and percentage saturation following Mortimer (1981)
  - Secchi depth measured using Secchi disk on a measured rope
  - Alkalinity and pH from integrated 0–5 m water sample
    - Alkalinity: Gran titration with a combined electrode
    - pH: calibrated electrode
  - Nitrogen and phosphorus analyses (UKAS-accredited methods)
    - NH4N: colorimetric analysis after filtration; calibrated with standards; QC standards every 10 samples
    - TON: colorimetric analysis after filtration; reduction of nitrate and diazo dye formation; QC standards every 10 samples
    - TP: digestion with potassium persulphate and molybdenum blue colorimetry; 880 nm measurement; calibration 0–0.2 mg/L; QC and reference materials
  - Silica (SIO2): colorimetric with ammonium molybdate and ascorbic acid; 880 nm; QC at start and every 20 samples
  - Phytoplankton chlorophyll a (TOCA): methanol extraction and spectrophotometric analysis after filtration

- Quality control status
  - Data presented are raw and not yet quality controlled or calibrated
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and visually validated by a database manager
  - Missing data attributed to weather, equipment limitations, or staff availability

- Provenance, funding, and references
  - Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme)
  - Data validation supported by NERC through UKCEH National Capability NE/Y006208/1
  - Method references include Mackereth et al. (1978), Mortimer (1981), and Talling (1974)