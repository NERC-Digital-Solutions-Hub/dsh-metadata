# The Land Cover Map of Great Britain

## Aim
- Provide a consistent, data-driven view of environmental condition to enable scrutiny of environmental health and policy performance over time.
- Deliver a standardized set of land cover outputs for analysis and monitoring, using established data and methods.

## Data and Classification Overview
- Based on Landsat Thematic Mapper imagery (25 m grid) with supervised maximum likelihood classification.
- Produces 25 target land cover types (plus an Unclassified category) and, for flexibility, an aggregated 17-key class system (A–Q).
- Two digital products:
  - 25-class dataset at 25 m resolution (values 0–25).
  - 1 km summary dataset (per 1 km cell, per target class, as a percentage).
- The 25-class dataset can also be provided in a 25 m or 1 km format; the 17-key dataset is provided as a standard in some systems (Countryside Information System).
- Classes are designed to be ecologically meaningful, consistently mappable across Britain, and aggregatable by user needs. Subclasses (e.g., wheat vs. barley) are collapsed into broader target classes.

## Spatial Resolution, Registration, and Display Characteristics
- Minimum accurately mappable unit estimated around 1 ha; features as small as 1 ha are visible, with finer patterns for roads, farms, shelter belts, etc., down to about 0.125 ha (2 pixels) after removing isolated pixels.
- Landsat-derived maps aligned to 143 vector field maps; average positional shift ~0.8 pixels (20 m). 75 of 143 squares required no shift; 43 needed 1-pixel shift; 15 needed 2-pixel shifts; 10 needed more than 2 pixels.
- Registration accuracy is acceptable for most applications.

## Classification Accuracy and Validation
- Ground-truth data are limited in standard surveys; accuracy depends on reference methods and definitions.
- Comparisons against 508 independent 1 km squares show varying correspondence due to:
  - Differences in class definitions (e.g., hydrological vs. botanical definitions of bogs and differences in grassland classification).
  - Boundary pixel misclassification and mixed pixels (about 40% of boundary-adjacent pixels are mixed).
  - Temporal changes between surveys (e.g., pasture ploughed or hayed between dates).
- Reported correspondence ranges:
  - About 67% overall correspondence when considering differences in definitions and potential time-change.
  - 71% when boundary pixels are excluded.
  - Up to 76% when allowing for time-based changes; 82% excluding both boundaries and time-change factors.
- Realistic overall accuracy is considered to be in the range of 80–85%.
- End-users should anticipate regional/scale variations in accuracy and the effects of generalized class definitions.

## Land Cover Classes (25 Target; 17 Key)
- The 25 target classes are a practical set derived from Landsat data, representing ecologically meaningful vegetation and land-use types. Examples include:
  - Sea / Estuary
  - Inland Water
  - Beach / Mudflat / Cliffs (Coastal Bare Ground)
  - Saltmarsh
  - Grass Heath
  - Mown / Grazed Turf
  - Meadow / Verge / Semi-natural swards
  - Rough / Marsh Grass
  - Moorland Grass
  - Open Shrub Moor
  - Dense Shrub Moor
  - Bracken
  - Dense Shrub Heath
  - Scrub / Orchard
  - Deciduous Woodland
  - Coniferous Woodland
  - Upland Bog
  - Tilled Land (Arable Crops)
  - Ruderal Weed
  - Suburban / Rural Development
  - Continuous Urban
  - Inland Bare Ground
  - Felled Forest
  - Lowland Bog
  - Open Shrub Heath
  - Unclassified (0 in some datasets)
- For consistency and tool-specific needs, an aggregated 17-key class system (A–Q) maps to the 25 target classes via a defined crosswalk (Table 1 in the document). The 17-key set is provided as a standard option in some systems (Countryside Information System).

## How to Use the Data
- Available as:
  - 25-class dataset at 25 m resolution (grid cells labeled 0–25).
  - 1 km summary dataset (per 1 km cell, percentage cover per target class).
  - 17-key dataset (1 km summary) as a standard alternative, with a crosswalk to the 25-class system.
- Aggregation and customization:
  - Users can recombine subclasses differently (e.g., a “graminoids” map by aggregating grass subclasses); however, this may reduce consistency across imagery dates.
  - Subsets or non-standard aggregations can be produced digitally by reference to the original 25 m maps, depending on accuracy requirements.
- Minimum mapping and data interpretation:
  - A 2-pixel minimum (~0.125 ha) feature size is used in practice, but the true minimum accurate mapping is likely closer to 1 ha.
  - The 1 km summary data shows the percentage composition of each target class within each 1 km cell (e.g., if 320 of 1600 25 m sub-cells are class 10, the 1 km cell’s class-10 layer shows 20%).
- Practical cautions:
  - Class definitions are not absolute truths; different surveys may define boundaries differently.
  - The presence of mixed boundary pixels and timing differences between data acquisitions can affect accuracy.
  - Some rare classes (e.g., Ruderal Weed) may be inconsistently mapped across regions; a 17-key aggregation may mitigate this for national consistency.

## Unclassified Category
- About 2% of Great Britain remains unclassified in the 25 m data due to cloud cover, lack of cloud-free imagery for some locations, or unusual cover types not defined by the classifier.
- In 1 km data, unclassified areas are represented as the residual difference to 100% within the 1 km cell.

## References and Further Details
- The document cites methodological and accuracy references, including Congalton (1991) on accuracy assessment, and Fuller et al. (1989–1994) on the development, validation, and availability of the Land Cover Map and related datasets.