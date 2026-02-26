# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023

- Purpose and scope
  - Fortnightly monitoring dataset for 2023 covering surface temperature, surface oxygen, Secchi depth (water clarity), water chemistry (alkalinity, pH, nutrients) and phytoplankton chlorophyll a in Windermere South Basin, Cumbria, England.
  - Data intended to track spatially-relevant lake health indicators and support broader environmental assessments.

- Data assets and variables
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - pH: pH
  - NH4N: total ammoniacal nitrogen (µg N per L)
  - TON: total oxidised nitrogen (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon as SiO2 (µg per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)
  - Sample basis: integrated from 0 to 7 m; collected from a buoy at deepest lake location
  - Temporal coverage: January–December 2023
  - Data format: CSV with columns sdate (date), Variable (name), Value, Sign(if<LOD) indicating below detection limit

- Sampling regime and collection context
  - Part of an ongoing monitoring program; measurements taken from a boat at a fixed buoy.
  - Frequency: fortnightly throughout 2023.

- Measurement methods and instrumentation
  - Temperature and oxygen: measured with YSI ProODO handheld instrument; DO% calibrated daily; biweekly DO% calibration in water-saturated air; data used to compute oxygen saturation.
  - Secchi depth: measured with a Secchi disk and marked rope.
  - Alkalinity and pH: integrated water sample sealed to minimize atmospheric exchange; Gran titration with a combination electrode; electrode calibration before each sampling.
  - NH4N and TON: colorimetric analysis with SEAL AQ2 after filtration; NH4N: indophenol blue method; TON: reduction of nitrate to nitrite with hydrazine, colorimetric detection.
  - TP: digestion with potassium persulphate, followed by molybdenum blue colorimetric analysis; UV-Vis read at 880 nm.
  - SIO2: colorimetric silicon measurement (silicomolybdenum blue) at 880 nm.
  - TOCA: filtration, methanol extraction, spectrophotometric analysis.
  - QA/QC notes: routine calibration, use of control standards, and reference materials described; UKAS accreditation noted for specific methods.

- Data structure and metadata considerations
  - Data are raw and not yet quality controlled; some fields flagged for detection limits (<LOD).
  - Double-entry validation performed for TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA by separate operators; visual validation via graphs by database manager.
  - Missing data attributable to weather, equipment limitations, or staff shortages.
  - Data provenance includes field notebooks, paper records, Excel entry, and subsequent database validation.

- Data governance, provenance, and funding
  - Data collection funded by Natural Environment Research Council (NERC) under UK-SCaPE; data validation supported under NERC/UKCEH programs.
  - References to standard methods that underpin analytical approaches (e.g., Mackereth et al. 1978; Mortimer 1981; Talling 1974).

- Implications for data strategy and management (Data Leaders perspective)
  - Highlights the need for a robust QC pipeline to convert raw data into validated datasets suitable for analysis and reporting.
  - Emphasizes comprehensive metadata and method documentation to support data discoverability, interoperability, and reproducibility.
  - Demonstrates data lineage from field collection to laboratory analyses to data entry and validation; suggests opportunities to formalize governance, standardize detection-limit handling, and improve metadata completeness.
  - Provides a clear example of a multi-parameter lake health dataset with documented QA procedures that could inform similar data products across networks and partnerships.