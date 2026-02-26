# Landscape area data 1990 [Countryside Survey], Great Britain

- Two CSV files describe landscape area data from the Countryside Survey 1990 across 506 1km squares in Great Britain
  - LANDSCAPE_AREA_FEATURE_HAB_1990.csv
    - Core habitat data per 1km square
    - Key columns: SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (square metres), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07
  - LANDSCAPE_AREA_FEATURE_ATT_1990.csv
    - Additional attributes for each 1km square area
    - Key columns include: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A/B, ROAD_VERGE_A_NAME, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07

- Purpose and content
  - Areas of Broad and Priority Habitats by 1km squares for the 1990 survey
  - Habitat type codes and names; area coverage within each square
  - Rich attribute set capturing land use, species-related attributes, structure uses, physiography, road verge characteristics, forest metrics (DBH), land classification (ITE LC07), and administrative geography (COUNTRY, COUNTY)

- Data provenance and rights
  - Source: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH)
  - Acknowledgement required on all copies, publications, and presentations: “Countryside Survey data owned by NERC - Centre for Ecology and Hydrology”
  - Countryside Survey © Database Right/Copyright CEH. All rights reserved.

- References and further information
  - Countryside Survey website and methodology documents
  - ITE Land Classification of Great Britain (1996, 1981) and 2007 update
  - Jackson (2000) guidance on Biodiversity Broad Habitat Classification
  - Data Centre references and DOIs/links provided in the references section

- Implications for data strategy and governance (Data Leaders)
  - Metadata and discoverability: clear field definitions (codes and names for habitats, land classes, attributes) aid data integration and interpretation
  - Data standardization: crosswalks to LC07, ITE classifications, and EZ descriptions support interoperability with other datasets
  - Data quality and lineage: historical 1990 data; provenance and versioning are essential for correct usage and comparisons over time
  - Access and rights management: ensure proper acknowledgment in all outputs; plan data sharing within governance constraints
  - Reuse planning: leverage references for methodological context; integrate with wider Countryside Survey datasets and external biodiversity classifications
  - Collaboration potential: dataset useful for cross-sector partnerships in landscape analysis, habitat assessment, and land-use planning; consider aligning with broader data communities of practice for countryside/biodiversity data

- Practical considerations for implementation
  - Verify compatibility of LC07 and EZ_DESC_07 codes with internal data dictionaries
  - Establish data provenance trails and citation formats for outputs
  - Assess granularity and temporal relevance for current analyses, given the 1990 time point
  - Prepare guidance for users on interpreting complex attribute fields and cross-references to external classifications