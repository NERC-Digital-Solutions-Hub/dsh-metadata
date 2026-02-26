# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides digital-field mapping guidelines for the Countryside Survey 2007, focusing on habitat extent and features (WLFs, ponds, lines, and areas) within 1 km squares.
- Uses CS Surveyor, a customized ArcMap extension, to capture and edit landscape features.
- Aims for consistent, time-series data suitable for UK biodiversity reporting and portal/catalogue dissemination.
- Emphasises data provenance, standardized attribute schemas, and change semantics to support longitudinal analyses.

## Data Model and Feature Attributes (Key Focus: Woody Linear Features and Habitat Elements)
- Woody Linear Features (WLFs):
  - Height categories for canopy base and modal height, with change categories (e.g., <1m, 1-2m, 2-3m, >6m, etc.).
  - Base height refers to canopy base; classification includes notes on natural vs. shaped forms.
  - Species composition indicators (e.g., mixed species, >50% hawthorn, other species).
  - Evidence of recent management (e.g., newly planted, cutting, laying, coppicing) with time frames (<3–5 years).
  - Line of stumps, vertical gappiness (percentage of breaks from canopy to ground), and margins (left/right) with width categories.
  - Staked trees and tree protectors indicators.
  - Guidance to adjust shape if canopy is naturally shaped; otherwise record WLF as unnatural shape.
- Imagery and example illustrations accompany the manual to aid coding of WLFs (unnatural vs natural shape, base height, canopy composition, management signs).
- Habitat mapping supports complex mosaics and requires consistent coding for canopy and woody components.

## Data Collection and Editing Workflow (CS Surveyor)
- Create New Line:
  - Lines must be created within the survey square, at scale 1:5000 or better, with a minimum length of 5.0 meters.
  - Lines cannot cross themselves; intersections split lines automatically.
  - Each new line starts with a single Unsurveyed/Missing Data event.
- Modify Line:
  - Edit using vertex-level tools; add/delete/move vertices; shared boundary endpoints can require Shared Node Modify.
  - Ensure edits do not create invalid intersections with other features.
- Shared Nodes:
  - Modify shared endpoints carefully; ensure topology is preserved across adjoining lines.
- Cut Line:
  - Use a cut polygon to remove segments from a line; view cut lengths and remaining lengths; ensure resulting line segments meet minimum length requirements.
- Copy Tool:
  - Import features from other layers (e.g., OS Mastermap) to create precise cut-line edits; supports adding/removing features to a cut edit sketch.
- Delete Line:
  - Delete lines only when all events have valid Reason for Change; scale restrictions apply.
- Reshape Line:
  - Reshape lines by drawing a reshape graphic; must intersect the target line; tends to move the line to follow landscape boundaries.
- Reshape Line Follow Copy:
  - Allows a line to be reshaped to follow the boundary of a copied landscape-area feature.
- Validation and Edit Governance:
  - Edits must comply with the minimum length constraints; end nodes shared with other lines may require special handling.
  - Regular saves and explicit session termination (Save Session / End Session) are required.
  - Support channels (helpdesk, Wiki) are provided for updates and bug reporting.

## Pond Mapping and Survey (CS2007 Pond Mapping)
- Ponds are a central component of Standing Open Waters; every square must identify ponds and record basic attributes.
- A single pond is randomly selected as the survey pond for detailed condition assessment; a preselected list can be used if appropriate.
- Documentation requirements include pond boundaries, connections between ponds, distinctions from ditches/dammed streams, and pond attributes (area, water presence, loss/creation reasons).
- Detailed recording uses CS2007 Pond Mapping Recording Sheets and associated forms.

## Habitat Keys, Canopy and Woodland Attributes
- While the section in this chunk focuses on WLFs, the handbook references:
  - Vegetation keys for primary/secondary BH/PH attributes based on species composition and physiography.
  - Woodland keys for canopy and form, enabling mosaics within polygons.

## Data Quality, Change Management, and Provenance
- Distinguishes real ecological change from corrections to prior mappings to support time-series analyses.
- Provisions for data provenance reference baselines (CS1990, CS1998, CS2000) alongside field 2007 data for validation and reconciliation.
- Handling of loops and corrupted event data:
  - Procedures to mark, delete, and re-enter loop-related data to maintain dataset integrity.
  - Alerts and appendices provide loop IDs and remediation steps.

## Practical Governance and Usability Notes for Data Stewards
- Metadata and governance considerations:
  - Clear, standardized taxonomy for BHs, PHs, woodland types, and associated attributes.
  - Versioning and time-stamping of habitat allocations to support longitudinal analyses.
  - Standardized data capture protocols (MMU considerations not reiterated in this chunk, but implied by editing rules).
  - Centralized data access via CS Surveyor and ArcMap; defined pathways for data sharing and dissemination.
- Non-native species and orchard-related guidance included to capture anthropogenic influences.
- Support mechanisms:
  - Helpdesk and Wiki for field procedures, updates, and references to latest methodology.
- Document governance and usability emphasis:
  - Ensures data interoperability, robust change semantics, and reliable time-series biodiversity reporting.
  - Encourages reconciliation with earlier CS datasets and consistent application of keys and attributes.

## Appendices and Reference Material (Highlights)
- Appendix 4: CS2007 Pond Mapping Recording Sheet (per-square, pond-level data, survey pond selection).
- Appendix 5: Girth sizes of veteran trees (rules-of-thumb for classifying veteran status by species and girth).
- Appendix 6: Squares with loops (lists squares affected by loop data; guidance for remediation).
- Appendix notes provide detailed codings, species lists, and example codes to support field coding and data integrity.

## Takeaways for Data Stewards
- The Field Mapping Handbook provides a comprehensive, digital-data-centric workflow for mapping habitat extent and change, with robust classification (BH/PH), detailed attribute schemas (especially for WLFs), and explicit change semantics to support reliable time-series analyses.
- Data governance hinges on standardized keys, consistent polygon/line/point structures, and explicit recording of change (REAL vs. other change types) to ensure longitudinal biodiversity reporting quality.
- The methodology integrates pond mapping, line and woodland attributes, and habitat mosaics, enabling nuanced landscape-scale analyses while enforcing minimum mapping units and scale constraints.
- Ongoing data quality is supported by field procedures, controlled editing tools, and post-survey governance processes, all designed to produce interoperable data suitable for portals and catalogues.