# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Describes methodology, data model, and workflow for CS2007 habitat and landscape mapping across the UK.
- Shifts to digital map-based data collection (CS Surveyor on ArcMap) to capture Broad Habitats (BH), Priority Habitats (PH), changes over time, and vegetation/woodland attributes.
- Aims to support biodiversity monitoring and enable country-wide and UK-level analyses; outputs feed biodiversity reporting and policy monitoring.

## Data Model and Classification
- Areas (polygons) are primary mapping units with BH and, where applicable, PH; components describe internal mosaics within areas.
- Points and Lines capture smaller features (e.g., trees, hedges, streams); Lines support woody linear features (WLFs).
- PHs nest within BHs; PHs can override BHs in certain contexts; enclosure vs. unenclosed PHs distinguished.
- Vegetation Key, Key to Woodland Types/Features, and themes (Forestry, Agriculture/Natural Vegetation, etc.) drive BH/PH attribution and lineage.

## Mapping System and Data Capture
- CS Surveyor is a custom ArcMap extension used for field data capture; supports a 1 km square mapping workflow.
- Minimum mapping unit (MMU) is 1/25 ha (~400 m²); data entries must document sources and metadata for discoverability.

## Change, Baselines, and Extent
- Changes are recorded as REAL (genuine habitat change) or ERROR (correction of past errors).
- Baselines: unenclosed habitats reference 1990 CS1990 data; enclosed habitats reference 1998 data; PHs may override BHs where appropriate.
- When encountering a new habitat type, a new polygon is created; minor species changes within the same habitat type do not trigger new polygons.
- Post-survey GIS masks determine national extents for reporting PHs and support national estimates.

## Habitat, Woodland, and PH Integration
- BH/PH mapping guides consistent assignment across polygons and components; PHs map within BHs with detailed guidance on enclosure and nesting.
- Emphasis on recording multiple plant species per polygon (minimum two; up to four).

## Ponds Mapping
- All ponds within squares must be identified; a separate CS2007 Pond Mapping Recording Sheet is used.
- Survey pond: one pond per square selected for detailed condition survey (randomized selection among ponds in the square).
- Pond criteria: 25 m² to 2 ha, standing water for at least four months; can be temporary or artificial.
- Boundary determination uses winter water level, water marks, and visibility consistency to ensure comparability across surveys.

## Points, Woody Linear Features (WLFs), and Veteran Trees
- Points (trees, scrub, water bodies, veteran trees) recorded with components and attributes; buffer zones noted when present.
- Veteran trees documented with limits (e.g., up to 10 per square, up to two per species) and detailed attributes.
- WLFs captured with attributes such as height categories, canopy base height, species composition, evidence of management, line of stumps, vertical gappiness, and margin widths.
- Guidelines address recording away from curtilages and inclusion of recreation land with caveats.

## Linear Features and Events
- Linear features (width < 5 m) recorded as lines with events along their length (fences, hedges, woody features).
- Minimum line length: 20 m; lines must not cross themselves; events are tracked with attributes and reasons for change.
- Line editing includes creating, modifying, copying, cutting, and reshaping; shared nodes allow topology edits but require careful handling to avoid invalid intersections.
- Special procedures exist for handling unvisited lines (Visit Status) and corrupted loop data (delete-and-reinstate workflow).

## Posing Data and Outputs
- Emphasizes consistent, auditable datasets with clear metadata and data provenance linking to prior CS surveys.
- Outputs enable national biodiversity reporting, change detection, and habitat extent estimation; datasets support future scientific analysis and policy monitoring.

## Practical Guidance and Notes
- Field margins, set-aside areas, and agro-environment scheme features require careful BH/PH attribute application.
- Non-native/invasive species are recorded when present and can influence habitat polygon qualification.
- Orchard mapping interacts with agricultural datasets and curtilage classifications.
- GIS-based masks are applied post-survey to refine extent estimates and standardize national reporting.

## Legacy and Appendices
- References to CS2000 and older Field Assessment Booklets (FABs) for context and guidance; CS1990 and CS2000 mappings underpin baselines and historical changes.
- Appendix content covers coding schemes, veteran-tree girth guidelines, and squares with loop anomalies, illustrating data complexity and quality-control considerations.