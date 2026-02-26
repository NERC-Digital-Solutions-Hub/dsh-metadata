# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Provides a detailed methodology and digital workflow for mapping Broad Habitats (BH) and Priority Habitats (PH) using CS Surveyor within ArcMap.
- Emphasises a unified digital data model, metadata consistency, change tracking, and integration with broader datasets across habitats and themes.
- Covers field procedures, data capture rules, and intensive editing protocols for polygon (areas), line features, and point features across 1 km squares.

## Data Model and Digital Mapping System

- Central platform: CS Surveyor, a dedicated ArcMap extension for data capture, editing, and attribute management.
- Data types: Areas (polygons), Lines (linear features), Points (discrete features); all edited with an emphasis on habitat extent and change.
- Change management: Each edit requires a reason (REAL change, ERROR change, NEW BASELINE) and assessment of applicability of previous allocations; spatial accuracy is secondary to accurate habitat extent and change reflection.
- Time-series and integration: Designed to maintain longitudinal data across 1990, 1998, and 2007 mappings with potential PH allocations for updated PH mapping.

## Woodland and Landscape Features (WLF) and Attributes

- WLF attributes (example subset):
  - Unnatural shape indicators and line of stumps: base height, canopy height categories, species composition (e.g., >50% hawthorn), evidence of management (e.g., flail, laying, coppicing).
  - Line of stumps: Yes/No; vertical gappiness (% of canopy-to-ground breaks); margin widths (left/right); presence of stake trees and tree protectors.
  - Height and margin classification: base canopy height categories (<1m to >3m) and margin presence at various widths.
  - Notes on natural vs unnatural shapes and specimen composition to guide BH/PH allocations.
- Visual examples: Image set accompanying WLF section to aid field coding (unnatural vs natural shapes, base height, stumps, gappiness, margins, and management signs).
- Practical caveat: If base height is >2m, ensure woody components are trimmed or recorded as natural if appropriate.

## Field Mapping and Editing Workflows

- Create New Line: Must be created within the survey square, scale 1:5000 or smaller, minimum length 5.0 m, cannot cross itself; initial event is Unsurveyed/Missing Data.
- Modify Line: Vertex-level editing, including adding/deleting/moving vertices; end-point shared nodes edited via Separate Shared Node Modify; preserve topology and avoid creating self-intersections.
- Shared Nodes: Modify carefully to move intersection points so adjoining lines adjust consistently; prevents invalid intersections.
- Cut Line: Use a cut polygon to remove sections; pink/white guides show cut length vs remaining length; multiple cuts possible with validation.
- Reshape Line: Two variants (Reshape Line 1 and 2) to adjust lines by drawing a reshaping guide that intersects the line; final cut constrained by minimum feature length.
- Copy Tool: Import existing landscape-area features (e.g., from OS Mastermap) into an edit sketch to ensure accurate cuts; supports combining multiple features into a single edit sketch.
- Delete Line: Requires a valid Reason for Change on all events; scales and one-line-at-a-time constraint apply; cannot delete if events are missing a reason.
- Line Status and Loops: Check unvisited lines via attribute query; loops in data require a remediation workflow to delete and re-create lines to correct corrupted event data.
- Data integrity: Emphasis on coherent change logging, with supported workflows documented in the editing toolbox.

## Pond Mapping and Surveys

- Annexed process for CS2007 pond mapping:
  - Complete per square with pond polygon IDs, areas, and water presence; identify ponds no longer present and document reasons.
  - Randomly select a survey pond per square for in-depth condition surveying; maintain formal documentation workflow for pond creation and loss.
  - Use pond mapping sheets to log geometry, water presence, and reasons for loss/creation; pass forms to freshwater surveyors when needed.
- Pond governance: Pre-selected pond validation and iterative selection processes to ensure representative field sampling.

## Infrastructure for Data Governance and Support

- Updates and support: Field mapping updates and bug reporting routed through a helpdesk and a dedicated wiki; periodic methodology updates issued as Latest News.
- Documentation and training: Appendix materials (e.g., old Field Assessment Booklets, CS2000 references) provided to support interpretation and continuity with legacy data.
- Legacy integration: References CS1990/CS2000 structures to facilitate cross-era data integration and attribution coding schemes.

## Practical Considerations for Data Leaders

- System-wide coherence: A unified, auditable digital data model across habitat types with consistent metadata, attribute coding, and robust change tracking.
- Data discovery and reuse: Keys and attributes designed for cross-use across BH/PH allocations and compatibility with partner datasets and broader ecological indicators.
- User-centered product development: Iterative refinement of data products with ongoing user verification (policy colleagues) and feedback-driven updates to attribute definitions.
- Data gaps and access constraints: Acknowledges paywalls, data protection barriers, and sector coordination challenges; promotes collaboration, community of practice, and shared standards to enhance data quality and accessibility.
- Governance and access: Tight coupling of data capture with explicit procedural controls (MMU rules, change justifications, BH/PH allocations) and dissemination of updates through official channels.

## Endnotes and Supplementary Material (Highlights)

- Annexes and appendices supplement the core workflow:
  - Annex 3: CS2007 Pond Mapping Recording Sheet (per square, multi-sheet if needed).
  - Appendix 5: Girth-based guidance for veteran trees, with rules-of-thumb for categorizing tree ages and significance.
  - Appendix 6: Squares with loops (listing unique squares and associated metadata; data integrity notes for loop-related events).
- Historical context: References to CS1990 thematic mapping and the evolution toward BH/PH classifications in CS2007, including how attributes and codes evolved over time to support integrated analyses.