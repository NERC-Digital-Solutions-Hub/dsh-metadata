# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Defines methodology for mapping habitats, landscape features, and related attributes for Countryside Survey 2007 (CS2007).
- Aims to report land cover change by Broad Habitats (BHs) and Priority Habitats (PHs) at country and UK levels.
- Introduces digital data collection (CS Surveyor) and expands detail for unenclosed upland habitats; adds Wales squares; emphasizes time-series surveillance.

## Data model and mapping structure
- Mapping units within each 1 km square include polygons/areas, lines (linear features), and points (point features).
- Minimum mapping unit (MMU) is 1/25 hectare (400 m2); features smaller than MMU are generally not mapped unless part of a larger boundary.
- Five prior themes (forestry, agriculture/natural vegetation, boundaries, structures, physiography) are integrated into a single digital map per square.
- Outputs focus on extent and change of BHs/PHs, with detailed habitat and species attributes where available.

## Habitat classification and keys
- Two core keys:
  - Vegetation Key: assigns primary/secondary attributes and allocates polygons to BHs/PHs based on vegetation composition.
  - Key to Woodland Types/Features: classifies woody vegetation (belt/clump/hedges/lines, etc.) to ensure correct BH/PH assignments and to distinguish woodland from non-woodland features.
- Woodland approach: canopy >25% and alignment with woodland categories leads to BH/PH mapping; can be subdivided into blocks if composition differs.
- BHs/PHs are selected at the polygon level; component-level attributes are recorded under Forestry, Agriculture/Natural Vegetation, Inland Physiography, etc.
- Mosaic mapping is used when habitats cannot be precisely delimited; polygons contain multiple components with specified percentage covers summing to 100%.

## Woodland types and attributes
- Broad Habitat 1: Broadleaved Mixed and Yew Woodland (incl. certain beech/yew/coppice/parkland associations; references to NVC communities).
- Broad Habitat 2: Coniferous Woodland (non-native pine; includes native pine woodland and mixed conifers).
- Broad Habitats 3–19 cover boundaries and linear features, arable/horticultural habitats, grasses, moorland, bog/fen/marsh/swamp, rivers/streams, standing waters, montane, inland rock, urban, supra-littoral habitats, dunes, littoral sediments, sea, and mosaics.
- Woodland components include primary attributes (belt/clump/woodland/forest, line features) and secondary attributes; buffers recorded for management.

## Digital mapping system and workflow
- CS Surveyor extension for ArcMap used to view/edit features; field support provided.
- Field workflow emphasizes recording genuine change vs mapping errors and ensuring consistency with BH/PH keys.
- Editing modes:
  - Area editing: modify polygon attributes, copy/split/merge areas, update shapes.
  - Line editing: edit linear feature events (fences, hedges, woody belts) and their attributes.
  - Point editing: update attributes of point features (trees, ponds, etc.), manage components and buffers.
- Data integrity rules:
  - Changes require reason codes (real change, error correction, new baseline, etc.).
  - Habitat assignment is prioritized over precise geometry; geometry may be adjusted to reflect field conditions.
  - Save sessions frequently; end sessions to commit changes.

## Change determination and rules
- Distinguish REAL change from ERROR (misclassification) changes.
- Enenclosed habitats rely on CS1998 data where possible; unenclosed habitats combine CS1990 data with CS2000.
- When habitat type changes, create a new polygon; if species composition changes but habitat type remains, a new polygon may not be needed.
- Component-level attributes can be added/copied/deleted; multiple components may share a primary attribute; area-level editing requires at least one component per area.

## Pond mapping and surveying
- All ponds in each square must be identified; basic attributes recorded on the CS2007 Pond Mapping Recording Sheet.
- One pond per square (the survey pond) is selected for detailed condition assessment (random selection, with preselected ponds possible).
- Selection considers: new vs existing ponds, access, and preselected pond status; re-evaluate if ponds are added during mapping.
- Recorded pond attributes include polygon ID, area, water presence, reasons for loss/creation, and notes; survey ponds receive detailed, sampled freshwater assessment.

## Point features and specimen-level details
- Points represent features across themes; map scale must be 1:5000 or better for editing.
- Points may contain multiple components; veteran trees may be recorded (up to 2 per species per square) with detailed attributes (DBH, buffer zones, epiphytic cover, etc.).
- Buffer zones and defensive features (stakes, tree protectors) captured as attributes.
- Tree and shrub features include individuals, clumps, scattered trees, and scrub patches with species, cover, and DBH.

## Linear features
- Linear features include woody and non-woody lines with events (fences, hedges, woody belts).
- Minimum length 20 m; maximum width 5 m; wider/larger features mapped as a wide linear feature area.
- Events along lines require attributes; attribute copying between lines supported; new lines can be digitized or created from external polygon layers.

## Non-specific attributes and management notes
- Attributes such as bare ground, margins, roads/tracks, ditches, and signs of drainage apply across BHs/PHs.
- Field margins may be mapped as separate habitat components if they exceed MMU.
- Orchard guidance: identify traditional orchards and treat as an additional attribute; curtilages around houses may use Garden/Ground with trees plus Orchard as an attribute.

## Outputs and data usability
- Emphasizes creation of discoverable datasets with metadata and clear provenance.
- Supports rigorous QA/QC: traceable changes, standardized attribute codes, explicit change reasons.
- Data feed into national reporting for UK Biodiversity Action Plans and inform future policy; focus on temporal change tracking and cross-square comparability.
- Documentation references CS2000/1990 contexts and provides electronic access to Field Assessment Books and related codesheets for interpretation.

## Appendices and context
- Appendix materials describe CS1990/CS2000 themes, coding sheets, and example maps/data structures.
- Includes guidelines for veteran-tree girth assessments, loops in square data, and selection procedures for survey ponds.
- Contains references to field forms, codesheets, and data handling procedures to support consistent data capture and analysis.