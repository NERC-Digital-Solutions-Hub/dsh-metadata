# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Guidelines for the Countryside Survey 2007 (CS2007) digital field mapping of habitats and landscape features.
- Focus on change detection in Broad Habitats (BH) and Priority Habitats (PH) at country and UK levels.
- Data collected digitally to enable change detection, neighbourhood analysis, and linkage to UK Biodiversity Action Plans.

## Data model and habitat classification
- Two classification keys:
  - Vegetation Key: assigns polygons to BH/PH based on plant composition and flora indicators.
  - Key to Woodland Types/Features: classifies woody vegetation (e.g., belt/line/clump of trees) and supports attributes.
- Habitat structure and scale:
  - Enclosed habitats: edit from 1998 CS data; possible new PH attribute without altering BH base.
  - Unenclosed habitats: integrate CS1990 detail with CS2000 granularity; allow merging adjacent patches of uniform type.
- Broad Habitats (BH) exemplars and PH extents:
  - BH categories include woodland, boundaries, arable, grasslands, heaths, wetlands, rivers, water bodies, urban, and mosaics.
  - PHs mapped where possible; GIS masks bound PH extents post-survey.

## Vegetation and woodland types
- Vegetation Key attributes:
  - Primary attributes (dominant habitat) and secondary attributes (indicator species, community, etc.).
  - Rules allocate BH/PH based on canopy composition and indicators.
- Woodland types/features:
  - Primary attributes cover belts/lines/clumps of trees, woodland/forest, scrub components.
  - Canopy interpretation governs BH/PH allocation; canopy >25% often triggers woodland BH/PH assignment.
  - Detailed woodland data (species, cover, DBH, provenance) stored under Forestry theme.

## Digital mapping system and workflow
- CS Surveyor extension for ArcMap:
  - Central “Countryside Survey” data frame, user login, square-based workflow, and change recording required for mapped components.
- Data types and themes:
  - Areas (polygons), Lines (woody/linear features), Points (trees, ponds, etc.).
  - Thematic groups: Forestry, Agriculture/Natural Vegetation, Inland Physiography, Coastal Features, Structures, Recreation, Transport.
- Editing tools and processes:
  - Area editing: split, merge, copy attributes, update boundaries.
  - Point editing: create/move/delete; support multiple components per point; veteran trees entries.
  - Line editing: define events along lines; create/copy/delete events; manage margins and woody linear features.
- Data quality and change management:
  - Distinguish REAL change from ERROR change; minimum mappable unit (MMU) 1/25 hectare; mosaics allowed with 100% habitat sum in components.
  - Patches and mosaics reflected by multiple components with percent cover.

## Mapping areas and change logic
- General mapping rules:
  - Continuous woodland within a polygon maps to Woodland BH/PH regardless of other components.
  - Mosaic habitats represented with multiple components, each with percentage cover.
- Change attribution (6.a.ii):
  - REAL change, ERROR change, NEW BASELINE PH, or No change.
  - For unenclosed habitats, 1990 CS data informs descriptors; for enclosed habitats, 1998 data informs descriptors.
- Change validation:
  - Attribute Editor logs reasons for change; BH accuracy codes updated.
  - Merged areas require a new BH accuracy assessment and reason for change.

## Pond mapping and survey
- Ponds are a core focus; map all ponds in a square.
- CS2007 Pond Mapping Recording Sheet; a subset (survey pond) selected for detailed condition assessment.
- Selection process:
  - If multiple ponds exist, a random selection or preselected pond from CS2000 may be used; field decisions can override preselection.
  - Rules exist for using preselected vs field-selected ponds (new ponds, unmapped areas, access issues).
- Pond attributes:
  - Polygon ID, area, whether it contains water, reason for loss/creation, and notes.
  - Survey pond data collection occurs after all ponds are mapped.

## Points and woody linear features (WLFs)
- Points:
  - Edit point attributes; create/remove points; ensure a single Unsurveyed/Missing Data component for new points.
  - Tree/shrub features recorded as points outside curtilages; veteran trees limited to two per species per square.
  - Modal DBH categories captured; landowner buffer practices noted.
- Woody Linear Features (WLFs):
  - Natural shape vs hedged form; primary attribute indicates natural shape.
  - Features include belts of trees, lines of trees, hedges, lines of scrub, scattered trees.
  - Widths: belts typically 2–4 trees wide, up to 50 m; segments >5 m may be mapped as belts or areas.
  - Margins (height, width, left/right), segment events, and biodiversity attributes recorded.
- Margins and cross-features:
  - Margins recorded (typical ~6 m); multiple margins may be additive.
  - Cross features include stone/earth banks, grass strips, and other linear landscape elements.

## WLF specific attributes (illustrative guidance)
- Unnatural shape indicators include height categories, base height, species composition, signs of management, line of stumps, vertical gappiness, margins, staked trees, and tree protectors.
- Guidance notes and example sketches illustrate coding for unusual shapes and management history (e.g., cutting, laying, coppicing).

## Data recording and metadata
- Data tracked with source references and metadata to enable discoverability and reuse.
- QA steps include field checks, cross-referencing with previous surveys, and documenting corrections and justifications.

## Practical implications for analysts
- Provides a data-rich framework to model habitat extent, change, and mosaics over time.
- Supports predictive understanding of habitat distribution under different management scenarios via standardized attributes.
- Enables transparent change tracing, reproducible mapping, and integration with UK biodiversity reporting needs.

## Appendices and related materials (highlights)
- CS2000 and CS1990 mapping themes and code schemes; field assessment and data recording forms; lists of universal and theme-specific codes.
- Appendix materials cover veteran-tree girth guidelines, loops in squared data, and pond mapping templates.
- Appendices provide guidance for special cases, data coding, and historical references to previous surveys.