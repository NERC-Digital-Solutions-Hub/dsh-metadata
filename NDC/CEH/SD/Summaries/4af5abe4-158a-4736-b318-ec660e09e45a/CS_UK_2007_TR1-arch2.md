# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview and Aim
- Provides a comprehensive method for digitally mapping habitats and landscape features across 1 km squares as part of CS2007.
- Focuses on reporting land-cover change over time and reporting Broad Habitats (BH) and Priority Habitats (PH) to support biodiversity monitoring and policy reporting.
- Introduces PHs alongside BHs, with detailed habitat attributes in upland areas and Wales squares added to the survey.
- Emphasises a time-series data approach for consistent environmental health monitoring and policy performance assessment.

## Data Model and Outputs
- Outputs stored as a digital GIS dataset with polygons (areas), lines (linear features), and points (discrete items) representing BHs, PHs, vegetation types, and landscape features.
- Two core classification keys:
  - Vegetation Key: assigns primary/secondary habitats to BHs/PHs based on vegetation composition.
  - Key to Woodland Types/Features: classifies woody vegetation by canopy structure to support BH/PH attribution.
- Habitats organized into Broad Habitats (BH1–BH19, plus Mosaic) and Priority Habitats; includes non-specific and woodland-specific attributes to support mosaics and mixed areas.
- At polygon level, BH/PH allocations; at component level, detailed attributes (physiography, vegetation, species, cover, etc.) under themes like Agriculture/Natural Vegetation, Forestry, Inland Physiography, Coastal features.

## Methodology and Mapping Approach
- Time-series and monitoring goals drive the digital GIS model to preserve historical consistency while enabling new detail.
- Change documentation emphasised: REAL CHANGE vs ERROR CHANGE; note when a new PH baseline is applied.
- Data integration across CS datasets:
  - CS1990 merged with CS2000 data to improve PH identification and BH allocations.
  - Delineations for enclosed vs unenclosed upland influence BH definitions.
- Minimum mapping unit (MMU) is 1/25 hectare (400 m2); areas smaller than MMU are not mapped as polygons (lines may be used for sub-MMU features).
- Ponds and water bodies have dedicated procedures.

## Digital Mapping System and Data Capture
- CS Surveyor, a bespoke ArcMap extension, is used for data capture/editing within the CS GIS environment.
- Workflow: login, edit areas/lines/points, check/update attributes, save sessions to finalize edits.
- Key features:
  - Change recording is mandatory for habitat/feature edits.
  - Tools for editing polygons, lines, and points; supports copy, split, merge, and update of attributes.
  - Helpdesk and wiki-based fault logging for field issues.
- Spatial accuracy focus is on accurate representation of habitat extent and change over time, not just precise geometry.

## Mapping Procedures: Areas, Lines, and Points
- Areas (Polygons)
  - Primary BH/PH allocation using vegetation keys; align with BH 1998 or revised PH as applicable.
  - Mandatory checks: BH accuracy, change reason, visit status; clearly record real vs. erroneous changes.
  - MMU-based polygon creation; mosaics used when patches are indistinguishable or MMU-safe.
  - Two-tier attribute structure: polygon-level BH/PH and component-level attributes under themes (physiography, vegetation, agriculture).
- Copy, Split, Merge, Modify, and Update
  - Copy: transfer attributes from a source area to target areas (overwrites existing attributes).
  - Split: digitize boundary to create parts; update attributes accordingly.
  - Merge: combine areas with identical attributes; update reason for change.
  - Modify: adjust boundaries via topology tools; manage shared nodes carefully.
  - Update: replace several splits/merges with a single update polygon where suitable.
- Points (Woody features and discrete items)
  - Represent individual trees, scrub, or other features; one or more components per point.
  - Points must be created/moved/edited/deleted through controlled processes; deletions require a valid Reason for Change.
  - Buffer zones and buffer-related attributes may be recorded for landowner agreements.
