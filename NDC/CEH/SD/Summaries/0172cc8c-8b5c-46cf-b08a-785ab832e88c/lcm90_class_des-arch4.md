# The Land Cover Map of Great Britain

## Overview
- 26 target classes (25 visible types plus an Unclassified category) derived from Landsat Thematic Mapper data; class numbers renumbered to 1-26 in downloadable data (Unclassified originally 0).
- Map uses a 25 m grid and records 25 cover types plus an Unclassified category; summer and winter imagery combined to improve classification accuracy (88% of Britain classified from combined data; 0.4% cloud-on-both-season coverage; offshore islands ~0.1%).
- Aimed at providing ecologically meaningful, consistently mappable classes across Britain; classifications created via supervised maximum likelihood methods; regional generalization to distinguish lowland vs upland where useful.

## Data structure and classification framework
- Two-level output:
  - 25 target cover-types (25 m data and 1 km summary)
  - 17 key cover-types (A–Q) as an aggregation of the 25 classes; table provided detailing crosswalk between 25 target and 17 key classes.
- Outputs available as:
  - 25-class dataset at 25 m resolution (values 0–25 corresponding to target classes)
  - 1 km summary dataset (percent cover per 1 km cell for each target class)
  - 17-class dataset (1 km summary) as standard output in the Countryside Information System; 25-class data can be customized or aggregated as needed.
- Class definitions balance ecological meaningfulness, recognizability in imagery, and mapping practicality; some subclass distinctions (e.g., wheat vs barley) are collapsed to broader categories.
- Minimum mappable unit discussed; practical mapping possible for features down to ~1 ha; post-processing can reveal features as small as 0.125 ha (2 pixels) for certain elements.
- Regional masks separate lowland and upland types to improve consistency; some rare classes (e.g., ruderal weeds) may be inconsistently mapped due to training data limitations.

## Spatial resolution, alignment, and accuracy
- Spatial resolution and mapping scale:
  - Primary grid: 25 m; auxiliary 1 km summary products.
  - Features as small as 1 ha are generally recognizable; boundary pixels often produce mixed-class results.
- Registration and alignment:
  - Landsat-derived rasters registered to 1 km field-square overlays with average displacement around 0.8 pixels (≈20 m).
  - Most squares required no shift; some required 1–2 pixel adjustments; a small number needed larger shifts.
- Accuracy assessment:
  - Ground truth data are limited; multiple surveys use different definitions and objectives.
  - Across independent 1 km squares, correspondences vary with class definitions and landscape continuum (e.g., hydro, wet vs dry, grass vs heather).
  - Boundary pixels account for a major share of error; excluding boundaries raises correspondence to about 71%; including boundaries yields about 67–82% depending on time-based changes.
  - When accounting for temporal changes (e.g., pasture to plough), overall correspondence ~76% (including boundaries) or ~82% (excluding boundaries).
  - Realistic overall accuracy estimated at 80–85%.
- Important caveats:
  - “Ground truth” is artificial due to categorization choices; actual landscape patterns exist on a continuum.
  - Differences in class definitions between surveys (hydrological vs botanical) can drive apparent discrepancies.
  - Temporal changes between image dates can affect accuracy.

## Data products and format
- 25-class dataset (standard):
  - 25 m resolution: each cell labeled 0–25 (0 = Unclassified).
  - 1 km summary: for each 1 km cell, per-class percentages (e.g., 20% of class 10 within the 1 km cell).
- 17-class dataset (key classes):
  - Available as 1 km summary data; designed to provide more consistent national mapping when some 25-class classes are unevenly mapped.
  - Table 1 provides the crosswalk between 25 target classes and 17 key classes (A–Q).
- Unclassified class:
  - In 25 m data, value 0 indicates Unclassified (due to cloud, lack of cloud-free imagery, or unusual cover types).
  - In 1 km summaries, unclassified proportion is represented by the difference from 100% after summing the 17 key classes.

## Using the data: guidance and caveats for implementation
- The 25-class dataset is the standard and offers detailed thematic breakdown; the 17-class dataset provides more consistent nationwide results where regional inconsistencies exist.
- Data can be re-aggregated in GIS to meet specific objectives (e.g., creating a generalized 17-class map from the 25-class data).
- Users should be aware of:
  - Variability in class accuracy due to definitions and spectral separability, especially for rare or spectrally similar classes.
  - Boundary and misregistration errors, which can influence small-area assessments.
  - Temporal differences between imaging acquisitions; some observed changes reflect real land-cover change rather than mapping error.
- End-to-end data governance considerations:
  - Metadata should capture the dual-season methodology, spatial resolution, minimum mappable area, and crosswalks between class schemes.
  - Acknowledge potential regional inconsistencies when aggregating or comparing across areas.
  - Maintain alignment with the referenced quality assurance and accuracy studies to interpret results appropriately.

## Class descriptions (high-level groupings)
- Water and coastal features:
  - Sea / Estuary; Inland Water.
- Bare ground and disturbed/ developed areas:
  - Beach / Coastal Bare; Saltmarsh (intertidal vegetation); Inland Bare Ground; Unclassified.
- Grasslands and pastures:
  - Grass Heath; Pasture / Meadow / Amenity Grass (split into Mown/Grazed Turf and Meadow / Verge / Semi-natural swards); Ruderal Weed (bare ground with colonizing vegetation).
- Moorland, heath, and rough vegetation:
  - Moorland Grass; Rough Pasture / Dune Grass / Grass Moor; Marsh / Rough Grass; Bracken; Open Shrub Heath; Open Shrub Moor; Dense Shrub Heath; Dense Shrub Moor.
- Shrub, scrub, and woodland:
  - Scrub / Orchard; Deciduous Woodland; Coniferous / Evergreen Woodland.
- Wetlands:
  - Lowland Bog; Upland Bog.
- Cultivated and disturbed land:
  - Tilled Land (arable); Suburban / Rural Development; Urban Development.
- Other:
  - Inland Bare Ground; Unclassified.

## References
- Core methodological and accuracy context references include Congalton (1991); Fuller et al. (1989–1994); Wyatt et al. (1994); Townshend (1983); and related works on land cover mapping accuracy and Landsat-based classification.