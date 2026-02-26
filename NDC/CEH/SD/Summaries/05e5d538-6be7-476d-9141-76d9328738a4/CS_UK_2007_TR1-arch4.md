# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Digital field-mapping framework for Countryside Survey 2007 (CS2007) to map Broad Habitats (BH) and Priority Habitats (PH) across 1 km squares.
- Integrates five themes into a single GIS model to report habitat change over time at country/UK scales.
- Aims to support biodiversity monitoring and policy reporting through consistent, detailed habitat and landscape feature data.

## Data Model and Classifications
- Two main keys drive habitat assignment:
  - Vegetation Key: primary/secondary BH and PH attributes based on vegetation composition.
  - Key to Woodland Types/Features: classifies woody vegetation by canopy form (woodland, belts, clumps, lines, scattered trees) and assigns BH/PH attributes.
- Broad Habitats (BH): diverse classes (e.g., woodland, grassland, wetlands, urban, coastal features, water bodies, etc.).
- Priority Habitats (PH): nested within relevant BHs where applicable and may be constrained by GIS masks post-survey.
- Enclosed vs. unenclosed habitats affect attribute detail and data merging with earlier CS datasets.
- Attributes per polygon include primary BH/PH, secondary attributes, and up to 2–4 species to support habitat inference.
- Species lists rely on standardized frameworks; cover categories standardized (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%).
- Special categories include non-native species; woodland components can carry multiple attribute roles.

## Data Collection Platform and Workflow
- CS Surveyor: customized ArcMap extension for field data capture with mandatory change-recording tied to mapped habitats and features.
- Data structures:
  - Landscape Features: Areas (polygons), Lines (linear features), Points (point features).
  - Thematic groups include Inland Physiography, Inland Water, Coastal Features, Agriculture/Natural Vegetation, Forestry, Structures, Recreation, and Transport.
- Editing and quality checks:
  - ArcMap-based editing with topology tools (split, merge, update, copy attributes, modify vertices) to reflect ground changes.
  - Change status indicators: REAL change (new/higher accuracy habitat), ERROR change (correction), NEW BASELINE (new subdivision of land cover).
  - Minimum Mapping Unit (MMU) of 1/25 ha (400 m2); polygons below MMU generally not mapped unless part of a larger unit.
  - Spatial accuracy is secondary to accurately representing habitat extent and change; when needed, spatial adjustments are logged via attributes.
- Data governance and support:
  - Field staff can report bugs via a helpdesk and project Wiki; methodology updates appear in Latest News.
  - Designed to support cross-network data sharing and collaboration through a unified digital system and standardized attribute schemas.

## Pond Mapping and Water Features
- CS2007 requires identification and recording of all ponds within a square; Pond Mapping Recording Sheet captures polygon ID, area, water presence, reasons for loss/creation, and notes.
- A single survey pond per square is selected for detailed condition assessment; selection can use a preselected pond (CS2000) or field-randomization when new ponds are found or access changes.
- Clear criteria distinguish ponds from ditches, flushes, and dammed streams; pond attributes feed into the Inland Water theme and the broader habitat mapping framework.

## Governance, Standards, and Collaboration
- Methodology integrates habitat mapping with policy-relevant reporting to enable harmonized data exchange across partners and networks.
- Emphasizes consistent data standards (BH/PH keys, woodland attributes, MMU, species counts, cover percentages) to minimize ambiguity and support trend analyses.
- Regular updates and support channels (helpdesk, Wiki, Latest News) to maintain data quality and alignment with evolving monitoring needs.
- The data architecture supports cross-sector collaboration and a wide range of scientific applications while providing practical field-collection guidance.

## Practical Implications and Challenges for Data Governance
- Fragmentation and variability of data sources mitigated by standardized keys and a unified digital workflow.
- Time-series data handling requires careful management of REAL vs. ERROR changes and maintenance of baselines (CS1990/CS2000) for unenclosed/enclosed habitats.
- Access barriers (e.g., paywalls) and sector coordination issues exist in the broader data landscape; the handbook provides a centralized, auditable data collection approach to address these concerns.

## Appendices and Extensibility
- Appendices offer extensive guidance on non-specific primary attributes, woodland classifications, and numerous BH/PH attribute combinations.
- Pond Recording Sheets, non-native species lists, veteran tree guidance, and other detailed notes illustrate the depth required for policy-relevant data products.
- Includes historical context from CS2000 and CS1990 themes to support continuity and comparability over time.

## Key Takeaways for Data Leaders
- Establishes a comprehensive, GIS-based data model for habitat and landscape features designed to support national and UK biodiversity monitoring.
- Defines rigorous classification keys (Vegetation Key and Woodland Types) to ensure consistent habitat coding across teams and time.
- Demonstrates a structured workflow for field data capture, change tracking, and quality control, with explicit governance mechanisms (change reason codes, BH/PH accuracy checks, visit statuses).
- Emphasizes data accessibility, collaboration, and ongoing methodological updates to adapt to evolving monitoring needs and datasets.