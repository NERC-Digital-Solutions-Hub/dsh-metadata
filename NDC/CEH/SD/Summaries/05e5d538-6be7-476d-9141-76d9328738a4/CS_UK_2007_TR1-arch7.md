# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Presents methodology and data model for Countryside Survey 2007 (CS2007) habitat and landscape feature mapping.
- Switch to digital data collection to report change by Broad Habitats (BH) and Priority Habitats (PH), including upland/unenclosed habitats and Wales squares.
- Emphasizes consistency, time-series continuity, ability to map change, and correcting past allocations.

## Data model and classification framework
- Broad Habitats (BH) vs Priority Habitats (PH): polygon-level mapping with detailed component attributes.
- Enclosed vs unenclosed habitats: different mapping approaches; unenclosed data may integrate older CS1990/CS2000 data with finer detail where possible.
- Post-survey GIS masks used to delimit ranges and estimate extent of PHs and some BHs; ponds and standing waters have extensive dedicated mapping.
- Emphasis on extent and change over exact geolocation; MMU (minimum mapping unit) applied; new polygons created when habitat type changes.
- Nested PHs within BHs; PHs and BHs mapped with additional attributes and GIS masks.
- Classification keys:
  - Vegetation Key: habitat assignment based on plant species composition; supports nesting PH within BHs and historical corrections using 1990 CS data where applicable.
  - Woodland types/features key: classifies woody vegetation into belts, clumps, lines, woodland/forest, and Woody Linear Features (WLFs); attributes capture canopy structure and composition.
- Vegetation Key overview:
  - Primary/secondary attributes for BHs/PHs; emphasis on species composition, canopy cover, habitat indicators; upland/lowland variants; notes on coastal and Machair habitats; guidance on pulse/press disturbance mapping.
- Woodland habitats (BH1–BH4; plus others) and related features:
  - BH1: Broadleaved Mixed and Yew Woodlands (lowland).
  - BH2: Coniferous Woodlands.
  - BH3: Boundaries and Linear Features (woody and non-woody lines; areas if wide enough or lines/events otherwise).
  - BH4: Arable and Horticulture (fields and margins with detailed field-edge attributes).
  - BH5–BH19, BH21–BH23 cover grasslands, heath, fen/marsh, bog, rivers/streams, standing waters, montane, inland rock, urban, supra-littoral, mosaics.
  - PHs may nest within BHs and carry additional attributes.
- Outputs linked to UK Biodiversity Action Plans; mosaic approaches used when delineation is ambiguous or MMU constraints apply.

## Mapping workflow and data capture
- CS Surveyor: ArcMap-based data capture extension with a questionnaire-driven attribute editor and editing tools.
- Change management is mandatory: edits must be flagged REAL change, ERROR change, or NEW baseline, with justification.
- Data integrity and updates via helpdesk/wiki; methodology updates appear in Latest News.
- General data rules:
  - Continuous woodland with full canopy maps to BH/PH woodland.
  - MMU of 1/25 ha (400 m2); sub-MMU features not mapped as areas unless part of larger polygon.
  - New polygon created when habitat type changes; species changes do not create new polygons.
  - Record at least two species per polygon (up to four).

## Editing operations (areas, lines, points) and data management
- Areas (polygon editing)
  - Polygon-level attributes: BH/PH, 1998 BH accuracy, change status (REAL/ERROR/NEW BASELINE), visit status.
  - Change handling: differentiate REAL, ERROR, NEW BASELINE PH allocations; use 1990 CS data for unenclosed PHs when applicable.
  - Component-level attributes: polygons may contain multiple components; components can be added/copied/deleted; editing organized by themes.
- Copy, Split, Merge, Modify, Update
  - Copy Area: replicate attributes from source to targets.
  - Split Areas: digitize split; ensure MMU compliance; assign attributes for parts.
  - Modify Area: topology-based boundary edits; careful modification of shared nodes.
  - Update Areas Edit: create new landscape area via splitting/merging; manage intersections and attribute propagation.
  - Stop Editing: save or discard session.
- Points (and woody features)
  - Point editing: add/move/delete/copy attributes; points can contain multiple components; veteran trees and buffers may be recorded.
  - Minimum editing scale: 1:5000.
- Woody Linear Features (WLFs)
  - Natural-shape vs unnatural-shape forms; line of stumps possible.
  - Attributes include height classes, base canopy height, species composition (e.g., >50% hawthorn), evidence of management, line of stumps, vertical gappiness, margins, staked trees, tree protectors.
  - If >2 m base height, ensure woody species are cut/trimmed to remove unnatural shape unless natural shape is recorded.
  - Coding examples and images illustrate WLF forms and their mapping.
- Linear features and events
  - Lines: features <5 m wide; events along lines describe changes (fences, hedgerows, banks, margins).
  - Each line can have multiple events; events have type, length, condition, margins, species.
  - Copy Events tool allows replication along target lines.
- Ponds and water bodies
  - Identify all ponds per square; record basic attributes on CS2007 Pond Mapping Recording Sheet.
  - Designate a survey pond per square for detailed condition assessment; randomization used in the field when needed.
  - Pond boundary decisions and criteria documented; includes dry ponds and connected/dammed waters.
  - Pond attributes feed into Inland Water and BH/PH mapping.
- Non-native species and orchards
  - Checklist of non-native species to record within habitats; records may qualify habitats.
  - Orchards newly emphasized; record Orchard as an agricultural crop attribute; treat curtilage around houses with Gardens/Grounds plus Orchard attribute as appropriate.

## Practical guidance and cautions
- Spatial accuracy is not the primary concern; focus on correct habitat extent and change detection.
- Leverage CS1990/CS1998 data to support PH allocations and change validation when available.
- Use GIS masks and post-survey processes to estimate extents and maintain time-series integrity.

## Outputs and reporting
- Results presented by Broad Habitats and Priority Habitats to support national reporting and biodiversity plans.
- Mosaic approach used when Habitat boundaries are ambiguous or constrained by MMU.

## Implementation notes for GIS specialists
- The document provides extensive attribute schemas, vegetation/habitat codes, and data-entry guidance for polygon, line, and point features.
- Prescribes structured workflows for editing, copying, splitting, merging, and updating map features to ensure data consistency across squares and survey years.
- Emphasizes field readiness, troubleshooting, and governance of edits within the CS Surveyor ArcMap environment.

## Appendices and related materials (contextual references)
- CS2007 Pond Mapping Recording Sheet; square-by-square pond recording process.
- CS2000 and CS1990 thematic mappings and coding schemes; examples of parcel/attribute coding and data sheets.
- Appendix content covers veteran tree girth guidelines, loops in squares, and related methodological notes.
- Additional references to field assessment materials and data sheets for legacy mapping (FABs, CS2000 FABs, and old field handbooks).