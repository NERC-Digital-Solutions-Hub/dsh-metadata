# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Provides a detailed methodology for mapping Broad Habitats (BH) and Priority Habitats (PH) within Countryside Survey 2007 (CS2007).
- Focuses on reporting habitat change over time (since CS1990/CS1998) and delivering country- and UK-level summaries.
- Introduces CS Surveyor digital data collection and expands detail in unenclosed uplands, with new squares in Wales.
- Emphasises change-focused mapping and alignment with biodiversity reporting needs.

## Data model and classifications

- Broad Habitats (BH) cover broad landscape types; Priority Habitats (PH) are nested within BHs and mapped with extra detail (assemblages, indicator species).
- Two keys drive classification:
  - Vegetation Key: assigns BH/PH polygons from species composition and habitat attributes.
  - Woodland Types/Features Key: classifies woody features (woodland, belts, clumps, lines, scattered trees) and translates woody structure into BH/PH attributes.

## Mapping approach and reporting

- Change-focused: map genuine land cover change since previous surveys and correct past misallocations.
- Reporting framework prioritises BH/PH; PHs included where relevant to biodiversity action plans.
- Upland unenclosed habitats mapped with detailed vegetation descriptions; enclosed habitats aligned to 1998 definitions with PH attribution where needed.
- Post-survey GIS masks aid estimation of PH extent/distribution.

## Digital mapping system and GIS workflow

- CS Surveyor extension in ArcMap drives data capture; surveyors edit polygons (areas), lines (linear features), and points (point features) within a dedicated data frame.
- Editing generally at 1:5000 scale or better; spatial accuracy secondary to correct habitat extent and change detection.
- Data integrity: field visits to mapped components; log faults/updates via helpdesk/wiki; change status and habitat allocation as quality measures.

## Editing areas (polygons)

- Polygon-level attributes: assign BH/PH using the vegetation key; reassess against prior 1998 classifications.
- Change determination: REAL (genuine change) or ERROR (correction of past data).
- Component-level attributes: grouped themes (Inland Physiography, Inland Water, Forestry, Agriculture/Natural Vegetation, etc.) for efficient attribute selection.
- Tools and operations:
  - Copy Area: duplicate attributes from a source polygon to targets.
  - Split Areas: digitise split lines; manage MMU constraints.
  - Merge Areas: combine areas with identical attributes; require a change reason and BH accuracy field.
  - Modify Area: adjust boundaries/topology; edit shared nodes.
  - Update Areas Edit: create new polygons by splitting/merging intersections with existing areas.
- Rules and MMU:
  - MMU = 1/25 ha (400 m2); minimum width 5 m; new polygon created when habitat type changes.
  - At least two species per habitat polygon; maximum of four.

## Points and woody features (points)

- Points represent individual trees, shrubs, or woody features; multi-component points possible.
- Buffers around features; veteran trees: up to 10 per square, max 2 per species; capture extensive attributes (DBH, canopy, health, etc.).
- Point editing: Create/Move/Delete Point; Copy Point Attributes; scale/proximity constraints; typically at 1:5000 scale and not within 5 m of another point.
- Woody linear features (WLFs): record attributes for each segment (e.g., line of trees, hedges, hedgerows); distinguish natural vs hedged/managed forms; capture management indicators along segments/events (fence, hedge, ROW).

## Linear features (lines)

- Line features composed of events along lines; minimum length 20 m, maximum width 5 m; broader features may be recorded as an area.
- Events along lines (fence, hedge, ditch) have attributes; lines can be created, edited, or copied with topology considerations.
- Tools:
  - Copy Events: copy attributes from source to target lines; overwrite existing ones.
  - Split/Modify/Update: support complex edits; maintain shared nodes and boundary integrity.
- Shared nodes: edits to end nodes shared by multiple lines must preserve topology; modifications may require Shared Node Modify operations.

## Ponds and aquatic features

