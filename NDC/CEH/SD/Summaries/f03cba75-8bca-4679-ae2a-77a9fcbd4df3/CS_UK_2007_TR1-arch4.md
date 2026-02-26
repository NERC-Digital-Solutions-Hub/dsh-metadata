# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Presents a digital, GIS-based field-mapping framework used to map habitats and landscape features with a focus on accurate habitat classification, change attribution, and time-series data.
  - Supports policy-relevant biodiversity monitoring, planning, governance, and cross-sector analysis through standardized data capture and auditability.

- Digital field mapping system and data model
  - CS Surveyor: bespoke extension to ArcMap used for data capture across three feature types—Areas, Lines, and Points.
  - Data capture emphasizes habitat classification and change attribution over pinpoint spatial precision; spatial accuracy is secondary to correct classification and change rationale.
  - Attributes organized by themes (e.g., Vegetation, Forestry, Inland Water, Agriculture/Natural Vegetation, Structures) with extensive metadata.
  - MMU (Minimum Mappable Unit) is 1/25 ha; polygons smaller than MMU are not mappable unless representing a distinct habitat boundary change.
  - Editing workflow requires logging edits and maintaining session histories; structured procedures govern editing, copying attributes, splitting/merging polygons, updating areas, and managing shared nodes.

- Habitat and feature classification framework
  - Broad Habitats (BH) and Priority Habitats (PH) underpin the classification system; detailed habitat attributes accompany BH/PH designations.
  - Woodland attributes can be tracked at polygon (habitat) and component (woody feature) levels; emphasis on belts/patches, clumps, and woody configurations.
  - Non-native species are recorded as supplementary attributes when present.
  - Woodland and habitat attributes are designed to support time-series analyses and change attribution.

- Change mapping and attribution
  - Surveyors map genuine ecological change since 1998 CS data and correct past misallocations.
  - Change types include Real Change (new habitat allocation based on field evidence) and Error Change (correction of past misallocations).
  - For unenclosed habitats, changes are reconciled with older CS data; for enclosed habitats, data from 1998 is used where applicable.
  - A dedicated “Reason for Change” field and QA steps ensure traceability at both area and component levels.

- Pond mapping (CS2007 ponds)
  - All ponds within a square must be identified and described; a single “survey pond” is selected for detailed condition assessment.
  - Boundaries are delineated using winter water level boundaries and associated vegetation/build-interfaces.
  - Distinctions are made among ponds, temporary ponds, fen/marsh/bog ponds, and connected ditches (ditches are not ponds; dammed streams may not be ponds if flow persists).
  - Detailed pond data are compiled on a CS2007 Pond Mapping Recording Sheet and shared with freshwater surveyors.

- Point and line feature mapping and editing workflows
  - Point features: trees, standing water bodies, ponds, etc.; points can have multiple components; veteran trees may be recorded with detailed attributes (e.g., DBH, epiphytic cover, buffers).
  - Line features: woody linear features, hedges, walls, fences, etc.; lines can contain multiple events (e.g., a hedge with a fence replacement in places) with attributes such as species composition and vegetation cover.
  - Editing tasks (Lines):
    - Create New Line: lines must start at or below 1:5000 scale, be 5.0m minimum length, cannot cross themselves, and must be created within the survey square.
    - Modify Line: edit shape via vertices; shared boundary endpoints are edited via Shared Node Modify; multiple validation checks prevent invalid edits.
    - Shared Nodes: modify intersection points between lines; moving a node updates connected lines while preserving topology.
    - Cut Line: define a cut polygon to remove a segment; length calculations are shown to guide edits.
    - Reshape Line 1/2: reshape existing lines using edit sketches or copied line boundaries; edits must maintain minimum feature length.
    - Copy Tool: use existing polygons from other layers to inform cut-line edits; supports assembling complex cut edits from multiple features.
    - Delete Line: ensure all events have a valid Reason for Change; lines are deleted one at a time at 1:5000 scale or better.
  - Line edit governance ensures edits are traceable, repeatable, and conform to data standards.

- Data governance, quality, and collaboration
  - Strong emphasis on auditability, metadata, and discoverability; encourages co-ownership and collaboration with the wider data community.
  - Rapid deployment of CS Surveyor; bug reporting through a helpdesk and Wiki fault-logging pages; updates published under Latest News.
  - Procedures and mandatory attributes ensure consistent data across squares and over time; transparent change tracking supports policy and governance needs.

- Practical resources and supporting material
  - Appendix-like materials include pond mapping sheets, BH/PH codes, and vegetation keys with indicator species and associations.
  - Detailed guidance for pond boundary identification, temporary pond recognition, and distinctions among ponds, ditches, and dammed streams.
  - Appendix 1 covers using old Field Assessment Booklets (FABs) and older CS2000 references for context and interpretation.
  - Appendices provide field codes, data sheets, and coding structures to standardize data entry and interpretation.

- Historical context and complementary datasets
  - CS2000 and CS1990 provide historical mapping contexts with distinct themes and coding schemes; CS2007 expands to full BH/PH mapping and digital workflows.
  - Previous themes and codes are documented (e.g., five themes in CS1990; six themes in CS2000), with mappings to current codesheets and data structures.
  - Appendix materials include veteran-tree girth guidance and a catalog of loops in square data to assist data quality checks.

- How this supports data-leadership aims
  - Establishes a unified, digitized data framework with standardized feature types, attribute sets, and change-tracking across scales and networks.
  - Enables time-series analyses, policy-aligned biodiversity monitoring, and cross-sector collaboration through consistent metadata and governance.
  - Provides structured data capture, validation workflows, and transparent auditing to support high-quality analytics, reporting, and decision-making.
  - Facilitates scalable data governance and community engagement by documenting changes, providing codesheets, and offering procedures for data correction and updates.