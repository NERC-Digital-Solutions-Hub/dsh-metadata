# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 1990, calculated using the 2007 ITE Land Classification.
- Two data products accompany the dataset:
  - CSV stock file (CS1990_Broad_Habitat_Stock.csv) with area estimates by Land Class and Broad Habitat.
  - Raster stock file (cs1990_stock.tif) with 1 km pixel estimates of habitat percentages.
- Freshwater habitats were modeled differently; there was no separate Montane (BH15) class in 1990.

## Data products and structure

### CSV stock file: CS1990_Broad_Habitat_Stock.csv
Columns:
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class code (Bunce et al. references)
- BROAD_HABITAT: Broad Habitat code
- BROAD_HABITAT_NAME: Broad Habitat description
- LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
- MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha)  
  - Note: negative values may occur due to the statistical model; treat as 0.
- LOWER_ESTIMATE: Lower 95% confidence interval (000s ha)
- UPPER_ESTIMATE: Upper 95% confidence interval (000s ha)

### Raster stock file: cs1990_stock.tif
- Each 1 km pixel contains a mean percentage estimate of habitat within that square.
- Bands correspond to Broad Habitat classes; mapping provided (see notes below).
- Montane (BH15) does not exist in 1990; hence Band 15 = BH16 and Band 16 = BH17.
- Example band-to-habitat relationships are provided, indicating how Broad Habitat 1 and Broad Habitat 2 combinations map to bands (e.g., “Broad Habitat 2, Broad Habitat 1 = Coniferous Woodland,” etc.).

## Spatial reference and data extent

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain
- Notes: Raster bands encode percentage estimates; data are aligned with the 1 km survey squares within each Land Class strata.

## Data quality, limitations, and caveats

- MEAN_ESTIMATE may be negative due to the underlying statistical model; treat negatives as zero.
- Freshwater analyses used a different model; no Montane (BH15) class in 1990.
- 1990 estimates are tied to the 2007 ITE Land Classification framework for comparability with later datasets.
- Band-to-broad-habitat mappings are specific to 1990 and include adjustments (e.g., no Montane class leads to Band 15/16 mapping).

## Use, attribution, and governance

- Acknowledgement required for all CS data: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; CS © data rights apply.
- Data and publications referenced provide methodological background (e.g., CS 1990 main report, Scott 2007 statistical report, ITE Land Classification documents, field handbooks, JNCC guidance).

## Provenance and references

- The dataset draws from Countryside Survey outputs and associated methodological reports:
  - Countryside Survey: UK Results from 2007 and related technical reports
  - Countryside Survey 1990: Main report
  - ITE Land Classification of Great Britain (1996; 1981; 2007)
  - Field Handbook and guidance documents for habitat interpretation
- Publications and links accompany the data, providing context and methods for generating national estimates from 1 km survey squares.