# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- Overview
  - The field handbook documents how habitat attributes are mapped to produce time-series, attested data across squares for ecological analysis and policy-relevant insights.
  - Data are intended to be discoverable, stored, shared, and reused, with governance, standards, provenance, and versioning in place.

- Visit status and survey workflow
  - Each Event, Point, and Area includes a VISIT STATUS field to track survey progress:
    - 0 = UNSURVEYED
    - 1 = IN PROGRESS
    - 2 = COMPLETED
    - 3 = REFUSED ACCESS
  - Use of VISIT STATUS:
    - REFUSED ACCESS identifies areas not surveyed; IN PROGRESS indicates partial or ongoing work; COMPLETED should be used only when the feature is fully mapped.
    - When a square is finished, all features should be marked as COMPLETED or REFUSED ACCESS to reflect survey completion.
    - VISIT STATUS helps ensure the entire square is surveyed and data are ready for analysis.
  - How to search and manage by VISIT STATUS:
    - Layer choices: Landscape Points, Landscape Events, or Landscape Areas.
    - Fields: VISIT STATUS (selected from a dropdown; enter 0, 1, 2, or 3 by number).
    - Find command: quick method to locate unsurveyed or in-progress features; flashes on map; supports panning and zooming to features.
    - Select by Attributes: highlights all features meeting criteria; can search across multiple terms and layers; can be saved for reuse.
    - Attribute Table: lists features; SHOW SELECTION must be used to view only selected items; multiple criteria can be used sequentially but typically one at a time.
    - Tips: you can keep Find open during edits; to remove highlights use the clear selection option; unique values mode can simplify number entry.
  - Practical guidance:
    - Use Find or Select by Attributes to drive follow-up surveys and ensure timely completion.
    - The SEARCH tools are not multi-layer in a single query; you must switch layers between searches.

- Managing Minimum Mapping Units (MMU) and editing
  - No polygon or line should be mapped smaller than the designated MMU.
  - When small fragments occur at square edges, include them in the adjoining polygon or leave as is for edge cases.
  - For splitting a larger polygon into parts:
    - Preferred approach is to use UPDATE to split and merge in one operation, avoiding the creation of an MMU-sized polygon that would be problematic.
    - Selection and editing can involve combining features from Mastermap and Landscape Areas; Copy + and Copy - allow adding or removing areas from a selection to facilitate complex edits.
  - Freehand selection tools and multi-layer copying enable efficient edits without losing data integrity.

- Ancient and veteran trees: identification guidance
  - Definition: ancient/veteran trees are old relative to others of the same species; indicators include large girth, substantial dead wood, hollow trunks, and other aging features.
  - Girth considerations:
    - Tree girth is measured at 1.3 meters above ground (DBH) and is used as a proxy for identifying ancient status, but it is not infallible.
    - Species-specific minimum girth thresholds exist (examples in a species table); larger trees are more likely to be ancient, but confirmation should consider additional indicators.
  - Other indicators of ancient trees:
    - Large amounts of dead wood, hollow trunks, cavities, naturally forming water features, trunk damage, decay holes, bark loss, crevices, presence of sap, fungi, epiphytes, and high biodiversity value.
  - Measurement guidance:
    - DBH is the standard measurement; use a girth tape at 1.3 meters height; note that pollarded or managed trees may not meet simple girth thresholds yet still be ancient.
  - Practical notes:
    - The table of species-specific girth thresholds provides a framework, but validation should rely on a combination of girth and aging features.
    - The terms ancient tree and veteran tree are interchangeable in this context; thresholds are guides rather than strict cutoffs.

- Data governance and documentation implications for data stewards
  - Ensure VISIT STATUS fields are consistently populated to support data quality and surveying completeness across squares.
  - Maintain clear provenance and versioning for habitat attributes, including updates to ancient tree records and any MMU-related edits.
  - Enforce standardized querying and reporting practices (Find, Select by Attributes, Attribute Table) to support reproducible analyses.
  - Capture metadata and field notes that contextualize survey results, including reasons for refused access and any partial mappings.
  - Ensure integration of VISIT STATUS with other governance layers to support analytics, reporting, and monitoring of dataset health over time.

- Practical challenges and governance considerations
  - Incomplete user needs or gaps in survey data may require robust standards and thorough metadata.
  - Variability in data receipt timing from field teams necessitates clear timelines and validation steps.
  - Interoperability across diverse systems and formats requires standardized attribute schemas and GIS masks.
  - Handling large data volumes, mosaics, and repeat surveys while preserving analytic integrity and historical comparability.