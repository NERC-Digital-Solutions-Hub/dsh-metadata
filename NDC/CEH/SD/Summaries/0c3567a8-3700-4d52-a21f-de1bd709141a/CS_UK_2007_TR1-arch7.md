# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Comprehensive GIS workflow for Countryside Survey 2007 (CS2007) mapping of habitats, landscape features, and related attributes.
- Introduces a unified digital map model with Broad Habitats (BH) and Priority Habitats (PH) classifications, plus procedures for editing polygons (areas), lines (linear features), and points (point features) in ArcMap via the CS Surveyor extension.
- Emphasises mapping change, data quality, multi-resolution data integration, field validation, and iterative testing.

## Data Model and Habitat Classification
- Two-tier habitat framework: Broad Habitats (BH) and Priority Habitats (PH) nested within polygon/area structures.
- BH cover major landscape types; PH provide finer, rarer delineations within BHs.
- Each habitat assigned at polygon level; component-level attributes capture sub-features (e.g., Woodland Features).
- Recording guidance includes capturing at least two species per habitat polygon (up to four) and using vegetation indicators and physiography.

## Vegetation Key and Woodland Features
- Vegetation Key assigns primary (and some secondary) attributes to BH/PH based on species composition and structure.
- Woodland Types/Features classify woody vegetation by canopy form and extent (e.g., Belt of Trees, Clump of Trees, Woodland, Line of Trees).
- Decision rules help distinguish between BH/PH woodland versus linear features (hedges, belts, lines); detailed criteria for recording species and cover.

## Digital Mapping System and Tools
- CS Surveyor: a bespoke ArcMap extension for CS2007 data capture/editing.
- Users log in, select a square, and edit within a CS data frame with preset symbology.
- Enforces change status tracking (REAL, ERROR, NEW BASELINE) and correction of prior mis-allocations.
- Support: dedicated helpdesk, fault logging, and regular updates.

## Methodology for Mapping Polygons (Areas)
- Polygon-level attributes: area, BH/PH selection, accuracy checks against older data, change status.
- Component-level attributes: multiple components per area, grouped by themes (physiography, vegetation, forestry, agriculture); components can be added/copied/deleted.
- Operations: Copy Area, Split Areas, Merge Areas, Modify Area, Update Areas Edit; stop editing requires saving.
- MMU-based rules govern minimum mapping units and boundary handling.

## Methodology for Mapping Points
- Points represent features smaller than 20x20 m; each point must have at least one component and be edited at scale 1:5000 or finer.
- Points can denote trees, standing water, ponds, etc.; multiple components may form a single feature.
- Include buffer-related attributes for woody lines/features; record modal DBH categories and species composition.

## Ponds and Inland Water
- Ponds are mandatory in every square; basic attributes captured on a pond mapping sheet.
- One survey pond per square selected randomly for detailed environmental and water-quality assessment.
- Delineation can be challenging; includes definitions for winter water levels and temporary ponds; guidelines for distinguishing ponds from ditches, dammed streams, and flushes.
- Detailed pond fields cover area, water presence, creation/loss reasons, and survey status; pond condition data collected separately.

## Methodology for Mapping Linear Features
- Linear features: width < 5 m but length > 20 m; mapped as lines with events (e.g., fence, hedge, ditch) and can be subdivided into events.
- If feature expands to >5 m width, map as an area with BH attribution.
- Events along lines are editable; new lines can be created; existing lines edited with length/attribute details.
- Margins (e.g., field margins) recorded as additional vegetation features; typical margins around 6 m.

## Special Topics and Guidance
- Non-native species: maintain a list for habitat recording.
- Orchard guidance: map as primary Orchard under Agriculture/Natural Vegetation with secondary attributes, or as curtilage garden with orchard as an additional attribute.
- Buffer zones: record presence/absence; important for post-survey analyses.
- Mosaic habitats: specify percentage coverage for each component to total 100%.
- Urban and coastal features integrate with multiple themes (Forestry, Structures, Recreation, Transport, Agriculture/Natural Vegetation).

## Practical Notes for GIS Specialists
- Data quality prioritized over absolute spatial precision; focus on accurate habitat extents, change status, and correct BH/PH attribution.
- Adhere to MMU guidelines; small polygons below MMU are not mapped as separate features unless part of a larger boundary.
- Edits should be performed at 1:5000 or finer; maintain polygon/component/event/attribute hierarchies.
- Regular saves and completion of reason-for-change protocols are required when updating data.

## Appendices and Reference Context (Highlights)
- Links to CS1990/CS2000 mapping approaches and codesheets; older FABs (Field Assessment Booklets) provided electronically for interpretation.
- Pond Mapping Recording Sheet and survey-pond selection process described, including pre-selected pond usage and contingencies.
- Loops in linear feature data noted; special procedures to correct corrupted loop data and reinstate features.
- Veteran-tree girth guidance and species-specific rules of thumb included as appendices (illustrative metrics for notable trees).