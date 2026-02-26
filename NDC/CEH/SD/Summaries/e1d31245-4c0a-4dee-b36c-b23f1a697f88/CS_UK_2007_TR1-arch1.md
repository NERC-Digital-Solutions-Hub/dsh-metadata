# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Guidance for CS2007 field mapping of woodland landscape features and habitats within 1 km squares.
  - Digital data collection to report habitat change, support monitoring, and enable change detection over time.
  - Includes procedures for mapping Woodland Landscape Features (WLFs), ponds, and related attributes; supports integration with CS1990/CS1999 data where relevant.

- Woodland Landscape Features (WLF) data attributes
  - Height categories: various height ranges (e.g., <1 m, 1–2 m, 2–3 m, >3 m, up to >6 m) with base canopy height notes.
  - Base height: canopy base height (<2 m or >2 m).
  - Species composition: e.g., mixed species, >50% hawthorn, or >50% other species.
  - Evidence of management: categories for recent management (e.g., newly planted, cutting, laying/coppicing) and time since intervention.
  - Line of stumps: whether the WLF forms a line of stumps.
  - Vertical gappiness: percentage of breaks from canopy to ground (e.g., <10%, 10–<25%, 25–<50%, 50–<75%).
  - Margin Left/Right: width of margins on both sides (with presence/absence and width categories).
  - Staked trees: presence of stakes for individual trees (Yes/No within specified margins).
  - Tree protectors: use of protective tubes around newly planted trees (Yes/No within specified margins).
  - Notes: guidance to handle shapes, natural vs unnatural forms, and how to record features that deviate from typical shape.
  - Coding guidance and illustrative examples accompany the pages (images show real-world coding examples for WLFs).

- Interpretation and coding guidance
  - If base height exceeds 2 m, check that woody species are cut or trimmed to maintain natural shape, otherwise record as WLF with natural shape.
  - Distinguish WLFs with unnatural vs natural shapes; record historic management when evident.
  - A set of image-based examples (1–8) illustrates common WLF configurations (unnatural shape, line of stumps, base height, species composition, and management signs).

- Field editing tools and workflow (CS Surveyor)
  - Create New Line: draw a new line within the square; minimum length 5.0 m; line must be within the square; line cannot cross itself; each new line starts with a single Unsurveyed/Missing Data event.
  - Modify Line: edit line geometry by adding/moving/removing vertices; manage shared boundary topology via Shared Nodes; end-point vertices of shared boundaries require Shared Node Modify.
  - Shared Nodes: modify intersection points where multiple lines meet; changes propagate to connected lines; ensure edits do not create invalid intersections.
  - Cut Line: define a polygon along the line to cut, specifying the portion to remove; pink/white vs red highlighting shows cut vs remaining lengths.
  - Modifying the Edit Sketch: adjust the cut shape by moving vertices before finalizing the cut.
  - Copy Tool: reuse features from other layers (e.g., OS Mastermap) to build accurate edit sketches; integrate with Cut Line edits.
  - Delete Line: delete a line only if all attached events have valid Reasons for Change; scale restriction applies (1:5000 or less).
  - Reshape Line: adjust lines by drawing a reshape graphic to define the start/end of the edit; requires scale restriction.
  - Reshape Line 2 (follow line): reshape a line by following an existing boundary copied feature; ensures edited line follows landscape boundary.
  - Checks and validation: line edits must maintain minimum lengths and avoid creating new intersections; shared node edits must preserve topology.

- Line editing and data integrity considerations
  - Edits must be scoped to the survey square and must preserve dataset integrity; avoid creating invalid intersections.
  - Endpoints shared with other lines require special handling via Shared Node Modify.
  - Deleting lines requires valid Reasons for Change for all events on the line.

- Line visit status and data quality checks
  - Unvisited lines are highlighted via a Select By Attributes workflow (Landscape Events, VISIT_STATUS = 0).
  - Special handling for loops: a set of loop features in the data requires corrective actions (marking as Deleted Feature, setting Reason for Change to No Change, completing visits, and re-creating the lines as needed).

- Pond mapping and survey protocol (CS2007)
  - All ponds in a square must be recorded on the CS2007 Pond Mapping Recording Sheet; a survey pond is selected for detailed condition assessment (pond sampling) via a documented randomization process.
  - Records include pond polygon ID, area, water presence, reasons for pond loss/creation, and notes.
  - For CS2000 ponds, reasons for loss or retention are captured to trace changes since earlier surveys.
  - Boundary delineation relies on winter water levels, vegetation boundaries, and break-of-slope markers; temporary and interconnected ponds require careful boundary identification.

- Data provenance, metadata, and governance
  - Emphasis on data provenance, traceability, and accompanying metadata for datasets created or modified in CS Surveyor.
  - Focus on capturing extent and change over time, with spatial accuracy treated as secondary to consistent habitat representations and change detection.
  - Methodology supports UK Biodiversity Action Plans through standardized BH/PH classifications and detailed vegetation attributes.

- Practical challenges and analyst considerations
  - Methods are designed to unify data from multiple sources, handle local-scale variations, and integrate historical CS datasets for change detection.
  - Acknowledges data accessibility challenges, the need for standardization, and the importance of metadata and dataset discoverability for reuse and analysis across time and geography.

- Appendices and supplementary material (highlights)
  - Appendix 5: Girth sizes of veteran trees—rules of thumb for assessing veteran status by species based on maximum girth, with threshold percentages for potentially interesting, valuable, and truly ancient classifications.
  - Appendix 6: Squares with loops—listing of unique squares containing looped features and associated route/bounding box data (illustrative of data quality concerns requiring remediation).
  - Appendix 3: CS2007 Pond Mapping Recording Sheet—format and fields for per-square pond data collection, including reason codes for pond loss/creation and pre-selection logic for survey ponds.
  - Appendices for historical data (CS1990/CS2000) illustrating legacy coding, parcel numbers, and data sheets to support data integration and change analysis.

- Publication and access
  - Document is a Natural Environment Research Council (NERC) publication; reproductions permitted for research and internal use with proper attribution.
  - Countryside Survey project information and contact details provided for further information.