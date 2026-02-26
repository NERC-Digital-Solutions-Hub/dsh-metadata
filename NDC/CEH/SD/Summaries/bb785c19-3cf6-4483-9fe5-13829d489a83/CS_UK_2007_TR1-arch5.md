# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Provides a comprehensive, auditable field-mapping workflow for habitats and landscape features (BH/PH) across 1 km squares.
- Aims to support UK biodiversity monitoring, enable time-series analyses, and produce reusable datasets for policy and research.
- Emphasises data governance, provenance, and interoperability to aid discovery and reuse.

## Data Model and Structure
- Three feature types: Areas (polygons), Lines (linear features), Points (point features).
- Broad Habitats (BH) and Priority Habitats (PH) are assigned at the polygon level; components carry detailed attributes.
- Minimum mapping unit (MMU) is 0.4 hectares; polygons smaller than MMU are treated as lines unless forming a valid sub-unit.
- Data capture supports change over time and cross-square comparability.

## Classification Keys and Attributes
- Vegetation Key: primary/secondary attributes and vegetation composition; incorporates NVC references where relevant.
- Woodland Key: distinguishes canopy structure and classifies features into Belt, Line, Wood/Forest, Clump, etc.; guides BH/PH assignment and habitat block subdivision.

## Digital Mapping System and Workflow
- CS Surveyor extension integrated with ArcMap; editing organized around Areas, Lines, and Points with dedicated toolkits.
- Change management: every feature has a Change status (Real Change, Error Change, No Change) with justification; critical for accurate BH/PH allocation and baseline updates.
- Editing rules emphasize correct habitat representation and change documentation; saves are required to persist edits.
- Line and boundary editing includes vertex manipulation, shared-node modification, cut, copy, reshape, and deletion workflows with scale and length constraints.

## Ponds, Wetlands, and Water Features
- Ponds are recorded on CS2007 Pond Mapping Recording Sheets; ponds have area, water presence, and reasons for loss/creation.
- Sampling and selection procedures for survey ponds; boundaries defined by winter water level and hydromorphological markers.
- Definitions distinguish ponds from ditches, flushes, and other water bodies within fen/marsh/bog contexts.

## Points and Woody Linear Features (WLFs)
- Points capture individual features (trees, shrubs, ponds) with potential buffers and multiple components; veteran trees have detailed attribute tracking.
- WLFs include hedges, belts, avenues, and lines of trees; distinguish natural shapes from managed features; record width, length, margins, and species composition.
- Events along lines (fences, walls, woody features) are georeferenced with start/end positions; management indicators (stakes, protectors, underplanting, windthrows) are recorded as attributes.

## Change Detection, Data Quality, and Governance
- Focal point is capturing REAL ecological change; erroneous prior allocations can be corrected as part of governance.
- GIS masks are used to delineate PH ranges post-survey to support extent consistency.
- Validation prioritizes habitat extent and change over pixel-perfect precision; cross-referencing with CS1990 and CS2000 ensures provenance and true ecological change.
- Post-survey governance includes methodology updates, field helpdesk support, and ongoing documentation.

## Metadata, Documentation, and Data Stewardship
- Emphasises standardization of BH/PH coding, vegetation and woodland attribute schemas, and non-native species buffers.
- Every edit requires a stated reason for change; changes are recorded at area and component levels.
- Thorough documentation for ponds and wetlands enables reproducibility and interoperability with other datasets.
- Clear update cycles and uptake of best practices via CS Surveyor Wiki and helpdesk support.

## Appendices and Tools
- Appendices provide FABs (Field Assessment Books), CS2000/CS1990 code schemas, pond recording sheets, preselected pond lists, and plotting sheets.
- Includes tools for pond selection, code sheets, and data sheets to support fieldwork and data capture.
- Additional materials cover veteran-tree girth guidelines and loops data (noted as data quality issues requiring specific procedures).

## Practical Governance for Data Stewards
- Enforce data standardization across BH/PH classifications and habitat components to ensure interoperability.
- Maintain a robust audit trail: document each edit with a rationale and preserve provenance across survey cycles.
- Establish and communicate update procedures, bug fixes, and methodology changes; provide user support and training resources.
- Ensure datasets are stored and structured to support reuse in biodiversity monitoring, policy analysis, and cross-dataset comparisons.

## Endnotes and Accessibility
- The Handbook facilitates data discovery and reuse by providing metadata-rich, governed field-mapping workflows.
- Acknowledges data-derived challenges (e.g., loops in Appendix 6) and prescribes corrective workflows to maintain data integrity.