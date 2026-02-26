# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Defines the CS2007 field mapping project and its shift to digital data capture for habitat and landscape features across 1 km squares.
- Aims to report land cover change by Broad Habitats (BHs) and Priority Habitats (PHs) at country/UK levels, with finer detail for unenclosed uplands and Wales.
- Integrates five previous themes into a single digital map model, emphasizing change reporting, data quality, and cross-partner collaboration.

## Data Architecture and Classification
- Data model includes three feature types: Areas (polygons), Lines (linear features), Points (points), with a component-based structure for Areas.
- Minimum Mapping Unit (MMU) is 1/25 hectare; features below are not mapped as areas unless necessary (e.g., lines).
- BH and PH classifications are polygon-level; PH nests under BHs. PHs may be newly mapped and require GIS masks for extent estimation.
- Two instructional keys used for classification:
  - Vegetation Key: assigns BH/PH based on vegetation composition and supports change validation.
  - Key to Woodland Types/Features: classifies woody vegetation with primary/secondary attributes.
- Detailed habitat list (e.g., BH1 Broadleaved Woodland, BH2 Coniferous, BH3 Boundaries, BH4 Arable, BH5 Improved Grass, etc.), with mosaics used when MMU or boundary ambiguity applies.
- Woodland attributes include primary (e.g., Belt of trees, Clump of trees, Woodland/Forest) and secondary attributes (species, DBH, structure); non-native species monitored.
- Species data recorded within habitat polygons (minimum two species; up to four).

## Data Collection Workflow and Tools
- Digital system: CS Surveyor extension within ArcMap; integrates CEH and ESRI tech, with standardized data frame and symbology.
- Focus on extent and change rather than precise spatial accuracy; field edits ensure habitat representation matches conditions.
- Change reporting is mandatory for each mapped habitat/feature, distinguishing real changes from corrections (errors) to baselines (1990/1998).
- Wales expansion adds squares to enable country-level PH reporting.
- Pond mapping protocol:
  - Map all ponds in a square; designate one survey pond for detailed condition assessment.
  - Documentation includes pond area, water presence, gain/loss reasons, and creation/reason notes.
  - Preselected ponds may be used if valid; random selection via random-number table when needed.
- Data stored in CS2007 layers; pond data linked to a preselected pond file on the tablet.
- Point features: review/edit point attributes; create/move/delete points with rules (scale ≤ 1:5000, within square, minimum separation).
- Linear features: record as lines with events (fences, hedges, woody lines, walls, etc.); some lines treated as wide linear features (BH 3) when warranted.
- Editing toolbox supports copy/merge/split/update operations, topology edits, and mandatory “Reason for Change” fields.

## Data Quality, Change Management, and Governance
- Clear criteria for real changes versus errors; back-correcting 1990 CS1990 and 1998 data where applicable.
- PH mapping uses GIS masks to constrain extent; mosaics used when precise delimitation isn’t possible or MMU constraints apply.
- Habitat polygons include at least two species recorded (up to four); canopy/vegetation attributes include percent cover.
- Support and governance tools: dedicated helpdesk, Wiki fault-logging, methodology updates in Latest News.
- Buffer zones are recorded to reflect landowner practices and compliance.

## Data Management and Shareability
- Dataset designed for broad, cross-network use and UK-wide program integration.
- Post-survey processing relies on standardized habitat keys and coding to maintain consistency across partners.
- Metadata completeness, provenance, and audit trails are emphasized for all changes (including reason for change and visit status).

## Implications for Data Leaders (Data Strategy Perspective)
- Establish and enforce a robust data governance framework for field mapping data:
  - Standard BH/PH codes, clear change management rules, and audit trails.
- Prioritize data quality and consistency:
  - Adhere to MMU constraints, two-key allocation approaches, and mandatory species documentation per polygon.
- Invest in scalable data architecture:
  - Support polygon/area, line, and point editing with component-level attributes for mosaic/mixed-vegetation scenarios.
- Promote discoverability and interoperability:
  - Maintain standardized attribute schemas, metadata, and cross-partner sharing practices.
- Address data protection and access barriers:
  - Develop governance policies and foster sector collaboration to minimize duplication and improve access to restricted data.
- Plan for ongoing system maintenance and user support:
  - Support structures (helpdesk, bug logging) given CS Surveyor/ArcMap complexity and multi-partner use.

## Practical Takeaways for Implementation and Leadership
- Enforce stringent habitat classification, woodland delineation, and change-tracking procedures to enable consistent landscape-scale data over time.
- Leverage digital mapping to enable rigorous change detection; use pond sampling protocol for representative pond data.
- Foster collaboration with the wider data community and use standardized keys/masks for scalable, repeatable analysis.
- Ensure training and ongoing support are available to sustain data quality and governance across partners.