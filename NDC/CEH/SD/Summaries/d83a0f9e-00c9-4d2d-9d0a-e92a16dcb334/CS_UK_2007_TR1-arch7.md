# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - guides field mapping workflow for Countryside Survey using CS Surveyor (ArcMap extension)
  - aims to document habitat extent and change across 1 km grid squares
  - focuses on Broad Habitats (BH) and Priority Habitats (PH) with post-survey GIS editing and data quality checks

- Data model and habitat classification
  - BHs with nested PHs; polygon-based mapping with attributes stored per polygon and per component
  - woodland types/features classified with primary and secondary attributes (e.g., belts, clumps, canopy, DBH, species)
  - two primary keys: Vegetation Key (BH/PH allocation) and woodland features key

- Digital mapping system and workflow
  - CS Surveyor is an ArcMap extension enabling on-map data capture, change logging, and central database integration
  - workflow: login, select 1 km square, work within a dedicated Countryside Survey data frame
  - three feature types editable: Areas (polygons), Lines (boundaries and linear features), Points (woody features, water bodies, etc.)
  - emphasis on habitat extent and attribution; spatial position accuracy is secondary
  - built-in data quality guidance, helpdesk, and Wiki fault-logging

- Editing Areas (Polygons)
  - MMU: minimum mapped unit is 1/25 hectare (400 m2); features smaller than MMU not mapped as areas unless boundary lines
  - polygon attributes include BH/PH allocation, accuracy, change reason, and visit status
  - component-level attributes allow multiple components per area
  - change status categories: REAL change since 1998, ERROR change, NEW BASELINE PH
  - rules for polygon creation, merging, and attribute inheritance when merging
  - editing tools: save sessions, copy/merge/split/adjust boundaries, update areas from sketches or copied shapes
  - guidance: prioritize correct habitat extent and attribution over precise geometry for cross-square comparability

- Editing Points
  - points capture discrete features (trees, standing water, veteran trees, etc.)
  - editing scale must be 1:5000 or finer
  - points can have multiple components; components can be added, copied, or deleted
  - support for buffer zones and veteran-tree attributes (e.g., DBH, health)

- Editing Linear Features (Lines)
  - lines represent features typically longer than 20 m and under 5 m wide; consist of multiple events (e.g., fence, hedge, ditch)
  - events on lines carry attributes; lines can be split, merged, or edited at the event level
  - lines widen to areas if the width exceeds the minimum mappable unit
  - margin and cross-boundary rules apply for hedges/ditches
  - copia and updating of events across lines are supported

- Line editing operations and quality controls
  - Create New Line: minimum length 5.0 m, cannot cross itself, must be within the square, creates an Unsurveyed/Missing Data event
  - Modify Line: vertex-level editing with insert/delete/move; end nodes shared with other lines require Shared Node Modify
  - Shared Nodes: modify intersections of multiple lines while preserving topology
  - Cut Line: create a cut polygon to remove a segment; ensure resulting segments meet minimum length
  - Reshape Line: reshape using a red overlay to interpolate the desired change; must maintain valid geometry
  - Copy Tool: use landscape areas to guide cut sketches; add/remove features to the edit sketch
  - Delete Line: lines with valid Change for Change reason; scale and single-line deletion enforced
  - Visit status checks for lines: select by attributes to highlight unvisited lines
  - Loops in data: procedures to resolve corrupted loop features by marking as Deleted Feature and re-creating

- Pond mapping methodology
  - map all ponds within a square; designate one survey pond per square for detailed condition assessment
  - pond definitions: standing water 25 m2 to 2 ha, water present for at least 4 months
  - CS2007 Pond Mapping Recording Sheet used to capture pond-level attributes
  - random selection for survey pond; preselected ponds from CS2000 may be retained
  - all ponds mapped before selecting survey pond; CS Surveyor reflects pond status under Inland Water

- Methodology for mapping point features (detailed)
  - points cover trees, water bodies, wells, springs, etc., with one or more components
  - allow creation, movement, deletion, and copying of point attributes and components
  - map scale 1:5000 or finer; points cannot be added outside the square or within 5 m of existing points
  - buffers and other attributes recorded as needed

- Methodology for mapping lineal features (events)
  - lines consist of events along their length; events carry attributes
  - multiple events along a single line; lines can be edited to reflect changes in events

- Woodland types and forestry details
  - polygon-level BH/PH allocation with component-level forestry attributes
  - primary attributes: belts of scrub/trees, belt widths, clumps, woodland/forest, etc.
  - secondary attributes: DBH, species, canopy cover, regeneration, management signs, margins, buffers
  - forestry-related attributes cover management practices (fencing, grazing, pollarding, windthrow) and uses (conservation/recreation)
  - orchards guidance: record traditional orchards as PH opportunities and reflect management intensity

- Practical guidance and support
  - data quality relies on user feedback via helpdesk and wiki fault logging
  - methodology updates issued as Latest News
  - strong emphasis on auditable change accounting (REAL vs. ERROR vs. NEW BASELINE)
  - spatial accuracy is secondary to ensure consistency for UK and country-level reporting

- Summary of key procedures for GIS specialists
  - use CS Surveyor in ArcMap to edit Areas, Lines, and Points; maintain MMU compliance and BH/PH allocation
  - record change status with justification for polygons
  - map habitat types with consistent primary/secondary attributes; capture species data (minimum two species per polygon where applicable)
  - map ponds comprehensively; select survey pond per square for detailed sampling
  - digitize woody linear features with attention to natural shapes vs hedge-like forms; assign appropriate attributes and qualifiers
  - maintain regular save sessions and robust documentation to support cross-square comparability
  - consult Appendix materials (FABs, CS2000/1990 mappings) for historical context and coding schemes as needed