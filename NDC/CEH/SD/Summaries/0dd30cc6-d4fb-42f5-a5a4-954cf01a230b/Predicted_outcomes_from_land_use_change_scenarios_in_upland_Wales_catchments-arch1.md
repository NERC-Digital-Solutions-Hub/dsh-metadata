# Predicted outcomes from land use change scenarios in upland Wales catchments

## Overview
- Predicts land use change outcomes under four upland scenarios (Agricultural Intensification, Business-as-Usual, Managed Extensification, Agricultural Abandonment) for 127 Duress sub-catchments.
- For each scenario, provides both maximum and minimum predicted change as two CSV datasets each, totaling eight CSVs, all with 9 columns.
- Outputs are tabular summaries of habitat area before and after, with change metrics, rather than spatial datasets.

## Datasets included
- Predicted Maximum Change datasets (one per scenario) and Predicted Minimum Change datasets (one per scenario).
- File titles include:
  - Predicted Maximum Change
  - Duress_intensification_max_area.csv
  - Duress_bau_max_area.csv
  - Duess_managed_e_max_area.csv
  - Duress_abandoment_max_area.csv
  - Predicted Minimum change
  - Duress_intensification_min_area.csv
  - Duress_bau_min_area.csv
  - Duress_managed_e_min_area.csv
  - Duress_abandonment_min_area.csv
- All eight CSVs share the same 9 columns.

## Collection and data sources
- Geographic scope: uplands of Wales; 127 Duress sub-catchments.
- Data sources used to predict outcomes:
  - Land Cover Map 2007 (LCM2007): 25 m x 25 m raster; 13 aggregated classes ( Wales) mapped to 11 relevant classes; source details and aggregation approach described.
  - Agricultural Land Classification (ALC): MAFF 1988 framework; modified for non-agricultural land using soil and ecological site classifications; urban and freshwater areas integrated to align datasets; used differently across scenarios (see below).
  - Designated area layers: SSSI, SAC, SPA, Ancient Woodland Inventory 2011, Historic landscapes, National Parks.
  - Ownership boundary layers: MoD land, National Trust land, Common Land, National Forest Estate boundaries.
  
## Analytical method
- Scenario translation: Each narrative scenario (as per Prosser et al. 2014) is translated into two expert-led rule-bases predicting probabilities of maximum and minimum land-use change across 11 land-cover types within each sub-catchment.
- Filtering and variables:
  - Filter A: Agricultural Land Classification (ALC) class
  - Filter B: Ownership type
  - Filter C: Nature conservation status (designation)
- Probability scales (1–5):
  - 0: Very low probability
  - 1: Very low
  - 2: Low
  - 3: Medium
  - 4: High
  - 5: Very high
- Workflow (ArcGIS-based):
  - Identify applicable information, create spatial units for max and min change, join rule-bases, assign identifiers, and generate two polygon layers.
  - For each sub-catchment, compute:
    - Baseline area and percentage by land-cover type
    - Post-scenario area and percentage
    - Change in area (m^2) and percentage
    - Change yes/no flag
  - Output format is tabular (no spatial output datasets).
  
## Details of data structure
- For each scenario, two CSVs summarise predicted land-cover change outcomes per sub-catchment (minimum and maximum).
- All eight CSVs have the same 9 columns.
- Columns (example descriptions):
  - Sub catchment
  - Habitat type
  - Area Before (m^2)
  - Area Before (%)
  - Area After (m^2)
  - Area After (%)
  - Difference (m^2)
  - Difference (%)
  - Change (Yes/No)
- Scenario-specific descriptions:
  - Agricultural Intensification: increases in production-focused practices (e.g., conversion of temporary to permanent grassland, hedgerow reductions, etc.).
  - Business-as-Usual: ongoing overgrazing and maintenance of common land for production with environmental tensions.
  - Managed Extensification: carbon/biodiversity focus; restoration of peatlands; expansion of wetlands and woodlands.
  - Agricultural Abandonment: decline in farming activity; rewilding tendencies with increased tree and heather cover.
- Each scenario entry includes a narrative description of the scenario and a tabular record for each sub-catchment with habitat type and area metrics both before and after the scenario.

## Outputs and interpretation
- The primary outputs are eight tabular CSV datasets (min and max for each scenario), intended for analysis of how land cover could change under different policy and management futures.
- Outputs enable assessment of predicted magnitude and direction of habitat change, as well as how changes vary by sub-catchment, initial habitat type, and regulatory/designation context.