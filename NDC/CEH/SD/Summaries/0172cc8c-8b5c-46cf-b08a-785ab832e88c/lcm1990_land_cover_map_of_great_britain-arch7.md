# Land Cover Map of Great Britain

## Overview
- A digital land cover dataset (LCMGB1990) derived from Landsat Thematic Mapper imagery, at 25m resolution, with 25 target classes plus an unclassified category.
- Based on supervised maximum likelihood classification; combines summer and winter imagery to improve accuracy.
- Data describe land cover types across Great Britain, suitable for map-based data visualisations and GIS analyses.
- Provides wide-ranging applications (e.g., agriculture, ecology, conservation, forestry, water, urban planning, transport, recreation, telecommunications).
- The 1990 product has been followed by Land Cover Map 2000, with information and sample data available online.

## Data content and classification
- 25 target classes (encoded 1–25) plus UNCLASSIFIED (0). Classes include sea/estuary, inland water, coastal bare ground, saltmarsh, various grassland types, pastures/meadows, shrub heath, bracken, woodlands (deciduous and coniferous), bogs, tilled land, suburban/rural and urban development, inland bare ground, ruderal weed, felled forest, and more.
- 25m resolution data; a coarser 1km summary is available, aggregating into 17 key classes. In 1km data, each class is represented as the proportion (0–100%) of the 1km cell occupied by that key class.
- Two data representations:
  - 25m data: single layer with values 0–25 corresponding to the 25 target classes.
  - 1km data: 17 layers (one per key class A–Q); values indicate the percentage cover of each key class within the 1km cell.
- Data can be ordered for specific geographic areas and provided as 25m or 1km products; licences cover usage types.

## Methodology and accuracy
- Classification method: supervised maximum likelihood using Landsat TM data; multi-date approach (summer and winter) improves accuracy.
- Reported accuracies:
  - Approximately 84% correspondence between Landsat classification and ground truth in a quality assurance exercise against field data; considering definitional differences, typical overall correspondence with field surveys is around 67–71%.
  - When excluding mixed boundary pixels, correspondence improves to about 71–82%.
  - Overall, a realistic accuracy estimate is typically around 80–85%, accounting for temporal changes and definitional differences.
- Common error sources:
  - Boundary pixels (roughly 40% of pixels adjacent to vectors) where mixed classes occur.
  - Minor spatial misregistrations; hard to separate misclassification from misregistration in some cases.
- Observations emphasize that accuracy figures are averages and can vary locally; differences in class definitions across surveys affect comparability.
- Ground-truth data limitations and the need to consider data model, scale, and class definitions when assessing accuracy.

## Usage, interpretation, and good practice
- The dataset is suitable for planning, management, and monitoring across sectors (agriculture, ecology, conservation, forestry, environment, water, urban development, transport, telecommunications, recreation, minerals).
- It supports detection of land-cover change, landscape management, and context-specific analyses (e.g., bracken mapping for health studies, motorway environmental assessments, telecom planning).
- The 25-class product can be aggregated or re-aggregated in a GIS to suit user objectives; 17-class 1km outputs provide a summarized view.
- Guidance notes and a Data Assessment Report (DAR) accompany the data to aid interpretation, quality control, and feedback.

## Stand-alone datasets, licensing, and access
- Data can be supplied for specific geographic areas with appropriate licensing; formats include 25m (single-layer) and 1km (summary) products.
- Licensing options range from single-user research licences to corporate multi-user licences; additional license forms can be developed to ease access.
- Data charges are divided into three bands by end use: commercial (highest), non-commercial, and research (lowest). UK academics may receive further reductions under NERC arrangements.
- Contact for ordering and licensing: Land Cover Map Sales, CEH Wallingford, +44 (0)1491 692315; email spatialdata@ceh.ac.uk.
- The 2000 version (Land Cover Map 2000) is available with more information and sample data online.

## Class descriptions (selected highlights)
- A Sea/Estuary: open sea and coastal waters up to the first bridging point; not intended to map inland limits; label 1.
- B Inland Water: freshwater/inland waters and estuarine waters above the bridging point; label 2.
- C Coastal Bare Ground: intertidal mud/sand/shingle and bare coastal habitats; label 3.
- D Saltmarsh: intertidal saltmarsh up to normal high-water levels; label 4.
- E Rough Pasture / Dune Grass / Grass Moor: coastal dunes and inland acid grasslands; spectral separation possible; label 5.
- F Pasture / Meadow / Amenity Grass: cropped swards with distinctions between mown/grazed turf (6) and semi-natural/meadow types (7); label 6–7.
- G Marsh / Rough Grass: encompasses marshy and rough grass areas; includes subtypes like ruderal weeds (19) and felled forest (23) which are aggregated for display; label 8–9.
- H Grass / Shrub Heath: open shrub/heath and moorland components are represented, with aggregation in the 17-class product; label 10, 25, etc.
- I–J Shrub Heath / Open Shrub Moor: lowland vs upland shrub-dominated or dwarf shrub moorland; labels correspond to the detailed 25-class scheme.
- K–L Deciduous/Mixed Wood and Coniferous/Evergreen Wood: includes deciduous woodland (15) and coniferous/evergreen woodland (16); label range.
- M–N Bog (Herbaceous) and Tilled Land (Arable Crops): upland/lowland bogs (17, 24) and arable crops with seasonal bare ground (18); label 18–24.
- O–P Suburban/Rural Development and Urban Development: mixed built-up areas with partial vegetation (20) or fully developed pixels (21); label 20–21.
- Q Inland Bare Ground: natural or human-altered bare ground (22); UNCLASSIFIED 0.

## Appendix and color guidance
- Appendix 2 provides the colour specifications (RGB values) for each of the 25 target classes to support map production and visual consistency.

## Additional notes
- The document includes guidance for interpreting the dataset, cautions about accuracy, and references for methodological context.
- The dataset is complemented by ongoing developments (LCMGB1990 context and DAR) and is superseded for some uses by the Land Cover Map 2000 product, which is also accessible via the Countryside 2000 resources.