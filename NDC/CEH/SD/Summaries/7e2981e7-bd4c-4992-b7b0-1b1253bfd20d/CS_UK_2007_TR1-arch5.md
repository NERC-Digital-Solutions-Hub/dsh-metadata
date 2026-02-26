# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose: Establish a comprehensive, digital data collection framework for Field Mapping of Broad Habitats (BH) and Priority Habitats (PH) across the UK to support national biodiversity monitoring; emphasize standardization, change management, and metadata-rich attribute schemas for long-term discoverability and interoperability.
- Data capture platform: CS Surveyor extension within ArcMap; standardized map layers with pre-set symbology; data stored as Areas (polygons), Lines (linear features), and Points (point features).
- Minimum mapping unit: MMU of 1/25 hectare for areas; defined minimums for lines and points; spatial accuracy secondary to extent and change tracking.
- Pond-centric approach: every square documents ponds; one survey pond per square selected for condition assessment; pond selection relies on preselected or randomly chosen ponds depending on square history and new pond discoveries.

## Data Model and Digital Mapping System
- Three core feature types:
  - Areas: BH/PH classifications with extensive thematic attributes.
  - Lines: woody and non-woody linear features, including hedges, belts, fences, banks; line events captured along lines.
  - Points: individual trees, ponds, structures, veteran trees, and other landscape features; support for multiple components and buffers.
- Ontology and classification:
  - BHs and PHs are organized (BH1–BH19, PH components) with nested relationships (PH often within BH in enclosed/unenclosed contexts).
  - Vegetation Key and woodland Key guide habitat assignments and woodland classifications.
- Data content and metadata: rich attribute schemas across themes ( Physiography, Vegetation, Species, Coverage, Land-use, etc.); explicit guidance on when/how to record each attribute; non-native species flagged.

## Data Collection and Workflows
- Digital collection mandatory for change reporting and correcting past allocations; ongoing square-by-square editing workflow.
- Change management:
  - Distinguish REAL ecological change from corrected errors (REAL vs ERROR).
  - Edits logged with explicit reasons (e.g., error, real change, new baseline).
- Habitat assignment workflow:
  - Use Vegetation Key and woodlandKey to assign BH/PH; post-survey GIS masks support standardized extent estimates.
  - Preselection/randomization of ponds ensures representative sampling; process accommodates squares without prior mapping and new pond discoveries.
- Data integrity and governance:
  - Mandatory fields; explicit saving of editing sessions; tracking of changes and rationale.

## Habitat Classification and Keys
- Detailed BH/PH framework:
  - BH categories (BH1–BH19) plus BH22 and related aquatic/coastal components.
  - PH components nested within BH contexts (e.g., PH nesting within BHs like grasslands, wetlands, woodlands).
- Classification guidance:
  - Vegetation-based primary/secondary attributes for polygons.
  - Woodland types/features tool for rapid classification (belts, clumps, woodlands, scrub, lines of trees, etc.).
- Special handling:
  - Enclosed vs unenclosed habitats treated to capture distinct vegetation structure and history; PHs are often nested within BHs.

## Features and Attributes
- Areas (polygons): BH/PH classifications plus themes such as Forestry, Agriculture/Natural Vegetation, Inland Physiography, etc., with corresponding attributes.
- Woodland attributes: Primary/Secondary woods, belts, clumps, hedges, parkland, and buffers; species presence, cover, and modal DBH data.
- Other BHs: Broad categories including Arable/Horticulture, Grasslands, Wetlands (Fen/Marsh/Swamp, Bog), Rivers/Streams, Standing Open Waters/Canals, Montane, Inland Rock, Urban, and coastal/mosaic landscapes.
- Ponds and water features: pond boundaries, area, maximum winter water level, water presence, and notes on pond status; one survey pond per square for detailed assessment.
- Points and lines: attributes for points (e.g., trees, ponds) and line features (e.g., hedges, fences, banks); margins, buffers, and event data along lines; scale requirements and edit constraints.

## Pond and Water Features
- CS2007 Pond Mapping Recording Sheet documents pond-level data for all ponds within a square; one pond per square designated as the survey pond.
- Delineation relies on winter water levels and vegetation transitions; forms capture pond area, presence/absence, and reasons for pond loss/creation.
- Process supports long-term pond inventory, sampling, and linkage to the broader habitat dataset.

## Mapping Point and Linear Features
- Points: creation, movement, deletion, and attribute editing; scale 1:5000 or better; support for multiple components per point; veteran trees tracked with specific criteria.
- Lines: creation, modification, cutting, reshaping, and copying; minimum line length enforced; shared nodes and topology considerations; line edits propagate to connected features.
- Edit tools and workflows:
  - Create Line, Modify Line, Cut Line, Reshape Line, Copy Features, Delete Line, and Reshape Following Copied Line.
  - Shared nodes and boundary edits require careful handling to preserve topology and avoid invalid geometries.
  - Event-level attributes along lines must have valid Reason for Change values for deletions and significant edits.
- Quality checks:
  - Checks for unvisited linear features via attribute queries; loops and data integrity issues documented with described remediation steps.

## Data Quality, Governance, and Change Management
- Central emphasis on governance: clearly differentiate genuine ecological change from corrections to earlier data.
- Data integrity rules:
  - Mandatory field values; explicit save of editing sessions; changes logged with reasons.
  - MMU-based polygon creation rules; small features (< MMU) generally not mapped unless edge cases require it.
- Pond selection process and sampling design ensure representative data across squares and years.
- Documentation and support:
  - CS Surveyor is Esri-based with bug reporting via helpdesk; updates are communicated through a News mechanism.
  - Appendices provide coding sheets, pond sheets, and field references to support consistent data entry over time.

## Data Access, Documentation, and Support for Data Stewards
- Data capture/editing occurs in ArcMap via CS Surveyor; datasets are designed for discoverability and interoperability through standard GIS portals.
- Comprehensive guidance on attribute schemas, data entry rules, and workflows to enable uniform governance across survey squares and years.
- Appendix materials include data collection sheets (CS2007 Pond Mapping Recording Sheet), coding sheets, random-number tables for pond selection, and field references for long-term continuity.

## Appendix and Supporting Materials
- Coding sheets, pond mapping sheets, random-number tables, and field references to support consistent data entry and historical continuity.
- Illustrative examples, stakeholder maps, and reference tables (e.g., for pond selection, wood/vegetation coding, and veteran tree criteria) accompany the handbook to facilitate implementation.

## Key Takeaways for Data Stewards
- The CS2007 Field Mapping Handbook provides a robust, digital framework for BH/PH habitat mapping, woodland classification, and pond/water features across the UK.
- It promotes standardization, rigorous change management, and metadata-rich attribute schemas to support national biodiversity monitoring, interoperability, and long-term discoverability.
- The data model integrates Areas, Lines, and Points with detailed thematic attributes, coupled with practical editing tools and governance procedures to ensure data quality, consistency, and traceability over multiple survey years.