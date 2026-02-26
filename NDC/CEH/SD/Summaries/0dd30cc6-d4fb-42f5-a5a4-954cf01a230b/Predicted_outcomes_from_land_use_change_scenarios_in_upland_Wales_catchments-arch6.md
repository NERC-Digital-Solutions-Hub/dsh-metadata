# Predicted outcomes from land use change scenarios in upland Wales catchments

- Purpose and scope
  - Describes predicted land-use-change outcomes for upland Wales catchments under four scenarios and for both maximum and minimum change.
  - Outputs are tabular (CSV) summaries per sub-catchment, not spatial datasets.

## Datasets included

- Predicted Maximum Change datasets
  - Agricultural Intensification: Duress_intensification_max_area.csv
  - Business-as-Usual: Duress_bau_max_area.csv
  - Managed Extensification: Duess_managed_e_max_area.csv
  - Agricultural Abandonment: Duress_abandoment_max_area.csv
- Predicted Minimum Change datasets
  - Agricultural Intensification: Duress_intensification_min_area.csv
  - Business-as-Usual: Duress_bau_min_area.csv
  - Managed Extensification: Duress_managed_e_min_area.csv
  - Agricultural Abandonment: Duress_abandonment_min_area.csv

## Collection method and data sources

- Study area: uplands of Wales; 127 Duress sub-catchments.
- Spatial infrastructure (for context, not all datasets are spatial outputs)
  - Land Cover Map 2007 (LCM2007) at 25 x 25 m resolution used to assign broad habitats.
  - Aggregated Land Cover Map 2007 classes ( Wales: 11 applicable classes used).
  - Agricultural Land Classification (ALC) with a modified non-agricultural category for consistency with other datasets.
  - Designated area layers: SSSI, SAC, SPA; Ancient Woodland Inventory; Historic landscapes; National Parks.
  - Ownership boundary layers: MoD, National Trust, Common Land, National Forest Estate boundaries.
- Spatial extent: defined by a bounding box (Top Y 364310, Right X 344395, Bottom Y 218295, Left X 250915) within uplands of Wales.
- Methodological note: existing spatial datasets were incorporated; data manipulation occurs in ArcGIS.

## Analytical method

- Two expert-led rule-bases per scenario to predict probabilities of maximum and minimum land-use change across the 11 land-cover types, considering:
  - Agricultural Land Classification (ALC)
  - Ownership
  - Designation/Nature conservation status
- Probability scale (1–5) with qualitative labels:
  - 0: Very unlikely
  - 2: Unlikely
  - 3: Possible
  - 4: Likely
  - 5: Very likely
- Maximum change analysis driven by ALC class filter; minimum change analysis driven by ALC, ownership, and designation.
- Stepwise workflow (ArcGIS)
  - Identify relevant data for rule-bases
  - Create spatial units for maximum/minimum change per catchment
  - Create unique identifiers and perform joins
  - Compute baseline (before) and after-change areas and percentages
  - Compute change in area and percentage; produce tabular output
- Output format: tabular data; no spatial dataset outputs are produced.

## Data structure and outputs

- For each scenario, two CSVs (minimum and maximum) summarize predicted land-cover change outcomes per sub-catchment.
- All eight CSVs share the same 9 columns:
  - Sub catchment
  - Habitat type
  - Area Before (m^2)
  - Area Before (%)
  - Area After (m^2)
  - Area After (%)
  - Difference (m^2)
  - Difference (%)
  - Change (Yes/No)

## Scenario descriptions and interpretation

- Agricultural Intensification
  - Focus on increased production (e.g., conversion of temporary to permanent grassland, fodder crops); potential reduction of hedges and linear features to maximize production.
  - Descriptions and expectations draw from Prosser et al. (2014) and the Upland Scenarios project.
- Business-as-Usual
  - Production-focused but balanced with environmental protection; potential continuation of overgrazing and common land use for agriculture.
  - Based on Prosser et al. (2014).
- Managed Extensification
  - Carbon and biodiversity-centered management; restoration of peatlands, expansion of wetlands and woodlands to boost biomass and regulate soil carbon exports.
  - Emphasizes land-management shifts toward biodiversity and carbon outcomes (Prosser et al. 2014).
- Agricultural Abandonment
  - Policy/market pressures lead to farm decline and rewilding; increased tree and heather cover; reduced farming activity (Prosser et al. 2014).

## Additional information and provenance

- Full scenario descriptions and context are drawn from Prosser, Pagella, and Durance (eds.) 2014 Upland Scenarios: what will the future look like? Duress Project report card.
- The data resource includes references to:
  - LCM2007 (UK Land Cover Map)
  - Agricultural Land Classification (modified for non-agricultural areas)
  - Designated area and ownership boundary datasets
- Output is designed to support data exploration and product development, enabling end users to self-serve via the provided CSV summaries and associated scenario descriptions.