# The Land Cover Map of Great Britain

## Overview
- The Land Cover Map of Great Britain (LCMGB) is an automated Landsat TM-based classification at 25 m resolution.
- It records 25 target cover types (with 18 semi-natural vegetation types described in the document) by combining summer and winter imagery to improve accuracy.
- The map aims to detail cover types, map resolution, and how classes are depicted, with cross-references to related surveys.

## Data, Resolution, and Registration
- Spatial resolution: 25 m grid; 25 target classes (also available as a 1 km summary) and 17 key classes as alternatives.
- Feature scale: minimum mappable unit is effectively about 1 ha (though analyses can detect features down to ~0.125 ha when isolated pixels are removed).
- Registration accuracy: Landsat-derived maps aligned to 1 km field squares show an average displacement of about 20 m (0.8 pixels); most squares required little or modest shifts.
- Boundary and geometry: misregistration and mixed boundary pixels exist; about 40% of pixels are boundary-adjacent; excluding boundary pixels raises correspondence to ~71%.
- Temporal considerations: some differences reflect real cover changes between surveys (e.g., pasture ploughed, hay removed), affecting accuracy estimates.

## Classification Accuracy
- Ground-truth data are scarce and often not directly comparable due to differing methodologies and objectives across surveys.
- Overall, a realistic accuracy for LCMGB is estimated at 80–85%, accounting for methodological differences and temporal changes.
- Comparisons with independent ground reference data (508 1 km squares) show varying correspondences due to differing class definitions (e.g., hydrological vs botanical definitions, and how grass/weed mixtures are segmented).
- The biggest single error source is misclassification of mixed boundary pixels; when boundary pixels are excluded, correspondence improves.

## Land Cover Classes and Structure
- Two-tier classification:
  - 25 target cover-types (detailed, mapping values 1–25; also includes a 0 unclassified category).
  - 17 key cover-types (A–Q) as a coarser, more consistently mapped set, available in 1 km summary data and used as standard in the Countryside Information System.
- 25 m data: each grid cell contains a value 0–25 identifying the target cover-type.
- 1 km data: comprises 25 layers; within each layer, a 1 km cell holds the percentage of that target type within the cell (e.g., layer 10 value indicates the percent coverage of target type 10 in that 1 km cell).
- 17 key classes are designed to be ecologically meaningful and consistently mappable nationwide; some rare classes may be inconsistently mapped and can be aggregated into 17 key classes for reliability (Table 1 provides the mapping between 25 target classes and 17 key classes).
- Examples of major classes and concepts:
  - Sea / Estuary (1) and Inland Water (2)
  - Beach / Mudflat / Cliffs (3) and Saltmarsh (4)
  - Pasture / Meadow / Amenity Grass (6) with subtypes: Mown/Grazed Turf (6) and Meadow/Verge/Semi-natural sward (7)
  - Marsh / Rough Grass (8), Ruderal Weed (19), Felled Forest (23), Rough/Marsh Grass (8)
  - Bracken (12), Grass Heath (5), Moorland (9), Bog (17), Deciduous Woodland (15), Coniferous Woodland (16)
  - Tilled Land (18), Suburban/Rural Development (20), Urban Development (21)
  - Inland Bare Ground (22) and Unclassified (0)
- Subclasses and regional nuances (e.g., lowland vs. upland, dune grass vs. grass heath) are acknowledged; some areas may be aggregated for consistency or due to limited discriminative power in imagery.

## How to Use the Classification
- Available products:
  - 25-class dataset at 25 m resolution (values 0–25) corresponding to the 25 target cover-types.
  - 1 km summary dataset with 25 layers, each representing the percentage of a target cover-type in each 1 km cell.
  - 17-class dataset available as 1 km summary data (uppercase A–Q) for more consistent national mapping.
  - Customizable outputs: users can aggregate 25 classes into fewer categories or generate tailor-made aggregations in GIS.
- Data accessibility:
  - 25 target classes are provided as standard.
  - 17 key classes (A–Q) are provided as standard in the Countryside Information System.
  - Non-standard/custom data options are available (e.g., selecting a subset of classes).
- Practical considerations:
  - The 25 m data is best for detailed mapping; 1 km data is suitable for broader analyses and national summaries.
  - Subclass distinctions (e.g., different arable crops) can be reinterpreted or aggregated digitally based on user objectives, acknowledging potential inconsistent separations due to image date and spectral similarity.

## Enduring caveats and interpretation guidance
- Class definitions and mapping can differ from other surveys (e.g., hydrological vs botanical definitions for bogs or boundary delineations between grassland types), so cross-survey comparisons should be done with caution.
- Some rare or ephemeral classes (e.g., ruderal weeds) may be inconsistently mapped due to limited training data; aggregation to 17 key classes can improve consistency.
- Coastal and tidal influences create discrepancies around shorelines due to imaging tide levels; mapping reflects the tide level on imaging days.
- The minimum mappable area is effectively around 1 ha in practice; extremely small features may not be depicted.
- Ground truth quality varies, and achieving exact validation is challenging; results should be interpreted as average error rates with acknowledged regional variation.

## References
- Congalton, R.G. 1991. A review of assessing the accuracy of classifications of remotely sensed data.
- Fuller et al. 1989–1995 series on Landsat TM classification, accuracy assessments, and data availability.
- Wyatt et al. 1994. Comparison of land cover definitions.
- Townshend 1983. Effects of spatial resolution on classification.
- Additional methodological and contextual references listed in the document.