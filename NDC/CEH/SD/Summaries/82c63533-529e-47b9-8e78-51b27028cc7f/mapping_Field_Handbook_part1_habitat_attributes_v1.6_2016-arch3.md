# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat Attributes

## Purpose and audience
- Field protocol for the Glastir Monitoring and Evaluation Programme (GMEP) to map habitat attributes for environmental health monitoring, policy scrutiny, and informing future decisions.
- Designed for survey teams producing standardized, time-series habitat data across 1km squares, aligned with Countryside Survey methodologies for historical comparability.

## Data scope, governance and openness
- Emphasizes generating datasets suitable for analysis, reporting, dashboards, and governance.
- Requires explicit metadata and openness: underlying data should be shared where appropriate; data governance processes are essential.
- Encourages data quality, consistency, verification against origin data, and documentation of data gaps or changes.
- Data management considerations include public sharing constraints and maintaining data standards from the source.

## Core methodological framework
- Mapping is polygon-based within 1km squares with time-series continuity to enable trend analysis.
- Reports Broad Habitats (BH) and Priority Habitats (PH); uses BHs and PHs to ensure compatibility with CS and other surveys.
- Two keys guide habitat attribution:
  - Vegetation Key: assigns patches to BHs and PHs based on vegetation composition; PHs nest into BHs.
  - Woodland Types/Features: classifies woody vegetation (e.g., belt of trees, clump of trees, lines, scrub) and informs mapping to BHs/PHs.
- Surveyors edit polygons and assign primary/secondary attributes; PHs can be attributed within BHs where applicable.

## Structure and recording of habitat data
- Editable Polygon/Habitats Layer: surveyors create and edit habitat polygons; polygons can be BH/PH with nesting PHs where relevant.
- Recording themes and attributes:
  - Forestry: woodland features and related attributes (e.g., Woodland/Forest, Belt of trees, Clump of trees; DBH, species, canopy, age indicators, management signs).
  - Agriculture/Natural Vegetation: non-woodland habitats (grasslands, moorlands, heaths, bogs, marsh, fen, scrub); includes sward height and indicator species.
  - Inland Water: ponds, lakes, rivers, streams, and related aquatic features.
  - Structures, Recreation, Transport, Coastal: used for associated features (e.g., fences, walls, roads, car parks).
- Recording requirements:
  - Each vegetated polygon should record at least two characteristic species (up to four) to anchor habitat classification.
  - Woodland: primary attributes (e.g., Woodland/Forest, Belt of trees) and secondary attributes (shrub layers, deadwood, regeneration).
  - Species lists linked to BRC or equivalent for vegetation typing.
- Minimum mapping unit (MMU) and fidelity:
  - MMU is 1/25 ha (400 m2); features smaller than MMU are not mapped as areas unless part of a larger polygon.
  - Emphasis on extent and relative position over exact GPS boundary precision; prioritizes consistency and comparability.

## Change mapping and repeat-square activities
- In 2016, a subset of CS squares from 1978 mapped for change rather than de novo habitat.
- Surveyors confirm polygon accuracy and determine real change vs. prior misallocations; update BH/PH assignments and attributes accordingly.
- Focus on habitat extent and attribute validity rather than precise spatial accuracy.

## Broad Habitat and Priority Habitat structure
- BH 2–22: includes Coniferous Woodland, Boundaries/Linear Features, Arable/Horticultural, various Grasslands, Bog/peat, Rivers/Streams, Standing Waters, Montane, Inland Rock, Urban, Supra-Littoral/Coastal, Littoral/Sea, and Mosaic (used when BH/PH boundaries are indistinct or below MMU).
- Mosaic: component-level habitat percentages must sum to 100% when BH/PH boundaries are indistinct or minor patches exist.

## Woodland-specific guidance
- Woodland BH/PH classification differentiates native vs non-native mixes, beech/yew mosaics, wet woodlands, parkland, and non-native/invasive influences.
- Woodland components are recorded under Forestry with primary/secondary attributes, DBH, species composition, and canopy cover.
- Orchards: traditional orchards may be PH if appropriate; intensive orchards may fall under Arable and Horticulture BH.

