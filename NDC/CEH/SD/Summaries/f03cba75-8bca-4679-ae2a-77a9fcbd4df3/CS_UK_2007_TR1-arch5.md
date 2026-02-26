# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Establishes a standards-based, digital workflow for field mapping of habitat and landscape features across 1 km squares, enabling measurement of habitat extent and change over time using Broad Habitats (BH) and Priority Habitats (PH).
- Supports biodiversity monitoring and policy through a consistent data model, classifications, and an integrated data collection system.

## Data model and classifications

- Uses Broad Habitats (BH) and Priority Habitats (PH) with nested structure; PHs provide finer, policy-relevant detail within BHs.
- Two main keys guide mapping:
  - Vegetation Key: assigns primary (and some secondary) attributes based on plant composition.
  - Key to Woodland Types/Features: classifies woody vegetation by canopy form (belt, clump, woodland/forest, hedges) and supports BH/PH assignment.
- Distinctions between enclosed (lowland) and unenclosed (upland) habitats influence attribute detail; PHs added post-survey via GIS masks to enable broad national estimates and rarity assessment.
- Emphasizes area-based mapping; mosaics allowed when boundaries are indistinct or below minimum mapping unit (MMU); PH extents constrained by post-survey GIS masks.

## Data collection system and workflow

- Field data captured with CS Surveyor, a custom ArcGIS extension, for field data capture, editing, and management.
- Change governance:
  - All habitat/feature changes are logged; surveyors must distinguish real ecological change from earlier mapping errors.
  - Changes require explicit Reason for Change; some PHs introduced as new baselines.
  - Updates tracked at polygon (area) and component (sub-area) levels; data entered via themed attribute editors.
- Data integrity and reproducibility:
  - Methodology updates published (Latest News); helpdesk support provided.
  - Baselines may come from earlier surveys (e.g., CS2000, CS1990, CS2007 inputs) and are refined for comparability.

## Minimum mapping unit and geometry rules

- MMU is 0.25 ha (400 m²) or a 20 m × 20 m square; features smaller than MMU are generally not mapped as separate units unless they define a boundary or are a linear/distinct boundary feature.
- When habitat changes, a new polygon is often created; otherwise, changes may be captured within the same polygon.
- PH extents post-survey are controlled by GIS masks; detailed vegetation attributes supplement site-specific context.

## Data entry and validation

- Mandatory fields are enforced; missing values block progression.
- Regular methodology updates and support channels are provided to ensure consistent data entry.

## Field operations by feature type

- Areas (polygons)
  - Attributes include BH/PH and change status; component-level attributes organized under thematic groups (Physiography, Agriculture/Natural Vegetation, Forestry, etc.).
  - Operations include copying area attributes, splitting/merging, boundary updates; species data required per habitat polygon (minimum 2, maximum 4).
- Points (individual landscape features; ≤ 20 × 20 m)
  - Used for trees, standing water, ponds, veteran trees, etc.; each point can have multiple components.
  - Edited via a dedicated Points tab; scale limited to 1:5000 for editing; buffers recorded as Yes/No per feature.
- Linear features (lines)
  - Features typically < 5 m wide; minimum length 20 m; lines can contain multiple events (e.g., fences with hedgerows).
  - Events have attributes (fence type, height, condition, margins); lines may be mapped as areas if width or complexity warrants.
  - Margins and belts recorded as primary attributes with canopy details.
- Woody vegetation and woodland designations
  - Woodland BHs can be Broad or Priority Habitats; primary and secondary attributes capture belt/clump/woodland/forest, species composition, and canopy cover.
  - Veteran trees: capped at 10 per square, with buffer zones, canopy percent, DBH, health; detailed how-to for documentation.
  - Orchard and parkland components may be recorded within woodland/arable contexts.
- Ponds and inland water features
  - Ponds mapped with defined attributes; one survey pond selected for in-depth condition data; boundaries delimited using vegetation/hydrological cues.
  - Inland water features include canals, rivers, lakes (natural/artificial), springs, etc., with attributes organized under Inland Water themes.
- Coastal and supra-littoral features
  - Includes maritime cliffs, shorelines, sand dunes, strandline veg, machair (post-survey attribution); coastal features mapped under coastal domain with height, habitat type, and related attributes.

## Non-native species and management notes

- Non-native taxa are flagged; surveyors record occurrences within habitats to support mapping accuracy and future management.

## Pond mapping specifics

- CS2007 Pond Mapping requires recording all ponds in a square; a survey pond is chosen for detailed assessment (randomly or preselected).
- Boundaries defined by winter water level indicators; temporary ponds recognized if they meet pond criteria (holding water for at least ~4 months).
- Ponds tracked with polygon ID, area, water presence, creation/creation reasons, and loss reasons; environmental/chemical data collected by freshwater specialists for survey ponds.

## Data governance, quality, and reporting

- Change management differentiates REAL changes from ERROR corrections; baselines from prior surveys are refined with CS2007 data for consistency.
- Spatial accuracy is balanced with accurate habitat representation; the dataset prioritizes habitat extent and change over pinpoint geographic precision.
- Documentation, support channels, and training materials (FABs, old field handbooks) facilitate reproducibility and cross-survey comparability.

## Practical reminders and constraints

- Ensure polygons meet MMU; avoid mapping multiple distinct habitats within a single polygon unless boundaries truly separate them.
- Woodland areas with continuous canopy typically map to Woodland BH/PH; other features map to BH3 or appropriate BHs.
- Use CS Surveyor and ArcMap for edits; save sessions regularly; ending a session discards unsaved changes.
- Post-survey analysis uses PH extents defined by GIS masks, while detailed vegetation attributes provide ecological context.

## Governance and sharing implications for data stewards

- A comprehensive, rules-based data model and standardized digital workflow support governance, data quality, and reproducibility.
- Role-based data entry, explicit change logs, and support processes help maintain data integrity and facilitate data sharing and longitudinal analyses for biodiversity action and policy monitoring.