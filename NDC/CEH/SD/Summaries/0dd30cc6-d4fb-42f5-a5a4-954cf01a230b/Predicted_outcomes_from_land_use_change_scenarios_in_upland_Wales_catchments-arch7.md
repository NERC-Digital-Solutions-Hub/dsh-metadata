# Predicted outcomes from land use change scenarios in upland Wales catchments

## Overview
- Study of predicted land-use change outcomes within 127 Duress sub-catchments in upland Wales.
- Produces two sets of results per scenario: predicted maximum change and predicted minimum change.
- Data delivered as eight CSV files (two per scenario) with a common structure; each CSV contains 9 columns describing changes per sub-catchment.

## Datasets and spatial context
- Study location: upland Wales catchments; analysis area bounded by Top Y: 364310, Right X: 344395, Bottom Y: 218295, Left X: 250915.
- Primary data inputs and reference layers used to predict outcomes:
  - Land Cover Map 2007 (LCM2007): 25 m raster; 23 classes reduced to 13 classes in Wales; cross-walked to Duress aggregation.
  - Agricultural Land Classification (ALC): standard framework; modified for non-agricultural land (inferred as poor soil/peat characteristics for non-agricultural areas); urban and freshwater classes integrated for consistency in some analyses.
  - Designated area layers: SSSI, SAC, SPA boundaries.
  - Ancient Woodland Inventory 2011; Historic landscapes; National Parks boundaries.
  - Ownership boundary layers: MoD, National Trust, Common Land, National Forest Estate boundaries.
- Note: Some data (e.g., MoD/National Trust) require permission for use.

## Analytical method
- For each narrative scenario (Agricultural Intensification, Business-as-Usual, Managed Extensification, Agricultural Abandonment):
  - Two expert-led rule-bases predict probabilities of maximum and minimum land-use change across the 127 sub-catchments.
  - Filtering logic uses three criteria:
    - Filter A: Agricultural Land Classification (ALC)
    - Filter B: Ownership
    - Filter C: Nature conservation status/designation
  - Probabilities are rated on a 1–5 scale (very unlikely to very likely) for each filter criterion.
  - Workflow steps (ArcGIS-based):
    - Identify relevant dataset information for the rule-base.
    - Create spatial units describing baseline and post-scenario land covers.
    - Generate unique identifiers for dataset-rule-base joins.
    - Create polygon layers and join the scenario rule-base.
    - Compute per-sub-catchment: baseline area/percentage, post-scenario area/percentage, and change (area and percentage).
    - Output is tabular (not spatial) data.

## Data structure and outputs
- For each scenario, two CSVs exist: one for minimum change and one for maximum change.
- All eight CSVs share the same 9 columns (per sub-catchment):
  - Sub catchment
  - Habitat type
  - Area Before (m^2)
  - Area Before (%)
  - Area After (m^2)
  - Area After (%)
  - Difference (m^2)
  - Difference (%)
  - Change (Yes/No)
- Descriptions indicate that the data capture baseline habitat extent, post-scenario extent, and quantified change per sub-catchment.

## Scenarios at a glance
- Agricultural Intensification
  - Focus on increased production; potential conversion of grassland types and reduction of hedges/woodland features to maximize production.
- Business-as-Usual
  - Continuation of current practices with emphasis on balancing productivity and environmental protection.
- Managed Extensification
  - Emphasis on carbon and biodiversity management; restoration of peatlands; expansion of woodlands and wetlands; reduced livestock pressure.
- Agricultural Abandonment
  - Decline in farming activity; rewilding trends with increased tree and heather cover; natural regeneration dominates land use.

## GIS implications and usage
- Outputs are tabular but derived from spatial rule-bases; can be mapped by joining CSV results to sub-catchment polygons.
- Useful for creating map-based data products that show predicted changes by sub-catchment and habitat type under each scenario.
- Scenarios and datasets align with ArcGIS-based workflows for analysis, visualization, and communication to policy colleagues, clients, or the public.

## Important notes and considerations
- Modified ALC used for some scenarios; original ALC used for others; careful alignment needed when integrating results.
- The eight CSV files provide non-spatial summaries; to produce maps, join results back to spatial catchment boundaries.
- Data restrictions apply for certain ownership and designation layers; ensure permissions are in place for reuse.