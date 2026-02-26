# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Documents Countryside Survey 2007 (CS2007) field mapping methodology for recording habitats and landscape features in 1 km squares.
- Aims to report land cover change by Broad Habitats (BHs) and Priority Habitats (PHs) at country and UK levels; introduces more detailed habitat attributes and PH mapping in upland and unenclosed areas; extends to Wales with new squares.
- Data collected digitally and integrates five prior themes (forestry, agriculture/natural vegetation, boundaries, structures, physiography) into a single editable GIS map.

## Data model and outputs
- Mapping produces polygons (areas), lines (linear features), and points (point features) with standardized attributes.
- Outputs organized around two keys:
  - Vegetation Key (for BHs/PHs via vegetation characteristics)
  - Key to Woodland Types/Features (woody features like belts, clumps, lines, woodlands)
- Emphasis on change mapping: surveyors indicate genuine habitat/feature change and correct mis-allocations from earlier surveys.

## Change management and data lineage
- Surveyors map changes against previously surveyed squares (CS1990/CS1998/CS2000) to verify and adjust allocations.
- Distinguishes REAL change vs ERROR change (correcting past misallocations); uses historical data to support decisions.
- Post-survey GIS masks refine PHs/BHs in certain cases.

## Digital workflow and tools
- CS Surveyor extension for ArcMap (ESRI-based); surveyors log in and edit within a dedicated Countryside Survey data frame.
- Change-recording is mandatory when editing mapped habitats/features; field staff must verify and justify changes.
- Regular guidance updates and a helpdesk support field issues.

## Mapping units and rules
- Minimum mapping unit (MMU): 1/25 hectare (400 m²); polygons smaller than MMU not mapped unless representing a boundary segment; length-only mappings used for features below MMU.
- Editing tools cover polygons (areas), lines, and points with specific operations (split, merge, copy attributes, update, etc.) within the Landscape Feature Editing toolbox.
- Special treatment for ponds with a detailed pond mapping protocol; one pond per square selected for a detailed condition survey.

## Ponds and aquatic features
- All ponds in a square must be identified and recorded; one pond is chosen for a detailed condition assessment (the survey pond).
- CS2007 Pond Mapping Recording Sheet captures pond ID, area, water presence, reasons for pond loss/creation, and notes.
- Preselected ponds used when available; field selection may adjust for new ponds during CS2007.

## Editing capabilities and workflows
- Points: edit individual features (trees, ponds, water bodies, etc.); components can be added/copied/deleted; buffer zones may be recorded.
- Areas: edit polygons to change broad/habitat attributes, record change status (real/error/no change), manage components, modify boundaries/shared nodes, and update via splits/merges.
- Lines: edit linear features (fences, hedges, woody edges); add/copy/delete events; minimum event length 5 m; top-level length adjustments available; careful handling of shared nodes and line intersections.
- Shared nodes: modify intersections of lines; changes propagate to connected lines; edits must preserve topology and avoid invalid intersections.

## Woodland types and forest attributes
- Woodland features (BHs and PHs) can be polygon-level BH/PH with component-level forestry attributes (primary/secondary).
- Primary attributes include belts, clumps, woodland/forest, and other wood-related forms.
- Secondary attributes record species, canopy cover, DBH, and management features (fencing, regeneration, underplanting, windthrow, etc.).
- Guidance covers recording orchards, beech, coniferous woodland, wet woodland, non-native species, and other woodland types.

## Broad Habitat classifications (BH1–BH22 plus Mosaic)
- BH1: Broadleaved mixed and yew woodland (plus variants like wet woodland, parkland, upland ashwoods, upland oakwood, beech/hazel mosaics).
- BH2: Coniferous woodland (native pine woodland; attributes align with BH1).
- BH3–BH22 cover boundaries/linear features, arable/horticultural, various grasslands, heaths, fen/bog, inland/water features, rivers/streams, standing open waters, montane/inland rock, urban, supra-littoral and littoral habitats, sea contexts, mosaics, and related components.
- Mosaic: used when areas cannot be clearly delimited by a single BH/PH; assigned mosaic with component-level percentage covers.

## Non-native species and survey ethics
- Guidance encourages recording non-native species encountered to provide supplementary habitat context and potential BH/PH qualification.

## Data accessibility and value
- Key challenge: increasing the value of CS datasets by combining with other relevant data sources.
- Emphasizes enabling access to underlying data used to create outputs to support policy scrutiny and environmental health analyses.

## Practical considerations for analysts
- Ensure datasets are stored and uploaded to appropriate portals; maintain standardized formats for cross-policy monitoring.
- Use Vegetation and Woodland keys to drive habitat classification; follow MMU and change-detection guidance for consistent time-series data.
- Monitor and document data quality issues; utilize CS helpdesk and wiki for fault logging and updates.

## Appendices and additional resources
- Pond Mapping Recording Sheet and guidance for selecting the survey pond.
- CS2000 background: themes, coding structure, and historical data lineage.
- Appendices include field assessment codes, loop notes (for data quality issues), and references to veteran-tree girth guidelines and related tools.
- Acknowledges funding and partnership sources (DEFRA and NERC) and provides contact information for the Countryside Survey program.