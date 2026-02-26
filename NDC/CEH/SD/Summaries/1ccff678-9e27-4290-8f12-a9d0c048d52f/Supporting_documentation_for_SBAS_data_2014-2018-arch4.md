# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2014 to 2018

- Overview
  - Part of an ongoing fortnightly monitoring dataset for the South Basin of Windermere, Cumbria, England (2014–2018).
  - Covers surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH, ammonium (NH4N, µg N L−1), nitrate (NO3N, µg N L−1), soluble reactive phosphate (PO4P, µg P L−1), total phosphorus (TOTP, µg P L−1), dissolved reactive silicon (SIO2, µg SiO2 L−1), and phytoplankton chlorophyll a (TOCA, µg L−1).
  - Water samples are integrated from 0–7 m; measurements taken from a boat at a marked buoy location in the deepest part of the lake.
  - Data cover January 2014 through end of 2018.

- Data Content and Units
  - Variables and units are explicitly defined in the dataset (see below for structure).
  - Values below detection limits are indicated with a < sign in the corresponding field.

- Sampling Regime and Collection Methods
  - Fortnightly sampling regime as part of long-term monitoring.
  - Sample and measurement details align with a fixed geographical target (deepest part of the lake, buoy).

- Data Structure and Access
  - Delivered as a comma-separated values (CSV) file.
  - Columns include:
    - Date: measurement date.
    - Description (variable): e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA.
    - Value: numeric measurement for each variable.
    - Sign (if<LOD): indicates if value is below the detection limit.
  - Variable descriptions provide the specific units:
    - TEMP: degrees Celsius
    - OXYG: % air-saturation
    - SECC: metres
    - ALKA: µg CaCO3 per litre
    - pH: unitless
    - NH4N: µg N per litre
    - NO3N: µg N per litre
    - PO4P: µg P per litre
    - TOTP: µg P per litre
    - SIO2: µg SiO2 per litre
    - TOCA: µg per litre

- Quality Control and Limitations
  - Data are raw and have not yet undergone formal quality control or calibration.
  - Visual double-entry verification has been performed.
  - Missing data are primarily due to weather conditions or staff shortages.
  - Users should account for potential measurement biases prior to analysis and inter-dataset comparisons.

- Provenance and Funding
  - Collected under Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
  - Dataset has supported multiple recent publications across climate, limnology, and ecological informatics.

- Usage and Impact
  - Used in studies on climate and storm impacts on lakes, temperature variability, hydrological and chemical dynamics, and ecological indicators.
  - Examples of related publications illustrate the dataset’s applicability to long-term ecological and climate-related research.

- Data Governance Considerations (for Data Leaders)
  - QC status: plan and implement formal QC/calibration workflows to upgrade raw data to validated datasets.
  - Metadata completeness: ensure detailed documentation of sampling methods, instrument specifics, detection limits, and location accuracy to improve discoverability and interoperability.
  - Data standards and interoperability: align with broader lake/limnology data standards to facilitate cross-site comparisons and integration with other Windermere basins or regional datasets.
  - Gap analysis and updates: establish a schedule for data updates, handling of missing values, and maintenance of detection-limit indicators.
  - Accessibility and discoverability: maintain clear data licensing, access instructions, and cross-reference to related datasets and publications to maximise reuse.
  - Coordination with data community: consider broader sector coordination to reduce duplication and improve data sharing practices across partners.