## Special features and organisms to capture
- Non-native species: targeted recording of invasive species (e.g., Buddleia, Reynoutria, etc.).
- Tree diseases: recording of diseases (e.g., Chalara/Ash dieback, Phytophthora, Dutch Elm disease); pilots for disease data capture in trees/woodlands.
- Bare ground and disturbance: recording bare ground components within habitat contexts; disturbance indicators (Inland Physiography).
- Ponds and aquatic sampling: every square with ponds identified; one pond per square selected for detailed freshwater condition assessment.
- Historic Environment Assets: SAMs and HEFs recorded with GIS identifiers; photographic documentation encouraged.

## Ponds and boundaries: practical guidance
- Pond definition: standing water from 25 m2 to 2 ha, typically present for at least 4 months/year, including temporary/man-made ponds.
- Boundary identification: use winter water level as a boundary proxy; boundaries may be ambiguous in fen/marsh/bog contexts; use breaks in slope or vegetation transitions when unclear.
- Distinguishing ponds from ditches/streams: apply consistent definitions; ditches with standing water are not ponds; dammed streams are not ponds if flow persists.

## Ponds data capture workflow
- Grid Square Inventory for Ponds and Square Inventory forms to record ponds.
- Pond selection: identify one pond per square for in-depth condition surveying.
- GPS and location sharing: promptly share GPS coordinates of ponds and stream sites with the freshwater team.

## Historic features and documentation
- Historic Environment Assets (HEA): SAMs and HEFs recorded; site types and digital identifiers provided; photographic documentation encouraged for condition assessment.

## Photographs and reporting
- Use structured photo naming conventions (e.g., SAM/PHN_date_desc) to support condition reporting and archiving.

## Practical outputs and documentation
- Data organized by habitat type and attribute themes to support policy-relevant monitoring, trend analysis, and decision-making.
- The handbook provides concrete field protocols, attribute schemas, and decision rules to support rigorous monitoring framework development and evaluation.

## End notes
- The document serves as a comprehensive field protocol and reference for habitat attribute mapping within the Glastir Monitoring & Evaluation Programme, with explicit instructions on data collection, classification, change tracking, and ancillary environmental data capture (ponds, historic features, non-native species, diseases, mosaics, and linear features).

## Visit status (survey progress tracking)
- VISIT STATUS field across Events, Points, and Areas to indicate survey progress:
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- Usage:
  - Helps identify unsurveyed or in-progress features to finish surveys.
  - Used to determine whether a square is fully surveyed.
- How to search and manage statuses:
  - Options include searching by layers (Landscape Points, Landscape Events, Landscape Areas) and by VISIT STATUS using Find, Select by Attribute, or Attribute Table.
  - Find allows single-criteria searches (0, 1, 2, 3) and can flash features on the map for quick locating.
  - Select by Attribute can search with multiple terms but does not produce a list; highlights features on the map.
  - Attribute Table provides a list-based approach; can invert selections to find non-completed features.
  - For lines and areas, unsurveyed state applies when a square is blank; disappears after first split.
- MMU considerations with Visit Status:
  - Cannot map below MMU; use merging/splitting via UPDATE to manage small portions without creating sub-MMU polygons.
  - Copy/Paste and selection tools allow integrating edits from different layers to maintain consistency.

## Identifying Ancient Trees (ancient/veteran tree guidance)
- Definition: trees that are old relative to their species, indicated by characteristics such as large girth, substantial deadwood, hollow trunks, and other aging features.
- Important caveats:
  - Girth alone is insufficient; growth conditions and management affect size.
  - Look for a combination of features (deadwood, cavities, decay, fungi, epiphytes, old look, high wildlife associations, cultural value, pollard form).
- Girth guidance:
  - A species-specific table provides minimum girth thresholds (e.g., several species have threshold girths ranging from approximately 0.8 m to over 6 m, with descriptors like “potentially interesting,” “valuable,” and “truly ancient” based on percentiles of maximum girth).
  - Rule of thumb: if the girth value exceeds the species-specific threshold, the tree may be notable as ancient.
- Practical note: use a combination of girth and qualitative aging indicators to assess veteran status; individual trees may not fit strictly by girth alone.