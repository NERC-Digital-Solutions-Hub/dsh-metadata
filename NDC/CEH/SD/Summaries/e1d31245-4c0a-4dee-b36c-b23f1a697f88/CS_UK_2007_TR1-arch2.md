# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Standardizes field mapping for CS2007, focusing on habitat and landscape feature mapping across 1 km squares.
  - Extends mapping to include pond data and upland/wales attributes, enabling time-series monitoring for policy performance.
  - Uses CS Surveyor on ArcMap for digital data collection and supports reporting on Broad Habitats (BHs) and Priority Habitats (PHs).

- Woody Linear Features (WLF) and habitat attributes
  - WLF features are categorized by height, base canopy height, species composition, and evidence of management.
  - Key attributes for WLF include: unnatural vs natural shape, line of stumps, vertical gappiness, canopy height, margin widths, staked trees, tree protectors, and notes on natural shape when applicable.
  - Guidance emphasizes distinguishing artificial shaping from natural forms and recording variations along lines and sections.

- Data collection and field editing workflow
  - Field data are captured with a tablet-based workflow embedded in the CS Surveyor extension of ArcMap.
  - In-field tasks include creating and editing polygons (areas), lines (linear features), and points (individual features) with strict spatial and attribute rules.
  - Lines must meet minimum criteria (e.g., minimum length 5.0 m); lines cannot cross themselves; intersections cause automatic splits.
  - A comprehensive log of changes and a Save Session workflow are mandated for traceability.

- Line editing and topology rules
  - Create New Line: new lines added within the survey square at scales of 1:5000 or finer; each new line starts with an Unsurveyed/Missing Data event.
  - Modify Line: vertex-level editing (insert/delete/move) with restrictions on end-point edits; shared nodes can be edited via Shared Node Modify.
  - Cut Line: define a cut along a line using a polygon; the cut length is shown for user confirmation.
  - Reshape Line: reshape edits via a follow-line or reshape graphic; edits must not create invalid geometries.
  - Copy Tool: reuse existing features to build accurate edit sketches (Cut Edit Sketch) by importing features from other layers.
  - Delete Line: requires valid Reason for Change on all events; allows one-line deletion at a time with scale constraints.
  - Shared Nodes: modify intersections where multiple lines meet; ensure edits do not create unintended intersections.
  - Visit Status: unvisited linear features are highlighted to guide field verification.
  - Loops: data loops identified as corrupted; procedure includes marking as Deleted Feature, completing change logs, deleting, then reinstating the correct line geometry.

- Pond mapping and freshwater component
  - All ponds in a square must be recorded; a survey pond is selected for detailed condition assessment by freshwater surveyors.
  - Ponds may be temporary; outer winter water level defines extent; guidelines address distinguishing ponds from ditches, flushes, and dammed streams.
  - Preselection and random selection processes are documented and logged.

- Change and data quality management
  - Distinguishes genuine habitat change from mis-recording; both polygonal and linear features are assessed for real change.
  - Back-corrections may be needed for unenclosed habitats due to improved keys; enclosed habitats use prior CS1998 data for attribute inference.
  - PH allocation within BHs depends on GIS masks and historical data, with reliability considerations for rare PHs.

- Practical guidance for analysts and data reuse
  - Emphasizes increasing data value through reuse and cross-dataset integration.
  - Outputs are designed for interoperability with other monitoring databases and policy evaluation tools.
  - Clear decision rules for polygon creation, PH within BH allocation, mosaics, and complex habitat mixtures to support robust time-series analyses.

- Appendices and additional guidance
  - Appendix 1: Using old Field Assessment Booklets (FABs); CS1990/CS2000 context and how older data inform current interpretation.
  - Annex 3: CS2007 Pond Mapping Recording Sheet (structure and usage details for pond data collection across squares).
  - Appendix 5: Girth sizes of veteran trees; rules of thumb for classifying veteran timber by species and girth thresholds.
  - Appendix 6: Squares with loops; catalogues unique squares with spatial metadata and route references.

- Training, support, and governance
  - Step-by-step instructions for CS Surveyor usage, including login, navigation, editing sessions, and saving changes.
  - Notes on field issues, bugs, and the role of helpdesk and Wiki for fault logging and updates.
  - Final takeaway: CS2007 provides a comprehensive, standardized GIS-based framework to map habitat extent and change over time, integrating BHs and PHs with detailed woodland/vegetation taxonomy to support rigorous environment health monitoring and policy evaluation.