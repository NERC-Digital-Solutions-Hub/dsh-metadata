# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

## Overview
- Extract from 1995 describing the 26 target land cover classes (25 plus an unclassified category) for Great Britain.
- Map produced by supervised maximum likelihood classification of Landsat TM data; 25 m grid; combines summer and winter imagery to improve accuracy.
- About 88% of Britain classified from combined images; 12% from single-date data; cloud impact minimal (0.4% obscured on both seasons); offshore islands represent ~0.1%.

## Data resolution and inputs
- Spatial resolution: 25 m grid; two output formats:
  - 25-class dataset: each cell labeled 0–25 (0 = unclassified in practice).
  - 1 km summary dataset: for each target class, the percentage of 25 m cells within a 1 km grid cell.
- Two classification schemes:
  - 25 target cover-types (standard).
  - 17 key cover-types (aggregation for consistency; higher-level, more reliably mapped).
- Datasets are available in both 25 m and 1 km resolutions; 17-class data provided as 1 km summary.

## Classification scheme and structure
- 25 target classes include Sea/Estuary, Inland Water, Beach/Coastal Bare, Saltmarsh, Grass Heath, Mown/Grazed Turf, Meadow/Verge/Semi-natural, Ruderal Weed, Felled Forest, Rough/Marsh Grass, Bracken, Dense Shrub Heath, Scrub/Orchard, Deciduous Woodland, Coniferous Woodland, Upland Bog, Tilled Land, Suburban/Rural Development, Continuous Urban, Inland Bare Ground, and Unclassified, with class numbering reflecting addition order.
- 17 key classes provide a condensed framework (A–Q) corresponding to the 25 target classes; Table 1 maps relationships between the 25 and 17-class systems.
- Minimum mappable unit: conceptually two pixels (0.125 ha), though real mapping quality is closer to about 1 ha; accuracy and detectability vary by class.
- Some rare classes (e.g., ruderal weeds) were not consistently mapped across the full national extent; authors suggest a simplified 17-class approach for regional consistency.

## Class definitions and mapping notes
- Class descriptions emphasize ecological meaning and practical separability from satellite imagery, with allowances for regional and management-related variability.
- Complex Grasslands: explicit distinctions between improved vs. unimproved pastures, and between mown/grazed turf and meadow/verge/semi-natural swards, reflecting management regimes.
- Wetlands and moorlands (bogs, heaths, moors) are distinguished by hydrology (upland vs. lowland) and vegetation, with some aggregated in 17-class data for consistency.
- Agricultural and urban classes account for seasonal changes (e.g., tillage and bare ground during winter).

## Accuracy, validation, and caveats
- Validation against ground truth: comparisons to 508 one-kilometre squares show variable correspondences due to differing definitions and objectives among surveys.
- Overall accuracy is realistically around 80–85% when accounting for definitional differences and temporal changes.
- Boundary-related errors are a major contributor: about 40% of pixels lie on vector boundaries and can be mixed; excluding boundary pixels raises correspondence to ~71%.
- Misregistration vs. misclassification can blur interpretations; boundary misplacement and temporal lags (data from different years) contribute to discrepancies.
- Ground-truth data often come from different methodologies and objectives, so exact “truth” is elusive; results reflect average error rates with local deviations possible.

## Registration, geometry, and data quality
- Landsat-based maps registered to 1 km field-square overlays; average displacement around 0.8 pixels (20 m); most squares require minimal shifting.
- Minor geometric discrepancies are possible, particularly in dissected landscapes; results may reflect accurate cover patterns with small spatial offsets.

## Implications for data stewardship and use
- Dual data products support diverse needs: detailed 25-class maps for fine-scale analyses and 17-class aggregates for more consistent regional use.
- The 1 km summary format enables rapid regional assessments; the 25 m dataset supports detailed spatial analyses but may require careful interpretation for rare or ambiguously defined classes.
- Important to document:
  - Sensor and date(s) of imagery; seasonal fusion approach.
  - Classification method (maximum likelihood) and minimum mappable area constraints.
  - Boundary handling and potential for mixed pixels.
  - Temporal mismatch considerations (data from different years).
  - Available class mappings between 25 and 17 classifications.
  - Known limitations (rare classes, regional inconsistencies, and potential reclassifications in GIS).
- End-user guidance: consider custom aggregations in GIS to align with local definitions or objectives; acknowledge regional variability in grassland and heathland classifications.

## Practical governance notes
- Clear, standardized documentation of class definitions, data formats, and the 25 vs 17 class mappings supports discoverability and interoperability.
- Maintain metadata on accuracy ranges, accuracy validation methods, and known sources of error (boundary pixels, misregistration, time-based changes).
- Provide versioning notes and provenance (source imagery, processing steps, and any regional masking or corrections applied).

## References and context
- Ground-truth comparison and accuracy concepts drawn from Congalton (1991) and related remote sensing accuracy literature.
- Methodological foundations and prior work by Fuller, Wyatt, Jones, Parsell, and collaborators (1994–1995) on Land Cover Map of Great Britain and related classification research.