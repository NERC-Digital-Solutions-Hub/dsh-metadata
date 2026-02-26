# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- Dataset examining pollinators (bumblebees, honey bees, and other visitors) in winter-sown oilseed rape (Brassica napus) fields and their relation to local plant diversity and landscape characteristics.
- Part of the Wessex BESS project (NERC Biodiversity and Ecosystem Service Sustainability program); collects data 2014–2015 in the Wessex region, southern England.
- Designed to be used with other Wessex BESS WP4 datasets to study pollinator–habitat relationships.

## Data Collection and Scope
- Survey methods:
  - Field surveys across 12 fields per year using three 58 m transects per field (perpendicular to field edge; stratified to include hedges and margins).
  - Pollinator sampling with two complementary approaches:
    - Transect observations for bumblebees (Bombus spp.) and honey bees (Apis mellifera).
    - Pan traps (15 cm, UV yellow) for solitary bees, hoverflies, and other visitors.
- Local plant diversity:
  - Assessed in field margins and cropped areas using quadrats (five 1 m² per margin; random placement near transects).
- Landscape context (within 0.5–3 km radius buffers around collection points):
  - Grassland types (intensive, restored, species-rich), semi-natural habitats, other habitat types, and proportions of arable land.
  - Crop composition within buffers; hedges and field margins recorded.
- Timing and conditions:
  - Transects conducted between 10:00 and 16:00; >12°C and wind <6–8 m/s.
  - Growth stage of oilseed rape recorded within 2 m of pan traps.
- Data collection and ethics:
  - Protocols standardized; QA via MS Access data entry; ethics approved by University of Exeter committee.

## Data Structure and Variables
- Four linked data files:
  - NERCPollinatorSpeciesList.csv
  - NERCPanTrapData.csv
  - NERCPollTrans.csv
  - NERCPollLandscapeSurvey.csv
- Core linking identifiers (to connect datasets):
  - FarmID, FieldID, TransectID, PointCode, SpeciesCode
- Key data types and measures:
  - Pollinators: counts by species/caste (Apis mellifera, Bombus spp., other visitors) from transects and pan traps; species identified to the extent possible.
  - Local plant diversity: margin and in-crop plant diversity (quadrats; species identifications and percent cover).
  - Landscape metrics: area and type of grasslands, semi-natural habitats, oilseed rape (OSR), arable land; hedges; margins; and related spatial buffers (0.5–3 km radii) with multiple interval steps.
  - Habitat structure: margin length, hedge length/height/width, margin width, and derived estimates of insect-pollinated plant area.
  - Crop context: year, growth stage of OSR, average corner growth stage near pan traps.
- Taxonomy and data notes:
  - Taxonomic resolution in NERCPollinatorSpeciesList includes species, genus, family, and superfamily levels; some groups identified only to higher taxonomic levels.
  - Some missing data entries (e.g., pan traps damaged; missing species data in certain columns).

## Data Quality, Provenance and Access
- Data quality:
  - Adheres to predefined field and lab protocols; training provided; QA in MS Access.
  - Data entries include explicit notes on missing values and data gaps.
- Provenance:
  - Collected as part of the Wessex BESS WP4 work; links to broader NERC data standards and cited methodological references.
- Access and linkage:
  - Metadata-rich with consistent identifiers across files enabling joins (e.g., linking species codes to pan traps and transects).
  - Designed for integration with other Wessex BESS WP4 datasets.

## Limitations and Gaps
- Missing data:
  - Several pan traps damaged, leading to missing data in specific columns for certain points.
  - Some taxa identified only to higher taxonomic levels; some species codes may lack complete gender/ caste assignments.
- Taxonomy and metadata:
  - Some species groups lack full species-level identification; functional group assignments for pollen delivery may be incomplete for rare visitors.
- Field coverage:
  - Twelve fields per year; temporal snapshot limited to 2014–2015 within a specific geographic region.

## Linkages and Potential for Use
- Interoperability:
  - Data can be linked within the four-file structure using FarmID, FieldID, TransectID, PointCode, and SpeciesCode.
  - Suitable for cross-site comparisons and integration with wider WP4 datasets and GIS-based landscape metrics.
- Potential use cases for data leaders:
  - Develop data products and indicators on pollinator abundance and diversity in relation to landscape structure and plant diversity.
  - Inform data strategy for ecosystem service assessments and habitat management planning.
  - Identify data gaps and standardize metadata/taxonomic resolution for future collections.
  - Facilitate governance around data sharing with partners; document lineage, quality checks, and linking keys for reproducibility.

## Practical Considerations for Data Leaders
- Ensure consistent metadata standards across datasets to support discoverability and reuse.
- Maintain and enhance linkage keys (FarmID, FieldID, TransectID, PointCode, SpeciesCode) to enable robust data integration.
- Plan for higher taxonomic resolution where possible to improve product value and analytical power.
- Document data quality notes and known gaps to support transparent downstream use and data-driven decision making.