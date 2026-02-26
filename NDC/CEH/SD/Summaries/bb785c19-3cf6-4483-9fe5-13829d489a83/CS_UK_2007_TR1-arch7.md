# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and audience
- Provides a GIS-driven field mapping framework for habitat types, Broad Habitats (BH) and Priority Habitats (PH), and vegetation attributes.
- Aims to support UK biodiversity monitoring, policy reporting, and time-series analyses.
- Targets map-based data products and end-user understanding (policy colleagues, clients, public).

## System, workflow and audience
- Field data captured with CS Surveyor, a GIS extension for ArcMap.
- End-user collaboration and iterative quality assurance are emphasized.
- Focus on producing map-based data understandable to non-specialists.

## Data model and habitat classification
- BH (Broad Habitats) describe broad vegetation/land-cover types; PH (Priority Habitats) nest within BHs and require additional attributes; PH extent estimated with region-specific masks.
- BHs defined by a structured set (e.g., BH1–BH23) and linked to woodland types/features; PHs integrated where relevant.
- Key attributes depths include habitat, physiography, forestry, agriculture/natural vegetation, and structures.
- Components may exist within polygons; mosaics and percentage shares are required for mixed habitats.
- Minimum data requirements per habitat type include multiple species indicators and habitat indicators.

## Mapping structure and rules
- Feature types: Areas (polygons), Lines (boundaries, hedges, features), Points (trees, ponds, etc.).
- Minimum mapping unit (MMU): 1/25 ha; sub-400 m2 areas not mapped unless part of a polygon with a habitat change.
- Mosaic polygons must document composition with 100% shares.
- Time-series and change focus: differentiate genuine ecological change (REAL) from corrections (ERROR); PH masking and post-survey GIS masks aid reporting.
- All land must be assigned to BH/PH; even minimal vegetation is classified.

## Pond and hydrology mapping
- Ponds are mapped in every square; pond mapping forms record basic attributes and boundary details.
- A survey pond is selected for detailed condition assessment; selection can be preselected or field-dependent.
- Ponds are integrated with Inland Water attributes; boundaries consider seasonal water extent, water marks, and connected features.
- Aquatic macrophytes and vegetation are captured within pond habitats with defined cover categories.

## Using CS Surveyor: editing workflow
- Editing sessions use the Landscape Feature Editing toolbox with three tabs: Areas, Lines, Points.
- Areas (polygons): edit polygon area, BH/PH assignment, accuracy status, and reasons for change (REAL, ERROR, NEW BASELINE PH).
- Components: add, copy, delete; polygons may be split/merged; geography rules permit new polygons only on habitat changes.
- Points: individual features (trees, scrub, ponds) edited one at a time; scale must be 1:5000 or finer; multiple components per point possible; optional buffers.
- Lines: linear features typically <5 m wide but longer than 20 m; lines edited as events with attributes; lines cannot cross themselves; end-nodes may be shared and edited via Shared Nodes.

## WLF Unnatural shape (woody linear features)
- Focused section detailing woody Linear Features (WLFs) with rich attribute fields:
  - Height categories: e.g., <1m, 1-2m, 2-3m, >3m, and higher finer categories.
  - Base height: canopy base height categories.
  - Species composition: e.g., mixed species, >50% hawthorn, etc.
  - Evidence of management: e.g., no recent management, newly planted, cutting, laying, coppicing.
  - Line of stumps: yes/no.
  - Vertical gappiness: percent breaks from canopy to ground (e.g., <10%, 10-<25%, etc.).
  - Margin widths (Left/Right): various width categories including “not present” and specific meter ranges.
  - Staked trees: yes/no.
  - Tree protectors: yes/no.
- If features exceed certain thresholds (e.g., >2m height), record whether woody species are trimmed to appear natural; otherwise record as natural shape.
- A sequence of example images guides coding of multiple sections of WLFs with consistent attribute combinations.

## Editing lines: Create, modify, copy, and reshape
- Create New Line:
  - Map scale must be 1:5000 or less; lines must be at least 5.0 m long; lines cannot cross themselves.
  - New line starts with an Unsurveyed/Missing Data event covering the full length.
  - Lines cannot extend outside the survey square; only one line added at a time.
- Modify Line:
  - Use vertex editing to add, delete, or move vertices; end points of shared boundaries are edited via Shared Nodes.
  - Save changes to apply spatial edits.
- Shared Nodes: 
  - Modify by selecting the node; moving a node moves adjoining lines; careful handling to avoid intersections with other lines.
- Cut Line:
  - Digitize a cut polygon along the line to remove a segment; show pink/white length to be cut and red length remaining.
  - Cut edits cannot create lines shorter than the minimum length.
- Copy Tool:
  - Use features from other layers (e.g., OS Mastermap) to form accurate cut-line edits; multiple features can be added to the edit sketch.
  - After composing the cut sketch, apply Cut and return to the Lines toolbox.
- Delete Line:
  - Deleting requires a valid Reason for Change on all events; scale must be 1:5000 or less; one line at a time.
- Reshape Line:
  - Reshape following an existing line or a copied feature; create a reshape graphic that intersects the line at start/end and refine with vertex edits.
- Reshape Line (follow copied line):
  - Use a shape to follow a boundary or copied feature; the original line is moved to follow the boundary; ensure intersections are correct.
- Checks and constraints:
  - Edits must not create invalid intersections; minimum lengths must be respected.
  - Shared nodes are edited with care to maintain topology.

## Checking visit status and handling loops
- Use Select By Attributes to identify unvisited linear features (VISIT_STATUS = 0).
- Loops in the data (loops in Appendix 6) have corrupted event data; procedure includes deleting and reinserting the line, then reinstating the feature in-field.

## Pond mapping and survey procedures (Appendix references)
- Appendix 3 outlines the CS2007 Pond Mapping Recording Sheet and a detailed process for selecting a survey pond.
- Pond data includes area, boundary notes, presence/absence of water, and reasons for changes since earlier datasets.
- Pond data connects to Inland Water attributes and supports standardized pond-based sampling.

## Appendices and practical aids
- Field Assessment Booklets (FABs) and CS2000-era codes provide historical context and crosswalks.
- The document includes extensive code sheets, plotting maps, and example data for consistency and coding in the field.
- Veteran-tree guidelines and related appendices (e.g., Appendix 5 on girth rules) support field-verified characteristics.

## Governance, quality assurance and support
- CS Surveyor includes helpdesk support, fault logging, and methodology updates via Latest News.
- Explicit procedures exist for stopping edits, saving, and logging off to preserve data integrity.

## Practical guidelines and data constraints for GIS specialists
- Data standards must be consistent; gaps resolved via cleansing and integration across sources.
- All land must be classified as BH or PH; even minimal vegetation warrants assignment.
- Emphasize extent and change rather than ultra-precise spatial accuracy; changes should align with field observations.
- MMU 1/25 ha; specific length/width thresholds for lines; PH masking and post-survey masks apply to PH extents.
- Ponds require standardized definitions and boundaries; all ponds mapped, even if dry during surveys.
- Edits are scale-constrained and require validated Reason for Change values.

## Outcome for GIS specialists
- A comprehensive GIS-based field mapping framework enabling broad habitat extents, detailed woodland/woody feature mapping, robust change detection across surveys, and standardized reporting for policy and conservation programs.