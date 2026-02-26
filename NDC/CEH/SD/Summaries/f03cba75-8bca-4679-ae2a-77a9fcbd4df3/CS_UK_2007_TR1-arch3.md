# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Purpose: nationwide field mapping of environmental habitats and landscape features to monitor change, support policy decisions, and inform future actions.
- Goals: produce standardized, auditable data; emphasize time-series reporting, data quality, metadata, governance, openness, and avoiding data duplication.

## Data Model and Scope
- Coverage: mapping conducted in 1 km square units across the country.
- Structure: combines themes into a single digital map; Broad Habitats (BH) with Priority Habitats (PH) nested within where applicable.
- Reporting: PHs mapped within BH framework; GIS masks delineate upland/lowland ranges; detailed upland mapping in certain areas; time-series require consistent attribute detail and regular updates.
- Habitat types: extensive BH list (e.g., woodland types, grasslands, wetlands, rivers, seas) with PHs integrated; mosaics used where MMU-based delineation isn’t possible.
- Data attributes: detailed structures for BH/PH, including primary attributes, qualifiers, vegetation type, species lists, and cover percentages.

## Classification and Attribute Structure
- Vegetation Key: assigns primary/secondary BH/PH based on plant composition; supports identifying PHs within BHs and habitat-specific attributes.
- Woodland Types/Features Key: classifies woody vegetation by canopy form and records attributes such as DBH, species composition, margin management, veteran trees, and hedges/lines as BH/PH where applicable.
- Woody Features: systematic handling of lines of trees, belts, hedges, and other woody features with decision trees guiding BH/PH allocations.

## Data Collection, Survey Design, and Reporting
- Focus: habitat extent and change; validation and correction of previous allocations; thorough vegetation attribute collection for each polygon.
- PHs: may require combining new baseline data with existing information to support detection and reporting in rare or scattered habitats.
- Pond mapping: mandatory identification and recording of ponds in every square; pond data feed into survey outputs.

## Field Mapping System and Workflow (CS Surveyor)
- Tooling: ArcMap extension (CS Surveyor) for capturing and editing habitat, woodland, and landscape features.
- Data capture: areas (polygons), lines (linear features), and points; emphasis on accurate representation for change detection rather than absolute spatial precision.
- Change governance: every edit requires a Reason for Change; categories include Real change, Error change, New baseline, and No change.
- Editing capabilities: create, modify, copy, split, merge, update areas; edit line events and topology; manage shared nodes and complex boundary edits.
- Mapping thresholds: minimum mappable unit (MMU) of 1/25 hectare; editing scale at 1:5000 or better; lines must be at least 5.0 m long; lines cannot cross themselves; shared nodes link line topology.
- Quality controls: bug reporting and methodology updates via helpdesk/wiki; emphasis on recording genuine changes vs. errors.

## Pond Mapping Protocol
- Square-based pond inventory: map every pond in each square; select a single survey pond for detailed condition assessment.
- Pond criteria: 25 m2 to 2 ha, water presence for at least four months per year; boundaries defined by winter water levels and vegetation.
- Distinction rules: ponds vs. ditches/flushes/dams; determine whether connected ponds are separate or part of one pond.
- Data capture: CS2007 Pond Mapping Recording Sheet records polygon ID, area, water presence, loss/creation reasons, and notes; pre-selected pond lists streamline selection.

## Edition, Woodland Management, and Woody Features
- Woodland data: primary and secondary attributes covering forest/woodland type, margins, management indicators, DBH classifications, species composition, and veteran trees (limits per square).
- Woody Linear Features (WLFs): categorization as belts, lines, hedges, or woodland components; distinction between natural and managed shapes; all BH/PH allocations documented.
- Attribute guidance: detailed woodland attribute lists and decision trees to classify features consistently.

## Change Management, Data Quality, and Governance
- Change taxonomy: Real change (genuine habitat/attribute change since baselines), Error change (correcting past misallocations), New baseline (PH subdivision within polygons), No change (no substantive change).
- Back-correction: unenclosed upland habitats may require back-correction of 1998 data to align with enhanced 1990/1998 detail.
- Species recording: minimum of two and maximum of four species per habitat type, with habitat-specific guidance.
- Governance and openness: metadata and data-sharing principles are integral to the monitoring framework; emphasis on reproducibility and transparent data provenance.

## Practical Notes and Training Resources
- Training: practical guidance for ArcMap interface, CS Surveyor workflows, and field/data management.
- Editing workflows: step-by-step tasks for editing areas, lines, points; managing topology; handling shared nodes; and updating boundary edits.
- Appendix references: codified attribute lists, habitat descriptions, and example workflows to support field operatives and data managers.

## Outputs, Data Management, and Appendices
- Outputs: standardized habitat allocations (BH/PH), time-series data, pond records, and woodland/woody feature inventories to inform policy and biodiversity monitoring.
- Data management: ongoing governance, metadata standards, and openness to ensure reproducibility and future decision-making.
- Appendices: historical context (CS2000/CS1990) mappings, pond recording sheets, and detailed code sheets for data capture and interpretation.