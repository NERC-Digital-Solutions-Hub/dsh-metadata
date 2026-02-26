# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Aim and scope
- Establishes the CS2007 field mapping framework to report land cover change by Broad Habitats (BH) and Priority Habitats (PH) at country and UK levels.
- Builds on CS2000/CS1990 data; introduces digital data collection and a unified GIS model; emphasizes change reporting and correcting past allocations; supports time-series analyses for policy monitoring.

## Data model and habitat classification
- Two-tier habitat system: Broad Habitats (BH) and Priority Habitats (PH) nested within polygon/area data.
- Distinguishes enclosed (lowland) vs unenclosed (upland) habitats; unenclosed BHs require finer vegetation detail when possible.
- PHs nest within BHs; some PH extents rely on GIS masks/post-survey to support national estimates.
- Baselines updated (1998 for 2007 allocations; 1990 CS data integrated) to improve PH identification and consistency.
- Reporting framework supports UK Biodiversity Action Plans through consistent BH/PH attribution.

## Keys, attribution rules and classification
- Vegetation Key assigns polygons to BHs and PHs based on vegetation composition and indicators.
- Key to Woodland Types/Features classifies woody vegetation by canopy form (woodland, belt, line, clump, etc.) and sets thresholds (e.g., >25% canopy, >0.25 ha) for delineation.
- Woodland components (belt of trees, line of trees, clump, woodland/forest) are allocated to BH or PH with appropriate primary attributes and qualifiers.

## Data collection, MMU and field details
- Minimum Mappable Unit (MMU): 1/25 hectare (400 m2).
- Each land-habitats polygon must map to a BH or PH; mosaics allowed when multiple habitats share boundaries; extents must sum to 100%.
- Detailed vegetation and species data collected where possible; minimum two and up to four species per polygon.
- Non-vegetated features (bare ground, rock, physiographic features) recorded under relevant BHs/PHs.

## Digital mapping system and ArcMap integration
- CS Surveyor is an ArcMap extension enabling on-tablet data capture and GIS editing within a 1 km square.
- Surveyors log in, edit polygons/areas, and record changes; change recording is mandatory when editing.
- System supports creating, copying, splitting, merging, modifying areas; editing attributes at polygon and component levels; and logging change reasons (REAL change vs ERROR correction).
- Data quality prioritizes habitat extent/accuracy over pinpoint geographic precision; spatial checks available but secondary to habitat classification.

## Mapping areas, lines and points
- Areas: primary BH/PH attribution with component attributes (physiography, vegetation, species, cover).
- Lines: woody linear features (fences, hedges, walls, ditches) with events along lines; wide linear features may form from events ≥5 m.
- Points: discrete features (individual trees, standing water bodies, ponds); used for features smaller than MMU or discrete occurrences.
- Woody Linear Features (WLFs): categorized by natural vs hedged/managed shapes; include attributes such as DBH, canopy, margins, and management signs.

## Change detection, editing workflow and quality control
- Change status distinguishes REAL habitat change since 1998 from ERROR corrections of past misallocations.
- For unenclosed habitats, 1990 CS data inform 2007 attributes where 1998 data were lacking; for enclosed habitats, 1998 data drive baselines.
- Editing tools cover area attribute editing, copying attributes, splitting/merging areas, boundary updates, and post-edit attribute checks.
- Stop/Save workflow required to preserve edits; editing scales are typically <= 1:5000 for points/lines; MMU/topology guidance ensures data integrity.

## Pond mapping and surveying
- All ponds within a square must be identified and recorded on the CS2007 Pond Mapping Recording Sheet.
- One survey pond per square is selected for detailed condition assessment; selection can be preselected or randomized per Appendix procedures.
- Detailed pond attributes include area, water presence, boundary delineation, and reasons for pond loss/creation; pond data underpin freshwater condition assessments.

## Ponds, point features and habitat details
- Ponds are classified considering winter water level and surrounding vegetation; temporary ponds recorded if typically water for ≥4 months.
- Point features capture density and composition (e.g., veteran trees with detailed attributes).
- Advisory list of non-native species to record within habitats to aid monitoring of invasive threats.

## Outputs, accessibility and data handling
- Outputs designed for consistent cross-temporal monitoring and policy performance evaluation; enable scrutiny of environmental health and biodiversity outcomes over time.
- Data stored and uploaded to appropriate portals; emphasis on enabling access to underlying data used to produce outputs and on producing outputs suitable for UK biodiversity reporting.

## Key habitat descriptions (high-level BH/PH coverage)
- Broad Habitat 1–23 cover major vegetation and land-cover categories, including broadleaved mixed and yew woodland, coniferous woodland, boundaries and linear features, arable and horticultural, improved/neutral/calcareous/acid grasslands, bracken, heath, fen/marsh/swamp, bog, rivers/streams, standing open waters/canals, montane, inland rock, urban, various coastal and mosaic types, plus non-specific primary attributes for recording bare ground, margins, scattered trees, etc.

## Pond and water body identification guidance
- Guidelines differentiate ponds from ditches, streams, flushes, bogs, and other water bodies; include boundary delineation, winter water presence, and sampling considerations; ponds can be man-made or natural.

## Caveats, support and updates
- Helpdesk and Wiki-based fault logging available for CS Surveyor issues; methodology updates published in Latest News.
- Cross-reference with CS2000 and older field assessment materials for context and historical attribute coding.

## Relevance for environment analysts
- Provides a standardized, auditable framework for tracking habitat extent and change over time.
- Enables integration with other data sources via common BH/PH classifications.
- Supports policy performance monitoring through consistent time-series habitat data and change records, with accessible underlying data for scrutiny and reuse.