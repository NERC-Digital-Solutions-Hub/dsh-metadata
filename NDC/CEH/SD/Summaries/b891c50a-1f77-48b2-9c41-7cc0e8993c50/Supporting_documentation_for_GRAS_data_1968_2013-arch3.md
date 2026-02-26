# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

- Overview
  - Long-term monitoring dataset from Grasmere, Cumbria, England, covering 1968–2013 for surface temperature, surface oxygen, Secchi depth (water clarity), water chemistry, and phytoplankton chlorophyll a.
  - Sampling frequency ranged from weekly to fortnightly; some variables began in 1968; others later.
  - Data designed to support environmental health monitoring, policy scrutiny, and informing future decisions.

- Data provenance and stewardship
  - Collected initially by the Freshwater Biological Association; since 1989 by CEH and its predecessor Institute of Freshwater Ecology.
  - Data provided as raw (not quality controlled or calibrated) except for double entries from 2005 onwards; visual quality checks performed.
  - Dataset encourages public sharing of underlying data; governance/metadata considerations relevant for reuse.

- Variables and units (and data structure)
  - TEMP: surface temperature, degrees Celsius (TEMP)
  - OXYG: surface oxygen saturation, % air-saturation (OXYG)
  - SECC: Secchi depth (water clarity), metres (SECC)
  - ALKA: alkalinity, micrograms CaCO3 per litre (ALKA)
  - PH: pH (PH)
  - NH4N: ammonium, micrograms N per litre (NH4N)
  - NO3N: nitrate, micrograms N per litre (NO3N)
  - PO4P: soluble reactive phosphate, micrograms P per litre (PO4P)
  - TOTP: total phosphorus, micrograms P per litre (TOTP)
  - SIO2: dissolved reactive silicon, micrograms SiO2 per litre (SIO2)
  - TOCA: phytoplankton chlorophyll a, micrograms per litre (TOCA)
  - Data are provided in a CSV with columns: sdate (measurement date), variable/description, value, sign_if_LT_LOD (below detection limit indicator), flag (sampling location indicator).

- Sampling regime and methods
  - Water samples collected from a marked buoy at the deepest part of the lake; when the buoy was inaccessible, shore samples were taken (Flag 2).
  - Integrated sampling from 0–5 m when possible; otherwise not integrated.
  - Measurements span June 1968 to end of 2013.

- Quality control and limitations
  - Raw data not quality controlled or calibrated (except for some duplication checks from 2005 onward).
  - Values below detection limits indicated with a < sign in sign_if_LT_LOD.
  - Visual checks performed; no formal QC/QA described in the dataset metadata.

- Example uses and significance
  - Used in studies of lake carbon and nutrient dynamics, including:
    - Catchment productivity controls on CO2 emissions from lakes (Nature Climate Change, 2013).
    - Long-term phosphorus enrichment and phytoplankton ecology (Freshwater Biology, 2012).
    - Research on carbon-silicon geochemical cycles and lake temperatures (Scientific Reports, 2016; and related summaries in climate reports).

- Implications for monitoring frameworks
  - Strengths for policymakers and framework authors:
    - Demonstrates value of long-running, multi-parameter lake monitoring across physical, chemical, and biological indicators.
    - Provides a clear data structure and metadata description useful for governance and interoperability.
  - Key challenges to address in framework design:
    - Data gaps and access delays; raw data require processing and QC before use in decision-making.
    - Silos and data sharing barriers; need for open metadata and standardized data formats.
    - Metadata adequacy and variable definitions; documentation of detection limits and sampling protocols is essential.
    - Data transformation needs (unit harmonization, integration of multi-parameter time series) and transparent provenance.
  - Governance and data management considerations:
    - Clear data provenance (originators and custodians) and ongoing stewardship (CEH and predecessors).
    - Establishment of data quality assurance, calibration procedures, and versioning.
    - Public sharing policies balanced with data governance; explicit handling of below-detection values and sampling flags.
  - Practical takeaways for monitoring frameworks:
    - Include long-term, multi-indicator lake datasets as core components for policy evaluation.
    - Build robust metadata schemas, data dictionaries, and QC workflows to enhance reuse.
    - Design dashboards and reports that clearly communicate complex findings from integrated physical, chemical, and biological indicators.