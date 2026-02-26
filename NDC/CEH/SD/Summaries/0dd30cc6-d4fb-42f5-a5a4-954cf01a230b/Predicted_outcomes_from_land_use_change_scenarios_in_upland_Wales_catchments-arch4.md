# Predicted outcomes from land use change scenarios in upland Wales catchments

- Purpose and scope
  - Documents predicted land-use change outcomes under eight scenarios across upland Wales sub-catchments (minimum and maximum changes for each scenario).
  - Data are organized into two CSVs per scenario (minimum and maximum), totaling eight CSVs.

- Datasets (file-level overview)
  - Predicted Maximum Change:
    - Agricultural Intensification: Duress_intensification_max_area.csv
    - Business-as-Usual: Duress_bau_max_area.csv
    - Managed Extensification: Duess_managed_e_max_area.csv
    - Agricultural Abandonment: Duress_abandoment_max_area.csv
  - Predicted Minimum Change:
    - Agricultural Intensification: Duress_intensification_min_area.csv
    - Business-as-Usual: Duress_bau_min_area.csv
    - Managed Extensification: Duress_managed_e_min_area.csv
    - Agricultural Abandonment: Duress_abandonment_min_area.csv
  - All eight CSVs share the same 9 columns and report, per sub-catchment, habitat area before/after, percentage covers, differences, and a Change Yes/No flag.

- Collection methods and data sources
  - Study area: uplands of Wales; sub-catchments defined as Duress units.
  - Spatial data inputs:
    - Land Cover Map 2007 (LCM2007): 25 x 25 m rasters; 13 classes in Wales (aggregation detailed in the study).
    - Agricultural Land Classification (ALC): used to assess land-use potential; modified ALC for non-agricultural areas in most analyses (with notes on specific scenarios).
    - Designated area layers: SSSI, SAC, SPA boundaries.
    - Ancient Woodland Inventory, Historic Landscapes, National Parks boundaries.
    - Ownership boundaries: MoD, National Trust, Common Land, National Forest Estate (with permission requirements for MoD and National Trust data).
  - Data rights: multiple datasets are Crown copyright or licensed; some ownership layers require permission.

- Analytical approach and workflow
  - Two expert-led rule-bases translate narrative scenarios into probabilities of land-use change for 11 land-cover types across 127 sub-catchments.
  - Filtering criteria:
    - Filter A: Agricultural Land Classification (ALC) as primary constraint.
    - Filter B: Ownership (investment/resources and governance aspects).
    - Filter C: Nature conservation status (designation constraints).
  - Probability scale (1-5): 0 (very unlikely) to 5 (very likely) to rate change likelihood.
  - Processing steps (ArcGIS-based):
    - Identify relevant data for rule-bases; create spatial units for maximum/minimum change; generate identifiers; join rule-base to layers.
    - Compute baseline (current) habitat area and percentage; apply scenario to obtain Area After and Area After (%); compute differences and Change flag.
    - Output provided as tabular data (not spatial datasets).

- Data structure and content of the outputs
  - For each scenario, two CSVs (minimum and maximum) summarise predicted land-cover change per sub-catchment.
  - Each CSV has 9 columns shared across all eight files.
  - Columns (example definitions):
    - Sub catchment: name of the Duress sub-catchment.
    - Habitat type: habitats present in the sub-catchment.
    - Area Before (m^2): habitat extent before the scenario.
    - Area Before (%): pre-scenario habitat share.
    - Area After (m^2): habitat extent after the scenario.
    - Area After (%): post-scenario habitat share.
    - Difference (m^2): change in habitat area.
    - Difference (%): change in share (increase/decrease).
    - Change (Yes/No): whether there was a change.

- Scenario descriptions and references
  - Agricultural Intensification: production-focused shift (e.g., temporary to permanent grassland, hedgerow reductions, etc.).
  - Business-as-Usual: continued over-grazing and common land use with some environmental considerations.
  - Managed Extensification: focus on peatland restoration, wetlands, and woodlands for carbon/biodiversity; landscape-scale management for ecosystem services.
  - Agricultural Abandonment: rewilding trends with natural regeneration and increased tree/heather cover.
  - Full scenario descriptions are documented in Prosser et al. (2014) Upland Scenarios; additional details for the datasets are provided within the study.
  - Note: Some dataset filenames show minor inconsistencies (e.g., Duress vs Duess) that should be reconciled when aligning files.

- Practical considerations for data leadership
  - Data provenance and metadata are tied to multiple external sources with licensing and permission requirements (ownership layers and MoD/National Trust boundaries).
  - Analyses combine raster land-cover data, classified land capability, and governance/designation constraints to produce non-spatial tabular outputs; no spatial data is delivered with the results.
  - The modified ALC approach is applied selectively depending on the scenario, which has implications for comparability across all eight outputs.
  - Potential uses include policy planning, scenario testing, and stakeholder engagement to understand habitat and land-use changes under different upland management futures.