- Linear features (Lines)
  - Implemented as lines with events (borders, hedges, fences, roads, etc.).
  - If a feature is wide enough to form an area, map as BH3: Boundaries and Linear Features.
  - Events along lines edited for length/location; copy attributes between lines; minimum length 5 m.
- Vegetation and species data
  - For each polygon, record at least two species (maximum four); link vegetated polygons to species data.
  - Record species cover percentages (e.g., <10%, 10–25%, etc.).
  - Woody vegetation described with canopy structure; may be subdivided into blocks if variation exists within the same area.

## Pond Mapping and Water Bodies
- Ponds are central; identify all ponds in a square and record on a CS2007 Pond Mapping Recording Sheet.
- One pond per square is selected for a detailed condition survey (the survey pond).
- Selection uses preselected ponds (on tablet) or random field process; pond creation may require re-selection.
- Pond identification considers boundaries, seasonal water presence, and differentiation from ditches/streams/bog features.
- Detailed pond attributes and reasons for pond loss/creation are specified; survey pond data passed to freshwater surveyors.

## Woodland and Broad Habitats
- BH typologies include BH1 Broadleaved Mixed and Yew Woodland, BH2 Coniferous Woodland, BH3 Boundaries/Linear Features, and BH4–BH19 covering Arable/Horticulture, various grasslands, heaths, wetlands, rivers, urban, supra-littoral habitats, and Mosaic BHs.
- For woodland components, capture primary attributes (e.g., Belt of Trees, Clump of Trees, Woodland/Forest) plus qualifiers (parkland, boundary lines), plus species, DBH, and canopy cover.
- Orchards noted as a potential PH inclusion; orchard attributes may appear with other habitat types.

## Change, Quality Assurance, and Data Access
- QA emphasis and documentation of change:
  - REAL CHANGE vs ERROR CHANGE; new baselines for PHs when applicable.
  - Integration with CS1990/CS2000 data to strengthen habitat attribution.
- Outputs support monitoring linked to policy frameworks (e.g., UK Biodiversity Action Plans) and enable consistent comparisons over time/space.
- Analysts encouraged to consider the value and reusability of underlying data; data should be stored and accessible via appropriate portals.
- Field-specific challenges acknowledged (e.g., evolving vegetation keys; ambiguous boundaries in unenclosed uplands) with guidance to improve consistency.

## Practicalities, Support, and Access
- Wales expansion: CS2007 adds 60 squares for country-level habitat reporting.
- CS Surveyor status: rapidly deployed; bugs possible; contact helpdesk and use wiki fault logging.
- Training and navigation: ArcMap/CS Surveyor guidance with step-by-step tasks for editing polygons/lines/points and saving/logging off.

## Practical Example: Landscape Feature Data (WLF) and Editing
- WLF Unnatural shape data fields:
  - Height categories (e.g., <1m, 1–2m, 2–3m, >3m, etc.)
  - Base height of canopy
  - Species composition (e.g., mixed, >50% hawthorn)
  - Evidence of recent management (no management, newly planted, cutting, laying/coppicing)
  - Line of stumps (Yes/No)
  - Vertical gappiness (percent breaks from canopy to ground)
  - Margins (Left/Right) with width categories
  - Staked trees (Yes/No)
  - Tree protectors (Yes/No)
  - Note: if >2m, ensure canopy species are trimmed or record natural shape
- Example imagery and coding rules illustrate various WLF shapes and management signs.
- Tablet line editing tasks include creating, modifying, copying, cutting, and reshaping lines with rules on scale, minimum lengths, shared nodes, and change reasons.

## Endnotes: Key Takeaways for Analysts Monitoring the Environment
- CS2007 provides a standardized, digital framework to map habitat extent, change, and BH/PH classifications across the UK, including Wales.
- Emphasises data consistency, time-series analysis, and accessibility of underlying data to support policy evaluation and environmental health monitoring.
- Combines detailed vegetation keys and woodland classifications with robust GIS tools to capture area, line, and point features, while enforcing MMU and clear change documentation.
- Explicit protocols for ponds and water bodies ensure comprehensive, repeatable data for future monitoring cycles.