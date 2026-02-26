# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Provides a comprehensive, GIS-based framework for field mapping to monitor habitat extent and change across the UK.
- Shifts to digital data collection to enable time-series analysis for environmental monitoring and policy evaluation.
- Integrates multiple themes into a single digital map per 1 km square and supports UK-wide reporting, including Wales.
- Aims to produce repeatable, standardised outputs (habitat classifications, vegetation, water features, and built features) suitable for policy assessment and biodiversity planning.

## Habitat Classification Framework
- Two-tier classification: Broad Habitats (BH) and Priority Habitats (PH) nested within BHs.
- BH categories cover major habitat types (e.g., woodland, grassland, wetlands, urban, aquatic features); PHs are mapped where present and may require GIS masking for extents.
- Distinctions between unenclosed upland habitats (mapped in greater detail) and enclosed lowland habitats (edits to 1998 mappings).
- Vegetation Key and Woodland Key used to assign habitat type and classify woodland features (belt of trees, clumps, woodland/forest, hedges, lines).
- PHs and BHs guide both allocation and subsequent attribute data (species composition, structure, and physiography).

## Data Collection and Attributes
- Hierarchical data structure:
  - Polygon (area) level: BH/PH allocation, accuracy, and baseline PH/BH categorisation.
  - Component level: detailed attributes within each habitat (vegetation type, species, cover, habitat qualifiers).
- Vegetation attributes:
  - Primary and secondary attributes; indicator species; physiography.
  - Species lists with cover categories (<10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%); up to 4 species per polygon; minimum 2 species per vegetated polygon.
  - DBH data for trees; modal DBH for groups; woodland components include belts, clumps, and forests.
- Non-woody features (margins, edges, fences, hedges, gates, etc.) tracked with event-based attributes.
- Woodlands and related features:
  - Attributes include belts, clumps, woodland/forest, and management signs (grazing, fencing, underplanting, windthrow, etc.).
- Ponds and water features:
  - All ponds mapped; one survey pond per square selected for in-depth condition assessment; detailed pond mapping recorded via CS2007 Pond Mapping Recording Sheet.
  - Distinctions among ponds, ditches, canals, and standing waters; temporary ponds identifiable by signs such as wetland vegetation.
- Point and line features:
  - Points record discrete features (trees, standing water, ponds); lines capture woody linear features, fences, walls, hedges, etc.
  - Change-tracking and component-level editing supported for both points and lines.
- Minimum Mapping Unit (MMU):
  - MMU = 1/25 hectare (400 m2); polygons smaller than MMU not mapped unless part of a larger habitat boundary.
- Mosaic mapping:
  - When a boundary cannot be clearly delineated, mosaics recorded with component-level percentages summing to 100%.

## Digital Mapping System
- CS Surveyor: ArcMap-based extension for capturing/editing habitat data; ESRI-based platform.
- Features:
  - User login, data frame management, Landscape Feature Editing toolbox (Areas, Lines, Points).
  - Mandatory change tracking: surveyors must record genuine habitat change and correct past misallocations.
  - Workflow controls: Save Session, End Session, periodic portal uploads.
- Editing procedures:
  - Areas: allocate BH/PH, assess accuracy, justify changes; handle genuine changes, mis-recordings, and new baselines.
  - Components: manage multiple components per habitat with add/copy/delete functions.
  - Copy/Split/Merge/Modify/update operations for areas with detailed attribute management.
  - Points: add/move/delete; manage point components; special rules for veteran trees and buffers.
  - Lines: manage events along lines (fences, hedges, woody lines, walls); copy/split/merge lines; ensure spatial/topological integrity.
- Data quality:
  - Primary focus on extent and change accuracy rather than spatial precision.

## Pond-Specific Methodology
- Every pond must be mapped; all ponds documented on the CS2007 Pond Mapping Recording Sheet.
- One survey pond per square selected for in-depth environmental and water-chemistry assessment.
- Pond selections guided by Appendix 4 random-number table; adjustments in the field allowed for new ponds or access issues.
- Clear criteria for pond identification, boundary delineation, and distinguishing ponds from ditches, flushes, and dammed streams.

## Field Procedures and Practical Considerations
- Field governance:
  - Bug reporting and methodology updates via helpdesk or project wiki; monitor Latest News for changes.
- Practical mapping rules:
  - No MMU-based sub-unit mapping; map only areas above MMU.
  - Enclosed BH mapping uses 1998 data; unenclosed mapping uses an integration of 1990 CS1990 with CS2000 details for vegetation typing.
  - Orchard mapping: orchards recorded as PHs or as an attribute within woodland/scrub polygons or gardens, depending on context.
- Non-native species:
  - Monitor listed invasive species for potential habitat qualification or as separate notes.
- Buffer zones:
  - Record presence/absence of buffers around mapped features.

## Time-Series, Policy Relevance, and Outputs
- Outputs designed to support scrutiny of environmental health and policy performance over time.
- Datasets are stored and uploaded to portals to enable access, reuse, and broader monitoring.
- Standardised, repeatable GIS methods support both UK-wide reporting and country-level reporting (including Wales) with an emphasis on time-series consistency.
- Methodology aligns with UK Biodiversity Action Plans and provides a consistent baselining framework across time.

## Appendices and Reference Material
- Supporting material includes:
  - CS2000 and CS1990 coding schemes and mapping themes.
  - Pond Recording Sheets, code sheets, and random-number tables for pond selection.
  - Veteran tree guidelines and other practical aids.
  - Appendix 6 outlines squares with loops and data integrity considerations.
- Appendices emphasize compatibility with UK biodiversity planning and long-term baselining.

## Summary for Analysts Monitoring the Environment
- CS2007 establishes a rigorous, GIS-based, standardised framework for monitoring habitat extent and change across the UK, integrating BH and PH classifications with detailed vegetation, woodland, water, and built features.
- The workflow prioritises data quality, change detection, and time-series consistency, enabling robust environmental health assessment and policy evaluation.
- Outputs are designed to be clear (maps, charts, reports) and shareable, with underlying data stored in portals for accessibility and reuse.
- Analysts should expect to work with comprehensive attribute schemas, change-tracking requirements, and field procedures that emphasise extent, habitat change, and cross-temporal comparability, while remaining aware of data accessibility challenges for broader stakeholder use.