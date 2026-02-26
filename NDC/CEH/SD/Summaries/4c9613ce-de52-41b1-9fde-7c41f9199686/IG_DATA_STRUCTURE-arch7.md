# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG)

- Data Originator: ECN Data Centre, Centre for Ecology and Hydrology
- Dataset Owners: UK Environmental Change Network (ECN) programme with multiple sponsoring UK government departments and agencies
- Publication/request guidance: Acknowledge data use; send one reprint of any citing publication

## Overview

- Purpose: Monitor abundance of ground predators (Carabidae) using pitfall traps
- Sampling cadence: Fortnightly data collection from May to October
- Geographic scope: 12 ECN sites across the UK
- Data access note: Data are stored across multiple structures and require accompanying quality metadata for proper use

## Protocol and data usage notes

- Protocol: Pitfall trap method used to estimate ground predator abundance
- Temporal coverage: Fortnightly measurements between May and October
- Quality information: Must be consulted/attached when using these data
- Attribution: Acknowledge ECN and provide a reprint if your work cites ECN data

## Data structure and access

- Core storage: Oracle database
- Site-specific tables:
  - D1IG_xxx: Core data (one table per site)
  - D2IG_xxx: Trap placement/outcome timing data (set-out dates)
  - D3IG_xxx: Habitat information (habitat descriptors)
- Site codes: T01 through T12
  - T01 Drayton
  - T02 Glensaugh
  - T03 Hillsborough
  - T04 Moor House - Upper Teesdale
  - T05 North Wyke
  - T06 Rothamsted
  - T07 Sourhope
  - T08 Wytham
  - T09 Alice Holt
  - T10 Porton Down
  - T11 Y Wyddfa - Snowdon
  - T12 Cairngorms
- Site metadata: Each site includes name, location coordinates, and date range in the dataset (example ranges span from early 1990s to around 2012)

## Data schema (core elements)

- D1IG_xxx (Site data)
  - SITECODE: Site code
  - LCODE: Location code
  - SDATE: Sampling date (dd-mmm-yyyy)
  - TRAP: Trap number (optional)
  - FIELDNAME: Field name (maps to species code or quality code)
  - VALUE: Numeric value (catch count or measurement)
- D2IG_xxx (Trap timing and set-out)
  - SITECODE, LCODE
  - FROMDATE: Date traps were set out
  - SDATE: Date traps were collected
- D3IG_xxx (Habitat information)
  - SITECODE, LCODE
  - HABDESC: Habitat description
- Metadata layers
  - Core metadata tables: referenced by standard metadata documentation
  - Fieldname: holds species code or quality code
  - Common quality fields: Q1–Q8 with corresponding quality codes

## Species and field codes

- Fieldname content: species codes or quality codes
- Species codes: extensive taxonomy mapping for ground beetles (Carabidae) and related taxa
  - Examples include codes for genus and species (e.g., Cicindela, Carabus, Bembidion, etc.)
  - The dataset provides structured mappings from codes to Latin names, ranks (GENUS/SPECIES), and taxonomic groupings
- Utility for GIS: Enables creation of species distribution and abundance maps across sites and habitat types

## Data quality and quality codes

- ECN quality codes: assigned by site managers to indicate data quality and potential issues
- Codes range with descriptions (e.g., 100 No information available, 101 No sample/reading taken, 105 Snow in funnel, 200 Adverse weather, 999 Unusual event text)
- Quality text: If a non-standard situation occurs, a free-form quality text description is provided
- Importance for GIS: Quality codes help assess reliability of spatial data layers and filtering for analysis

## Data usage and GIS applications

- GIS-friendly aspects:
  - Site coordinates and site/habitat descriptors support spatial joins and mapping
  - Structured site (T01–T12) and table (D1–D3) organization facilitates multi-site aggregations
  - Rich species and habitat metadata enable habitat-based distribution analyses
- Typical GIS products:
  - Map layers of ground predator abundance by site and trap location
  - Habitat-based distribution maps using HABDESC and LCODE
  - Temporal visualizations aligning SDATE with catch counts
- Data preparation considerations:
  - Integrate across D1IG_xxx, D2IG_xxx, and D3IG_xxx to build complete spatial datasets
  - Use accompanying quality metadata for filtering and quality control
  - Resolve site-specific coding schemes when combining data across sites

## Practical considerations and challenges for GIS specialists

- Data housed in multiple places and structures; careful data integration required
- Data gaps and varying resolutions across sites; plan for harmonization
- Consistent data standards may be lacking; validate against quality codes and metadata
- Large/complex datasets may require data cleaning and transformation prior to GIS use
- Collaboration with data stewards recommended to ensure correct attribution and quality interpretation

## Attribution and publications

- Acknowledge ECN data usage in outputs
- Provide one reprint of any publication citing ECN data
- Protocol and quality metadata should accompany data usage to ensure reproducibility