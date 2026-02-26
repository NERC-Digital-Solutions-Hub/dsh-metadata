# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and purpose
- Methodology for mapping habitats and landscape features within Countryside Survey 2007 (CS2007) squares.
- Digital mapping shift: data collected digitally; integrates multiple themes into a single editable map per 1km square.
- Aims: report land-cover change by Broad Habitats (BH) and Priority Habitats (PH); maintain disaggregated data records for policy/science use.
- Wales expansion: adds ~60 new squares for country-level reporting.
- Primary data model: polygons (Areas), lines (Linear features/landscape features), and points (Point features); emphasis on extent and change over precise placement.

## Data model and mapping structure
- Areas (polygons): primary habitat units; minimum 0.04 ha (400 m2); larger continuous woodland map to BH/PH; new habitats require new polygons.
- Components: sub-units within an Area; can have multiple components with shared/different attributes; attributes grouped by themes.
- Lines (linear features) and Events: woody lines, fences, walls, ditches, hedges, etc.; include width/length constraints; events describe segments.
- Points (point features): individual trees, scrub patches, standing water, etc.; multiple components per point; buffers recorded for landowner agreements; veteran trees recorded with limits.
- Data integrity: MMU (minimum mapping unit) and mosaic mapping allow for sub-polygon delineation; polygon sizes and mosaic percentages are explicitly defined.
- Editing and QA: strict procedures for area/component/line edits; changes require justification (REAL vs ERROR) and documentation.

## Habitat classification keys
- Vegetation Key: assigns primary and selected secondary habitat attributes to polygons based on vegetation composition; BH/PH allocation determined here.
- Woodland Types/Features Key: classifies woody vegetation units (e.g., belt of trees, clump of trees, woodland/forest); supports polygon and component-level coding; records DBH, species, canopy cover.
- Enclosures and unenclosed uplands: refined delineation of unenclosed BHs (e.g., bogs, heath) with detailed vegetation attributes; PHs nested within BHs.
- Orchard guidance: traditional orcurtilage orchards treated as agricultural attributes within existing polygons.

## Ponds and water bodies
- Comprehensive pond mapping protocol: identify all ponds within a square; standing water definition ranges 25 m2 to 2 ha; water presence usually for at least 4 months.
- Survey pond: one pond per square selected for detailed condition assessment; selection is random with a pre-defined process; CS2000 data considered for preselection.
- Recording: pond polygon ID, area, water presence, creation/loss notes; detailed pond mapping sheets used.
- Temporary ponds: signs documented to determine status.

## Woody Linear Features (WLFs) and points
- WLFs: lines that may be lines of trees, hedges, or scrub; coding depends on natural shape vs hedged form; include gaps, width, and multi-part lines.
- Attributes for WLFs (example coding): height categories (e.g., <1m to >3m), base canopy height, species composition (e.g., >50% hawthorn), evidence of management (recent cutting, laying/coppicing), line of stumps (yes/no), vertical gappiness percentages, left/right margin widths, presence of staked trees, and tree protectors.
- Special notes: if >2m tall, ensure woody species are trimmed to shape in cataloging; if natural shape, record accordingly.
- Points and lines: points capture individual trees/scrub; lines capture woody linear features; both support component-level attributes and buffers.

## Editing workflows and tools
- Line creation: map at scale 1:5000 or smaller; lines cannot exceed square boundaries; minimum length 5.0 m; lines cannot cross themselves; new line starts with an Unsurveyed/Missing Data event.
- Line modification: edit vertices, insert/delete/move vertices; shared nodes require Special handling (Shared Node Modify); edits must not create invalid intersections.
- Cut lines: digitize cut polygon along a line to remove a segment; length of cut is shown; cuts must meet minimum length requirements.
- Copy features: use existing polygons from other layers (e.g., OS MasterMap) to form edit sketches; copy+ to include features in the edit sketch.
- Reshape: redraw along existing lines to align with field shape; must intersect line at start/end; can be performed in steps with vertex edits.
- Delete lines: requires valid Reason for Change on all events; scale constraint 1:5000 or less; single-line deletions.
- Shared nodes: modify intersections between lines; careful to avoid new intersections; can move shared nodes to adjust multiple lines.
- Visit status: unvisited lines can be identified via Select By Attributes; handle looped/corrupted events by converting to Deleted Feature with a No Change reason, then recreate as needed.
- Practical constraints: field editing emphasizes habitat extent/change over pinpoint spatial accuracy; zoom levels and MMU govern edits.

## Ponds, water bodies, and associated procedures
- Detailed pond protocol: multiple attributes per pond; one survey pond per square for condition assessment; random selection aided by Appendix guidance.
- Pond mapping sheets: CS2007 Pond Mapping Recording Sheet collects pond-level data; separate forms for ponds present vs. lost since CS2000.
- Documentation: pond polygon IDs, area, water presence status, reasons for creation/loss, notes; consistent with the broader habitat mapping framework.

## Practical guidance and constraints
- Field constraints: ArcMap CS Surveyor requires specific zoom levels; spatial accuracy is secondary to correct habitat attribution and extent.
- Data limits: MMU 0.04 ha for areas; up to four species per polygon; non-native species monitoring included.
- Documentation: extensive appendices and guidance for specialized habitats, species, and physiography; references to NVC communities and CSS habitat standards.
- Masks: national/regional GIS masks applied post-survey to constrain/adjust PH extents (upland vs lowland) in different countries.
- Support and processes: bug reporting, helpdesk/wikis, regular updates; contact points and project office details provided.

## Summary for GIS practitioners
- CS2007 standardizes digital habitat change mapping across 1km squares using CS Surveyor in ArcMap.
- Habitat classification relies on two keys: Vegetation Key (bh/ph allocation) and Woodland Types/Features Key (woody vegetation structure).
- Data model centers on polygons (areas), lines (events), and points (features) with modular components and theme-based attributes.
- Editing workflows cover creation, modification, splitting/merging, updating, and copying of areas, components, and events, with strict change-tracking rules.
- Ponds are governed by a detailed, multi-step mapping and sampling protocol plus a random selection process for condition assessment.
- Spatial accuracy is secondary to accurate habitat extent and change attribution; MMU and mosaic mapping guide polygon creation.
- Practical guidance includes feedback channels, bug reporting, and procedures for recording non-native species and orchard attributes.