- CS2007 Pond Mapping: map all ponds within each square; identify a survey pond per square for detailed sampling.
- Pond definition: standing water 25 m2 to 2 ha, persisting at least 4 months; distinguish ponds from other waters (ditches, flushes, etc.).
- Data capture: pond polygon or point attributes stored under Inland Water; Pond Mapping Recording Sheet tracks pond-specific data and rationale for creation/loss.
- Condition sampling: one pond per square sampled for environmental and water chemistry data.

## Point and coastal feature integration

- Inland Water and coastal features integrated into BH/PH framework with dedicated themes (Inland Water, Coastal Features) and cross-referencing with Vegetation and Physiography data.
- Coastal features include cliffs/slopes, supralittoral rock, dunes, strandline vegetation, saltmarsh, and related mosaics.

## Patches, mosaics, and non-specific attributes

- Mosaic option used when habitats are indistinguishable spatially or MMU constraints prevent discrete delineation; assigns percentage cover that sums to 100%.
- Non-specific primary attributes capture bare ground, signs of drainage, scattered trees/scrub, and related features across BH/PH contexts.

## Outputs and data quality

- Digital data products support UK Biodiversity Action Plans and long-term environmental surveillance.
- Emphasis on extent and change rather than pinpoint spatial precision; change status and habitat allocation are primary quality measures.
- Methodology updates and bug reporting via helpdesk/wiki support field teams.

## Practical notes for GIS specialists

- Expect large, multi-resolution datasets; harmonise data across 1990, 1998, and 2007 resolutions.
- GIS masks support PH distribution estimation; ensure masks align with the latest survey year and National Heritage/Museum guidance.
- Maintain thorough documentation of attribute schemas, field constraints, and the cost/benefit of mosaic vs discrete polygon delineation.
- Leverage Vegetation Key and Woodland Types/Features Key for consistent BH/PH assignment and woodland attribute recording.
- Ensure buffer-zone and management-status fields are consistently populated to support downstream governance and land-management analysis.

## WLF Unnatural shape: key attributes and editing guidance

- Height categories (e.g., <1 m, 1-2 m, 2-3 m, >3 m), base height, species composition, evidence of recent management, line of stumps, vertical gappiness, and margin widths.
- Staked trees and tree protectors attributes; natural vs unnatural shapes noted; up to four example illustrations are provided for coding and interpretation.
- Rules for handling "unnatural shape" vs "natural shape" within lines of woody features; if necessary, record natural shape and separate the unnaturally shaped segment.
- Editing tasks for lines include:
  - Create New Line: scale must be 1:5000 or better; minimum length 5 m; lines cannot cross themselves; one line per edit; new line starts with an Unsurveyed/Missing Data event.
  - Modify Line: edit vertices, endpoints, and shared nodes; preserve topology; disallow edits that create invalid line intersections.
  - Copy/Copy+ tools: use external features (e.g., OS Mastermap) to inform cut-line edits; manage multiple features in a single edit sketch.
  - Cut Line: define cut polygons along lines; preview lengths to cut and lengths to remain; multiple cuts per line allowed with validation.
  - Reshape Line: draw reshape guides to adjust lines; ensure edits intersect original line appropriately.
  - Shared Nodes: modify with care to avoid invalid intersections; shared node edits require precise selection.
- Validation rules: edits must maintain minimum linear feature length; end-node edits affect shared lines only via Shared Node Modify.

## Appendices and ancillary context

- Appendix 1: Using old Field Assessment Booklets (FABs); electronic FABs available for issue-specific habitat interpretation.
- CS2000 field themes and codes provide historical linkage (Agriculture/Natural Vegetation, Boundaries, Forestry, Structures, BH).
- Appendix 5: Girth-size rules for veteran trees (species-specific thresholds and classifications for notable/ancient status).
- Appendix 6: Squares with loops; describes loop-affected squares and data integrity concerns; procedures for correcting corrupted loop data.

## Output considerations for GIS practitioners

- Large, multi-resolution data demands careful harmonisation and consistent documentation.
- PH extent estimation relies on masks and yearly alignment with NHM/NVS guidance.
- Two-tier BH/PH assignment workflow supported by Vegetation Key and Woodland Types/Features Key ensures consistency across datasets.
- Buffer, management-status, and cross-theme attribute population are important for downstream governance and land-management analyses.