# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

## Overview
- Describes the Land Cover Map of Great Britain (LCMGB), produced from supervised maximum likelihood classifications of Landsat TM data at 25 m resolution, covering 25 target land cover types plus an unclassified category.
- Uses a summer–winter data mix to improve classification accuracy; about 88% of Britain classified from combined images, 12% from single-date images.
- Notes small areas obscured by cloud (0.4%) and offshore missing areas (0.1%).

## Data structure and formats
- 25 target classes mapped on a 25 m grid; values 0–25 where 0 = Unclassified.
- An alternative 1 km summary dataset exists, with 25 layers (one per target class). In each 1 km cell, the value represents the percentage of that target class within the cell (e.g., 320 of 1600 25 m cells = 20%).
- A secondary 17-class (key) aggregation is provided for national consistency; these are referred to by letters A–Q and are available as a 1 km summary dataset.
- Minimum mappable size: practice indicates about 1 ha (though stated as 2 pixels or 0.125 ha in one section); some 0.125 ha features may appear due to data nuances.
- Tables describe the correspondence between the 17 key classes (A–Q) and the 25 target classes (1–26 on download, with 0 for Unclassified).
- Custom or non-standard aggregations are possible digitally, allowing users to tailor outputs to objectives.

## Classification approach and accuracy
- Classifications are based on supervised maximum likelihood methods using Landsat TM data, integrating multiple dates to improve spectral separability.
- Accuracy assessments:
  - With independent ground reference data across 508 1 km squares, overall accuracy is realistically 80–85%.
  - When accounting for differences in class definitions and temporal changes, observed correspondence with field data ranges around 67–71% (Landsat vs field) and up to ~76% including boundaries, 82% excluding boundaries.
- Key sources of error:
  - Boundary pixels (about 40% of pixels touch vector boundaries) contribute to misclassification; excluding boundaries raises agreement to ~71%.
  - Distinctions between continuum classes (e.g., various grasslands, moorlands, bogs) depend on definitions and timing; temporal changes (e.g., pasture to plough) affect comparisons.
  - Misregistration vs misclassification can be hard to separate; some spatial displacement differences are acceptable for many applications.
- QA findings suggest alignment between ground surveys and satellite results is feasible but varies by class and geography.

## Land cover classes (high level)
- Water and coastal features: Sea / Estuary; Inland Water.
- Bare ground and coastal areas: Beach / Mudflat / Cliffs; Inland Bare Ground; Unclassified.
- Intertidal and marsh: Saltmarsh; Marsh / Rough Grass (combines several lowland/rough vegetation types).
- Grassland and pastures: Grass Heath; Mown / Grazed Turf; Meadow / Verge / Semi-natural swards; Pasture / Meadow / Amenity Grass (subclasses include Mown/Grazed Turf and Meadow/Verge/Semi-natural).
- Sem-natural and rough vegetation: Ruderal Weed; Bracken; Rough Pasture / Dune Grass / Grass Moor; Open Shrub Heath; Open Shrub Moor.
- Moorland and uplands: Moorland Grass; Upland Bog; Lowland Bog (with upland vs lowland distinctions in several categories).
- Shrubs and woodlands: Scrub / Orchard (deciduous scrub and orchards treated with Deciduous Woodland in 25-class outputs); Deciduous Woodland; Coniferous / Evergreen Woodland; Dense Shrub Heath; Dense Shrub Moor; Open Shrub Heath.
- Forest and trees: Felled Forest (to be aggregated with rough grass in many displays); Coniferous / Evergreen Woodlands.
- Human land use: Suburban / Rural Development; Continuous Urban.
- Special notes: Some rarer classes (e.g., ruderal weeds) may not be mapped consistently across regions; a 17-class aggregation is recommended for national consistency.

## How to use the data products
- Two standard digital products:
  - 25-class dataset at 25 m resolution (grid cells coded 0–25).
  - 1 km summary data with per-layer percentages for each target class.
- 17-key (A–Q) dataset provides a coarser, more consistently mappable classification; available as a 1 km summary dataset and used as standard in the Countryside Information System.
- Customization:
  - Users can aggregate or reclassify to suit objectives (e.g., create a “grassland” composite from multiple target classes).
  - Non-standard customized data can be requested or produced by selecting a subset of classes.
- Data interpretation:
  - The 25-class data are designed for end-user self-service and integration into GIS; boundary and temporal considerations should be accounted for in analysis.
  - Regional considerations (upland vs lowland) and timing of imagery influence class delineation and accuracy.

## Practical considerations and limitations
- Regional differences and the use of regional masks help generalize certain classes (e.g., grasslands) but may introduce cross-region inconsistencies if not handled in GIS.
- Some classes are defined by spectral signatures that may vary with management practices (e.g., mowing, grazing) and season, affecting detectability.
- Ground-truth data for accuracy assessment are imperfect; the report emphasizes that “truth” in land cover is inherently abstract due to class generalization.
- The dataset is framed to balance ecological meaningfulness with mapping feasibility at the 25 m scale, with guidance to reaggregate for consistent national results when needed.

## References and context
- Key sources include Fuller et al. (1994a, 1994b), Wyatt et al. (1994), Congalton (1991), and related remote sensing studies on land cover classification and accuracy assessment.
- The document discusses methodological aspects such as registration errors, boundary effects, and timing differences between summer and winter imagery.