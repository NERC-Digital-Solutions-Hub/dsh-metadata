# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Field mapping guidance for Countryside Survey 2007 (CS2007): habitat, landscape, and water feature mapping.
- Emphasizes spatial extent and change over pinpoint precision; data collected via CS Surveyor (ArcMap extension) and tablet-based fieldwork.
- Builds on prior CS surveys (CS1990, CS1998, CS2000) to support time-series analysis and policy-relevant biodiversity monitoring.

## Woody Linear Features (WLF) – Attributes and Coding
- Unnatural shape: coded features describe non-natural forms of woody lines.
- Height categories (base canopy height): <1m, 1-2m, 2-3m, >3m, with finer breakdowns (e.g., 3-4m, 4-6m, >6m) and a base height flag (<2m or >2m).
- Species composition: mixed species; >50% hawthorn; >50% other species; applies to individual lines and sections.
- Evidence of management: none recent; newly planted; cutting (e.g., flail or saw) within 3 years; laying or coppicing within 5 years; or both.
- Line of stumps: whether the WLF is a line of stumps (Yes/No).
- Vertical gappiness: percentage of breaks from canopy to ground with categories (e.g., <10%, 10-<25%, 25-<50%, 50-<75%).
- Margins: left and right margin widths with categorical options (e.g., not present, <2m, 2m-<4m, etc.).
- Staked trees: Yes/No for individual trees within the feature.
- Tree protectors: Yes/No (e.g., lightweight plastic tubes about 1m high).
- Special note: if >2m height, components should be trimmed to reflect natural shape; if natural shape, record accordingly.
- Visual exemplars: a set of annotated images illustrate various WLF shapes and their coding.

## Data Capture and Editing Workflow (CS Surveyor)
- Create, edit, and manage lines and other landscape features; editing requires a map scale of 1:5000 or better.
- Mandatory change logging: every edit must be categorized as REAL, ERROR, or NEW BASELINE, and recorded against BH/PH attributes.
- Line creation constraints:
  - Lines must be at least 5.0 m long.
  - Lines cannot cross themselves; intersections split lines automatically.
  - New lines start with an Unsurveyed/Missing Data event for the full length.
  - Editing preserves topology; shared boundaries and nodes require special handling.
- Line modification:
  - Modify vertices (insert/delete/move) via a vertex tool; end-vertex edits on shared boundaries are restricted to Shared Node Modify.
  - Ensure edits do not produce invalid intersections or sub-theshold events.
- Shared nodes:
  - Modify by selecting the node itself; moving a shared node propagates changes to adjacent lines.
  - Must ensure edits do not create invalid topology or new unintended intersections.
- Cutting lines:
  - Use a cut polygon to remove a segment of a line; the cut length is shown, and the remaining length is indicated.
  - Edits must maintain minimum feature length post-cut.
- Copy tool:
  - Copy features from other layers (e.g., OS MasterMap) to form edit sketches; supports building accurate cuts by following copied features.
- Deleting and reshaping:
  - Deleting lines requires a valid Reason for Change; single-line edits are performed item-by-item.
  - Reshape lines by drawing a reshape sketch that intersects the line at its start and end; changes apply to the targeted segment.
- Validation:
  - Edits are guided by provenance rules, ensuring consistency with previous allocations (1998/1990) and baseline changes.

## Change Management, Provenance and Time-Series
- Emphasis on comparing CS2007 data with CS1990/CS1998/CS2000 to distinguish:
  - REAL change: genuine habitat/feature change since earlier datasets.
  - ERROR: correction of past misallocations.
  - NEW BASELINE: subdivisions within an existing BH/PH.
- Unenclosed upland habitats may require back-corrections due to improved data; earlier datasets inform attributes where later data were lacking.
- Time-series outputs include reporting by Broad Habitats and Priority Habitats with detailed baselines for research and policy use.

## Pond Mapping Documentation
- CS2007 Pond Mapping Recording Sheet governs pond documentation within each square.
- Each pond has a polygon ID, area, water presence, and notes on loss/creation; a dedicated “survey pond” is selected for detailed condition assessment to support long-term time series.
- Distinguishes ponds from ditches, flushes, bogs, and rivers; seasonal water level changes may affect boundaries.
- Appendices provide random-numbers-based guidance for pond selection and forms for pond mapping and loss/creation reasoning.

## Standards, Documentation and Support
- Documentation and keys accompany field procedures:
  - Vegetation Key (BH/PH) and Woodland Key for attribute allocations.
  - Non-native species lists and appendices to support field coding.
- Appendices include field forms, codesheets, and example data sheets to support consistent data capture.
- Support mechanisms:
  - CS Surveyor updates and bug reports via helpdesk, wiki fault-logging, and project support.

## Practical Considerations for Data Stewards
- Governance of multi-theme datasets with BH/PH hierarchies and mosaic options; robust provenance and time-series capabilities.
- Ensuring data quality, versioning, and traceability across CS surveys.
- Consistent use of classification keys, minimum mapping units, and change-status logic.
- Aim to maintain usable, up-to-date, interoperable data that supports discovery, reuse, and policy-relevant biodiversity monitoring.