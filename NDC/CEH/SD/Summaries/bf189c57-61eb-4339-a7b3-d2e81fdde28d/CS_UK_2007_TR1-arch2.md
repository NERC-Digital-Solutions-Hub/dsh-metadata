# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Defines the 2007 Countryside Survey field mapping methodology, data model, and digital workflow to map Broad Habitats (BH) and Priority Habitats (PH), report land-cover change, and support UK-wide environmental surveillance over time.
- Aims to enable time-series monitoring and integration of PHs with BHs to enrich baseline data for biodiversity policy evaluation.

## Data Model and Outputs
- Polygon-based mapping within 1 km squares; outputs categorized as Broad Habitats (BH) and Priority Habitats (PH), with PHs nested inside BHs.
- PHs may require GIS masks post-survey to constrain extents; enclosed habitats edited from 1998 data; unenclosed habitats combine finer 1990 vegetation detail with 1998/2000 mapping for refined attributes.
- Change reporting centers on genuine ecological change (REAL) versus correction of prior mis-recordings (ERROR); standardized attributes support national reporting and policy evaluation.
- Data products are designed for national datasets and downstream analysis; datasets stored and uploaded to appropriate portals.

## Mapping Scope and Habitat Types
- BHs are broad habitat classifications; PHs are more detailed and nested within BHs.
- Enclosed habitats rely on 1998 allocations with refined attributes; unenclosed habitats blend 1990 vegetation detail with later maps; GIS masks delineate native ranges for certain PHs.
- Mapping expands to upland unenclosed areas and Wales squares; consolidates prior themes into a single digital map for 1 km squares.

## Digital Mapping System and Data Capture
- CS Surveyor: a dedicated ArcGIS extension (built on ArcMap) for CS2007 data capture, integrated with CEH/Esri tools, including helpdesk support and fault logging.
- Data capture uses three feature types: Areas (polygons), Lines (linear features), and Points (point features).
- Editing requires map scale ≤ 1:5000; spatial accuracy is secondary to representing habitat extents accurately.

## Editing Areas and Polygons
- 6.a Editing Area Attributes: polygon-level attributes include BH/PH designation, accuracy, and reason for change; Change type: REAL, ERROR, or no change.
- Component-level attributes: components can be added/copied/deleted; at least one component per area; shared primary attributes possible across components.
- 6.b Copy Area; 6.c Split Areas; 6.d Merge Areas; 6.e Modify Area; 6.f Update Areas: maintain topology and allow creating new areas via splits/merges or copies.
- Editing workflow includes saving sessions and managing changes with clear reasons.

## Core Mapping Rules and MMU
- Minimum Mappable Unit (MMU): 1/25 hectare (400 m2); polygons smaller than MMU mapped as lines unless justified by criteria.
- Habitat allocation: a polygon with continuous woodland >25% canopy is mapped as BH/PH; new polygons created for habitat occurrences; changes may reflect habitat-type changes or shifts.

## Ponds and Inland Water
- Pond mapping requires identifying every pond per square; detailed attributes captured on a Pond Mapping Recording Sheet; one survey pond per square selected for detailed condition assessment.
- Cycle includes pond selection, data flows to freshwater surveyors, and reasoned explanations for ponds added or lost (e.g., drainage, infilling, creation).

## Points, Features, and Woody Linear Features (WLFs)
- Points: landscape elements < 20x20 m; features such as trees and ponds recorded as points; buffer zones and multiple components supported.
- Woody Linear Features (WLFs): include hedges, lines of trees, belts, screens, and other linear woody elements; categorized by natural lines versus hedge-form shapes; events carry attributes (length, height, condition, etc.).
- WLF components can be natural or managed; margins and species composition influence BH/PH allocation.

## WLF Attributes (Examples from the Field)
- Height categories (e.g., <1 m, 1-2 m, 2-3 m, >3 m, with higher categories available) and base height (canopy base) values.
- Species composition (e.g., mixed species; >50% hawthorn; >50% other).
- Evidence of management (e.g., newly planted, flailed, coppiced, laying).
- Line of stumps (Yes/No); vertical gappiness (percentage ranges) along the WLF.
- Margins (left/right) width classes; presence of staked trees; tree protectors in use.
- Notes on natural vs. non-natural shapes; modal DBH values for veteran-like management history when applicable.

## Editing Procedures for Linear Features
- Create New Line: define at map scale ≤ 1:5000; minimum length 5.0 m; lines cannot cross themselves; new lines start with an Unsurveyed/Missing Data event.
- Modify Line: edit geometry by moving vertices; handle shared boundary nodes with special Shared Node Modify; ensure no new intersections with other lines.
- Shared Nodes: modify intersections where lines share nodes; maintain topology constraints.
- Cut Line: digitize a cut polygon along a line to remove segments; lengths shown for cut and remaining portions.
- Copy Tool: reuse existing features from other layers (e.g., OS Mastermap) to shape edit sketches; multiple features can be combined in a cut sketch.
- Delete Line: remove lines with valid Reason for Change values on all attached events; cannot delete lines with unresolved attributes.
- Reshape Line: redraw portions of a line along an edit sketch; must intersect start/end points and adapt with a reshape tool.
- Reshape Following a Copied Line: follow line edits using copied landscape features to shape edits.
- Validation and constraints: edits must maintain MMU compliance; end nodes shared with other lines require appropriate modify tools; edits cannot create invalid intersections.

## Practical Guidance and Support
- Helpdesk available for CS Surveyor issues; ongoing methodology updates in the system.
- Emphasis on correct habitat extent and change rather than ultra-precise geolocation; tools support improved accuracy where needed.
- Reference material includes old Field Assessment Booklets (FABs) and CS2000-era documentation for context.

## Operational Flow and Data Management
- Build a digital GIS model mapping 1 km squares with BH/PH attributes; collect detailed vegetation and species attributes where applicable.
- Record changes against mapped components and verify against CS1990/CS1998/CS2000 to classify REAL vs ERROR changes.
- Identify survey ponds per square; select survey pond for detailed condition assessment; complete pond mapping sheets and route data to freshwater teams.
- Use CS Surveyor to create, split, merge, modify, and update areas; manage components, lines, and associated attributes.
- Ensure data quality, sharing, and storage via standardized datasets and portals; enable broader data access for downstream analyses and policy evaluation.

## Relationship to Legacy Data
- CS2000 themes and parcel-based data sheets documented previously mapped features; CS2007 consolidates multiple themes into standardized BH/PH mappings with a unified digital workflow and updated attribute codes.