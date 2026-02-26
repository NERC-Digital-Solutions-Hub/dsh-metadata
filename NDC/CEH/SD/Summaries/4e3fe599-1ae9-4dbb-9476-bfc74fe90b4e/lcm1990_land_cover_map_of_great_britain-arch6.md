# Land Cover Map of Great Britain (1990)

## Overview
- A digital land cover map of Great Britain produced from Landsat Thematic Mapper data (1990).
- Provides 25 land cover classes at 25 m resolution, plus a 1 km summary dataset in 17 key classes.
- Based on a supervised maximum likelihood classification using combined summer and winter imagery to improve accuracy (88% of Britain classified from combined dates; 12% from single-date data).
- Intended for wide applications across business, government, and research (e.g., agriculture, ecology, conservation, forestry, urban planning, water resources, transport).

## What the data contains
- 25 target land cover classes at 25 m resolution (or 1 km summaries in 17 key classes).
- Two data formats:
  - 25 m data: single layer with values 0–25 representing the designated target class (0 = unclassified).
  - 1 km data: 17 layers (one per key class). Each cell value is the percentage (0–100) of the 1 km cell covered by that key class.
- The 25 classes cover sea/inland water, beaches/bare ground, arable land, pastures/meadows, moorlands, various heath and scrub types, bracken, bogs, and both deciduous and coniferous woods, plus urban and bare ground.
- Stand-alone data orders available for specific geographic areas; licensing options range from single-user to corporate multi-user licenses.

## Data structure and usage
- Two levels of classification:
  - 25 target cover-types (standard 25 m product).
  - 17 key cover-types (standard 1 km summary product).
- Aggregation and tailor-made outputs can be created digitally (e.g., recombining subclasses) to fit user objectives.
- Minimum map-able unit considerations:
  - Map-able features typically exceed 0.125 ha (two Landsat pixels), though the practical minimum is often closer to 1 ha.
  - Some features may be small but detectable due to spectral signatures (e.g., roads, shelter belts).
- Note on change and time:
  - Differences between time periods (e.g., land-use changes) can affect accuracy and class boundaries.

## Class taxonomy (high-level)
- A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture / Dune Grass / Grass Moor; F Pasture / Meadow / Amenity Grass; G Marsh / Rough Grass; H Grass / Shrub Heath; I Shrub Heath; J Bracken; K Deciduous / Mixed Wood; L Coniferous / Evergreen Wood; M Bog (Herbaceous); N Tilled Land (Arable Crops); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; UNCLASSIFIED.
- The 25-class scheme is designed to be ecologically meaningful and consistently mappable across Britain.
- A 1 km summary provides 17 “key” classes with percentage cover in each 1 km cell.

## Spatial resolution, registration, and accuracy
- Resolution: 25 m (target 25 m data) and 1 km (summary data).
- Registration: Landsat-derived rasters aligned to 1 km field-square vectors; average displacement around 0.8 pixels (20 m); most squares require little or no shift.
- Accuracy and validation:
  - Ground-truth data are imperfect and definitions vary; comparisons show average correspondences around 67–71% depending on how boundaries and definitions are treated.
  - When accounting for class definition differences and temporal change, a realistic overall accuracy is estimated at 80–85%.
  - Boundary (mixed) pixels contribute significantly to errors; excluding boundary pixels raises correspondence to about 71%.
  - Temporal differences (2-year gaps between field surveys and imagery) also affect agreement (e.g., pastures ploughed or grasslands altered between dates).

## Usage guidance and caveats
- The dataset maps land cover, not exactly land use; inferring use from cover requires care.
- Accuracy is scale- and definition-dependent; users should interpret results within the context of the generalizations and class definitions used.
- Substantial differences can arise from hydrological vs botanical definitions of certain classes and from how continuous gradients are discretized into distinct classes.
- The minimum mapping unit and spectral separability mean some ecologically meaningful groups may be aggregated or not fully distinguishable at 25 m resolution.
- A Data Assessment Report (DAR) is provided with data to collect user feedback and practical insights.

## Access, licensing, and related information
- Data can be provided for any area under Licence; licensing options include single-user, multi-user, corporate, etc.
- Data charges are tiered (commercial, non-commercial, and research); UK academics may receive further reductions under NERC arrangements.
- Licences signed by a responsible person within the organization; students require supervisor signatures.
- Availability: through the Countryside Information System data download site; CEH Wallingford contact: Land Cover Map Sales; tel +44 (0)1491 692315; email spatialdata@ceh.ac.uk.
- Land Cover Map 2000 is now available with sample data and download access.

## Appendix and additional notes
- Appendix 2 provides a color recipe for LCM1990 mapping (color assignments for each class).
- The document emphasizes the 1990 map’s role as a national, satellite-derived land cover product and notes cross-references to related studies and methodologies (e.g., accuracy assessments, comparisons with ground surveys).