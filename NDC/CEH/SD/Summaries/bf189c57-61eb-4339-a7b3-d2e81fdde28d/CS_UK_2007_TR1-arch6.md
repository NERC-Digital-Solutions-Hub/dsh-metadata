# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Provides a guide for digital field mapping of habitats and landscape features in CS2007.
- Defines data model, workflows, quality controls, and outputs to produce self-describing data products for UK-wide biodiversity reporting.
- Geographic focus: Countryside Survey CS2007 across 1 km squares, emphasizing Broad Habitats (BH) and Priority Habitats (PH) with time-series potential and cross-agency sharing.

## Data Model
- Core feature types:
  - Areas (polygons) with BH/PH attribution and components.
  - Lines (linear features) with events and possible upgrades to wide linear features.
  - Points (features) for woody elements and other landscape features.
- Habitat framework:
  - Broad Habitats (BH) 1–23 with detailed subtypes; Priority Habitats (PH) nested within BHs.
  - Mosaic mapping when areas are indistinguishable or below minimum mapping unit (MMU).
- Classification keys:
  - Vegetation Key for BH/PH assignment based on plant community/species composition.
  - Woodland Types/Features Key for belts, clumps, lines, and other woody structures; supports PH/BH attribution at polygon and component levels.
- Attribute structure:
  - Polygon-level attributes (BH/PH, change status, habitat description).
  - Component-level attributes organized by themes (Inland Physiography, Inland Water, Coastal Features, Forestry, Agriculture/Natural Vegetation, etc.).

## Attribute Framework and Recording Guidance
- Data categories:
  - Broad/Priority Habitat attributes (area and component levels).
  - Vegetation indicators and species cover with specified recording limits.
  - Physiography, land use, forestry, margins, agricultural edges.
  - Non-native species notes and potential PH/BH modifiers (orchard, hedges, parkland).
- Recording rules:
  - Minimum 2 species per vegetated polygon; up to 4 species per polygon.
  - Species cover categories defined (e.g., <10% to 95–100%).
  - Woodland components: record DBH, species, canopy attributes; document vascular/bryophyte components as appropriate.
  - Margins and woody linear feature events recorded with lengths and widths.
- Data integrity:
  - Use theme-based editors and groupings to guide data entry; buffer zones captured where relevant.

## Mapping System, Workflows & Editing
- Core software: ArcMap with CS Surveyor extension.
- Workflow components:
  - User login, square loading, editing features at scale ≤ 1:5000.
  - Areas: creation, attribute copying, boundary edits, splits/merges; component management.
  - Points: addition, movement, deletion; component management; buffers.
  - Lines: event editing along lines; create, modify, cut, reshape, and shared-node operations.
- Data quality controls:
  - Mandatory recording of genuine habitat changes vs. error corrections; baseline comparisons against 1998 CS data.
  - MMU: minimum mappable unit is 1/25 hectare; sub-MMU features are lengthened or mosaicked.
  - Mosaic descriptions used when necessary to represent small or indistinguishable areas.

## Change Management and Data Quality
- Change assessment framework:
  - Distinguish genuine ecological change from corrections to prior data; use 1990 and 1998 data to adjudicate.
  - PH allocations may be introduced where appropriate; 1998 baseline generally governs attributes.
- Change decisions:
  - Prioritize 1998 baseline unless a real change or PH allocation justifies update.
  - Apply detailed rules for establishing a new baseline PH code.
- Precision and geometry:
  - MMU constraints ensure consistent mapping precision; mosaic approach used for spatially indistinguishable areas.

## Special Procedures and Key Features
- Ponds and Inland Water:
  - Map all ponds per square; random or preselected survey pond for detailed condition assessment.
  - Pond definitions and attributes documented on dedicated sheets; ponds inform PH/BH allocations and habitat status.
- WLF (Woodland/Landscape Features) Attributes:
  - Data fields include: Unnatural shape/line of stumps, Base height, Species composition, Evidence of management, Line of stumps, Vertical gappiness, Margin widths, Staked trees, Tree protectors.
  - Consistent coding and thresholds guide interpretation (e.g., modal height, gappiness, margin assessment).
- Woodland Keys and Metrics:
  - Primary attributes: belts, clumps, lines, woodlands; secondary attributes: species composition, canopy, DBH, management indicators.

## Outputs and Applications
- Alignment with UK Biodiversity Action Plans by BH/PH frameworks.
- Supports country- and UK-level reporting, as well as long-term time-series analyses.
- Digital GIS-based dataset designed for sharing across agencies; enables policy development and further analyses.

## Historical Context and Data Sources
- References to CS1990 and CS2000 legacy data and themes; mechanisms to integrate older field assessment materials (FABs) with CS2007 processes.
- Appendix materials illustrate coding schemes, historical parcel numbers, and data-sheet formats used to support consistent data capture and change tracking.

## Support, Help and Contacts
- CS Surveyor helpdesk: 01524 595812 or 0773869398; fault logging via project Wiki; updates via Latest News.
- Operational guidance:
  - Regularly save edits; follow documented change and baseline allocation rules.
  - Use preselected ponds where appropriate; consult methodology for complex change decisions.

## Illustrative Data Capture Example (WLF)
- Example fields and values demonstrate typical entries for woodland/landscape features, including height categories, canopy base, species composition, management evidence, stumps, vertical gappiness, margins, and protective measures.
- Visual aids and step-by-step editing tasks (e.g., creating, modifying, cutting, and reshaping lines) accompany practical guidance for field editors.