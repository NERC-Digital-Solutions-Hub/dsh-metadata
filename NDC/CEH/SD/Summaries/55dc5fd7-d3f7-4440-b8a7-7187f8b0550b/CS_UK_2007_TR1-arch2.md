# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Provides a digital, time-series framework to map Broad Habitats (BH) and Priority Habitats (PH) across 1 km squares, enabling monitoring of habitat extent and change for biodiversity policy.
- Integrates prior CS iterations (CS1990, CS2000) and adds detail for unenclosed upland habitats, PHs, and country-wide continuity.

## Aims, Scope and Data Philosophy

- Map changes in land cover and landscape features by BH/PH to support biodiversity action plans and policy monitoring.
- Build a country-wide, digitally collected time series of disaggregated environmental surveillance data for scientific and policy use.
- Emphasize consistent outputs (reports, maps, charts) and longitudinal comparability over spatial precision alone.

## Data Model and Workflow

- Digital GIS-based mapping system (CS Surveyor) embedded in ArcMap; surveyors edit a single map per square.
- Five mapped themes consolidated into a unified feature map: forestry, agriculture/natural vegetation, boundaries/structures, physiography, and others.
- Mapping units: Areas (polygons), Lines (linear features), Points (point features); MMU for areas is 1/25 hectare (400 m²).
- Time-series focus: capture genuine ecological change and correct prior misallocations; Wales adds detail to maintain continuity.
- Post-survey GIS masking supports country- and UK-level extent estimates.

## Habitat Classification and Allocation

- BH and PH assigned at polygon (area) level; component-level attributes refine woodland/habitat structure.
- Detailed vegetation keys and criteria cover upland unenclosed and enclosed lowland habitats; mosaic mapping allows percentage shares for unclear boundaries.
- Tools include vegetation keys and a Woodland Types/Features key to distinguish woodland vs. woody features.
- Change coding: REAL change (new habitat) vs. ERROR change (correcting prior allocation).

## Woodland and Woody Linear Features (WLFs)

- Woodland BH/PH attribution possible at polygon and component levels; woody features include belts, clumps, lines, belts, hedges, and woodland patches.
- Attributes cover canopy characteristics, species composition, diameter at breast height (DBH), line width, and management (grazing, fencing, staked trees, etc.).
- WLFs include hedges and linear tree features; distinction between natural vs. managed forms is recorded.

## The Digital Mapping System (CS Surveyor)

- ArcMap extension; surveyors login and edit the current square’s data.
- Enforces change recording (REAL vs. ERROR) and guides attribute assignment via keys and habitat descriptions.
- Editing toolkit for Areas, Lines, and Points; includes helpdesk support and session save reminders.

## Mapping Areas, Lines and Points: Key Rules

- Areas: must allocate BH/PH attributes; accuracy and change reason codes required. Components capture physiology, vegetation, and other themes; multiple components can share a primary attribute.
- Lines: minimum length 5.0 m; record events (fences, hedges, woody lines); editing features to insert, delete, move vertices; handles shared nodes via Shared Node Modify.
- Points: represent individual landscape elements (trees, ponds, etc.); record species, DBH when possible, provenance, buffers, veteran trees (up to 10 per square, max 2 per species); edit at scales up to 1:5000.
- Line editing operations include Create, Modify, Cut, Delete, Reshape; sharing nodes, alignment with boundaries, and maintaining topology constraints are emphasized.
- Copy tool lets surveyors reuse existing landscape area boundaries to refine line edits; multiple lines can be cut in one edit.
- Scale constraint: map must be 1:5000 or finer for line edits; lines cannot cross themselves; shared nodes ensure consistent topology.

## Pond Mapping Protocol

- Inland Water BH heavily emphasizes ponds; map all ponds in a square and collect basic attributes.
- Each square selects a survey pond for a detailed condition survey; selection uses CS2000 data and Appendix 4 randomization if needed.
- Pond attributes include boundary delineation, water presence, area, and reasons for pond loss/creation; fen/marsh/bog contexts may affect boundaries.
- A dedicated CS2007 Pond Mapping Recording Sheet is used to capture pond data before selecting the survey pond.

## Non-native Species, Buffers and Orchards

- Record notable non-native species within habitats; these records can influence habitat qualification.
- Capture presence or absence of buffer zones around mapped features.
- Orchards: emphasized as PH attributes within Agriculture/Crops; document Orchard as a secondary/associated attribute where relevant.

## Quality, Standards and Outputs

- Prioritize standardized data outputs for long-term monitoring of environmental health and policy performance.
- Emphasize accurate habitat extent and change representation over pure spatial precision; geometry can be adjusted when necessary.
- Data are intended for storage in appropriate data portals and for dissemination to support monitoring and policy objectives.

## Practical Guidance for Analysts

- Start habitat classification with BH/PH framework, then apply vegetation and woodland keys for refinement.
- Use MMU and mosaic concepts to decide on creating new polygons or merging with existing units.
- Record two to four species per habitat where possible; ensure at least two species per polygon.
- Regularly save editing sessions; apply REAL vs. ERROR coding to document changes.
- Follow the pond mapping protocol in CS2007 and use the Pond Mapping Recording Sheet for pond-level data.

## Data Integrity and Loops (Appendix Reference)

- In some squares, data loops exist and are corrupted; surveyors must follow a defined procedure to delete and re-create affected linear features, then re-establish the correct geometry and attributes.

## Context and Background

- CS2000 and earlier field assessment practices provided historical codes and parcel-based data for features; this handbook builds on those foundations with digital, standardized coding schemes and time-series capabilities.

- The document concludes with legal and attribution notices regarding NERC copyright and distribution for research and internal organizational use.