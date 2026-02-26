# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Defines field mapping procedures for CS2007, with emphasis on digital mapping of woodland landscape features (WLF), line editing, pond mapping, and data capture governance.
- Provides coding schemes, attribute tables, and interactive editing workflows to document habitat attributes, management, and spatial changes.
- Aims for consistent, repeatable data collection, traceability, and integration with other data themes (vegetation, boundaries, structures, physiography).

## Woodland Landscape Features (WLF) - Key Attributes
- Height categories: <1m, 1-2m, 2-3m, >3m (with guidance to adjust category as needed), 3-4m, 4-6m, >6m.
- Base height: height of canopy base; categories include <2m or >2m.
- Species composition: e.g., mixed species, >50% hawthorn, >50% other.
- Evidence of management: none, newly planted, cutting (<3 years), laying or coppicing (<5 years), or both.
- Line of stumps: Yes/No.
- Vertical gappiness: percentage of canopy-ground gaps; categories <10%, 10-<25%, 25-<50%, 50-<75%.
- Margins: Left and Right margin widths or “not present.”
- Staked trees: Yes/No (for individual trees within features).
- Tree protectors: Yes/No.
- Notes: guidance to record natural shape for WLFs when applicable; images illustrate various configurations and coding cases.

## Visual References and Coding Conventions
- A set of example images illustrate feature types and coding (e.g., WLF unnatural shape vs natural shape, base height, canopy composition, management signs, and margins).
- Each example is mapped to a code that corresponds to its described attributes (e.g., WLF unnatural shape with line of stumps, base height, horizontal gappiness, hawthorn dominance, evidence of management).

## Line Features - Creation, Editing, and Management
- Create New Line: must be created within a survey square, at scales 1:5000 or finer, minimum length 5.0 m, cannot cross itself, added as an Unsurveyed/Missing Data event.
- Modify Line: edit shape via vertices; end-point shared nodes can only be edited via Shared Node Modify; ensure edits do not create invalid intersections.
- Shared Nodes: move junctions where lines meet; adjoining lines move with the node; careful to avoid intersections post-edit.
- Cut Line: cut along a polygon using a cut sketch; visualize length cut vs length remaining; edits must meet minimum feature length.
- Copy Tool: copy features from other layers to form a cut edit sketch; supports adding/removing features in the edit sketch.
- Delete Line: requires a valid Reason for Change for all events; scale constraint applies; single-line deletion per operation.
- Reshape Line: reshape by drawing a reshape graphic; must intersect the original line; minimum length constraints apply.
- Reshape Following Copied Line: follow a copied boundary to reshape; requires intersection and careful handling of copied features.
- Validity Rules: edits must keep lines within the survey square, maintain minimum lengths, and avoid creating new invalid intersections.
- Visit Status for Linear Features: use Select By Attributes to highlight unvisited lines; unvisited lines appear in blue.
- Loops Issue: a set of loop features with corrupted event data; procedure to mark as Deleted Feature, complete with Change Reason and Visit Status, delete lines, then reinstate by re-adding lines and events.

## Data Quality, Provenance, and Workflow
- Emphasises a robust digital workflow for data quality, traceability, and interoperability.
- Requires explicit change logging and justification for edits; maintains data lineage (source datasets, edits, rationale).
- Integrates multiple data sources (vegetation, physiography, boundaries, structures) into a unified dataset.
- Anticipates field-level bugs and provides channels (helpdesk, Wiki) for issue resolution.
- Metadata and discoverability are prioritized to support reuse and interoperability.

## Pond Mapping Methodology
- All ponds within each CS square must be identified; use the CS2007 Pond Mapping Recording Sheet.
- A designated survey pond is selected for detailed freshwater condition assessment; selection can be pre-determined or random using Appendix-based random numbers.
- Pond definitions and boundaries are established by winter water level, vegetation shifts, water marks, or break of slope.
- Attributes to record for all ponds; detailed condition data for the survey pond is captured and linked to freshwater assessments.
- Protocol ensures pond identification and recording even when ponds fall below the MMU.

## Appendix Highlights (Referenced Elements)
- CS2007 Pond Mapping Recording Sheet: structured form for per-square pond data, including pond polygon IDs, areas, water presence, and notes on losses/creations.
- Appendix 3–5: supporting materials (field sheets, veteran-tree girth guidelines, and loops/square data for quality control).
- Appendix 6: Squares with loops (example records of looped features and associated metadata).

## Data and Reporting Implications for Analysts
- The handbook provides a detailed, repeatable approach for capturing habitat extents, line-based changes, and pond inventories at 1 km square scales.
- Documentation and metadata practices support dataset discoverability and reuse across projects and policy-relevant outputs.
- The digital workflow supports integration with other CS themes and facilitates consistent national reports on biodiversity and habitat mapping.

## End Notes
- The Field Mapping Handbook is part of a broader Countryside Survey effort to map habitat composition and change across the UK, with strong emphasis on data quality, digital capture, change tracking, and policy-relevant reporting.