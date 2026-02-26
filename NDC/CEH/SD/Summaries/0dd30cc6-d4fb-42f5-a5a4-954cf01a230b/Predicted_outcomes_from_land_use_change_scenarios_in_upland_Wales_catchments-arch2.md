# Predicted outcomes from land use change scenarios in upland Wales catchments

## Overview
- Presents predicted land-use change outcomes for upland Wales catchments under four scenarios, with both maximum and minimum change assessments.
- Outputs are organized into eight CSV datasets (two per scenario) containing standardized, catchment-level results suitable for monitoring environmental health and policy performance.

## Datasets included
- Predicted Maximum Change
  - Agricultural Intensification: Duress_intensification_max_area.csv
  - Business-as-Usual: Duress_bau_max_area.csv
  - Managed Extensification: Duess_managed_e_max_area.csv
  - Agricultural Abandonment: Duress_abandoment_max_area.csv
- Predicted Minimum Change
  - Agricultural Intensification: Duress_intensification_min_area.csv
  - Business-as-Usual: Duress_bau_min_area.csv
  - Managed Extensification: Duress_managed_e_min_area.csv
  - Agricultural Abandonment: Duress_abandonment_min_area.csv

## Collection method and data sources
- Location: Duress study catchments in upland Wales; data spatially bounded by Top 364310, Right 344395, Bottom 218295, Left 250915.
- Existing spatial datasets used to predict outcomes:
  - Land Cover Map 2007 (LCM2007): 25 x 25 m rasters, 13 classes in Wales (11 applied); aggregation details provided.
  - Agricultural Land Classification (ALC): modified non-agricultural areas (mostly forestry/woodland) inferred to be poor soil, resembling ALC grade 5; urban and freshwater areas integrated with ALC to ensure correspondence.
  - Designated areas: SSSI, SAC, SPA; Ancient Woodland Inventory 2011; Historic Landscapes; National Parks.
  - Ownership boundaries: MoD land; National Trust land; Common Land; National Forest Estate boundaries.
  
## Analytical method
- Scenarios are implemented via two expert-led rule-bases per scenario to predict probabilities of maximum and minimum land-use change across 127 Duress sub-catchments.
- Filters and rules (probability ratings 1–5) used:
  - Filter A: Agricultural Land Classification (ALC)
  - Filter B: Ownership
  - Filter C: Nature conservation status (designation)
- Maximum change: determined by ALC filter only.
- Minimum change: determined by ALC, ownership, and designation.
- Process steps (summary):
  - Identify relevant dataset information for rule-bases.
  - Create spatial units describing baseline and post-scenario land cover/ALC for each catchment.
  - Join scenario rule-base to data layers with unique identifiers.
  - Compute baseline (current) and post-scenario land cover areas and percentages, and the differences.
  - Output as tabular data (not spatial), implemented in ArcGIS.
  
## Details of data structure
- For each scenario, two CSVs summarize predicted land cover change outcomes for each Duress sub-catchment (minimum and maximum).
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

## Scenario descriptions
- Agricultural Intensification
  - Increased production emphasis; potential conversion of temporary grassland to permanent grassland or fodder crops; possible reduction of hedges, woodland strips, isolated trees, shrubs, or river margins to maximise production (Prosser et al. 2014).
- Business-as-Usual
  - Production-focused management with ongoing tension between agricultural productivity and environmental protection (e.g., continued overgrazing, maintenance of common land for production) (Prosser et al. 2014).
- Managed Extensification
  - Carbon and biodiversity-focused management; restoration of peatlands; expansion of wetlands and woodlands to enhance biomass and regulate soil carbon exports (Prosser et al. 2014).
- Agricultural Abandonment
  - Policy and market pressures lead to reduced farming activity and rewilding; increased tree and heather cover as land reverts to less intensive use (Prosser et al. 2014).

## How this supports environmental monitoring
- Provides standardized, comparable, catchment-scale projections across multiple plausible futures.
- Facilitates assessment of policy performance and environmental health over time by offering clear, tabular outputs that can be integrated into reporting portals and GIS workflows.
- Enables data-driven scrutiny by combining these outputs with other datasets to enhance monitoring value beyond single-use applications.