# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and scope
- Defines methods for mapping Broad Habitats (BH) and Priority Habitats (PH) within Countryside Survey 2007.
- Moves to digital data collection and reporting of land cover change at country and UK levels.
- Maps change in habitats and landscape features; records PHs in addition to BHs; includes unenclosed upland and Wales squares.
- Emphasises time-series data, detailed habitat attributes, and alignment with UK biodiversity monitoring.

## Data model and mapping units
- Map to a 1 km grid using a digital GIS model; edits impact habitat type and attributes.
- Primary data units: Areas (polygons), Lines (width < 5 m), Points.
- Minimum mappable unit (MMU) = 400 m2; polygons below MMU mapped as lines.
- Areas store habitat type plus primary/secondary attributes; real changes or error corrections recorded.
- Lines represent linear features with multiple events along a single line.
- Points represent discrete features (e.g., trees, ponds, buildings) and can have multiple components.

## Habitat classifications
- Broad Habitats (BH) cover major landscape types; Priority Habitats (PH) nested within BHs and mapped post-survey.
- BH examples include woodland, grasslands, heaths, wetlands, rivers/streams, urban, etc.
- PHs constrained within BHs using GIS masks; mosaic polygons allowed when BH/PH separation is unclear; components must sum to 100%.

## Vegetation key and woodland features
- Vegetation Key assigns primary/secondary attributes to BHs/PHs based on species composition.
- Woodland Types/Features provide a decision tree for canopy/crown structure (trees vs. shrubs, belts, clumps, lines) and BH/PH attributes.
- Woodland attributes recorded at polygon and component levels; distinctions include belts, clumps, and lines.

## Using the CS Surveyor digital mapping system
- CS Surveyor is an ArcMap extension for data capture in each square.
- Surveyors select a square and edit areas, lines, and points within a preloaded data frame.
- Emphasis on recording change; spatial accuracy is secondary to correct habitat attribution and extent.
- Regular saves required; issues reported to helpdesk.

## Methodology for mapping polygons/habitat areas
- Focus on reporting change in land cover and landscape features rather than exact geometry.
- Enclosed vs unenclosed habitats; PH allocation rules differ accordingly.
- Old datasets (CS1990, CS1998, CS2000) supplement CS2007 for enhanced detail, especially in unenclosed uplands.
- Welsh squares include additional new squares; Scotland uses SNH masks for Blanket Bog; England/Wales masks may be applied post-survey.
- Unenclosed habitats may require back-correction of earlier maps; new squares and PHs require attribute validation.

## Editing area attributes and polygon/area management
- Polygon-level editing: assign Broad/Priority habitat; indicate accuracy; record change reason (REAL vs ERROR vs NEW BASELINE).
- Determine if changes reflect genuine habitat change, historical misallocation, or new subdivision.
- Visit status tracked (In progress, Completed, Refused access).
- MMU and polygon history influence which habitat code is applied.

## Component and area editing
- Areas can contain multiple components; components can be added, copied, or deleted.
- Copy Area: propagate attributes to multiple targets; overwrites target attributes.
- Split Areas: digitise split lines to create new polygons; manage minimum areas.
- Modify Area: topology-based boundary edits; careful handling of shared nodes.
- Update Areas: create new areas by combining splits/merges; can replace edits with a single update.
- Editing session lifecycle: Stop Editing saves; End Session discards.

## General rules for mapping areas
- Continuous woodland cover in a polygon -> map as woodland BH/PH.
- MMU = 400 m2; features smaller than MMU mapped as lines unless part of a larger MMU polygon.
- New polygons created when habitat type changes; internal species composition changes do not automatically create new polygons.
- Record at least two plant species per polygon; up to four (applies to agricultural/neutral/grassland types).

## Non-specific attributes, buffers, and non-native species
- Bare ground, shrub/tree reconnaissance, scattered trees, and other non-specific features can be allocated to BH/PH with relevant physiography attributes.
- Buffer zones: record Yes/No for landowner buffer management around features.
- Non-native species: record listed species within a habitat and MMU where applicable.

## Ponds and pond mapping
- All ponds in a square must be identified; data captured on CS2007 Pond Mapping Recording Sheet.
- A single pond per square is selected for a detailed condition assessment (survey pond).
- Ponds defined as standing water 25 m2 to 2 ha, typically with water for at least four months.
- Guidance on identifying temporary ponds, boundaries, ditches, dammed streams, and flushes.
- Distinguish ponds from other water bodies; record boundary and vegetation cues.
- If a pond from CS2000 no longer exists, indicate reason (L, I, B, O, U).
- Preselected ponds may be used if valid; otherwise selection via Appendix 4 and pond mapping sheet.
- Pond coordinates and attributes entered in the landscape editing toolbox as Pond sampled or Pond.

## Methodology for mapping point features
- Points cover individual features under themes like trees, waterbodies, buildings, etc.
- Scale requirement: map at 1:5000 or smaller to edit points; each point has at least one component.
- Points can be created, moved, deleted, or have components edited; buffering and veteran trees recorded where applicable.

## Methodology for mapping line features
- Linear features (<5 m width) mapped as lines with events; minimum length 20 m; gaps up to 20 m allowed.
- Some lines may be reclassified as areas if warranted (e.g., fence along a boundary).
- Line events record attributes (e.g., fence type, width, species, height) and can be copied.
- Margins, hedges, belts, ride/firebreaks, and other line-related features have defined attributes.

## Woody Linear Features (WLFs)
- Distinguish natural lines of trees/shrub lines from management-made hedges.
- Buffer zones and spacing influence classification; components include Belt of trees, Belt of shrubs, Clump of trees, Woody Linear Features.
- Canopy data and species composition recorded for components.

## Ponds: sampling and condition assessment
- After mapping all ponds, select the survey pond; pond data captured on CS2007 Pond Mapping Recording Sheet.
- Condition survey data collected separately by freshwater surveyors.

## Data integrity, provenance, and governance
- Emphasis on documenting data sources, lineage, and metadata for habitat and species attributes.
- Change status and reason codes help distinguish genuine ecological change from data corrections.
- Post-survey GIS masks constrain PH extent; national estimates adjusted accordingly.
- Analysts should expect multi-level data (polygon, component, event) with extensive attribute schemas.
- Ensure habitat codes align with Vegetation Key and Woodland Key; use mosaic where needed.
- Maintain data provenance and make datasets discoverable with metadata for reproducibility.
- Be prepared to navigate data access and IT constraints described for field deployments.

## Practical guidance for analysts
- Manage data at multiple levels (polygon, component, event) with rich attribute schemas.
- Align habitat codes with Vegetation Key and Woodland Key; apply mosaic approach when necessary.
- Track provenance; keep datasets discoverable with metadata for reproducibility.
- Anticipate data access limitations and IT constraints in field deployments; plan accordingly.

## Appendices and references (conceptual overview)
- Contains codes, species cover categories, and field guidance for pond sheets, woodland types, and vegetation classifications.
- Details for integrating old datasets (CS1990, CS1998, CS2000) and GIS mask applications for habitat extent estimation.
- Includes sections on loops, veteran tree girth guidelines, and square-specific loop data (Appendix 6).