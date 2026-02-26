# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Aimed at guiding field mapping and documentation of Countryside Survey 2007 habitats and landscape features across 1 km squares, using CS Surveyor (ArcMap extension) to collect areas, lines, and points and record change against mapped features.
- Focuses on producing habitat extent and change metrics (Broad Habitats and Priority Habitats) with baseline consistency for national reporting.

## Data Model and Classification

- Datasets are organized into Broad Habitats (BH) and Priority Habitats (PH); PH mappings nest within BHs and require GIS masking for extent estimation.
- Core classification keys:
  - Vegetation Key (BH/PH)
  - Woodland Types/Features Key (woody vegetation and related features)
- Minimum mapping unit and change rules:
  - MMU of 0.4 ha (1/25 ha); polygons smaller than MMU generally not mapped unless part of a larger habitat change.
  - A new polygon is created when habitat type changes; internal species composition changes may not require a new polygon unless the habitat type changes.
- Emphasis on mosaic mapping and detailed attribute schemes to support consistent national estimates.

## Spatial Data Model and Components

- Data captured as polygons (areas), lines (linear features), and points (point features).
- Areas carry BH/PH attributes plus multiple thematic attributes (Physiography, Vegetation, Agriculture/Natural Vegetation, Forestry, etc.).
- Components subdivide areas to support mosaics; woodland features described by primary attributes (e.g., Belt of Trees, Clump of Trees, Forest/Woodland) with possible secondary attributes (species, DBH, regeneration).
- Recording units (A = Area, L = Linear, P = Point) standardize data capture.
- Specific mapping rules govern MMU application, boundary delineation, and when to split/merge features.

## Data Collection System and Workflow

- CS Surveyor extension within ArcMap drives data capture:
  - Secure login to CS Surveyor DB; edit Areas, Lines, and Points without leaving the extension
  - Mandatory change logging for each mapped component; sessions saved to persist edits
- Editing operations include:
  - Area edits (copy, split, merge, modify, update)
  - Component edits (add/copy/delete components; edit primary/secondary attributes)
  - Line edits (line events; edit event attributes; copy events)
  - Point edits (add/edit points; manage buffers)
- Scale and data integrity:
  - Editing points and lines requires map scale 1:5000 or better
  - Focus on accurate habitat extent and change status; spatial precision is secondary to correct habitat classification
- Change management:
  - Record REAL (genuine change) or ERROR (correction)
  - Consider baselines (1990/1998/CS2000) when assessing change; document rationale for changes

## Ponds and Water Features

- Inland water mapping centers on ponds; all ponds in a square identified and described; one pond per square selected as the survey pond for detailed condition data.
- Pond definitions:
  - Standing water from 25 m2 to 2 ha, typically water-filled for at least 4 months/year
  - Temporary ponds recorded if they typically hold water
- Recording process:
  - Use CS2007 Pond Mapping Recording Sheet; record basic attributes; random preselected pond may be used as survey pond
  - Pond data references CS2000 or CS2007 field sheets; document loss/creation reasons
  - The survey pond is used for detailed environmental and water chemistry data collection

## Data Standards, Metadata, and Quality

- Mandatory and optional fields organized by thematic attribute groups; key attributes include:
  - Vegetation type, species, cover percentages; DBH for trees
  - BH/PH habitat codes; updated accuracy and reason-for-change fields
- Species recording:
  - Minimum two species per polygon; up to four can be recorded
  - Non-native species monitoring encouraged
- Documentation of methodology changes, masks, and basemaps to support consistent national estimates
- Emphasis on robust metadata, field definitions, data lineage, and change history

## Roles, Procedures, and Training

- Surveyors:
  - Map and verify habitat extent, change, and mosaic components
  - Use vegetation and woodland keys to classify vegetation and woody features
  - Record and justify changes with explicit reasons; adhere to MMU rules
  - Iteratively update attributes for polygons, components, lines, and points within a square
- Data governance and onboarding:
  - Standardized classifications, keys, and attribute schemes to ensure cross-team consistency
  - Support channels for CS Surveyor issues; training implied through detailed procedures

## Challenges and Risks for Data Stewards

- Complex and evolving BH/PH taxonomy and post-survey masking
- Timeliness and completeness of field data across many systems/formats
- Managing large datasets with detailed attribute requirements (e.g., multiple species per polygon, mosaic components)
- Reconciling incomplete user needs with strict data standards; legacy data from earlier surveys
- Field delineation challenges in unenclosed habitats; ensuring consistent PH allocations
- Potential CS Surveyor tool bugs; need for ongoing support and updates
- Appendix items (e.g., loops in linear features) indicate data integrity risks requiring specialized remediation

## Governance Implications and Recommendations

- Establish and enforce standard data models for BH/PH, woodland attributes, and linear/point features
- Maintain provenance across baselines (CS1990, CS1998, CS2000, CS2007); clearly document REAL vs ERROR changes and rationale
- Use GIS masks and published keys to deliver consistent national PH/BH extent estimates
- Implement robust metadata practices: field definitions, data lineage, and change history
- Ensure data quality checks, training, and escalation paths for tool issues
- Align data sharing and downstream use with reporting requirements (e.g., UK Biodiversity Action Plans) and preserve audit trails across datasets