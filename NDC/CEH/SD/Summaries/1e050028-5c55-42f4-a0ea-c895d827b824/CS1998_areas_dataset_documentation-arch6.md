# Landscape area data 1998 [Countryside Survey], Great Britain

- Two CSV data files describe habitat areas and related attributes for 569 1km squares across Great Britain, sampled in 1998.
- Data are from the Countryside Survey (CS) data owned by NERC - Centre for Ecology & Hydrology (CEH).

## Data files and structure

- LANDSCAPE_AREA_FEATURE_HAB_1998.csv
  - Purpose: Contains habitat area measurements for each 1km square.
  - Key columns:
    - SQUARE: 1km square sampling site code
    - YEAR: Year of survey (1998)
    - ID: Landscape area polygon identifier (unique within a year)
    - BROAD_HABITAT: Broad habitat code
    - BROAD_HABITAT_NAME: Broad habitat name (as per Jackson 2000)
    - AREA: Area of habitat within the 1km square (square metres)
    - LC07, LC07_NUM: ITE Land Classification 2007 codes
    - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
    - COUNTY: County or Council
    - EZ_DESC_07: Environmental Zone description (with related documentation)
- LANDSCAPE_AREA_FEATURE_ATT_1998.csv
  - Purpose: Additional attributes for areas within the 1km squares.
  - Key columns (selection):
    - YEAR, SQUARE, ID: as above
    - THEME, THEME_NAME: Theme code and description (land use)
    - PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME
    - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE, STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A, ROAD_VERGE_A_NAME
    - ROAD_VERGE_B, ROAD_VERGE_B_NAME
    - MODAL_DBH, MODAL_DBH_NAME
    - MOSAIC_PRECENT_AREA
    - LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07
  - Note: Includes a broad set of attribute codes and descriptive names, linking to land use, species, structure, physiography, road verge, and other landscape characteristics.

## Data usage and interpretation tips

- Use the SQUARE, YEAR, and ID keys to join HAB_1998 and ATT_1998 datasets for comprehensive habitat and attribute information per 1km square.
- LC07 and LC07_NUM provide ITE Land Classification (GB 2007) context for landscape classification.
- EZ_DESC_07 provides the Countryside Survey Environmental Zone description for environmental context.
- AREA gives the extent of each habitat type within the 1km polygon (in square metres).
- The ATT file offers a rich set of attributes (theme, species, cover, qualifiers, structure, physiography, road verge, DBH, mosaic area) to enable more detailed analyses of habitat composition and landscape structure.
- These data are suitable for landscape-scale analyses, habitat mapping, change detection when combined with other CS years, and informing policy or planning at local to national scales.

## Acknowledgement, rights and usage conditions

- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text (to be used on copies, publications, and presentations):
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- The CS data are copyrighted; all rights reserved.

## References and publications

- Countryside Survey Website: general overview and methodologies (http://www.countrysidesurvey.org.uk/).
- Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain.
- Bunce et al. (1981, 1990/1996) Merlewood papers describing land classes and GB classifications.
- Jackson (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007 (dataset DOI/Link provided).
- Additional links and DOIs provided in the dataset documentation.

## Access notes

- Data are provided with the above file descriptions and column definitions; see accompanying documentation for detailed methodology and lineage.
- Relevant environmental zone descriptions and classification references are included in EZ_DESC_07 and linked publications.