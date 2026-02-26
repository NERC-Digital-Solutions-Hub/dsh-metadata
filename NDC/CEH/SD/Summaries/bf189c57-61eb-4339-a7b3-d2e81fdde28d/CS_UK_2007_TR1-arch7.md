# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides guidance for field mapping of habitats, landscape features and associated attributes across Countryside Survey 2007.
- Aims to report land cover change by Broad Habitats (BH) and Priority Habitats (PH) at country/UK levels.
- Introduces a digital GIS mapping model integrating previous themes (forestry, agriculture/natural vegetation, boundaries, structures, physiography) and a CS Surveyor ArcGIS-based workflow.

## Key Concepts and Classification
- Broad Habitats (BH) and Priority Habitats (PH)
  - BHs are general habitat groups (BH1–BH19, plus Mosaic); PHs nest within BHs.
  - Some PHs are mapped post-survey using GIS masks; emphasis on consistent BH/PH attribution.
  - Enclosed vs unenclosed habitats: enhanced PH detail and spatial precision; upland BHs redefined for accuracy.
  - Masks applied post-survey to constrain extent estimates (upland/lowland, marine, etc.).
- Vegetation Key
  - Used to assign polygons to BH/PH based on vegetation composition and key indicators.
- Woodland Types/Features Key
  - Classifies woody vegetation into Belt of trees, Clump of trees, Woodland/Forest, etc., with canopy thresholds (e.g., >25% canopy).
- Data integrity and change
  - Surveyors distinguish real ecological change from prior data errors; change captured for primary/secondary attributes.
  - For unenclosed habitats, older datasets (CS1990/CS2000) may be merged to provide finer detail.

## Digital Mapping System and CS Surveyor
- CS Surveyor is an ArcGIS-based extension with pre-set symbology and data structures tuned for CS2007.
- Surveyors log in, load map squares, and edit polygon (areas), line (linear features), and point features.
- Emphasis on consistent data capture, traceable change, and regular saving of edits.
- Integration within a Countryside Survey data frame; standard ArcMap tools augmented by CS-specific editing tools.

## Mapping Rules and Geometry
- Geography and map units
  - Minimum mapping unit (MMU) is 1/25 ha (400 m2); features below MMU are not mapped as areas (lines used for narrow features).
- Areas (polygons)
  - 6.a Polygon-level attributes: area, BH/PH assignment, accuracy codes, visit status.
  - 6.a.ii Determining Change: assess whether 1998 allocation still applies, identify real change, or log errors; consider age of older data (CS1990/CS2000).
  - 6.a.iii Component-level attributes: areas may contain multiple components with individual primary/secondary attributes; components can be added/copied/deleted.
  - 6.b Copy Area: copy attributes from one polygon to multiple targets.
  - 6.c Split Areas: digitize a split line to create two polygons; use edit sketch or copy features for complex splits.
  - 6.c.i Modifying the Edit Sketch: adjust boundaries by editing vertices.
  - 6.c.ii Copy Tool: import existing features (e.g., from OS Mastermap) into the edit sketch to aid splitting.
  - 6.d Merge Areas: merge polygons with identical attributes; require a reason for change for the new polygon.
  - 6.e Modify Area: modify shared boundaries with topology-aware tools; changes propagate to adjacent polygons.
  - 6.f Update Areas Edit: create a new landscape area by splitting/merging existing polygons.
- Ponds
  - Every pond in a square must be mapped on a Pond Mapping sheet; a survey pond is selected for detailed assessment.
  - Boundary of ponds defined by winter water level; distinguishing ponds from other water bodies follows explicit criteria.
  - After mapping, ponds are sampled by freshwater specialists.
- Points and point features
  - Points capture features occupying less than 20x20 m; attributes edited/verified on tablet.
  - Veteran trees: up to 10 per square, with multiple components allowed.
  - Buffer zones around features; trees and shrubs recorded as points unless in building curtilages or near non-agricultural curtilages.
  - Scale constraints: map must be 1:5000 or smaller to edit points; points cannot be placed outside the square or within 5 m of another point.
- Linear features and events
  - Linear features are lines typically less than 5 m wide; longer features may be captured as areas if above MMU.
  - Events along lines (fences, hedges, woody features) have attributes and can be edited, added, deleted, or copied.
  - Attributes include line length, event from/to points, width, and related properties; margins around boundaries are recorded (typically 6 m, variable).
- Non-native species and orchards
  - Guidance on identifying and recording non-native species; traditional orchards may be PH, mapped as Orchard under Agriculture/Crops with curtilage orchards mapped as Garden/grounds with Orchard as an extra attribute.

## Editing and Topology of Linear Features
- Creating, editing, and managing lines
  - Create Line: lines must be added within the square at 1:5000 scale or smaller, minimum length 5.0 m, cannot cross themselves.
  - Modify Line: vertex-level editing to reshape lines; end vertices with shared topology are edited via Shared Node Modify.
  - Shared Nodes: modify shared intersections carefully to preserve topology; avoid creating invalid crossing edits.
  - Cut Line: use a cut polygon to remove a segment; the cut length is shown, and the remaining line length is updated.
  - Copy Tool: import features from other layers to assist in creating edit sketches.
  - Delete Line: lines can be deleted only if all attached events have valid Reason for Change values.
  - Reshape Line: adjust line by drawing a reshape graphic; ensure edits intersect the line properly.
  - Reshape Line Following Copied Line: use a copied landscape area boundary as a guide to reshape.
- Checking and managing line edits
  - Edits must maintain minimum feature lengths; avoid creating intersections with other revised lines.
  - End-of-line end-nodes shared with other lines are edited via shared node modify.

## Visit Status and Quality Assurance
- Visit status tracking for areas and lines is integrated, with methods described for querying unvisited linear features.
- Loops in data: Appendix 6 lists squares with loops; corrupted event data require a specific corrective workflow (mark as Deleted Feature with No Change, then delete lines and re-create consistent lines).

## Pond Mapping Appendices and Practical Notes
- CS2007 Pond Mapping Recording Sheet: one form per square, one row per pond; includes survey pond selection and sampling workflow by freshwater specialists.
- CS2007 mapping requires consistent forms across squares; ponds may be re-mapped or listed as existing/dry with a reason for loss/creation.
- Appendices cover CS2000 and FABs (Field Assessment Booklets) for reference, including codes and guidance for legacy data comparison.

## Veteran Trees and Species
- Appendix 5 provides girth-based rules of thumb for identifying veteran trees, including species-specific thresholds and classifications (potentially interesting, valuable, truly ancient, notable).

## Workflow Summary
- Prepare CS Surveyor GIS model and map square; assign BH/PH using vegetation/woodland keys.
- Map areas (BH/PH), lines, points, and ponds with MMU guidance; record components where applicable.
- Use editing operations (split/merge/copy/update) with explicit reasons for changes; manage visit status.
- Conduct pond mapping with a designated survey pond and subsequent sampling by freshwater specialists.
- Capture point and linear feature attributes, including veteran trees and hedgerows/components.
- Save edits regularly; use helpdesk/resources for field issues; stay aligned with methodology updates via CS Wiki.

## Practical Notes
- The document emphasizes routine checks, field keys, specimen coding, and ongoing methodology updates.
- It provides extensive procedural detail for tablet-based field tasks, line editing, and data integrity management.