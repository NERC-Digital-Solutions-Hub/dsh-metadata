# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and audience
  - Comprehensive guide for mapping habitats, landscape features and related attributes in CS2007 using a digital GIS workflow.
  - Aims to produce map-based data products that clearly convey habitat types, landscape features, and their changes for policy support and reporting.
  - Introduces CS Surveyor, a GIS extension for ArcMap, to capture extent and change, manage data quality, and support time-series analysis.

- Data model and core classifications
  - Supports Broad Habitats (BH) and Priority Habitats (PH) with changes tracked over time.
  - Uses polygons (areas), lines (linear features), and points (discrete features), with components within areas and events along lines.
  - Two core keys for classification:
    - Vegetation Key (BH/PH attributes)
    - Key to Woodland Types/Features (woody vegetation structure and BH/PH allocation)
  - Time-series and data integration are central, enabling reporting at BH/PH levels with change history.

- Mapping approach and granularity
  - Enclosed (lowland) vs unenclosed (upland) habitats mapped with varying attribute detail.
  - Time-series emphasis: supports preserving and analyzing changes over multiple survey epochs.
  - Wales adds 60 new squares for country-level habitat reporting.
  - Detailed vegetation attributes are recorded for polygons; PH mapping is more precise for time-series work.

- The CS Surveyor tool
  - ArcMap extension used to edit Areas (polygons), Lines (linear features), and Points within a Countryside Survey square.
  - Data capture prioritizes extent and change over pixel-level spatial accuracy.
  - Regular saving and error handling via helpdesk or project wiki.

- Areas (polygons) editing and rules
  - Editing operations: Edit, Copy Attributes, Split Areas, Merge Areas, Modify Area, Update Areas.
  - Components within an area can be added, copied, or deleted; each area must contain at least one component.
  - Attribute editing at polygon level (area size, BH/PH assignment, accuracy, reason for change, visit status) and component level (primary/secondary attributes, vegetation type, species, proportions, DBH, qualifiers).
  - Change types:
    - REAL: genuine change in allocation (e.g., 1998 allocation no longer applies)
    - ERROR: prior allocation incorrect
    - NEW BASELINE: newly subdivided units (e.g., upland hay meadow vs Neutral grassland)
  - Mapping rules include:
    - Continuous woodland within a polygon maps to BH/PH accordingly
    - Minimum Mapping Unit (MMU) is 1/25 hectare (400 m2)
    - Record at least two species (up to four) per polygon
    - Mosaic polygons described with component-level habitat percentages totaling 100%

- Lines editing, events, and topology
  - Create Line: minimum 5.0 m length, scale ≤ 1:5000, lines cannot cross themselves, lines created with an Unsurveyed/Missing Data event.
  - Modify Line: edit shape via vertices, with shared nodes and topology considerations; end nodes shared with other lines can only be edited via Shared Node Modify.
  - Shared Nodes: modify intersections of multiple lines; preserves topological integrity.
  - Cut Line: cut along a user-defined polygon; edits show length to cut and length to remain; multiple cuts allowed but must meet minimum lengths.
  - Reshape Line: re-shape along an existing line using an edit sketch; requires scale constraint.
  - Copy Tool: use features from other layers (e.g., OS Mastermap) to form accurate edit sketches for cuts.
  - Delete Line: lines with events lacking a valid Reason for Change cannot be deleted; delete removes the line and its events.
  - Validation and constraints: edits must maintain topology, avoid creating invalid intersections, and respect minimum lengths.
  - Event attributes: lines can host multiple events along their length (e.g., fences, hedges, woody features) with length, condition, and classification.

- Points and woody linear features (WLFs)
  - Points: edited via Points tab; attributes include discrete landscape elements, with optional buffer zones; scale 1:5000 or smaller; one point per operation; minimum 5 m separation.
  - WLFs (e.g., hedges, line of trees): documented by form and attributes along the line; natural shape vs unmanaged vs hedge-like forms influence recording.
  - Important width, height, and composition cues are recorded; margins and staked trees are captured as field attributes.

- Woodland-specific attributes and veteran trees
  - BH/PH assignments can apply to woodland features; attributes include belt of scrub, belt of trees, clumps, forested belts, and canopy-related descriptors.
  - Tree-related data: modal DBH, species composition, species cover, buffer zones, and veteran trees (up to 10 per square; up to 2 per species).
  - Other forestry-related attributes: fences, grazing, regeneration, windthrow, staked trees, tree guards, orchard handling as agricultural crops when PH candidates.

- Ponds and inland water mapping
  - Pond mapping requires a CS2007 Pond Mapping Recording Sheet per square; one survey pond selected for detailed condition survey.
  - Pond criteria: 25 m2 to 2 ha area; typically water for at least four months; boundaries determined by vegetation changes, water marks, banks, or winter waterline.
  - Temporary ponds identified by wetland vegetation and other indicators.
  - Boundary decisions consider pond connectivity and whether ponds are distinct or merged.
  - Post-map workflow transfers pond details to CS Surveyor; detailed condition data captured via a dedicated pond form.

- Margins, buffer zones, and non-native species
  - Field margins mapped as areas; typical widths around 6 m, with potential additive margins.
  - Buffer zones around features recorded to reflect landowner requirements.
  - A predefined list of non-native species to record where present.

- Coding schemes and historical context
  - CS2007 codes and data sheets align with CS1990 and CS2000 practices, enabling comparability and time-series analysis.
  - Extensive code lists for themes (Agriculture/Natural Vegetation, Boundaries, Forestry, Physiography, Structures, etc.) and universal/broad attribute codes.
  - Appendix material covers old field sheets (FABs) and fieldhandbook references for interpreting habitat types and changes.

- Loops, data quality, and maintenance
  - Appendix 6 lists squares with loops; loops contain corrupted event data requiring a repair workflow:
    - Change event themes to Deleted Feature with appropriate Reason for Change (No Change)
    - Delete affected lines per protocol and reinstate lines accurately
  - Survey data includes procedures for identifying and resolving these loop issues during editing.

- veteran-tree girth guidelines (Appendix 5)
  - Provides rules-of-thumb for categorizing veteran trees by girth across multiple species, supporting standardized documentation of notable trees.

- Support, updates, and ongoing development
  - CS Surveyor and methodology are rapidly evolving; updates appear in the Latest News.
  - Helpdesk and wiki provided for fault logging, field guidance, and topographic editing.
  - The ArcMap interface and CS Surveyor are designed to facilitate habitat extent mapping, change detection, and robust time-series analysis.

- Legal and access notes
  - Publication is NERC copyright with rights for research and internal organizational use.
  - Countryside Survey program details and contact information provided for further inquiries.