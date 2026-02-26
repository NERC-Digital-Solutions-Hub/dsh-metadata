# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

- An automated land cover map (LCMGB) produced from supervised maximum likelihood classifications of Landsat TM data.
- Based on a 25 m grid, detailing 25 cover types (sea, inland water, beaches, bare ground, arable land, and 18 semi-natural vegetation types).
- Combines summer and winter imagery to improve accuracy; about 88% of Britain classified from combined dates, 12% from single-date data.
- Minimal cloud cover, with offshore islands contributing negligibly to missing areas.
- Document describes map classes, resolution, depiction of classes, and relational context to other surveys.

## Spatial resolution, registration, and accuracy

- Minimum accurately mappable unit: practical field-level scales; features as small as 1 ha are clearly depicted, with finer patterns (e.g., roads, tracks) visible in subsets as small as 0.125 ha (2 pixels) after removing isolated pixels.
- Registration: Landsat-derived rasters aligned to 1 km field-maps (1 km squares). Average displacement ~0.8 pixels (≈20 m); most squares require no shift or only 1-pixel shifts; a minority require more than 2-pixel adjustments. Error deemed acceptable for typical applications.
- Accuracy assessment: ground-truth data quality often uncertain; class definitions and generalization affect comparisons. Across 508 1 km squares, correspondence varies with detail level and definition differences (e.g., hydrological vs botanical classifications, grassland continua). Excluding boundary pixels increases correspondence from ~67% to ~71%. Including potential land-cover changes over time lowers observed correspondences; overall, a realistic accuracy estimate is about 80–85%.
- Temporal considerations: some discrepancies reflect actual land-cover changes between surveys (e.g., pasture ploughed), or differences in survey dates (up to ~2 years apart).

## Land cover classes

- Two standard classification schemes:
  - 25 target cover-types (standard digital product, 25 m resolution; also available as 1 km summary).
  - 17 key cover-types (aggregated, designed for consistency; provided as 1 km summary data; correspondences to the 25-class set detailed in Table 1).
- Data formats:
  - 25-class dataset: 25 m grid cells coded 0–25 (0 = unclassified).
  - 1 km summary: for each 1 km cell, 25 layers show the percentage of each target cover-type within that cell (e.g., 1 km cell with 320 of 25 m cells as type 10 yields 20% in layer 10).
  - 17-class dataset: available as 1 km summary data; can also be customized (subset of classes) if needed.
- Class characteristics:
  - A Sea / Estuary; B Inland Water; C Coastal Bare Ground (Beach / Mudflat / Cliffs); D Saltmarsh; E Grass Heath / Moorland (includes Rough Pasture / Dune Grass / Grass Moor; includes Subcategories like Grass Heath and Moorland variants); F Pasture / Meadow / Amenity Grass (subdivided into Mown/Grazed Turf and Meadow/Verge/Semi-natural swards); G Marsh / Rough Grass (and related Ruderal weeds considerations); H Grass / Shrub Heath (Open Shrub Heath); I Shrub Heath (Dense Shrub Heath / Dense Shrub Moor); J Bracken; K Deciduous / Mixed Wood (Scrub/ Orchard and Deciduous Woodland); L Coniferous / Evergreen Woodland; M Bog (Herbaceous) with Lowland/Upland variants; N Tilled Land (Arable Crops); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; plus an Unclassified category for small unallocated areas.
- Key mapping notes:
  - Classes reflect ecological meaningfulness and mapping reliability; their definitions acknowledge regional variation (e.g., lowland vs upland distinctions) and practical limits of spectral separability.
  - Some rarer classes (e.g., ruderal weeds) may not be consistently mapped across Britain; a simplified 17-class schema is suggested for national consistency, while the 25-class dataset remains available for detail.
  - Agricultural grasslands are represented with greater granularity due to management significance; two subclasses exist (Mown/Grazed Turf and Meadow/Verge/Semi-natural swards), though aggregation is possible depending on accuracy and user needs.
  - Boundary pixels (mixed cover types) are a major source of classification error; excluding them improves apparent accuracy.
  - Coastal boundaries depend on tide imaging; discrepancies can occur when tidal conditions differ between image acquisitions.
  - Some landscapes change between the date of imagery (seasonality, harvesting, ploughing, etc.), influencing classification outcomes.

## How to use this classification

- The product is available in two primary formats:
  - 25-class dataset (standard): 25 m resolution, with each cell coded 0–25.
  - 1 km summary: per 1 km cell, 25 layers representing percentage cover of each target type; also supports aggregation to 17-class schemes.
- The 17-class dataset (A–Q) provides a consistent national framework for broader mappings; Table 1 maps 17 key classes to their 25-target counterparts for users needing crosswalks.
- For practical applications:
  - Use 25-class data when detailed, ecologically meaningful distinctions are required; use 17-class data for consistent national-scale analyses.
  - Custom data products can be requested, e.g., a reduced set of classes; users should expect some loss of within-class detail.
  - Be mindful of the minimum mappable size (roughly 1 ha in practice) and the potential need for GIS-based post-processing to handle regional specificity or context-based separation (e.g., altitude or geography).

## Limitations and considerations for data stewardship

- Acknowledge inherent uncertainties in “ground truth” references and the artificial nature of hard class boundaries.
- Expect regional and temporal variability; document the image dates used and any known changes since data acquisition.
- Provide metadata that includes: classification approach (maximum likelihood), dates of imagery, resolution, class definitions, accuracy estimates, and notes on boundary/mixed pixels.
- Maintain crosswalks between 25-class and 17-class schemes to support interoperability; consider providing both resolutions (25 m and 1 km) for the broadest usability.
- Monitor and document sites where rarer classes are inconsistently mapped; consider regional adjustments or alternative aggregations in GIS workflows.
- Unclassified areas (~2% of Britain in 25 m data) should be treated explicitly in analyses; 1 km summaries handle unclassified areas via 100% summation across included classes.

## References and further details

- The document includes extensive method notes, accuracy discussions, and class definitions, with cross-references to Fuller et al. (1994a, 1994b), Wyatt et al. (1994), Congalton (1991), and related works.
- For detailed class definitions, coastal/tidal boundary handling, and the 25 vs 17-class crosswalk, refer to the full table and narrative in the source document.