# The Land Cover Map of Great Britain

## Overview
- Produced from supervised maximum likelihood classifications of Landsat Thematic Mapper data, yielding a 25 m grid with 25 target land cover types (including sea, inland water, beaches, bare ground, developed/arable land, and 18 semi-natural vegetation types).
- Combines summer and winter imagery to improve accuracy; about 88% of Britain classified from combined data, 12% from single-date data; minimal cloud and offshore island gaps.
- Aims to detail map classes, resolution, and depiction, and to relate the map to results from other surveys.

## Spatial resolution, registration, and data structure
- Minimum mappable feature size from TM data is about 3–5 ha; in practice, features as small as 1 ha can be resolved, with finer patterns (e.g., roads, fields) visible down to 0.125 ha (2 pixels).
- Landsat-derived maps registered to 1 km field squares with average displacement ~0.8 pixels (20 m); most squares aligned without shift; a minority required minor adjustments.
- Data available in two classifications: 25 target classes (25 m resolution) and 17 key classes (coarser aggregation). The 25-class dataset can be viewed as 25 m grid cells labeled 0–25; a 1 km summary dataset provides per-class percentages within each 1 km cell. The 17-class dataset is also available as 1 km summary data.
- The 25 m dataset is standard; 1 km summaries and 17-class aggregations offer flexibility for consistency and analysis.

## Classification accuracy and validation
- Ground-truth data used for quality checks, but ground-truth definitions vary; exact validation is challenging due to differences in class definitions and methods.
- Comparisons with independent 1 km ground reference data (508 squares) show accuracy varying with the detail level; overall correspondence about 67% (across all comparisons), rising to ~71% when boundary pixels are excluded, and up to ~76% if time-based changes are allowed, or ~82% excluding boundaries when accounting for changes.
- A realistic overall accuracy is likely in the range of 80–85%.
- Differences between field and satellite classifications often reflect definitional differences (e.g., hydrological vs botanical definitions) and temporal changes between surveys. See Fuller et al. (1994a) and Wyatt et al. (1994) for more detail.

## Land cover classes and classification approach
- The classification uses 25 Landsat-derived target cover-types, with 17 key classes available as an aggregation for consistency and operational use.
- The 25 target classes cover a broad spectrum including water, coast, vegetation, grasslands, heaths, moorlands, bogs, woodlands, arable land, and developed land. The 17 key classes consolidate some rarer or ambiguously mapped types to improve national consistency.
- The 25-class dataset is provided in two resolutions (25 m and 1 km summary). The 17-class dataset is provided as 1 km summary data; non-standard/customized aggregations are possible.
- The minimum mappable area is effectively around 1 ha (though the official minimum is two pixels, 0.125 ha).
- Regional distinctions (e.g., lowland vs upland) exist for many classes, and some regional inconsistencies may occur for rarer types. Subclasses (e.g., specific crops) are aggregated to ecologically meaningful target classes for reliability.

## Data products, usage, and customization
- The 25-class dataset (25 m) and 1 km summary data, plus the 17-class dataset, are designed for broad use in policy, planning, ecology, and GIS analyses.
- The 17-class set is the standard in the Countryside Information System; 25-class data remain the default, with 17-class aggregations available to improve consistency.
- Users can perform tailor-made aggregations or request customized data (e.g., selecting a subset of cover-types) depending on objectives and required accuracy.

## Key class descriptions and examples
- Major categories (represented in the 25-class system) include:
  - Sea / Estuary; Inland Water; Beach / Mudflat / Cliffs; Saltmarsh
  - Grass Heath; Pasture / Meadow / Amenity Grass (with subtypes: Mown/Grazed Turf and Meadow/Verge/Sem Natural)
  - Marsh / Rough Grass; Bracken; Ruderal Weed
  - Moorland Grass; Bog (Lowland/Upland)
  - Shrub Heath (Dense Shrub Heath; Open Shrub Heath)
  - Woodland (Deciduous / Mixed Wood; Coniferous / Evergreen Woodlands)
  - Tilled Land (Arable Crops); Suburban / Rural Development; Urban Development
  - Inland Bare Ground; Unclassified
- The 17-key-class system (A–Q) maps to the 25 target classes; table links provide the correspondences for standardized use and crosswalks.
- Descriptions emphasize ecological meaning, typical spectral signatures, and mapping constraints (e.g., spectral separability, management practices, seasonal effects).

## Unclassified areas
- Approximately 2% of Great Britain remains unclassified in the 25 m data, due to cloud cover, lack of a cloud-free scene, or unusual cover types not defined in the classifier.
- In the 1 km summary, unclassified portions are represented by the remaining percentage after summing the 17 key types to 100.

## References and further detail
- The document references extensive methodological background and accuracy discussions in Fuller et al. (1994a, 1994b) and Wyatt et al. (1994), with related groundwork on remote sensing classifications and ground-truth considerations.