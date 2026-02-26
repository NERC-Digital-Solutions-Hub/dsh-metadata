# CS Technical Report No.1/07: Field Mapping Handbook v1.0

## Overview
- Provides a standardized methodology for mapping habitats, landscape features, and associated attributes for Countryside Survey 2007 (CS2007).
- Aims to produce consistent, publishable data with traceability, documentation of changes, and data governance considerations.
- Supports reporting and scientific analyses through standardized data models, workflows, and quality controls.

## Data model and classifications
- Broad Habitats (BH) and Priority Habitats (PH): hierarchical classification with nested attributes; PHs map within BHs when applicable.
- Woodland types/features: two keys (Woodland Type/Feature and Field-level attributes) enable consistent classification of belts, clumps, lines, and canopy components; special provisions for buffers, veteran trees, DBH, species, and cover.
- Other attributes: non-woody/woody linear features, non-native/invasive species, and ponds/standing waters mapped with detailed protocols.
- Mapping units and granularity: MMU of 1/25 ha for areas, minimum lengths for lines (20 m) and points; mosaics allowed below MMU with explicit percentage compositions; components within an area must sum to 100%.

## Data capture workflow and tools
- CS Surveyor software integrated into ArcMap: login, load square, edit point/line/polygon features with dedicated toolboxes; standard symbology applied.
- Data capture lifecycle: areas (polygons), lines (linear features), and points (sites) edited with attribution and change logging; a helpdesk supports CS Surveyor issues.
- Emphasis on reproducibility and documentation of edits through structured attribute keys and vegetation keys.

## Editing operations and change management
- Polygon-level attributes: area, BH/PH assignment, accuracy, reason for change, visit status; changes recorded as REAL (genuine) or ERROR (legacy data correction).
- Area editing: copy, split, merge, modify boundaries, and perform updates; new baselines for PH/BH classifications may be applied.
- Line editing: record events (e.g., fences, hedges, ditches); manage multi-event lines; vertex-level edits; handling of shared nodes; cut and reshape operations; ensure minimum lengths and topology integrity.
- Shared nodes: modify via shared-node tool to move junctions without creating invalid intersections.
- Delete/reshape rules: deletions require valid reasons for change; lines must remain compliant with minimum lengths; reshape operations require proper intersecting edits.
- Copy/Cut tools: reuse features from other layers to improve edit accuracy; multiple cuts allowed per line with validation.
- Points: new points must be within the square, at scale ≤ 1:5000, and not closer than 5 m to existing points; buffer and related attributes applied as needed.
- Ponds: identify all ponds per square; select a survey pond for detailed condition assessment; record pond attributes, presence/absence, losses/creations, and coordinate with freshwater surveyors.

## Pond mapping and survey details
- Pond Mapping Recording Sheet: complete per square; record all ponds, identify survey pond, and coordinate with Pond Conservation and freshwater surveyors.
- Boundaries and winter water level delineation are defined; ponds recorded even if no longer present with stated reasons (land drainage, infilling, built over, etc.).
- Selection of survey pond may rely on preselected lists or randomization; documentation required if the preselected pond cannot be used.

## Data quality, standards, and governance
- Standardization: Vegetation Key and Key to Woodland Types/Features guide consistent BH/PH allocations; two separate keys ensure coherent habitat assignment.
- Validation: mandatory reason for change; classify as REAL or ERROR; minimum data requirements (e.g., two species per polygon) to ensure robust attribute data.
- Temporal baselines: CS1990/CS1998/CS2000 data underpin baselines for unenclosed vs enclosed habitats; GIS masks post-survey constrain PH extents and supports national estimates.
- Documentation and support: dedicated helpdesk; methodology updates published in Latest News; thorough documentation of field mapping workflows and data edits.
- Provenance and reproducibility: changes are traceable through structured metadata and change logs; appendices provide codesheets and historical tooling.

## Practical considerations and challenges
- Incomplete understanding of user needs for dataset discovery and usage; alignment of dataset publications with user requirements recommended.
- Data collection across diverse systems/formats; reliance on standardized keys and consistent attribute codes to enable interoperability.
- Handling complex habitat delineations, mosaics, and legacy data; integration of old datasets (CS1990/1998) with modern workflows.
- Large datasets and non-interoperable legacy systems present ongoing interoperability and transfer challenges.

## Documentation, references, and supporting materials
- Vegetation Key and Field mapping methodology: references for NVC communities, woodland types, and detailed habitat mappings.
- Field mapping methodology: rules for subdividing/aggregating areas, mosaics, and attribute assignments.
- Appendix references (CS2000/1990 tools, pond survey sheets, random-number tables for pond selection) and FAB/FAB-like materials for reference.
- Supplementary materials available in CS2007 FAB folder (code sheets, plot maps, photos, ownership maps) and CS2000-era references for context.

## Appendices and notable details
- Appendix content covers veteran-tree guidance, pond mapping sheets, and loop-related data issues (with recommended remediation steps).
- Loops in square data may require specific de-correlation and deletion/reinstatement processes to restore data integrity.
- Includes historical codesheets and field assessment tools to support interpretation and data aliasing if needed.