# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Overview
  - Purpose: Countryside Survey 2007 field mapping of habitats and landscape features across 1 km squares, focusing on Broad Habitats (BH) and Priority Habitats (PH), with time-series reporting to support policy and management decisions.
  - Background: Builds on CS1990/CS2000 mapping frameworks; introduces detail for unenclosed uplands and new Wales squares; data captured digitally to enable change detection and future analyses.

- Mapping framework and goals
  - Habitat focus: Change in land cover and PHs, with PHs nested within BHs; enhanced vegetation attributes for unenclosed uplands; baseline PH mapping.
  - Scope: Includes 60+ new squares in Wales; distinguishes enclosed vs unenclosed habitats; post-survey GIS masks delineate upland vs lowland PH extents.

- Data model and classification
  - Two primary keys:
    - Vegetation Key: assigns patches to BHs/PHs based on plant composition and habitat indicators.
    - Woodland Key: classifies woody vegetation (canopy structure and spatial form: belt, line, clump, scattered trees, woodland/forest).
  - Habitat delineation:
    - Enclosed habitats: PHs attributed within 1998 BHs; BHs retained where PH not present.
    - Unenclosed habitats: refined with detailed vegetation data; potential re-allocation of 1998 BHs.
  - Orchards: guidance that traditional orchards may qualify as PH; add Orchard as an attribute where appropriate.

- The digital mapping system (CS Surveyor)
  - ArcMap extension with a Countryside Survey data frame and predefined symbology.
  - Workflow: surveyors log in, choose a square, edit Points, Lines, and Polygons.
  - Editing requirements: 1:5000 or better for points; dedicated Landscape Feature Editing toolbox for Areas, Lines, Points.
  - Change status tracking: REAL change, ERROR change (correction of 1998 data), NEW BASELINE actions.
  - Versioned workflow: Save Session, End Session; regular saves recommended.
  - Data provenance: track data sources, metadata, and ensure discoverability via portals.

- Areas (polygons) and components
  - Primary mapping unit: Areas (polygons); minimum mapping unit (MMU) = 1/25 ha (400 m2); smaller features mapped as lines.
  - Multi-component areas: a polygon may contain multiple components within a single BH/PH assignment; components can be added, copied, or deleted.
  - Attributes: organized by themes (e.g., Inland Physiography, Agriculture/Natural Vegetation, Forestry, Structures); mandatory values highlighted.
  - Recording: up to 4 species per polygon with associated cover proportions; non-native species recorded.

- Change, merging, splitting, updating
  - Operations:
    - Copy Area: overwrite attributes from source to target areas.
    - Split Areas: create new boundaries within a polygon; ensure minimum area; assign attributes to each part.
    - Modify Area: adjust boundaries with topology integrity; shared nodes maintained.
    - Update Areas Edit: create new landscape area by splitting/merging existing polygons.
    - Merge Areas: combine areas with identical attributes; require a stated Reason for Change.
  - Rationale: distinguish genuine ecological change from previous mapping errors, especially for unenclosed habitats with older data.

- Attributes and vegetation/woodland keys (highlights)
  - BH/PH classification at area level; component-level attributes detail vegetation, species, and cover.
  - Species data: record up to 4 species per polygon with cover categories (<10%, 10-25%, 25-50%, 50-75%, 75-95%, 95-100%).
  - Woodland specifics: canopy structure and spatial form guide BH/PH assignments; tabled descriptions for woodland types (e.g., Broadleaved, Coniferous, Boundaries/Linear Features, Arable/Horticulture, Improved Grassland).
  - Special cases: orchards guidance integrated into attributes.

- Ponds and standing open waters (Pond Survey Protocol)
  - Every square with ponds must be mapped using the CS2007 Pond Mapping Recording Sheet.
  - Survey pond: one pond per square selected for detailed condition assessment via a random-number method (preselected ponds may be used if still valid).
  - Pond boundaries: defined by outer winter water level; include pond ID, area, water presence, and reasons for pond loss/creation; data feed into freshwater surveyors.

- Points and linear features (events and attributes)
  - Points: landscape elements (trees, ponds, buildings, etc.) with at least one component; veteran trees data fields (buffer zones, DBH, species, canopy, health).
  - Buffers: Yes/No for features around landowner-protected features.
  - Linear features: lines (minimum 5 m length); events along lines (fences, hedges, woody lines, walls) with attributes (length, type, condition).
  - Event editing: copy attributes along lines, adjust length/position, maintain continuity.
  - Margins: margins (grass margins, hedgerows) recorded in addition to standard margins with specified widths.

- WLF (woody linear features) data snippet (example attributes)
  - Unnatural shape, height classes, base height, species composition (e.g., >50% hawthorn), evidence of management, line of stumps, vertical gappiness, and margin widths.
  - Includes detailed coding examples and guidance for classifying and recording WLFs, including natural vs unnatural shapes and management signs.

- Practical guidelines and constraints
  - 1998 base allocation may be retained by default unless field evidence indicates change; PH allocations require careful attribution and possible reclassification.
  - MMU: ensures consistent mapping units; smaller features may be omitted unless necessary.
  - Spatial accuracy is balanced with accurate representation of extent and change; topology edits allowed to improve habitat representation.
  - Support: fault logging, helpdesk, and method updates posted in Latest News.

- Workflow and quality considerations for analysts
  - Rigorous, repeatable workflow: define habitat types (vegetation/woodland keys), map polygons and components, record attributes, and track change statuses with reasons.
  - Provenance and discoverability: track data sources, maintain metadata, and ensure datasets are accessible via data portals.
  - Change interpretation rules (REAL vs. ERROR vs. NEW BASELINE) enable robust trend analyses across survey rounds.
  - End-to-end capture: from square selection, digitization of areas/lines/points, pond surveying, to final validation, supporting reliable impact assessment and biodiversity monitoring.
  - Appendix-specific notes: guidance on loops (data issues), veteran-tree girth rules (Appendix 5), and loops data in Appendix 6.

- Historical context and scaffolding
  - CS2000 and CS1990 foundations described (themes, data forms, and unique parcel coding) to contextualize 2007 methodology and data structures.
  - Provides code sheets and mapping templates to support consistent attribute coding and data entry.

- Publication, rights, and contact
  - Copyright and reproduction rights outlined; publication supports research and internal use with proper acknowledgement.
  - Contact and project office details provided for Countryside Survey information and data inquiries.