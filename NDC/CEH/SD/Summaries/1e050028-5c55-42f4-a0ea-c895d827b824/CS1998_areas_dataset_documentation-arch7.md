# Landscape area data 1998 [Countryside Survey], Great Britain

- Landscape-area dataset from the Countryside Survey (1998) covering 569 1km squares across Great Britain.
- Data are provided in two CSV files:
  - LANDSCAPE_AREA_FEATURE_HAB_1998.csv: habitat area within each 1km square
  - LANDSCAPE_AREA_FEATURE_ATT_1998.csv: additional attributes for the same habitat areas
- Data origin and rights:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH)
  - All use of Countryside Survey data must be acknowledged with the specified wording
  - Countryside Survey © NERC-CEH; all rights reserved

- Scope and sampling:
  - Areas of Broad and Priority Habitats within 569 1km squares sampled in 1998
  - YEAR indicates survey year; SQUARE is the 1km grid code; ID is a polygon identifier unique within a year

- File 1: LANDSCAPE_AREA_FEATURE_HAB_1998.csv (habitat area)
  - Columns:
    - SQUARE, YEAR, ID
    - BROAD_HABITAT (habitat code) and BROAD_HABITAT_NAME (habitat name)
    - AREA (habitat area within the 1km square, in square metres)
    - LC07 (ITE Land Class 2007 code) and LC07_NUM
    - COUNTRY (England ENG, Scotland SCO, Wales WAL)
    - COUNTY (county or council)
    - EZ_DESC_07 (Environmental Zone description; link provided in documentation)

- File 2: LANDSCAPE_AREA_FEATURE_ATT_1998.csv (habitat attributes)
  - Columns include:
    - YEAR, SQUARE, ID
    - THEME and THEME_NAME (theme/land-use classification)
    - PRIMARY_ATTRIBUTE and PRIMARY_ATTRIBUTE_NAME
    - SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME
    - PRIMARY_QUALIFIER and PRIMARY_QUALIFIER_NAME
    - STRUCTURE_USE and STRUCTURE_USE_NAME
    - PHYSIOGRAPHY_COVER and PHYSIOGRAPHY_COVER_NAME
    - ROAD_VERGE_A, ROAD_VERGE_A_NAME
    - ROAD_VERGE_B, ROAD_VERGE_B_NAME
    - MODAL_DBH and MODAL_DBH_NAME
    - MOSAIC_PRECENT_AREA (proportion of area in a mosaic habitat)
    - LC07 and LC07_NUM
    - COUNTRY, COUNTY, EZ_DESC_07

- How to use in GIS:
  - Treat HAB_1998 file as polygon-level habitat extents within each 1km square, with AREA indicating habitat size
  - Use ID to join HAB and ATT files for per-polygon attribute enrichment
  - Combine with the 1km square grid to map spatial distribution of habitat types, land classes, and environmental zones
  - Leverage attributes for thematic mapping (Broad Habitat, LC07 classification, environmental zones, road verge attributes, etc.)
  - Potential analyses: area-weighted habitat coverage, cross-tabulations of habitat type with land class or physiography, spatial queries by COUNTRY/COUNTY

- Data quality, provenance, and notes:
  - Data are from 1998 Countryside Survey; unique per year (ID unique within a year)
  - Some fields use codes with corresponding names in THEME/ATTRIBUTE/SPECIES/LAND CLASS, requiring cross-reference with documentation
  - Data include diverse attributes (habitat, species, structure use, physiography, road verge widths, DBH, mosaic area)

- Acknowledgement and references:
  - All use must include: “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - References and suggested publications provided (e.g., Jackson 2000 on Broad Habitat interpretation; Bunce et al. on the ITE Land Classification GB 1996/2007)
  - Links and DOIs provided for deeper methodology and classification context

- Practical considerations for GIS specialists:
  - Data are historical (1998); verify currency for your analysis and document accordingly
  - Ensure proper field mapping when joining HAB and ATT files (matching on SQUARE and ID, unique within year)
  - Maintain the required acknowledgment in any published or shared outputs
  - Be aware of multiple classification schemes (Broad Habitat, LC07, environmental zones) and their cross-references when integrating with other datasets