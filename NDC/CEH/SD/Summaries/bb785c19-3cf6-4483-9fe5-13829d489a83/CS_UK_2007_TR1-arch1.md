# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview

- Purpose: Guidelines for Countryside Survey 2007 (CS2007) field mapping of Broad Habitats (BH) and Priority Habitats (PH) across 1 km squares, using a unified digital mapping model and CS Surveyor (ArcGIS extension) to support UK-wide reporting.
- Scope: Methods for data capture, habitat classification, pond mapping, and woody features; workflows for editing Areas, Lines, and Points; data provenance and change management to enable robust analysis, correlations, and predictive modelling.

## Data Model and Coverage Highlights

- Spatial units: 1 km squares edited in CS Surveyor; data objects include Areas (polygons), Lines (linear features), and Points (point features).
- Mapping rules: Minimum mapping unit (MMU) of 0.04 ha; polygons generally not created below MMU; single polygons preferred unless primary attribute changes.
- Habitat classification: BH and PH used to report land cover change and biodiversity; components may carry BH/PH attributes.
- Change recording: For each polygon, capture change status (Real Change, Error Change, New Baseline) and assess accuracy.
- Ponds: Comprehensive pond mapping with a designated survey pond per square for detailed condition surveys.
- Data lineage: Reconciliation of CS1990, CS1998, CS2000 data into CS2007 with refined attributes and metadata for discoverability.

## Woody Linear Features (WLF) Data Fields (Unnatural vs Natural Shapes)

- Height categories for WLF base height: 
  - Height: <1m, 1-2m, 2-3m, >3m, 3-4m, 4-6m, >6m.
  - Base height: <2m or >2m.
- Species composition: 
  - Mixed species; >50% hawthorn; >50% other.
- Evidence of management: 
  - No recent management; newly planted; cutting (<3 yrs); laying or coppicing (<5 yrs); both preceding.
- Structural details: 
  - Line of stumps: Yes/No.
  - Vertical gappiness: <10%, 10-<25%, 25-<50%, 50-<75%.
- Margins: 
  - Margin Left: not present, <2m, 2m-<4m, 4m-<6m, 6m-<12m.
  - Margin Right: not present, <2m, 2m-<4m, 4m-<6m, 6m-<12m, 12m-20m.
- Support features: 
  - Staked trees: Yes/No.
  - Tree protectors: Yes/No (e.g., 1 m high tubes).
- Important notes: If >2m height, ensure component woody species are cut or trimmed to avoid unnatural shapes; natural-shape records should be noted accordingly.
- Illustration: Sets of example images demonstrate WLF classifications and coding (unnatural shape/line of stumps, natural shape, hedged vs natural progressions).

## Field Editing Workflows for Linear Features

- New Line:
  - Create at map scale 1:5000 or better, within the survey square, minimum length 5 m, cannot cross itself, lines do not cross square boundaries.
  - New lines start with an Unsurveyed/Missing Data event.
- Modify Line:
  - Select and edit vertices; insert/delete/move vertices; end-node edits require Shared Node Modify if endpoints are shared with other lines.
  - Changes reflected in linked topology; minimum feature length constraints apply.
- Shared Nodes:
  - Modify by selecting a node (pink highlight) to move; adjoining lines follow; careful to avoid invalid intersections.
- Cut Line:
  - Digitize a cut polygon along the line to remove a segment; pink/pale line shows cut length; confirm to apply.
- Edit Sketch (reshape/copy):
  - Adjust the cut shape by editing vertices; reshape line using a dedicated tool; ensure edits produce valid geometry.
- Copy Tool:
  - Use existing landscape area features (e.g., OS Mastermap) to draft or refine cut-line sketches; supports multi-feature edits.
- Delete Line:
  - Requires all events to have valid Reasons for Change; scale must be <= 1:5000; one line per delete action.
- Reshape Line:
  - Reshape following digitized line or copied line per defined methods; edits must yield valid, non-crossing results.
- Visit Status and Loops:
  - Check unvisited lines via a Select By Attributes workflow; loops identified in Appendix 6 require cleaning: mark as Deleted Feature with appropriate Reasons for Change, complete visits, delete lines, then re-create as needed.

## Practical Considerations for Analysts

- Data quality vs geographic precision:
  - Emphasis on accurate representation of habitat extent and change rather than perfect geographic precision; provenance and update history are essential.
- Data harmonisation:
  - Integrates multiple vintages (CS1990, CS1998, CS2000) into a cohesive 2007 dataset; standardises attributes and BH/PH coding.
- Non-native species and orchard notes:
  - Includes inventories for notable non-native species and orchard-related attributes to reflect PHs and BH attributes accurately.
- Documentation and reproducibility:
  - Extensive documentation of workflows, change logs, and metadata; datasets intended to be discoverable and reusable via portals.
- Appendices and references:
  - Appendices cover old Field Assessment Booklets (FABs), CS2000 to CS2007 mappings, pond mapping sheets, and veteran tree girth guidelines (Appendix 5) to aid interpretation and data validation.

## Appendices and Reference Highlights

- Appendix 1: Using old Field Assessment Booklets (FABs) and 2000-era references.
- Appendix 2: CS2000 coding sheets and example data mappings.
- Appendix 3/4: CS2007 plot maps, plot sheets, and data sheets; FAB folders and mapping documentation.
- Appendix 5: Girth sizes and classification rules for veteran trees (country-specific guidelines and thresholds).
- Appendix 6: Squares with loops; enumeration of squares affected by loop issues and remediation workflow.

## Endnotes and Publication Details

- Copyright: NERC; distribution permitted for research, private study, and internal use with proper attribution.
- Disclaimer: Decisions/actions based on the report are at user risk; NERC not liable for damages arising from use.
- Contact: Countryside Survey project office at CEH Lancaster; funding and collaboration details with Defra and other partners.