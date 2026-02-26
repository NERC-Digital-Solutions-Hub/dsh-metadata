# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides GIS-based workflows for field mapping of woodland landscape features, with a focus on Woodland Linear Features (WLF) and line editing within CS Surveyor.
- Details attribute schemas, coding schemes, and step-by-step editing procedures for creating and modifying lines, including complex topology rules.

## Woodland Line Features (WLF) – Key Attributes
- Unnatural shape indicators
- Height, with categories (e.g., <1m, 1–2m, 2–3m, >3m, etc.)
- Base height (canopy base), with categories
- Species composition (e.g., mixed, >50% hawthorn, etc.)
- Evidence of management (e.g., newly planted, flailed, coppiced, laying)
- Line of stumps (Yes/No)
- Vertical gappiness (percent breaks from canopy to ground)
- Margins (Left and Right) with size categories
- Staked trees (Yes/No)
- Tree protectors (Yes/No)
- Note: If base height >2m, ensure woody species are cut or trimmed to shape; natural shapes should be recorded accordingly.
- Visual guidance: a set of example images indicates coding for different WLF configurations (unnatural vs natural shapes, margins, stumps, height categories, management signs).

## Data Coding and Handling Guide
- Use coded attributes to represent WLF characteristics (height, composition, management, margins, etc.).
- Distinguish WLF with unnatural shapes from natural shapes and apply appropriate attribute values.
- Images accompany the guidance to aid consistent coding across surveyors.

## Line Editing Tasks in CS Surveyor
- Access: Use the Lines tab in the Landscape Feature Editing Toolbox for all line-related edits.
- Create New Line:
  - Must be within the survey map at scale 1:5000 or better.
  - Lines cannot cross themselves and must be at least 5.0 meters long.
  - A new line starts with a single Unsurveyed/Missing Data event along its length.
- Modify Line:
  - Select a line and edit its geometry using vertices (insert, delete, move).
  - End-point nodes that are shared with other lines require the Shared Node Modify workflow.
  - Modifications must not create intersections with other revised lines.
- Shared Nodes:
  - Move intersection points carefully; adjoining lines adjust accordingly.
  - Only editable when selected as a node; ensure topology remains valid.
- Cut Line:
  - Digitize a cut polygon along the line to remove a segment; the length to be cut is highlighted.
  - After cutting, the remaining line length and new geometry are saved.
- Copy Tool:
  - Use features from other map layers (e.g., Landscape Areas) to draft an edit sketch.
  - Build the cut sketch by combining features; cut only where valid.
- Delete Line:
  - Requires a valid Reason for Change on all events attached to the line.
  - Can delete only one line at a time; scale must be 1:5000 or less.
- Reshape Line:
  - Reshape using a reshape line graphic that must intersect the target line at start and end.
  - Two modes: standard reshape and reshape following a copied line boundary.
- Checking Visit Status:
  - Use Select By Attributes to reveal unvisited Landscape Events; unvisited lines appear highlighted.
- Loops and Data Integrity:
  - Loops (loops in data) may be corrupted; procedure includes marking as Deleted Feature with No Change and Completed Visit Status, deleting lines, then reinserting the feature as observed in the field.

## Practical Rules and Quality Assurance
- Minimum mappable unit and accuracy guidance apply to WLF edits and line edits.
- Change assessment differentiates genuine ecological change from recording errors; unenclosed habitats may rely on older data.
- Ensure attributes are consistent when editing components of lines, not just the line as a whole.

## Appendices and Related Context
- Appendix references veteran-tree girth sizing (Appendix 5) and details on looped line data (Appendix 6), illustrating additional governance for wood-related features and data integrity.
- Contextual notes on older CS2000 and FAB resources provide historical mapping and coding references used to support current workflows.

## Practical Outputs for GIS Practitioners
- Structured WLF attribute data capturing height, composition, management, margins, stumps, and protective measures.
- Editable linear feature geometry with strict topology and change-tracking rules, enabling robust time-series analyses.
- Clear protocols for curating line edits, managing complex edits (cuts, reshapes, shared nodes), and addressing data anomalies (loops).
- Documentation of procedures to ensure reproducibility and comparability across survey squares.