# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

## Overview (data-focused)

- The document provides field data collection and governance guidelines for mapping habitat attributes, focusing on data capture, quality, and usability for policy and biodiversity reporting.
- Emphasizes structured attribute capture (primary/secondary BH/PH attributes, Vegetation Key, woody features, species lists, margins, water features, HEA) and standardized workflows for consistency across surveyors and squares.
- Supports integration with GIS (ArcGIS) layers and cross-referencing with Countryside Survey data for trend analysis.

## Visit Status: data management and quality control

- Each feature (Event, Point, Area) must have a VISIT STATUS field to reflect access and progress:
  - 0 = unsurveyed
  - 1 = IN PROGRESS
  - 2 = COMPLETED
  - 3 = REFUSED ACCESS
- Purpose of VISIT STATUS:
  - Documents access permissions, survey progress, and completeness for robust analysis.
  - Helps manage large areas or long linear features where full extent or species composition may be uncertain.
- Use and interpretation:
  - COMPLETED should only be used when the feature is mapped in full; otherwise use IN PROGRESS or REFUSED ACCESS.
  - After finishing a square, all features should be marked as COMPLETED or REFUSED ACCESS to reflect true completion.
  - VISIT STATUS informs data analysts whether a square has been fully surveyed.

## Searching and managing VISIT STATUS (three approaches)

- Three search modalities by layer: Landscape Points, Landscape Events, Landscape Areas.
- Options for searching VISIT STATUS (0–3) via:
  - Find: quick one-layer, one-criteria search (e.g., 0 or 1). Features flash on the map; use Zoom to feature to locate obscured items.
  - Select by Attribute: multi-criteria capable; can highlight features on the map for 0 and 1 simultaneously, but does not produce a list. Build queries with OR logic and apply; save queries for reuse.
  - Attribute Table: lists all features; use SHOW SELECTION to focus on selected items. Typically one criterion at a time; can invert selection to find non-completed features.
- Practical notes:
  - For efficient workflow, keep Find open during editing and use it to iteratively complete features.
  - If you need to survey different parts of a square, saved queries and multi-criteria searches can streamline the process.

## Handling MMUs (minimum mapping units) and editing

- No mapping for features smaller than MMU; small fragments may be included in adjoining polygons when unavoidable.
- To split or merge polygons without losing data:
  - Use UPDATE to split/merge in one operation, preserving attribute data.
  - Use copy/paste and layered selection (Landscape Areas vs MasterMap) to add or remove areas without creating new, invalid polygons.
  - FREEHAND drawing and ADD TO SELECTION can be combined across layers to manage complex edits.

## Ancient/Veteran trees: data definitions and measurement

- Definition and purpose:
  - Ancient (veteran) trees are identifiable by age-related features and contribute to habitat quality; not solely determined by size.
- Key identification criteria:
  - Morphological indicators: large girth for species, substantial dead wood, hollow trunks, cavities, decay features, and evidence of long-term stability.
  - Additional indicators: naturally forming water pools, bark loss, cracks, fungal fruiting bodies, epiphytes, high wildlife interdependence, historic/cultural value, and pollard history.
- Girth and measurement guidance:
  - Girth (diameter at breast height, DBH) is measured at 1.3 metres above ground using a girth tape.
  - Species-specific minimum girth thresholds are provided (various species listed) to guide categorization into levels such as potentially interesting, valuable, and truly ancient.
  - Thresholds are context-dependent; girth alone is not sufficient to determine ancient status.
- Practical caveats:
  - Pollarded or managed trees may not meet strict girth criteria yet display ancient characteristics.
  - Use a holistic assessment of multiple indicators rather than relying solely on girth.

## Data outputs and governance (data product readiness)

- Outputs include habitat maps with BH/PH classifications, vegetation and species lists with cover estimates, woodland attributes (DBH, veteran trees), pond inventories, and HEA data.
- Data are designed for integration into GIS workflows and cross-referencing with historical datasets to support policy, biodiversity monitoring, and trend analysis.
- Governance notes emphasize consistent documentation, versioning, and traceability of field protocols to ensure repeatability and data quality over time.