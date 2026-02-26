# Bird data fields and explanations

- Purpose and scope
  - This dataset provides identifiers, biological measurements, and chemical concentration data from post-mortem bird analyses, suitable for creating map-based data visualisations and spatial analyses.

- Key variables and what they mean
  - Identification
    - CEH_BIRD_CODE: Unique identifier assigned to bird on receipt.
  - Demographics and biology
    - SEX: Sex of bird (Male or Female).
    - AGE_CLASS: Age classification (Adult or Juvenile; Juveniles defined as birds hatched in the current or previous calendar year).
    - BODY_CONDITION: Condition (Starved or Non-starved; starved defined as lacking fat deposits at post-mortem).
  - Morphometrics
    - BOGY_WEIGHT_G: Bird weight at post mortem (grams).
    - LIVER_WT_G: Liver weight (grams).
    - PERCENT_LIPID_IN_LIVER: Percent lipid in liver (%).
  - Temporal information
    - MONTH_DIED: Month found deceased (seasonal units: April–Sept or Oct–Mar).
    - YEAR_BIRD_DIED: Year found deceased.
  - Contaminant and chemical data
    - BDE47, BDE99, BDE100, BDE138, BDE153, BDE154, BDE183: Concentrations of individual BDEs (ng/g lipid weight).
    - TOTAL: Concentrations of total BDEs (ng/g lipid weight).
  - Notes on data values
    - For BDE measurements, Not Detected (ND) values were assigned a value below the limit of detection (LoD) using the Hesel method; similar notes apply to all BDE-related fields.

- Data quality and handling
  - Data are drawn from multiple sources, which may introduce variability in standards and resolutions.
  - ND/LOD handling follows the Hesel method, implying some values are imputed if not detected.
  - Several fields have categorical or qualitative units (e.g., sex, age class, seasonality) that should be harmonised when integrating with other datasets.
  - Temporal fields (MONTH_DIED, YEAR_BIRD_DIED) enable seasonal and year-based mapping of results.

- How this dataset supports GIS and map-based analysis
  - Enables spatial visualisation of contaminant burden (BDEs) in birds across locations.
  - Allows mapping of biological indicators (body condition, liver metrics, age structure) to explore spatial patterns in health and exposure.
  - Temporal fields permit choropleth or point-time visualisations by month or year.
  - Can be joined to other spatial layers (e.g., habitat, pollution sources) using CEH_BIRD_CODE as a key.

- Practical notes for GIS specialists
  - Consider deriving a derived BDE_Total if not already provided, by summing relevant individual BDEs where appropriate.
  - Standardise units and handle ND values consistently to avoid misinterpretation in maps.
  - Create season-based categories from MONTH_DIED (e.g., spring, summer, autumn, winter) to enhance seasonal analyses.
  - Validate that data sources align on consistent definitions for sex, age class, and body condition before joining with spatial data.
  - Ensure proper handling of small sample sizes or high missing data in certain locations when visualising results.