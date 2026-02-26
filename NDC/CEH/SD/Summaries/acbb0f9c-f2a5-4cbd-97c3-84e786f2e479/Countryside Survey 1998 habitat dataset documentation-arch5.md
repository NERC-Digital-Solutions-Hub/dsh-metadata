# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1-17) for 1998, calculated using the 2007 ITE Land Classification.
- Estimates are given as total area in thousands of hectares per Land Class, with lower and upper 95% confidence limits.
- Freshwater habitats were analyzed using a different statistical model from terrestrial habitats.
- Survey fieldwork conducted in 1998 (with a few sites in 1999); commonly referred to as Countryside Survey 2000.

## Datasets included
- CS1998_Broad_Habitat_Stock.csv
  - Contains national estimates by Year, Land Class, and Broad Habitat (codes 1-17).
  - Columns provide: LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as zero.
- CS1998_stock.tif
  - A 1 km resolution raster with 17 bands.
  - Each band corresponds to a Broad Habitat class; pixel values are mean estimates of habitat percentage within that square.
  - Spatial reference: British National Grid, OSGB36, Transverse Mercator; extent covers Great Britain.

## Data fields and interpretation
- YEAR: Year of Survey.
- LAND_CLASS: ITE Land Class (taxonomy from Bunce et al. references).
- BROAD_HABITAT: Broad Habitat code (1-17).
- BROAD_HABITAT_NAME: Description of Broad Habitat.
- LAND_CLASS_AREA: Total area of the relevant Land Class (in 000s ha).
- MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha); may be negative due to model and should be treated as 0.
- LOWER_ESTIMATE / UPPER_ESTIMATE: 95% confidence interval bounds (000s ha).

## Temporal and survey context
- Based on data collected in 1998 (with some sites in 1999); commonly linked to Countryside Survey 2000 outputs.
- Uses Countryside Survey methodology and ITE Land Classification (reference frameworks and publications provided).

## Spatial and technical details
- CS1998_Broad_Habitat_Stock.csv
  - LAND_CLASS_AREA and estimates are in thousands of hectares.
- CS1998_stock.tif
  - Pixel size: 1 km (1000 m).
  - Bands 1–17 correspond to Broad Habitat classes 1–17 (mapping defined in the dataset documentation).
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator.
  - Extent: Great Britain.

## Data quality, limitations, and handling
- Negative MEAN_ESTIMATE values can occur due to the statistical model; treat these as zero in analyses.
- Freshwater habitats were analyzed with a different statistical approach than terrestrial habitats; consider this when integrating with other datasets.
- Metadata and crosswalks (e.g., Land Class definitions, Habitat codes) are anchored to the ITE Land Classification and related publications; consult referenced sources for methodological detail.

## Data governance, usage, and acknowledgements
- All use of Countryside Survey (CS) data must be acknowledged.
- Acknowledgement text (to be used in outputs): "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data are accompanied by extensive references and publications detailing methodologies and classifications.

## References and publications
- Countryside Survey project overview and outputs: http://www.countrysidesurve y.org.uk/ (note: reference text provided in dataset)
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
- Scott (2007) CS Technical Report No. 4/07: Statistical report on national estimates from the 1 km survey sample squares
- Bunce et al. (1996, 2007) ITE Land Classification of Great Britain (and related vector datasets)
- Barr (1998, 1998) Countryside Survey 2000 Field Handbook (habitat mapping methodology)
- Jackson (2000) Guidance on interpretation of the Biodiversity Broad Habitat Classification
- Various related methodological and data-source references linked to the ITE Land Classification and Countryside Survey outputs

## Copyright and access notes
- Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology.
- All rights reserved; data usage must follow the acknowledged citations and copyright statements provided above.