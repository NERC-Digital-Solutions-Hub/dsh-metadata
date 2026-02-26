# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview of WLF attributes and coding

- Woody Linear Features (WLFs) are described with detailed attribute fields to capture shape, structure, and management history.
- Key attributes include:
  - Height categories for canopy base and overall height.
  - Species composition (e.g., mixed species, >50% hawthorn, etc.).
  - Evidence of recent management (e.g., newly planted, cutting, laying or coppicing).
  - Line of stumps presence or absence.
  - Vertical gappiness (percent breaks from canopy to ground).
  - Margin width on left and right sides.
  - Staked trees and tree protectors (whether used to protect newly planted trees).
- Guidance emphasizes distinguishing unnatural vs natural shapes and recording shapes accordingly; examples illustrate how to code multiple sections of a WLF with varying characteristics.
- The dataset accommodates both unnatural and natural WLF forms and permits recording of veterans or managed features.

## Tablet-based line editing workflows (CS Surveyor)

- Create New Line
  - Lines must be edited at a map scale of 1:5000 or less, must be within the survey square, and must be at least 5.0 m long.
  - A new line starts with a single Unsurveyed/Missing Data event; subsequent attribute edits follow standard protocols.
- Modify Line
  - Vertices along a line can be added, deleted, moved; end-point vertices that are shared with other lines are edited via Shared Node Modify.
  - Shared nodes (junctions) can be moved to reposition connected lines; edits must avoid introducing intersections with other lines.
  - Edits must preserve topology; prohibited edits include creating new intersections where none should exist.
- Cut Line
  - Use an edit sketch polygon to define the portion to cut from the line; the length to be cut is highlighted and the remaining length is shown.
  - The Cut operation persists after Save Changes.
- Copy Tool
  - Ability to copy features from other layers (e.g., OS Mastermap) into the edit sketch to improve spatial accuracy (Cut edit sketch).
  - Supports adding or removing features within the same edit sketch.
- Delete Line
  - Deletion requires a valid Reason for Change value on all events; lines with invalid reasons cannot be deleted.
  - Deletions are performed one line at a time and within the 1:5000 scale constraint.
- Reshape Line
  - Reshape edits must intersect the original line at the start and end; can follow an existing line or a copied line.
  - The reshape graphic must intersect the line to be reshaped; endpoints may be adjusted using the reshape tool.
- Checking Visit Status on Linear Features
  - Unvisited lines are highlighted via a Select By Attributes workflow (Landscape Events -> VISIT_STATUS = 0).
  - Loops with corrupted event data require a specific remediation workflow: delete and recreate lines after marking events as Deleted Feature with appropriate Reason for Change and Visit Status.
- General data integrity
  - All edits occur in a single edit session; saving is required to persist changes.
  - Edits are constrained to a single survey square and must maintain geographic/topological integrity.

## Change management and data quality considerations

- Real vs. erroneous changes
  - REAL change denotes genuine habitat or attribute changes since previous surveys.
  - ERROR change indicates corrections to prior mis-recordings without ground-change.
- Administrative rules for edits
  - Reason for Change is mandatory when modifying areas or lines.
  - Edits must preserve dataset consistency and avoid invalid topology (e.g., intersecting lines, illegal vertex edits).
- Data provenance and reproducibility
  - The workflow supports maintaining metadata and linking edits to the CS Surveyor process, aiding reproducibility and cross-reference with earlier CS datasets.

## Ponds and CS2007 pond mapping (Annex 3)

- Complete one pond mapping form per square, listing ponds within the square and noting ponds from CS2000 that no longer exist.
- For each pond, capture:
  - Pond polygon ID and area.
  - Whether water is present (Y/N); if dry, indicate reason for loss or absence.
  - Reason for pond’s inclusion or loss in the CS2000 dataset (e.g., land drainage, infilling, built over, etc.).
  - Notes describing pond characteristics and boundary delineation.
- Selection of the survey pond
  - A pre-selected survey pond may be used; if not available or unsuitable, select another pond based on predefined criteria and practical access considerations.
  - The pond selection process accounts for multiple ponds within a square and aims to provide a representative detailed condition survey.

## Appendices and reference materials

- Appendix 1: Using old Field Assessment Booklets (FABs)
  - Provides electronic access to FABs and CS2000 references for interpreting habitats, with codesheets and data tables to support interpretation.
- CS2000 mapping themes and codesheets
  - Detailed codes and attribute structures for previous CS surveys (e.g., five themes in CS1990 and six themes in subsequent CS2000 iterations) to support cross-era data compatibility.
- Appendix 5: Girth sizes of veteran trees
  - Rule-of-thumb gird size thresholds by species to guide veteran-tree classification and sampling.
- Appendix 6: Squares with loops
  - Listings of squares that contain looped linear features, including route identifiers and bounding coordinates; context for data quality and loop remediation requirements.

## Analytical opportunities and data-use implications for Analysts

- Data-driven habitat quantification
  - Quantify habitat extent and change by Broad Habitats (BH) and nested Priority Habitats (PH) across squares, regions, and nationally.
- Correlations and landscape patterns
  - Model relationships between habitat change and landscape features (woodland structure, boundaries, water bodies, and line features).
- Change detection and provenance
  - Use REAL vs. ERROR change classifications to distinguish genuine habitat dynamics from corrections, aiding robust change-rate analyses.
- Habitat mosaics and connectivity
  - Exploit detailed WLF attributes and polygon-level attributes to study fragmentation, corridor viability, and connectivity within landscape mosaics.
- Pond dynamics and hydrological context
  - Integrate CS2007 pond data with broader land-use and hydrological features to assess pond creation/loss trends, aquatic habitat changes, and wetland support.
- Data accessibility and reproducibility
  - Leverage on-device metadata, change logs, and cross-references to earlier CS datasets to ensure reproducibility and facilitate meta-analyses.
- Practical considerations for analysts
  - Anticipate data accessibility challenges (e.g., complex data structures, large datasets, data protection considerations) and plan analyses around available metadata, provenance, and portal-ready datasets.