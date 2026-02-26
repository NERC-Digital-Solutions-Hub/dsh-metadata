# Landscape area data 1978 [Countryside Survey], Great Britain

- 256 1km squares across Great Britain were surveyed in 1978 to map areas of Broad and Priority Habitats.
- Data file: LANDSCAPE_AREA_FEATURE_HAB_1978.csv
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Data content and structure

- Purpose: Provide habitat area measurements within 1km sampling squares for 1978.
- Spatial scale: 1km squares (grid-based habitat areas).
- Records: Each row represents a habitat feature within a 1km square; areas are in square metres.

- Columns and meanings:
  - SQUARE: 1km square sampling site code (text)
  - YEAR: Year of survey (numeric; 1978)
  - ID: Landscape area polygon identifier (unique within a year)
  - BROAD_HABITAT: Broad or Priority Habitat code (numeric)
  - BROAD_HABITAT_NAME: Description of Broad/Priority Habitat (text)
  - AREA: Area of habitat within the 1km polygon (square metres)
  - LAND_CLASS90: ITE Land Class 1990 code (numeric)
  - COUNTRY: Country location of the square (ENG, SCO, WAL)
  - COUNTY: County (England & Wales) or Council (Scotland) (text)
  - EZ_DESC_07: Countryside Survey Environmental Zone description (text)

## Temporal and classification context

- Year of data: 1978
- Habitat classifications linked to:
  - ITE Merlewood Land Classification (ITE Land Classification of Great Britain) 1990
  - Biodiversity Broad Habitat Classification guidance (JNCC)
- Useful for GIS analyses that compare baseline habitat extents over time or integrate with other CS datasets.

## Data rights and acknowledgments

- All use must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Acknowledgment and copyright: Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- References and publications are provided for methodology and context (see Countryside Survey website and linked reports).

## Practical GIS usage notes

- Map visualization: Use SQUARE/COUNTRY/COUNTY to join to spatial grid boundaries; visualize HABITAT types and their extents within each 1km cell.
- Analyses: 
  - Aggregate AREA by BROAD_HABITAT_NAME to show total habitat area per type.
  - Compare habitat areas across COUNTRIES or COUNTIES (where applicable).
  - Link with LAND_CLASS90 for classification-based analyses or crosswalks with other GB land classifications.
- Integration tips:
  - The dataset is an 1978 baseline; combine with more recent CS data or other historical layers to assess change.
  - Ensure proper acknowledgment in any outputs, maps, or reports.