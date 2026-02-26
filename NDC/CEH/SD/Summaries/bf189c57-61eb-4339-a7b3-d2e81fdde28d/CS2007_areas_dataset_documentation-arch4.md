# Landscape area data 2007 [Countryside Survey], Great Britain

## Overview
- Data from Countryside Survey (GB) for 2007, version 1 (dated 15-01-2016). 
- Contains landscape area data for Broad and Priority Habitats across 591 1km squares in Great Britain.
- Refused access areas are excluded.
- Two CSV files cover habitat areas and associated attributes.

## Data Files and Structure
- LANDSCAPE_AREA_FEATURE_HAB_2007.csv
  - Contains area of habitat within each 1km square.
  - Key columns: SQUARE, YEAR, ID, BROAD_HABITAT, BROAD_HABITAT_NAME, AREA (m2), LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.
- LANDSCAPE_AREA_FEATURE_ATT_2007.csv
  - Contains additional attributes for areas within the 1km squares.
  - Key columns include: YEAR, SQUARE, ID, THEME, THEME_NAME, PRIMARY_ATTRIBUTE, PRIMARY_ATTRIBUTE_NAME, SPECIES, SPECIES_NAME, SPECIES_COVER, SPECIES_COVER_NAME, PRIMARY_QUALIFIER, PRIMARY_QUALIFIER_NAME, STRUCTURE_USE, STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER, PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A, ROAD_VERGE_A_NAME, ROAD_VERGE_B, ROAD_VERGE_B_NAME, MODAL_DBH, MODAL_DBH_NAME, MOSAIC_PRECENT_AREA, LC07, LC07_NUM, COUNTRY, COUNTY, EZ_DESC_07.

## Key Fields (Selected Details)
- SQUARE: 1km square sampling site code.
- YEAR: Survey year.
- ID: Landscape area polygon identifier (unique within a year).
- BROAD_HABITAT / BROAD_HABITAT_NAME: Broad habitat codes and names (including Priority Habitats per Jackson, 2000).
- AREA: Area of habitat within the 1km polygon (square metres).
- LC07 / LC07_NUM: ITE Land Classification 2007 codes.
- COUNTRY / COUNTY: Geographic location (England, Scotland, Wales; within counties or councils).
- EZ_DESC_07: Countryside Survey Environmental Zone description.
- THEME / THEME_NAME, PRIMARY_ATTRIBUTE / PRIMARY_ATTRIBUTE_NAME, SPECIES / SPECIES_NAME / SPECIES_COVER / SPECIES_COVER_NAME, PRIMARY_QUALIFIER / PRIMARY_QUALIFIER_NAME, STRUCTURE_USE / STRUCTURE_USE_NAME, PHYSIOGRAPHY_COVER / PHYSIOGRAPHY_COVER_NAME, ROAD_VERGE_A / ROAD_VERGE_A_NAME, ROAD_VERGE_B / ROAD_VERGE_B_NAME, MODAL_DBH / MODAL_DBH_NAME, MOSAIC_PRECENT_AREA: Additional attributes describing land use, species, structure, physiography, road verge metrics, dominant tree height, mosaic area, etc.

## Data Quality, Gaps and Limitations
- Snapshot data from 2007; reflects conditions as sampled in that year.
- Data gaps possible due to “Refused access areas” being excluded from the dataset.
- Attributes rely on established classifications (ITE Land Classification 2007, Broad Habitat classifications) with accompanying metadata and zone descriptions.
- Some fields and terminology (e.g., MOSAIC_PRECENT_AREA) reflect the original schema and naming conventions; users should align with current metadata when integrating with other datasets.

## Access, Licensing and Acknowledgement
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to include on copies, publications, and presentations:
  - “Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Data published by NERC - Centre for Ecology & Hydrology (CEH); Landscape area data is © CEH. Version information: Version 1, 15-01-2016.

## How to Use and Integrate
- Suitable for analyses of habitat area distribution across GB at 1km scale, linked with land classification and environmental zone descriptors.
- Can be joined across files using SQUARE, YEAR, and ID to create enriched habitat-area datasets with both area and attribute information.
- Useful for:
  - Assessing spatial patterns of Broad Habitats and Priority Habitats.
  - Linking habitat areas to land use, species cover, structural attributes, and physiography.
  - Historical comparisons when combined with data from other years or surveys.
- When using in reports or products, ensure proper acknowledgment and citation of the Countryside Survey data.

## References and Documentation
- Countryside Survey Website: general overview and methodology (http://www.countrysidesurvey.org.uk/).
- Bunce et al. (1996, 2007): ITE Land Classification of Great Britain; foundational methodology and classifications.
- Jackson (2000): Guidance on Biodiversity Broad Habitat Classification interpretations.
- ITE Land Classification of Great Britain 2007: NERC Environmental Information Data Centre dataset (doi: 10.5285/5f0605e4-aa2a-48ab-b47c-bf5510823e8f).
- Related datasets and publications provide definitions and usage guidance for habitat and land-use attributes.