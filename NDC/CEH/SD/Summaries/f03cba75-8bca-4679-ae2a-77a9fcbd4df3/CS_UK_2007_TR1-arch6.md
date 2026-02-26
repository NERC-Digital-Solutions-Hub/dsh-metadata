# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Documents the CS2007 digital field-mapping approach for reporting habitat change and land cover across the UK.
  - Focuses on Broad Habitats (BH) and Priority Habitats (PH) and supports time-series reporting for monitoring (e.g., UK Biodiversity Action Plan).
  - Extends prior CS surveys (CS1990, CS1998, CS2000) by adding more detail and delivering data digitally for broader analysis.

- Data model and habitat classification
  - Habitats are classified into BH and PH using two main keys:
    - Vegetation Key: assigns polygons to BHs/PHs based on plant composition and canopy attributes.
    - Woodland Key: classifies woody vegetation (belt, line, clump, woodland/forest, etc.) at the component level to aid BH/PH attribution.
  - Mapping units and attributes
    - Polygons represent habitat areas; components subdivide attributes within a polygon.
    - Enclosed vs unenclosed habitats have different recording approaches; mosaics allowed when delineation is not possible.
    - Outputs include detailed BH/PH attributes, including indicators such as dominant vegetation and presence of non-native species; orchard considerations integrated.
  - Support for transitions and complex boundaries
    - Explicit treatment of PHs within BHs and transitional zones (upland moss/peat, etc.).

- Mapping units and data attributes
  - Three central feature types: Areas (polygons), Lines (linear features), and Points (mapping points).
  - Areas (1) attributes at polygon and component levels; multiple components per area; MMU rule set.
  - Minimum mappable unit (MMU): 1/25 hectare (400 m2); smaller units not mapped as areas unless part of a larger polygon.
  - Vegetation descriptors require at least two species per polygon (maximum four).
  - Points capture individual trees, scrub, ponds, etc., with species and structural attributes.
  - Linear features capture fences, hedges, walls, ditches; larger features (>5 m wide at base) mapped as areas when appropriate.
  - Ponds mapping: 25 m2 to 2 ha, standing water for at least four months; all ponds in a square must be identified; one survey pond selected for condition assessment; boundaries defined by winter water level or vegetation/water cues; pond attributes recorded separately.

- Digital mapping system and workflow
  - CS Surveyor: ArcGIS-based extension used to capture, view, and edit mapping data for each 1 km square.
  - Change recording is mandatory for edits, distinguishing genuine ecological change from prior data errors.
  - Regular updates and fault logging; emphasis on recording habitat extent and change over exact geometry.
  - Guidance to ensure all mapped components are visited; spatial accuracy prioritized to reflect habitat extent and change.

- Data management, governance, and quality
  - Two-tier attribute system (primary and secondary attributes) organized by themes.
  - Change classification with audit trail: REAL vs ERROR; maintains clear baselines for PH allocations and outputs.
  - Data provenance and traceability are essential for policy-relevant biodiversity monitoring.
  - Standards to verify data quality (e.g., minimum two species per polygon) and robust recording of change reasons.

- Editing tools and workflows (within CS Surveyor)
  - Edits for areas: Split Areas, Merge Areas, Modify Area, Update Areas; topological edits and shared node edits.
  - Attribute copying to reduce duplicate entry across areas/components.
  - Lines editing: Create Line, Modify Line, Cut Line, Reshape Line, Copy features for accurate line edits; lines must meet minimum length and scale requirements.
  - Shared nodes: modify topology where lines intersect; careful handling to avoid invalid intersections.
  - Deletion and reshaping: lines edited with appropriate safeguards; 1:5000 map scale or less required for major line edits (delete/reshape).
  - Visit-status checks for linear features via attribute-based queries; procedures exist for handling data loops with corrupted event data.

- Pond mapping specifics and data sheets
  - Dedicated pond mapping workflow (Pond Mapping Recording Sheet) and CS Surveyor integration.
  - Preselection of survey pond; record-keeping for ponds that no longer exist; reasons for loss/creation documented.
  - Pond boundaries defined by winter water level or observable cues; pond condition data collected separately by freshwater surveyors.

- Outputs, documentation, and governance details
  - Outputs support time-series habitat change analysis and BH/PH reporting; integration with CS1990/CS1998/CS2000 datasets is managed via baseline designations and change classifications.
  - Documentation includes Field Assessment Booklets (FABs) and older CS2000 references to aid interpretation; electronic FABs and FAB-like references provided for field issues.
  - Appendices outline loops with corrupted data (Appendix 6) and procedures to resolve such issues and reinstate data.

- Practical implications for data management and analysis
  - Delivers a comprehensive GIS-centric data model enabling change detection, time-series analysis, and PH/BH reporting.
  - Provides structured data products (areas, lines, points) with consistent attribute schemas across themes (physiography, vegetation, forestry, structures, coastal features, etc.).
  - Facilitates integration with legacy CS datasets through careful change classification and baseline designation.
  - Establishes data quality controls, provenance, and audit trails essential for policy-relevant biodiversity monitoring.
  - Emphasizes ecological realism and consistency over ultra-precise spatial geometry, with explicit rationale documentation for all changes.

- Challenges and common considerations for data support
  - Time spent understanding the ask due to data gaps in wider teams.
  - Handling patchy data across diverse formats and systems.
  - Communicating complex information clearly to end users.
  - Promoting adoption and reuse of outputs to maximise impact.