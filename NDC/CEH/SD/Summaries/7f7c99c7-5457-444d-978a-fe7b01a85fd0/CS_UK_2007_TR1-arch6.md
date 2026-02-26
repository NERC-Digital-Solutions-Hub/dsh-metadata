# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Defines field mapping practices for the Countryside Survey 2007 (CS2007), including digital GIS workflow to map Broad Habitats (BH) and Priority Habitats (PH), with emphasis on habitat change, data capture, and time-series reporting.
- Provides detailed data models, attribute schemas, and coding schemes; outlines workflows for creating, editing, and validating habitat features and related landscape elements.
- Includes procedures for pond mapping, line and point feature editing, and governance to ensure data quality and reproducibility across squares.

## Overview of the mapping framework

- Digital, GIS-based field mapping to deliver country-wide habitat extents and change over time.
- Consolidates multiple themes into integrated digital maps per 1 km square; supports time-series biodiversity reporting and policy needs.
- Emphasizes self-serve data products (e.g., habitat extents, changes) with explicit reasons for changes and data quality checks.
- Includes appendices and supporting materials for consistent data capture and cross-walks with earlier surveys (CS1990, CS2000).

## Data Model and Attributes

- Two-tier habitat framework:
  - Broad Habitats (BH) and Priority Habitats (PH) mapped at polygon level.
  - Detailed attribute data captured at component level; PHs nest into BHs with GIS masks used to constrain ranges.
- Habitat classification guidance emphasizes vegetation attributes (species presence, cover, indicators) and careful handling of mosaics and nested PHs.
- Key feature types:
  - BHs, PHs, and WOODLAND/LINEAR features (WLFs).
  - Non-spatial attributes tied to components and areas, with change status and accuracy considerations.
- Minimum mapping unit (MMU): 1/25 ha (400 m²); smaller units only for clearly distinct habitat features.
- Data capture formats and attribute sets are designed to support longitudinal analyses and re-use across survey cycles.

## Wooded Linear Features (WLFs): Attributes and Coding (Extracted Focus)

- Unnatural shape versus natural shape;
- Height categories (e.g., <1 m, 1–2 m, 2–3 m, >3 m) and base canopy height;
- Species composition (e.g., mixed species; >50% hawthorn);
- Evidence of management (e.g., newly planted, cutting, laying or coppicing);
- Line of stumps (Yes/No) and vertical gappiness (percentage of canopy-ground gaps: <10%, 10–<25%, 25–<50%, 50–<75%);
- Margin widths (Left and Right) and presence of staked trees or tree protectors;
- Notes on natural vs. unnatural shape and septa for sections with varying shape and height;
- Images illustrating various WLF forms accompany the field guidance for consistent coding.

- Tabulated examples illustrate how to code lines and woody features in practice, including default and edge cases (e.g., hedgerows, belts, lines of stumps, and natural vs. cut shapes).

## Line Editing and Data Capture Workflows

- Create New Line:
  - Map at scale 1:5000 or smaller; lines must be 5.0 m minimum; cannot cross themselves; created with an Unsurveyed/Missing Data event.
  - Lines are added one at a time and cannot be drawn outside the survey square.
- Modify Line:
  - Edit geometry via vertices; end nodes on shared boundaries can require Shared Node Modify; must preserve topology and avoid intersections with other lines.
- Shared Nodes:
  - Modify line intersections by adjusting shared nodes; ensures topology remains valid across lines.
- Cut Line:
  - Define a cut polygon along the line; shows pink/white cut length and red remaining length; permits multi-location cuts with validation.
- Reshape Line:
  - Use a reshape tool to define alterations along an existing line; can only be performed if resulting shape remains valid and length constraints are met.
- Copy Tool:
  - Copy features from other layers (e.g., OS Mastermap) to refine edit sketches; supports building complex cut sketches with multiple features.
- Delete Line:
  - Requires all events on the line to have a valid Reason for Change; deletes the line and its events if validated.
- General rules:
  - Map scale requirements, minimum feature lengths, and non-self-intersecting constraints; topology and shared boundaries must remain consistent.
  - Events along lines carry attributes and a mandatory Reason for Change value; invalid records block edits.
- Status checks:
  - VISIT_STATUS and other event attributes used to identify unvisited linear features; specific procedures exist for handling loops or corrupted loop data (delete, recreate, and re-enter).

## Data Quality, Validation and Governance

- Clear delineation between real-change (genuine habitat change) and error-change (mis-recording); processes to update baselines and support time-series integrity.
- Mandatory logging of change reasons and post-edit accuracy checks to maintain data integrity across survey cycles.
- Handling of loops (data loops identified as corrupted) with prescribed remediation steps, including suppression of loop data and re-entry of corrected lines.
- Emphasis on self-contained, citable data products suitable for longitudinal biodiversity reporting.

## Pond Mapping Procedures

- Every square must map all ponds; one pond per square is selected for detailed condition assessment (survey pond) via Appendix 4 random numbers.
- Pond presence must consider seasonal water presence; ponds may be dry at survey but qualify if they typically hold water for at least four months.
- Detailed pond attributes are captured on mapping sheets; the survey pond is selected from a random pool and may be reselected to maintain randomization and coverage.
- Documentation includes pond polygon IDs, area, water presence, creation/loss reasons, and notes; forms support data traceability and linkage to CS2000 history.

## Outputs and Time-Series Considerations

- Outputs are designed to be self-contained, citable data products suitable for time-series analyses and biodiversity reporting.
- Outputs support habitat extents, change detection, and governance trails (reasons for changes, accuracy checks, and update procedures).

## Appendices and Supporting Materials

- Appendix materials provide:
  - Random numbers for pond selection and pond mapping recording sheets.
  - Species lists (BRC), BAP-related codes, and habitat-specific attribute fields.
  - Non-vegetation features, margins, and various attribute fields to standardize data capture.
- CS2000 and CS1990 crosswalks outline themes and codes for historical comparison and data compatibility.
- Appendix 5 covers veteran tree girth guidelines (rules of thumb by species) for identifying notable trees.
- Appendix 6 lists squares with loops and associated metadata for data cleansing and remediation efforts.

## Practical Notes for Data Support

- The handbook emphasizes rigorous standardization of attributes and consistent data capture across all survey squares.
- Data quality hinges on clear justification for changes, accurate line topology, and robust handling of complex features (e.g., mosaics, WLFs, ponds).
- The document provides concrete, field-tested procedures to enable end users to explore data via self-serve dashboards and time-series analyses while maintaining data integrity across survey cycles.