# Land Cover Map of Great Britain (1990)

## Overview
- Digital dataset classifying land cover into 25 classes at 25 m resolution, derived from Landsat 5 Thematic Mapper imagery.
- First complete land cover map of Great Britain since the 1960s; first nationwide satellite-derived digital land cover map.
- Covers a wide range of uses: planning, agriculture, ecology, conservation, forestry, environmental assessment, water, urban expansion, transport, telecommunications, recreation, and mineral extraction.
- Data available under Licence for any area; stand-alone datasets available for 25 m or 1 km resolutions.
- Applications include detecting changing land cover, landscape management, bracken mapping for health studies, motorway/environmental impact assessments, and telecom planning.

## Data Details and Structure
- Two levels of classification:
  - 25 target cover-types at 25 m resolution.
  - 17 key cover-types in 1 km summary data (proportion of each 1 km cell per key class, expressed as integer percentages).
- Mapping output:
  - 25 m grid cells labeled 0 (unclassified) or 1–25 for target classes.
  - 1 km data comprises multiple layers (one per key class A–Q), each cell showing the percent cover of that class within the 1 km cell.
- Minimum mapped units and area:
  - Features mapped only if above a minimum size (practically about 0.125 ha, two pixels); real-world minimum often closer to 1 ha.
- Class definitions and aggregation:
  - 25 classes are detailed; 17 key classes provide a coarser view suitable for various applications.
  - Regional upland vs. lowland, and other ecological distinctions are present; specialists can aggregate classes differently in GIS if required.
- Data access and licensing:
  - Available to order for specific geographic areas; licensing options include single-user, multi-user, corporate, etc.
  - Data charges apply with commercial, non-commercial, and research bands; UK academics may receive reductions.
  - Licensing arrangements can be customized; contact CEH Wallingford for details.

## Classification and Accuracy
- Methodology:
  - Supervised maximum likelihood classification using combined summer and winter Landsat TM imagery to improve accuracy.
- Coverage and quality:
  - Approximately 88% of Britain classified from combined seasonal data; 12% from single-date data (mostly summer); cloud-free coverage minimal (0.4% on both seasons); offshore islands coverage ~0.1%.
- Accuracy considerations:
  - Ground-truth data are limited; comparison across different land-cover definitions introduces variability.
  - Common issues: misclassification of mixed boundary pixels (about 40% of pixels touch vector boundaries); accuracy improves when boundary pixels are excluded.
  - Reported correspondences between Landsat classification and ground surveys vary by detail level; overall correspondence around 67% (including boundary pixels), 71% when boundary pixels are excluded; after accounting for temporal changes, overall accuracy realistically around 80–85%.
- Temporal and definitional differences:
  - Time-based changes (e.g., pasture ploughed) can affect accuracy; differences also arise from varying class definitions across surveys.
- Practical guidance for users:
  - Treat accuracy as an average with potential local variations.
  - Distinguish between inaccuracies due to data model/scale/interpretation and genuine errors in mapping.

## How Analysts Can Use and QA Data
- Standardized outputs facilitate scrutiny of environmental health and policy performance over time.
- QA considerations highlighted:
  - Ground-truth data are often limited; use cautious interpretation.
  - Distinguish misclassification from mis-registration; consider boundary effects.
  - Compare across seasons and time to account for land-cover change.
- Data management:
  - Clear documentation of class definitions, regional distinctions, and aggregation paths to ensure consistent use across projects.
  - Recognize that some classes can be aggregated or redefined in GIS to meet specific monitoring needs.

## How to Use the Class Descriptions (Overview)
- Two formats available:
  - Full 25 m 25-class dataset.
  - 1 km 17-class summary dataset (proportions per class per cell).
- Class A–Q (plus Unclassified) include:
  - A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture/Dune Grass/Grass Moor; F Pasture/Meadow/Amenity Grass; G Marsh/Rough Grass; H Grass/Shrub Heath; I Shrub Heath; J Bracken; K Deciduous/Mixed Wood; L Coniferous/Evergreen Woodland; M Bog (Herbaceous); N Tilled Land; O Suburban/Rural Development; P Urban Development; Q Inland Bare Ground; Unclassified.
- Detailed definitions address tidal level influence, seasonal variation, upland vs. lowland distinctions, management effects on spectral signatures, and potential for class aggregation.

## Applications and Examples
- Use for detection of changing land cover, landscape management, health-related bracken mapping, environmental assessments of infrastructure projects (e.g., motorways, telecom lines).
- Supports planning and monitoring across agriculture, ecology, conservation, forestry, water supply, urban development, transport, recreation, and minerals.

## Availability and Further Information
- Land Cover Map 2000 is now available with further details and sample data on the Countryside 2000 website; data downloadable via the Countryside Information System.
- Contact:
  - Land Cover Map Sales, CEH Wallingford
  - Tel: +44 (0)1491 692315
  - Email: spatialdata@ceh.ac.uk

## Appendix Highlights
- Appendix 1: Advice, recommendations, and good practice for LCMGB 1990 users; emphasises interpretation of land cover versus land use and the impact of imaging dates.
- Appendix 2: Colour mapping recipe for LCM1990; provides exact color values for each class, aiding consistent visualization.