# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides a consistent, time-series friendly framework for documenting environmental condition to enable scrutiny of ecological health and policy performance.
- Targets organisations with established monitoring duties, offering standardized methods for data capture, validation, and reporting.
- Emphasises mapping habitat change, reporting Broad Habitats (BH) and Priority Habitats (PH) at country/UK levels, and moving toward digital data collection for data reuse and broader accessibility.

## Data Model and Outputs
- Three feature types:
  - Areas (polygons): map BH/PH with detailed attributes.
  - Lines (linear features): map boundaries, fences, hedges, woody lines as events along lines.
  - Points: map discrete features like individual trees, ponds, etc.
- Outputs: digital maps, reports, and charts showing habitat extent, change, and BH/PH distribution over time.
- Quality assurance: data verified, cleaned, and stored in portals; change status distinguishes real ecological change from prior errors.

## Classification and Keys
- Vegetation Key: primary method for assigning habitat type to polygons, enabling BH/PH allocation.
- Woodland Keys: classify woody vegetation by canopy structure and inform BH/PH allocation; include veteran-tree provisions (limited per species per square).

## Habitat Coverage and Broad Habitats
- BH themes cover diverse landscape types with attributes and PH integration where applicable; post-survey GIS masks constrain PH ranges and upland/lowland, enclosed/unenclosed management attributes.
- Notable BH themes range from BH1 Broadleaved woodland to BH23 Mosaic, with BH3 and BH14/15 illustrating boundaries, waters, and montane contexts.

## Methodology and Digital Mapping System
- CS Surveyor: ArcMap-based digital extension enabling data capture, change indication, and QA in one workflow.
- Editing scales and rules: editing points at ≤ 1:5000; lines/areas via Landscape Feature Editing toolbox; clear change rationale required.
- Time-series focus: aggregates and refines earlier CS datasets (CS1990, CS1998, CS2000) for disaggregated habitat descriptions and PH reporting.

## Pond Mapping and Survey
- All ponds in a square must be identified; CS2007 Pond Mapping Recording Sheet used.
- A single pond per square (survey pond) is sampled in detail, selected randomly (preselected ponds allowed if valid).
- Workflow covers pond identification, boundary delineation, and differentiation from ditches/flushes; pond data flow into CS Surveyor.

## Data Collection and Editing Procedures
- Areas (polygons)
  - Create, copy, split, merge, modify with Landscape Feature Editing toolbox.
  - Attributes include area size, BH/PH designation, accuracy, change reason, visit status, and component-level attributes.
  - Change classifications include REAL change, ERROR, NEW BASELINE PH, etc. Multiple primary/secondary attributes per polygon; components expandable.
- Lines (linear features)
  - Represent features under 5 m wide; events describe sub-features along lines (fences, hedges).
  - Events store length, attributes, and spatial position; supports multi-part lines and editing (copying, adding, deleting, adjusting).
- Points (point features)
  - Capture discrete features (trees, ponds, etc.); edited individually; components allow multiple attributes; veteran-tree fields included; buffers possible for hedgerows.
- Habitat and vegetation attributes
  - For each habitat: primary attributes, vegetation type, species, and cover percentages (up to four species per polygon).
  - Species lists drawn from standard references; woodland trees/shrubs recorded with canopy-related data; margins, buffer zones, and management indicators mapped as additional features.

## Non-native Species
- Surveyors record a defined list of non-native species where present within a habitat, including area coverage considerations.

## Ponds: Recording Details and Survey Workflow
- For squares with ponds, use CS2007 Pond Mapping Recording Sheet to list pond polygon IDs, areas, water presence, and creation/loss drivers.
- Randomly select a survey pond from the compiled list; preselected ponds may be used with traceability updates.
- Post-mapping workflow: record survey pond in CS Surveyor and update the preselected ponds sheet.

## Accessibility and Data Sharing
- Strong emphasis on making underlying data accessible to others to maximise dataset value and support broad monitoring and policy evaluation.

## Practical Considerations for Analysts
- Supports long-term environmental monitoring through standardized habitat classification, change detection, and consistent data capture across time and space.
- Digital system and explicit QA/change rules enhance consistency and comparability of habitat extents, BH/PH allocations, and landscape features.
- Framework enables integration with supplementary data sources for enhanced environmental surveillance and policy assessment.