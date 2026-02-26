# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Provides methodology for field mapping in CS2007 UK Countryside Survey to monitor land cover change and habitats.
- Introduces digital data collection (CS Surveyor) integrated with ArcMap; emphasizes consistency, data quality, openness, and governance.
- Documents how woody linear features (WLFs) and other features are recorded, edited, and managed to support longitudinal habitat monitoring.

## WLF: Unnatural shape attributes
- Height (categories): <1m, 1-2m, 2-3m, >3m, 3-4m, 4-6m, >6m; base height refers to canopy base height.
- Species composition: e.g., mixed species, or >50% of a particular species (e.g., hawthorn).
- Evidence of management: none, newly planted, cutting (e.g., flail or saw <3 yrs), laying or coppicing (<5 yrs), or both.
- Line of stumps: yes/no.
- Vertical gappiness: percentage of breaks extending from canopy to ground (e.g., <10%, 10-<25%, 25-<50%, 50-<75%).
- Margin widths: left and right margins with categories (e.g., not present, <2m, 2m-<4m, etc.).
- Staked trees and tree protectors: yes/no for specific segments and 1m high protectors.
- Note: If >2m height, ensure that component species are trimmed to a natural shape; record as WLF natural shape if appropriate.

## Data entry fields and coding (example fields)
- WLF unnatural shape /line of stumps, height, base canopy height, species composition, management evidence, line of stumps, vertical gappiness, margins, staked trees, tree protectors.
- Coding examples illustrate how to record multiple sections/segments with differing attributes within the same WLF.

## Field editing procedures and tools
- Create New Line: add a new line at scale 1:5000 or better; minimum length 5.0 m; lines cannot cross themselves; a new line starts with an Unsurveyed/Missing Data event.
- Modify Line: edit shape via vertices; insert/delete/move vertices; end-point shared nodes can require Shared Node Modify; ensure edits do not create intersections with other lines.
- Shared Nodes: modify nodes where multiple lines meet; carefully move the node to maintain topology and prevent unintended intersections.
- Cut Line: use a cut polygon along the line to remove a segment; pink/white length shows cut portion; confirm to apply.
- Modifying the Edit Sketch: adjust the polygon used to cut; use vertex editing to refine before cutting.
- Copy Tool: import features from other layers (e.g., OS Mastermap) to construct accurate edit sketches; can Cut+ multiple features.
- Delete Line: delete only when all events have valid Reasons for Change; map scale must be 1:5000 or less; delete is single-line at a time.
- Reshape Line: reshape along existing line using a reshape graphic; ensure intersections and endpoints align with the original line; scale constraint applies.
- Reshape Line 2: follow a copied line boundary for reshaping; adjustments must intersect the target line at start/end; scale constraint applies.
- Checking Visit Status on linear features: use attribute queries to highlight unvisited lines; loops in data may require special handling (see Appendix 6).

## Editing constraints and data integrity
- Minimum linear feature length requirements; edits producing sub-threshold features are not permitted.
- Shared endpoints and shared nodes require special procedures to preserve topology.
- When complex edits could affect multiple lines, user feedback and safeguards prevent invalid edits.
- Loops and data integrity issues: a number of loops in the dataset may have corrupted event data; predefined procedures exist to mark as deleted and recreate as needed (see Appendix 6).

## Pond mapping and sampling
- Ponds mapped comprehensively within each square; one pond per square selected as the survey pond for detailed condition assessment.
- Pond size defined from 25 m2 to 2 ha; maximum winter water level used for size; boundaries clarified to distinguish ponds from ditches or other water bodies.
- Ponds may be pre-existing (CS2000) or newly recorded; documentation of pond creation or loss, with reasons (e.g., drainage, infilling, construction) recorded.
- Detailed forms (Pond Mapping Recording Sheet) used to capture pond attributes and changes; guidance provided for pre-selection and re-selection of survey ponds.

## Boundary and attribute consistency; field notes
- Emphasis on consistent use of Vegetation Key for habitat allocation; supports UK Biodiversity Action Plan monitoring.
- Non-native species guidance included; urban habitats and orchards treated with domain-specific BH/PH codes.
- Clear guidance on boundary delineation and attribute coding to ensure auditable, repeatable outputs for longitudinal analyses.

## Data governance, metadata, and outputs
- Data quality: explicit procedures for assessing spatial vs. attribute accuracy; robust metadata; appropriate public sharing of underlying data where applicable.
- Outputs are designed to be auditable and suitable for longitudinal analyses of habitat extent and change to inform policy decisions.
- Practical considerations and endnotes provide references to supporting materials, field manuals, and related CS2000/CS1990 methodologies.

## Endnotes and practical considerations
- The handbook includes extensive field and GIS editing guidance to ensure consistent, auditable monitoring outputs.
- It supports longitudinal habitat change analyses, enabling policy-relevant monitoring and decision-making.
- Appendices cover loops, veteran trees, and other field-aided decision-making aids.