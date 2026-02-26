# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Purpose: Provide guidance for country-wide, time-series mapping of habitats to report Broad Habitats (BHs) and Priority Habitats (PHs), and to map change between surveys.
- Scope: Digital field mapping in 1 km squares, integrating vegetation, woody features, boundaries, arable land, water bodies, and other landscape elements; supports UK Biodiversity Action Plans and national statistics.
- Outputs: Standardised extents and change datasets at country and UK levels; data stored/uploaded to portals for accessibility and scrutiny.

## Data lifecycle and governance
- Data requirements: Define needed data from established sources; quality assurance, cleaning, transformation, and storage for reuse.
- Outputs alignment: Outputs track habitat change, enable time-series and cross-square comparisons, and support policy/monitoring needs.
- Data access: Emphasises enabling access to underlying data and combining datasets to increase value; datasets uploaded for scrutiny and analysis.

## Mapping model and data structures
- Digital mapping system: CS Surveyor (an ArcMap extension) with a “Countryside Survey” data frame and editing tools for Areas (polygons), Lines (features), and Points (features).
- Minimum mapping unit (MMU): 1/25 hectare; smaller units not mapped unless part of a larger unit or boundary delineation.
- Mapping components:
  - Areas: habitat polygons (BH/PH and patches).
  - Lines: woody and non-woody linear features (e.g., hedges, fences, ditches) with events along lines.
  - Points: discrete features (trees, ponds, water bodies, fences) with editable components.
- Change and QA: Surveyors distinguish genuine habitat change from errors using change status fields and event attributes.

## Habitat classification and keys
- Vegetation/woodland keys: assign primary (and secondary) attributes to BHs/PHs based on species composition; support PH nesting within BHs.
- Woodland keys: classify woody vegetation into canopy/structure-based categories and enable mosaic approaches when appropriate.
- BH classifications (polygon level; attributes recorded by theme): BH1–BH23 with detailed subdivisions (e.g., BH3 Boundaries and Linear Features; BH14 Standing Open Waters; BH17 Urban; BH21 Littoral Sediment; BH22 Sea; BH23 Mosaic).
- PH integration: PH mapping embedded within the BH framework; GIS masks bound upland/lowland extents post-survey.

## Ponds, water bodies and wetlands
- Pond mapping: All ponds in each square identified; basic attributes captured on pond mapping sheets; a subset designated as survey ponds for detailed condition surveys.
- Pond criteria: Standing water 25 m2 to 2 ha; winter water level defined; boundary identified by vegetation transitions or fixed features.
- Recording and sampling: Data entered on sheets and in CS Surveyor; pond data integrated with Inland Water themes and Coastal features where relevant.

## Methodology for mapping edits and feature management
- Editing tools and workflows:
  - Areas: edit attributes, copy attributes, split/merge, boundary edits, and area updates.
  - Points: multiple components per point; scale constraint (≤ 1:5000) for edits; veteran trees recorded (up to 10 per square, max 2 per species).
  - Lines (WLFs): differentiate natural lines from hedges; document belts, clumps, and individual trees; record margins and buffers.
- Attribute management: components allow multiple attributes per feature; copy attributes for consistency.
- Line editing: extensive tools for creating, modifying, cutting, reshaping, and following lines; supports shared nodes and multi-segment edits.
- Quality checks during edits: ensure edits reflect genuine field observations; mandatory reasons for change; minimum feature lengths enforced.
- Special editing operations:
  - Copy features from other layers (e.g., OS MasterMap) to improve accuracy.
  - Cut lines with editable polygons; reshape lines; delete lines with valid reasons for change.
  - Shared node modification to adjust topology without creating invalid intersections.
- Visit status and data integrity: mechanisms to identify unvisited linear features; procedures to handle data loops and corrupted event data.

## Data quality, access and governance
- Quality assurance: prioritize truthful representation of extent and change; ensure time-series integrity; ability to back-correct prior allocations.
- Access and reuse: encourage sharing underlying data and integrating with other datasets to increase value; datasets uploaded to portals for scrutiny and policy analysis.

## Operational details and support
- Software and guidance: CS Surveyor is an ArcMap extension; bug reporting via helpdesk; monitor methodology updates.
- Field guidance: surveyors must verify attributes against vegetation keys; maintain MMU; avoid mapping under 5 m width unless necessary; ensure vegetation units are assigned to BH/PH.
- Upland vs enclosed habitats: revised mapping detail for uplands to preserve robust time-series; use 1998 CS data where possible for enclosed uplands.
- Non-native species: record presence as qualifiers within habitat records for ecological risk analysis.

## Non-native and other notable considerations
- Non-native species presence should be recorded as qualifiers within habitat records to support ecological risk analyses.

## Endnotes and appendices (context for Analysts)
- The handbook provides exhaustive, standards-based procedures for field mapping, data capture, and subsequent editing to support auditable environmental monitoring across the UK.
- Appendices (referenced) cover detailed coding schemes, pond forms, veteran-tree considerations, loops in data, and historical CS2000 methodologies; they support rigorous, auditable data work and continuity with prior surveys.

## Practical takeaway for analysts monitoring the environment
- Use standardized BH/PH classifications and the CS Surveyor workflow to produce time-series habitat extents and change data.
- Rigorously QA data at square/time intervals and preserve backward compatibility to allow cross-survey comparisons.
- Leverage underlying data accessibility to integrate with other datasets for enhanced monitoring value.
- Apply detailed editing protocols for areas, lines, and points to ensure reproducibility and auditability of habitat change.
- Incorporate pond/water body data and inland/water features into broader ecological assessments.
- Be mindful of upland/enclosed habitat differences and non-native qualifiers in analyses and reporting.