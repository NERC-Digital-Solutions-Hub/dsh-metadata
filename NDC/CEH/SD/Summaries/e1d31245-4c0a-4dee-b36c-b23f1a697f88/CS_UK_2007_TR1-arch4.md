# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose within Countryside Survey 2007 (CS2007): guide field mapping, change reporting, and data capture for landscape features using a standardized digital workflow.
- Data capture framework: features recorded as Areas (polygons), Lines (linear features), and Points (points) via the CS Surveyor ArcMap extension.
- Core priorities: maintain change/fidelity records, support metadata and updates, and enable co-ownership and user-focused data products.
- Legacy context: references CS1990/CS2000 schemes, with a move toward more detailed habitat (BH/PH) mapping and time-series capability.

## Woody Line Features (WLF) - attributes and coding
- Key attribute fields for WLF:
  - Unnatural shape / line of stumps
  - Height categories (e.g., <1m, 1-2m, 2-3m, >3m, etc.)
  - Base height (canopy base) categories
  - Species composition (e.g., mixed; >50% hawthorn; >50% other)
  - Evidence of recent management (none; newly planted; cutting; laying/coppicing)
  - Line of stumps (Yes/No)
  - Vertical gappiness (percentage bands)
  - Margin widths (Left and Right margins)
  - Staked trees (Yes/No)
  - Tree protectors (Yes/No)
- Guidance on shape: if features exceed 2m in height, check and record whether woody species are pruned to retain natural shapes; otherwise record as WLF in natural shape.
- Visual guidance: a set of example images illustrate natural vs unnatural shapes and associated attributes; coding follows a left-to-right, top-to-bottom sequence (examples 1–8).

## Line editing workflow - general rules and constraints
- Editing requires a map scale of 1:5000 or less for line creation and modification.
- Lines must be created within the survey square and cannot cross themselves; minimum length is 5.0 meters.
- When editing, lines are edited via a Lines tab in the Landscape Feature Editing Toolbox; changes are saved to commit spatial edits.
- Endpoints that are shared with other lines (shared nodes) are treated specially and can only be modified via Shared Node Modify to preserve topology.

## Core line editing operations
- Create New Line:
  - Draw on map, finish with double-click; all new lines begin with a single Unsurveyed/Missing Data event.
  - Ensure scale, square confinement, and minimum length requirements are met.
- Modify Line:
  - Edit geometry by moving vertices, inserting/deleting vertices, and adjusting endpoints.
  - Endpoints on shared boundaries require Shared Node Modify.
  - Validation prevents edits that create invalid intersections or too-short segments.
- Shared Nodes:
  - Modify intersections where multiple lines meet; moves propagate to connected lines while preserving topology.
- Cut Line:
  - Digitize a cut polygon along the line to remove a segment; pink/white dashed line shows cut portion, red shows remaining portion.
  - Multiple cut edits can be applied to a single line; line lengths must remain above minimum thresholds.
- Modifying the Edit Sketch:
  - Adjust the cut polygon by moving its vertices before finalizing the cut.
- Copy Tool:
  - Copy features from external layers (e.g., OS MasterMap) into the edit sketch to support accurate cuts.
  - Use Copy+ to add features and Copy- to remove features within the sketch.
- Delete Line:
  - Requires a valid Reason for Change on all attached events before deletion; cannot delete lines with invalid change records.
- Reshape Line 1:
  - Draw a reshape line along the existing line to define a new shape; edits are constrained to maintain topology and minimum feature length.
- Reshape Line 2 (Copy-followed reshape):
  - Follow a copied line to reshape; redraw in the context of the copied boundary, ensuring integration with the landscape boundary and other features.

## Quality control, change management, and governance within line edits
- Every change requires a defined Reason for Change; REAL (genuine change) vs. ERROR (mis-recording) concepts are applied in the lineage of edits.
- Validation rules prevent edits that would create invalid geometries or sub-minimum-length features.
- Edits must maintain the integrity of shared boundaries and avoid creating intersections with other revised lines.
- Sessions must be saved to persist edits; unsaved work is lost on exit.

## Managing visit status and data integrity for linear features
- Unvisited lines can be identified via a Select By Attributes workflow in the Landscape Events layer; unvisited lines appear highlighted.
- Data integrity note: there are known loops in the data (Appendix 6 lists many squares with loops) where event data is corrupted.
- Handling loops procedure:
  - Change the theme of involved events to Deleted Feature, set Reason for Change to No Change, and mark Visit Status as Completed.
  - Delete the problematic lines and re-create the line to reflect field reality, then re-enter attributes and events according to standard protocols.
  - After cleanup, reinstate the feature as observed in the field.

## Appendices and reference materials (context for data practitioners)
- Appendix 1: Electronic Field Assessment Booklets (FABs) and CS2007 FAB references; FABs provide habitat-specific guidance and interpretation aids for field issues.
- CS2000 references:
  - Features mapped across six themes (Agriculture/Natural vegetation, Physiography, Boundaries, ForestrY, Structures, etc.), with theme-specific codes and data sheets.
  - The CS2000 data structure fed into CS2007 workflows; mapping in CS2000 used parcel IDs and coded attributes.
- Appendix 5: Girth sizes of veteran trees - rules of thumb to assess notable or ancient specimens based on species-specific girth thresholds.
- Appendix 6: Squares with loops - catalog of squares containing loops that require special handling due to data structure or corruption.
- The document emphasizes cross-reference to a broader data governance framework, with ongoing methodology updates via the CS Surveyor platform.

## Practical takeaways for data leadership and management
- Establish rigorous line-level data governance around linear features:
  - Ensure clear Reason for Change, robust change history, and time-stamped, auditable edits.
- Enforce spatial and topological integrity:
  - Use shared-node editing for boundary consistency; avoid cross-intersections from ad-hoc edits.
- Implement standardized line editing workflows:
  - Follow Create/Modify/Cut/Copy/Delete/Reshape procedures with validation at each step.
- Address data quality issues proactively:
  - Monitor for loops and corrupted event data; apply prescribed cleanup workflows and re-build lines as needed.
- Leverage appendices and legacy references:
  - Use FABs, CS2000/1990/2000 mappings, and veteran-tree girth guidelines to enhance data interpretation, lineage, and time-series analyses.
- Facilitate training and support:
  - Rely on in-tool help, and ensure field staff can access the latest guidance (Latest News in CS Surveyor, Helpdesk) to minimize tool-related issues.