# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Sets out the CS2007 field mapping methodology for recording habitats and landscape features in 1 km squares and reporting land cover change by Broad Habitats (BH) and Priority Habitats (PH).
- Introduces CS Surveyor, a digital ArcMap extension, to support time-series data and ensure consistent standards.
- Provides guidelines for mapping change, new squares, enclosed vs unenclosed habitats, and detailed woodland/woody feature mapping, including pond mapping procedures.

## Data Model, Classification, and Standards
- Data consist of polygon habitats (areas), linear features (lines), and points, each with configurable attributes.
- Minimum Mapping Unit (MMU) = 1/25 hectare (400 m2); features below MMU are not mapped as separate areas unless part of a larger boundary.
- Mapping decisions governed by:
  - Vegetation Key: assigns primary/secondary habitat attributes (BHs and PHs) based on plant composition.
  - Woodland/Features Key: classifies woody vegetation into belts, clumps, woodland/forest, hedges, etc.
- BHs and PHs defined at polygon level; post-survey masks help distinguish upland vs lowland PHs and support national extent estimates.
- Major BHs include broadleaved/mixed woodlands, coniferous woodlands, boundaries/linear features, arable/horticulture, various grasslands, heaths, fens/marshes, bogs, rivers/streams, waters, urban, coastal habitats and mosaics.
- Enclosed vs unenclosed habitats treated with differing attribute detail to better capture PHs and vegetation composition.
- Recording rules emphasize spatially uniform units, documenting at least two species per polygon (up to four), and noting non-native species occurrences.

## Data Capture System and Workflows
- CS Surveyor (ArcMap extension) used to capture/edit habitat, vegetation, and landscape features within a square.
- Workflow emphasizes reporting change against mapped components, distinguishing genuine change from errors.
- Editing capabilities include:
  - Areas: split/merge, copy attributes, update attributes, handle multiple components within an area.
  - Lines: edit linear features (fences, hedges, woody lines) with event-level attributes; copy/modify/update events.
  - Points: edit point features (trees, ponds, water bodies) with components; add/move points; define buffers.
- Pond Mapping and Survey:
  - Every square with ponds must be surveyed; ponds identified/measured with CS2007 Pond Mapping Recording Sheet.
  - A survey pond is randomly selected for detailed condition assessment; preselected pond acceptable if still valid.
  - Guidelines for pond inclusion, boundary delineation, and differentiation from ditches/flushes/dammed streams.
- Data quality and field operations are supported by:
  - Mandatory vs optional fields in editors.
  - Stop rules requiring saving sessions to persist edits.
  - Regular field updates via helpdesk and a Wiki fault-logging system.

## Metadata, Provenance, and Change Management
- Rigorous change management to maintain data integrity across survey cycles:
  - REAL Change: genuine habitat allocation change.
  - ERROR Change: correction of previous incorrect allocations.
  - New Baseline: subdivision of previously mapped habitats (e.g., upland hay meadow separated from neutral grassland).
- For unenclosed habitats, integration of CS1990/CS2000 data to improve detail; enclosed habitats may use CS1998 data.
- Each area/component requires a Reason for Change; BH accuracy checks compare prior vs. current allocations.
- Change status tracked at polygon and component levels; visit statuses include In progress, Completed, Refused access.
- Documentation requires multiple attributes per habitat type, with at least two species per polygon (up to four) for robust ecological description.

## Quality Assurance, Data Governance, and Challenges
- Emphasis on data that meets user needs: discoverable, up-to-date, usable with appropriate metadata.
- Challenges aligned to Data Stewards archetype:
  - Incomplete understanding of user needs/priorities.
  - Timely receipt of data from creators/maintainers.
  - Ensuring metadata and standards compliance across many systems/formats.
  - Handling large and legacy datasets requiring bespoke/interoperability considerations.
- Handbook provides guidance to mitigate these by enforcing consistent methodologies, explicit attribute schemas, and clear change-control processes.

## Accessibility, Sharing, and Archiving
- Digital data capture via CS Surveyor with a central ArcMap data frame to standardize sharing and discovery.
- Updates and methodological changes disseminated through a helpdesk and a “Latest News” channel.
- Datasets intended for upload to portals/catalogues with detailed field-level documentation and metadata to support reuse and governance.

## Practical Takeaways for Data Stewards
- Enforce a consistent data model with well-defined BH/PH classifications and woodland/woody feature keys.
- Enforce MMU compliance and document habitat mosaics where required.
- Maintain provenance by recording original allocations (1990/1998/2000 data), documenting changes with explicit reasons, and distinguishing genuine changes from corrections.
- Preserve metadata quality: capture species counts, coverage categories, and detailed attribute themes (e.g., Inland Physiography, Inland Water, Agricultural/Natural Vegetation, Forestry, Structures, Coastal features).
- Implement robust change-management workflows within CS Surveyor, including mandatory fields, change statuses, and documented reasons.
- Facilitate data sharing by producing well-structured, survey-ready datasets with versioned documentation and timely methodology updates.

## Appendices and Additional Details (Referenced Concepts)
- CS2007 mapping themes and coding schemas; pond mapping forms; and guidelines for old CS2000/CS1990 data integration and legacy coding.
- Appendix materials cover specialized topics (e.g., looped linear features, veteran-tree girth guidelines, and codified attributes) that support data integrity and field interpretation.
- Illustrative imagery and step-by-step tablet editing procedures are included to aid field technicians in applying standards consistently.