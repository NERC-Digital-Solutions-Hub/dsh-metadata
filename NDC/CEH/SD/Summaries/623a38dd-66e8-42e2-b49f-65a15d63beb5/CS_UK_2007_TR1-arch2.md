# CS Technical Report No.1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Establishes a nationwide, time-series framework for mapping environmental habitat types and landscape features in 1 km squares.
- Uses standardized Broad Habitats (BH) and Priority Habitats (PH) for consistent reporting.
- Shifts to a digital GIS-based workflow (CS Surveyor on ArcMap) to record habitat extents, changes, and attributes for country- and UK-level biodiversity reporting.
- Aims to support data quality, policy analysis, and long-term monitoring of environmental health.

## Data Framework and Classification
- Two-tier habitat framework:
  - Broad Habitats (BH): polygon-level classifications describing broad land-cover units.
  - Priority Habitats (PH): finer or nested habitat units within BHs.
- Enclosed vs. unenclosed habitats:
  - Enclosed habitats edited from older maps with potential PH/BH reassignment.
  - Unenclosed habitats require more complex integration of historical detail to improve vegetation differentiation.
- Vegetation Key and Woodland Key:
  - Vegetation Key links plant communities to BH/PH allocations with primary/secondary attributes (e.g., canopy cover, indicator species, NVC associations).
  - Woodland Types/Features Key classifies woody vegetation by canopy structure and supports PH/BH attribution for woodland elements.
- Components and attributes:
  - Areas (polygons), Lines (linear features), Points (woody features, ponds, etc.).
  - Each area may include multiple components; attributes organized under themes such as Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, Recreation, and Transport.

## Data Collection and Field Methods
- Square-based survey design:
  - Map habitat and landscape features for each 1 km square to build a national time-series dataset.
  - Emphasize recording genuine ecological change and corrections to earlier misclassifications.
- Change recording:
  - Distinguishes REAL change from ERROR change; unenclosed habitat data may require careful interpretation due to older source data.
- Reporting and outputs:
  - Outputs are organized by BH and PH to support UK Biodiversity Action Plans, including statistical estimation for rare PHs.
- Distinctions:
  - Upland vs. lowland; unenclosed vs. enclosed habitats, with varying attribute detail and size thresholds.

## Data Capture Schemas and Keys
- Vegetation Key:
  - Assigns primary and selected secondary attributes to polygons to support BH/PH allocation and nesting of PH within BH.
- Key to Woodland Types/Features:
  - Classifies woody structures (belt of trees, clump, line, woodland/forest, etc.) and supports PH/BH attribution with canopy and spatial pattern qualifiers.
- Non-native species:
  - Provides a list to record non-native species present within habitats.
- Habitat-specific attribute templates:
  - For each BH/PH, primary attributes and qualifiers, vegetation types, and species cover categories (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).

## Digital Mapping System and Workflow (CS Surveyor)
- CS Surveyor extension for ArcMap:
  - Central interface for viewing/editing areas (polygons), lines (linear features), and points (woody features, ponds).
  - Pre-set symbology, data frame management, and a dedicated workflow for habitat mapping, change assessment, and attribute editing.
- Editing workflow (Areas, Lines, Points):
  - Areas: edit/copy/merge/split attributes; update boundaries; manage multi-component areas.
  - Lines: edit events (fences, hedges, woody linear features); add/copy/delete, set lengths, adjust margins/attributes.
  - Points: edit attributes; create/move/delete points; handle multiple components per point.
- Mapping rules and MMU:
  - Minimum Mapping Unit (MMU) is 1/25 hectare (0.04 ha); smaller units are not mapped separately unless part of a larger polygon.
  - New polygons triggered by changes in habitat type; minor species changes within the same habitat typically do not warrant new polygons.
- Pond mapping (CS2007):
  - Every pond mapped; one pond per square selected as survey pond for detailed condition assessment (random selection from ponds in the square).
  - Pond criteria include size (25 m2 to 2 ha) and winter water presence.
  - Detailed pond attributes collected for the survey pond; standard pond sheets capture basic attributes for all ponds.
- Editing rules and quality controls:
  - Escalated procedures for complex edits (e.g., line intersections, shared nodes, minimum lengths).
  - Procedures for recording changes with valid reasons and maintaining data integrity during edits.

## Applications and Outputs
- Time-series monitoring:
  - Enables longitudinal analyses of habitat extent and change to evaluate policy interventions and biodiversity outcomes.
- UK Biodiversity Action Plans alignment:
  - Outputs structured by BH/PH with extrapolation methods for rare PHs to support national reporting.
- Data accessibility and reuse:
  - Emphasizes open access to underlying data and metadata to promote verification, secondary analyses, and broader data integration.
  - Encourages combining CS datasets with other relevant data sources to increase data value beyond single-use outputs.

## Challenges and Considerations for Analysts
- Value enhancement and data access:
  - Linking datasets across themes (forestry, agriculture, boundaries, structures, physiography) to create richer, cross-cutting environmental datasets.
  - Providing access to underlying data and metadata to support scrutiny and reuse.
- Change interpretation:
  - Distinguishing genuine ecological change from data processing or historic misclassification, especially in unenclosed uplands.
  - Integrating historical datasets (CS1990, CS1998, CS2000) to improve habitat delineation and PH allocations.
- Data quality and standardization:
  - Maintaining consistent field keys, attribute definitions, and MMU thresholds to ensure comparability over time and across regions.

## Practical Resources and Appendices
- Appendices and codesheets provide coding schemes, species lists, and mapping rules (e.g., CS2000 codes, pond recording forms, random number sheets).
- Field and pond-specific sheets accompany the methodology (e.g., CS2007 Pond Mapping Recording Sheet).
- Historical context and data capture evolution from CS1990 and CS2000 illustrate the progression toward standardized BH/PH mapping and time-series reporting.