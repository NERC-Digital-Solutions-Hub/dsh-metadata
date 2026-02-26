# Predicted outcomes from land use change scenarios in upland Wales catchments

- Datasets
  - Eight CSV files summarize predicted land cover change outcomes, two per scenario (maximum and minimum change) across four scenarios:
    - Predicted Maximum Change: Duress_intensification_max_area.csv
    - Predicted Maximum Change: Duress_bau_max_area.csv
    - Predicted Maximum Change: Duess_managed_e_max_area.csv
    - Predicted Maximum Change: Duress_abandoment_max_area.csv
    - Predicted Minimum Change: Duress_intensification_min_area.csv
    - Predicted Minimum Change: Duress_bau_min_area.csv
    - Predicted Minimum Change: Duress_managed_e_min_area.csv
    - Predicted Minimum Change: Duress_abandonment_min_area.csv
  - All eight CSVs share the same 9 columns.

- Collection method
  - Study area: uplands of Wales; data arranged for 127 Duress sub-catchments.
  - Datasets used to predict outcomes:
    - Land Cover Map 2007 (LCM2007): 25 x 25 m raster, 13 classes in Wales (aggregated to 11 applied classes in this study). Mapping details provided in a conversion table.
    - Agricultural Land Classification (ALC): framework for long-term agricultural suitability; a modified ALC was used for some scenarios to include non-agricultural land, urban, and freshwater when aligning datasets.
    - Designated area layers: Sites of Special Scientific Interest (SSSI), Special Areas of Conservation (SAC), Special Protection Areas (SPA).
    - Ancient Woodland Inventory (2011), Historic landscapes, National Parks.
  - Ownership boundary layers: MoD land, National Trust land, Common Land, National Forest Estate boundaries (some require permission for use).

- Analytical method
  - For each narrative scenario (as per Prosser et al. 2014), two expert-led rule-bases predict probabilities of maximum and minimum land use change within each sub-catchment.
  - Filtering approach uses three criteria:
    - Filter A: Agricultural Land Classification (ALC)
    - Filter B: Ownership
    - Filter C: Nature conservation designation/status
  - Probabilities are rated on a 1-5 scale (very unlikely to very likely change).
  - Processing steps (a–g) cover data extraction, spatial unit creation, rule-base joins, and calculation of baseline and post-scenario land cover areas and percentages, plus differences. Output is tabular (not spatial).

- Details of data structure
  - For each scenario, two CSVs exist (minimum and maximum change) summarising predicted outcomes for each sub-catchment.
  - All eight CSVs use the same 9 columns:
    - Sub catchment, Habitat type, Area Before (m^2), Area Before (%), Area After (m^2), Area After (%), Difference (m^2), Difference (%), Change (Yes/No).
  - Content structure within the datasets reflects:
    - Sub catchment name and habitat type
    - Baseline area and percentage before the scenario
    - Area and percentage after the scenario
    - Change in area and percentage
    - A flag indicating whether there was a change

- Further information (scenarios and data fields)
  - Agricultural intensification
    - Scenario rationale and characteristics (e.g., conversion of temporary to permanent grassland, hedgerow reduction) with fields describing sub-catchment, habitat type, area before/after (m^2 and %), differences, and change flag.
  - Business-as-Usual
    - Scenario characteristics (ongoing overgrazing, maintained common land) with the same field structure.
  - Managed Extensification
    - Focus on carbon and biodiversity management (peatlands, wetlands, woodlands) with the same field structure.
  - Agricultural Abandonment
    - Scenario features (rewilding, natural regeneration, tree/heather cover increase) with the same field structure.

- Implications for monitoring and policy decisions
  - The dataset provides scenario-based, per-sub-catchment indicators of expected land cover shifts under different policy/farming paradigms, useful for:
    - Designing and evaluating environmental health monitoring indicators
    - Informing future policy decisions and governance around upland land use
  - Considerations for monitoring frameworks
    - Data availability and access: multiple underlying datasets; some boundaries require permissions; ensure timely access to metadata and provenance.
    - Metadata and data quality: likelihood of data gaps or aggregation issues; need for clear metadata to assess suitability.
    - Data governance and openness: some datasets require sharing guidelines; ensure appropriate sharing while respecting restrictions.
    - Communication of findings: outputs are tabular probabilities and changes; translate into understandable policy-relevant indicators and dashboards.