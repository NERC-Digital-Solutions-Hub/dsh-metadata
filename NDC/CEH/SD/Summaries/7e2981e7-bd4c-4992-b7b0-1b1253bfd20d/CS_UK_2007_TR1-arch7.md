# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Digital field mapping guide for Broad Habitats (BH) and Priority Habitats (PH) as part of Countryside Survey 2007 (CS2007) using the CS Surveyor extension on ArcMap.
- Aims to record habitat extents and changes, integrating vegetation keys, woodland keys, and landscape features into a unified digital model.
- Emphasizes auditable, country/UK-level reporting, with rules for change detection, baselines, and data quality.

## Data model and mapping concepts
- Features and geometry
  - Polygons: habitat units (BH/PH).
  - Lines: linear features (woody/other); may be mapped as lines or converted to areas if >5 m wide.
  - Points: discrete features (e.g., individual trees, ponds, culverts).
- Thematic structure
  - BH categories (BH1–BH23) and support themes (Inland Physiography, Inland Water, Coastal features, Forestry, Structures, Recreation, Transport, Agriculture/Natural Vegetation, etc.).
  - Woodland specifics handled via separate woodland keys and forestry attributes.
- Minimum mapping unit (MMU)
  - Generally 1/25 hectare (400 m²) for polygons; smaller areas mapped only if part of a larger unit or necessary for representation.
  - In practice, a minimum mappable unit of 20 m × 20 m is used in certain mapping rules.
- Change and baselines
  - Emphasis on change since 1998 or 1990 baselines; real changes distinguished from errors.
  - PH nesting into BH allowed when applying attributes; PHs may be mapped within BHs and vice versa.

## Keys and classification workflow
- Vegetation Key
  - Assigns primary/secondary attributes to polygons to allocate to BHs and PHs based on species and habitat structure.
  - Determines whether a polygon belongs to BH and which PHs apply.
- Key to Woodland Types/Features
  - Classifies woody vegetation by canopy structure and geometry (e.g., Belt of trees, Clump of trees, Woody Linear Features, Scattered trees).
  - Guides mapping of woodland components to BH/PH and recording of secondary attributes (species, cover, etc.).
- Practical workflow
  - Surveyors apply the woodland key first for woody features, then use the vegetation key for habitat assignment and PH nesting where relevant.
  - Woodland components can be mapped at polygon or component level, enabling mosaics.

## Digital mapping system and workflow (CS Surveyor)
- CS Surveyor extension in ArcMap
  - Bespoke ArcMap extension for CS2007 data capture with preset symbology and ready data frames.
  - Requires login; stores changes in a central database; supports Save Session vs End Session workflows.
- Editing landscape features
  - Areas (polygons): manage attributes, change status, area components; support splitting, merging, copying attributes, boundary edits, and area updates.
  - Lines (linear features): manage events along lines (e.g., fences, hedges, woody lines); record event attributes and lengths; support copying attributes between lines.
  - Points: capture discrete features; add/copy/delete components; manage point attributes and buffers.
- Change management and validation
  - Distinguish REAL ecological change from ERROR corrections; baselines (1998/1990) based on habitat type.
  - Unenclosed habitats may reference CS1990 data; enclosed habitats rely on CS1998 data.
- Data quality and field constraints
  - Editing typically requires scale ≤ 1:5000; focus on extent and change rather than exact ground-truth positions.
  - Mandatory fields are highlighted; errors block progression until resolved.

## Ponds and aquatic features (CS2007 Pond Mapping)
- Ponds are a central focus; every square with ponds must be identified and mapped.
- Data capture and survey process
  - Use CS2007 Pond Mapping Recording Sheet; record pond-level attributes (area, water presence, boundary, reason for loss/creation, etc.).
  - Identify all ponds in a square; select one pond as the survey pond for detailed condition assessment (pond-sampled).
  - Preselected ponds on tablet may be used if valid; otherwise, random selection is used in the field.
- Survey pond selection rules
  - If new ponds are found or access is refused or preselected pond no longer exists, select a new pond in the field following documented methods.
  - The survey pond is recorded in the Landscape Feature Editing toolbox with appropriate attributes.

## Methodology for polygons/areas and editing
- General mapping rules
  - A polygon with continuous woodland cover is BH/PH; boundaries should reflect habitat type changes rather than minor within-habitat variation.
  - Minimum mapping unit for areas is 20 m × 20 m; smaller areas are not mapped unless part of a larger changed unit.
  - When a habitat type changes, a new polygon is created; minor within-habitat species changes typically do not require a new polygon.
- Area editing tools (sections 6.a and beyond)
  - Polygon-level attributes: BH/PH, accuracy, reason for change, visit status; change types include REAL change, ERROR change, NEW BASELINE PH, No change.
  - Component-level attributes: manage components; group by themes (Physiography, Water, Forestry, etc.).
- Copy, Split, Merge, Modify, Update workflows (6.b–6.f)
  - Copy Area: copy attributes from a source polygon to targets (overwrite attributes).
  - Split Areas: digitize a new boundary to divide an area; enforce MMU rules for small splits.
  - Merge Areas: combine areas with identical attributes; require valid reason for change and BH accuracy for the merge.
  - Modify Area: adjust boundaries via topology tools; modify shared nodes with dedicated operations.
  - Update Areas Edit: create a new area by splitting/merging; use update polygon to intersect existing areas and form the new shape.
- Session management
  - Save Session to lock edits; End Session to discard changes; log off when finished.

## Specific habitat and feature guidance
- Broad Habitats (BH1–BH23)
  - BH1 Broadleaved Woodland; BH2 Coniferous Woodland; BH3 Boundaries and Linear Features; BH4 Arable and Horticulture; BH5–BH9 various grasses, heath, bog, fen, etc.; BH12 Bog; BH13 Rivers/Streams; BH14 Standing Open Waters and Canals; BH15 Montane; BH16 Inland Rock; BH17 Urban; BH18–BH23 coastal and mosaic types.
- Woodland specifics (BH1)
  - Primary attributes describing canopy structure and woodland types; secondary qualifiers for composition and management.
  - Recording of woody features (hedges, belts, lines) and buffer zones; inclusion of species composition, DBH classes, and mosaics.
- Non-native species
  - Record presence of specified non-native species within habitat units.

## Practical considerations for GIS specialists
- Data integration
  - Combine habitat classifications with landscape features (water bodies, structures, transport) and forestry attributes to produce integrated GIS layers.
- Change tracking and transparency
  - Use explicit Change vs. Error coding to support retrospective validation and reporting (including Biodiversity Action Plan alignment).
- Ponds and aquatic data
  - Maintain pond mapping sheets; ensure consistent pond boundaries and condition data for future cycles.
- Scale and precision
  - Emphasize habitat extent over exact ground-truth positions; ensure polygons meet MMU requirements and align with keys and GIS masks post-survey.
- Validation and help
  - Refer to CS Surveyor helpdesk and wiki for field bugs; monitor Latest News for methodology updates.

## Historical context and appendices (brief)
- CS2000 and CS1990 references
  - Concepts from CS2000/1990 include theme-based mapping and coding schemes; historic methods are documented and provide context for CS2007 transitions.
- Appendix topics
  - Pond mapping sheets, field assessment booklets (FABs), and coding sheets; guidance on data codes and legacy data.
  - Appendix sections include veteran-tree girth guidelines and loops in square datasets (noting data integrity considerations).