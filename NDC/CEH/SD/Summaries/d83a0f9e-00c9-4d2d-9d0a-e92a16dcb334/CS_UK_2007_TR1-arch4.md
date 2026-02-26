# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Establishes methodology for CS2007 field mapping of Broad Habitats (BH) and Priority Habitats (PH) across the UK, including new areas in Wales.
- Focus on reporting change in land cover and landscape features and collecting detailed habitat data to support UK Biodiversity Action Plans.
- Introduces a digital GIS-based workflow (CS Surveyor) for data collection, editing, and updating within a unified soil-vegetation-structure dataset.

## Data model and classification
- BH comprises 19 categories (BH 1–BH 19); PHs are nested within or linked to BHs; require consistent reporting of both BHs and PHs.
- Distinguishes Enclosed (often mapped against 1998 data) vs Unenclosed habitats (upland/peaty systems) with different baseline considerations.
- Mosaic option allowed when BH/PH units cannot be separated spatially; component percentages must sum to 100%.
- GIS masks (e.g., Beech/Pine ranges) aid extent estimation and PH budgeting.

## Keys and classification tools
- Vegetation Key assigns areas to BHs/PHs using vegetation composition, canopy cover, and indicator species; primary/secondary attributes derive from floristic data.
- Woodland Key/types classify woody vegetation by canopy structure (woodland, belts, clumps, hedges, lines) to support BH/PH assignments.
- Woody attributes can be applied at polygon (BH/PH) or component level, enabling mosaics within a single BH.

## Digital mapping system and workflow
- CS Surveyor extension for ArcMap captures location and attributes for areas, lines, and points; recording change is mandatory.
- A dedicated map data frame and preset symbology guide surveyors; sessions logged via the CS Surveyor toolbox.
- Emphasizes habitat extent and change over precise coordinates; spatial accuracy is secondary to ecological representation.
- Three landscape feature types with dedicated editing tools: Areas (polygons), Lines (linear features), Points (points).

## Mapping rules, units, and data governance
- Minimum mapping unit (MMU) is 0.25 ha; features smaller than MMU are not mapped as areas unless part of a larger unit.
- Areas with continuous woodland map to BH/PH; habitat-type changes trigger new polygons; minor species changes may not.
- Change classifications:
  - REAL change: genuine habitat change since 1998.
  - ERROR change: correction of earlier misallocation.
  - NEW BASELINE: new subdivision or redefinition of habitat.
- Enclosed vs unenclosed habitats have distinct attribution rules, including PH attribution to polygons when BH remains unchanged.
- Change recording required for primary and secondary attributes; coding requires justifications (e.g., error, real change, new baseline).

## Ponds and standing water
- CS2007 Pond Mapping Recording Sheet used; one pond polygon per square for in-depth condition assessment.
- Selection criteria for survey ponds include standing water area (25 m2–2 ha) and water presence for at least four months.
- Recording includes pond polygon ID, area, water presence, reason for pond loss/creation, and notes; data passed to freshwater surveyors.

## Point features and veteran trees
- Points map individual trees, ponds, and other landscape elements; components can be edited, added, copied, or deleted.
- Buffer zones can be recorded for owner-buffered features.
- Veteran trees: up to 10 per square (max 2 per species); detailed attributes collected for first two veteran trees per species.

## Woody linear features and margins
- Woody Linear Features (WLFs) include hedges, lines of trees, belts, and other woody edges; classification distinguishes natural shape vs managed hedges.
- Recording includes DBH, canopy attributes, margins, and management features (staked trees, tree protectors, underplanting, windthrow, etc.).
- Margins documented with height and width and corresponding vegetation types.
- Rules for WLF editing emphasize maintaining topological integrity and field-accurate shapes.

## Editing tools and operations
- Areas: edit attributes, copy attributes, split/merge areas, modify boundaries, update areas, manage components.
- Lines: create, modify (including vertex edits and shared-node modifications), cut, reshape, copy features, and manage events along lines.
- Points: add/move/delete, copy attributes; new points initialized as Unsurveyed/Missing Data.
- Lines editing enforces minimum lengths, scale constraints (1:5000 or smaller), non-crossing rules, and proper handling of shared boundaries.

## Data attributes and themes
- Data organized into themes with attribute groups:
  - Inland Physiography
  - Inland Water
  - Coastal features
  - Agriculture/Natural Vegetation
  - Forestry
  - Structures
  - Recreation
  - Transport
- For each habitat, includes primary/secondary attributes, vegetation types, species lists (via referenced lists), cover percentages, and qualifiers.
- Notes cover non-native/invasive species, orchard mapping, and buffer-use indicators.

## Practical guidance and support
- Helpdesk and a Wiki available for fault logging; regular updates via Latest News.
- Tools aim to support time-series analysis, partner standardization, and cross-network collaboration.

## Implementation considerations for data leaders
- Emphasis on a consistent data model enabling reporting by BH/PH and tracking habitat change over time.
- Strong governance around change validation (REAL vs ERROR vs NEW BASELINE) to maintain data integrity across survey cycles.
- Comprehensive metadata and theme-wide standardization to facilitate data sharing with policy colleagues, researchers, and networked partners.
- Data system balances detailed ecological characterization (vegetation keys, species) with practical field constraints (MMU, time, logistics).
- Support for longitudinal analyses and governance across partner networks to improve data discoverability, update processes, and prioritization.

## Appendices and notes (high-level)
- CS2000/CS1990 context and legacy mapping schemas; evolution toward CS2007 BH/PH framework.
- Loops and data integrity notes (e.g., loops in Appendix 6 require special handling and deletion/reinstatement procedures).
- Veteran tree girth guidelines and species-specific considerations (Appendix 5) and data structure examples (Appendix 1–4) for reference.