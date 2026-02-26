# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Details methodology for Countryside Survey 2007 (CS2007) to map land cover change, Broad Habitats (BHs) and Priority Habitats (PHs) across 1 km squares using a digital GIS-based system.
  - Aims to report habitat change and composition at country/UK levels, with enhanced detail for unenclosed uplands and specific Wales squares.
  - Introduces digital data collection and consolidates themes into a single editable map model.

- Data model and mapping units
  - Three feature types edited in GIS: polygons (areas), lines (woody/linear features), and points (single features).
  - Each square assigns BHs/PHs at the polygon level; attributes recorded at both polygon (primary) and component (secondary) levels.
  - Minimum Mapping Unit (MMU) = 1/25 hectare (400 m²); smaller elements handled as lines/points or inside larger polygons.
  - Spatial accuracy secondary to representing habitat extent and change; emphasis on recording changes and field-correcting allocations.
  - Data provenance and metadata tracked; datasets may be made discoverable via portals.

- Broad Habitats (BH) and Priority Habitats (PH)
  - BHs categorize major habitat types; PHs are more specific or rare and nested within BHs; PHs mapped post-survey with GIS masks where appropriate.
  - Detailed BH/PH framework with numerous BH categories (e.g., BH1–BH23) and primary/secondary attributes; mosaic BHs allowed when boundaries are unclear, with components summing to 100%.

- Vegetation and woodland keys
  - Vegetation Key assigns primary (and some secondary) BH/PH attributes based on species composition.
  - Key to Woodland Types/Features classifies woody vegetation into belts, clumps, lines, woodland blocks, etc.; supports assigning BH/PH attributes and sub-attributes (e.g., parkland, belt width, canopy cover).
  - Woody features can be recorded as areas or points; include buffers and veteran trees (up to two per species per square).

- Change reporting and data quality
  - Emphasis on recording genuine habitat change vs. previous allocation errors.
  - Surveyors assess whether 1998/CS2000 allocations still apply, or whether new baseline PHs/BHs should be used.
  - In unenclosed habitats, prior data are integrated to improve detail and support PH identifications.
  - Data provenance and metadata tracking; datasets may be made discoverable.

- The CS Surveyor digital mapping system
  - CS Surveyor is an ArcGIS-based extension within ArcMap to edit CS2007 data, with a dedicated data frame and pre-set symbology.
  - Provides fault logging, supports change tracking against mapped components (areas/lines/points), and emphasizes field-observed edits.
  - Encourages regular saving of edits and session management to avoid data loss.

- Methodology for mapping areas
  - Editing Area Attributes: assign BH/PH at polygon level; compare against 1998 data; record reason for change (real change, error, new baseline).
  - Determining Change: decide if 1998 allocation remains, or if a real or error change occurred; exercise caution with older unenclosed data.
  - Component Level Attributes: areas may contain multiple components; primary attributes may be shared across components.
  - Copy / Split / Merge / Modify / Update Areas: tools to duplicate, subdivide, combine, adjust topology, or update areas; require valid reasons for change and ensure MMU compliance.
  - Saving edits: explicit save required; edits are not autosaved.

- Methodology for mapping points
  - Points (≤20×20 m) are edited via the Points tab; include trees, standing water bodies, ponds, etc.
  - Map scale must be 1:5000 or finer; points cannot be added outside the square or within 5 m of existing points.
  - Buffers and veteran trees recorded as part of point data; some attributes include Yes/No buffers.

- Methodology for mapping line features
  - Lines are under 5 m wide with minimum length of 20 m; may contain multiple events (e.g., fence, hedge, ditch).
  - Widened features (belts) may be mapped as belts of trees or scrub; events along lines carry attributes and can be copied/moved.
  - Margin buffering and line event attributes (fences, walls, woody features, margins) are recorded; events can be copied or deleted.

- Field and data capture guidance
  - Create new woodlands, hedges, belts, clumps based on canopy cover, age, and structure; record woody features across diverse land-use contexts (recreation land, orchards, etc.).
  - Non-native species list to be recorded when encountered.
  - For woodland BHs, capture attributes related to deer fences, parkland, grazed areas, and forestry uses.

- Woodland and WLF (Woodland Linear Features) coding example
  - WLF attributes include height categories, base canopy height, species composition, evidence of management, line of stumps, vertical gappiness, and margin widths.
  - Includes classifications for unnatural vs natural shapes, management signs (cutting, laying, coppicing), presence of margins, stumps, buffer details, and tree protectors.
  - Visual examples provided to guide coding decisions on shape, height, and composition; important for distinguishing linear features and their condition.

- Pond mapping and freshwater survey
  - Every pond in a square must be identified and described on the CS2007 Pond Mapping Recording Sheet.
  - A single survey pond per square is selected for in-depth condition assessment; selection may be pre-seeded or randomised in the field.
  - Pond boundaries identified by winter water level or slope markers; ponds may be dry but recorded if they typically hold water for four or more months.
  - Different pond statuses (existing, lost, created) are recorded with reasons; newly recorded ponds influence survey pond selection to ensure consistency.

- Practical guidance and workflow
  - ArcMap/CS Surveyor tools for navigation, editing, and data capture; editors should zoom to scale < 1:5000 for edits; focus on habitat extent/change rather than precise spatial precision.
  - Mandatory fields must be completed; errors prevent saving.
  - Multi-component structures: changes to attributes propagate across components according to defined rules.

- Data structure and attributes (high-level)
  - Attributes organized by BH/PH, theme (e.g., Inland Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, Coastal features), and hierarchical levels (polygon vs component vs event).
  - Woodland BHs include canopy, belts, clumps, woody lines, and related forestry uses; arable BHs emphasize crops, margins, and species composition.
  - Standing waters, ponds, rivers, and coastal habitats include detailed aquatic and physico-chemical descriptors alongside vegetation data.

- Note for analysts
  - The document outlines a rigorous, instrumented data collection approach designed to support analyses of habitat extent, change detection, PH/BH reporting, and generation of a rich, multi-layered dataset for environmental monitoring and policy-relevant work.
  - Key challenges include integrating data across scales (local to national), unifying diverse data formats, navigating data protection and public health considerations, overcoming IT barriers, and ensuring data discoverability with robust metadata.

- Appendices and legacy context
  - CS2000 and older Field Assessment Booklets provide historical context, codesheets, and thematic mappings; CS2007 builds on these with updated attributes and digitised workflows.
  - Pond mapping forms and example code sheets illustrate data collection practices; older CS1990 data demonstrate how prior surveys informed change assessment and PH/BH identifications.
  - Additional materials cover veteran-tree girth guidelines and loops in square data (noting data integrity considerations and remediation steps).