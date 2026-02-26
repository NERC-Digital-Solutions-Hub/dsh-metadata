# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Countryside Survey 1990 estimates of Broad Habitat areas (Habitats 1–17) for Great Britain.
- Derived using the 2007 ITE Land Classification; national stock estimates are in thousands of hectares with lower and upper 95% confidence intervals.
- Freshwater habitats were modeled separately; there was no Montane (BH15) class in 1990.

## Data files and contents
- CS1990_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - Year of survey; Land Class (ITE), Broad Habitat code and description; total area for the land class (000s ha); mean estimate (000s ha) with possible negative values (treat as 0); 95% confidence interval bounds.
- cs1990_stock.tif
  - 1 km pixel raster; each pixel (band) contains the mean percentage estimate of habitat for that Broad Habitat class within that square.
  - Note: 1990 had no Montane class, so Band adjustments: Band 15 = BH16, Band 16 = BH17 (Band-to-BH mapping described below).

## Spatial and technical details
- Spatial resolution: 1 km (pixel size 1000 m).
- Coordinate system: British National Grid (OSGB36), Projection: Transverse Mercator.
- Extent: Great Britain.

## Band / class mapping (raster)
- In each 1 km band, the value represents the mean percentage of habitat for the corresponding Broad Habitat class within that pixel.
- Note on 1990 mapping: there was no Montane (BH15); adjustments include Band 15 and Band 16 corresponding to BH16 and BH17, respectively. The table below describes the associations described in the dataset documentation (relationships between Broad Habitat codes and raster bands are provided in the data notes).

- Broad Habitat associations (illustrative mappings described in the dataset):
  - Broad Habitat 2, Broad Habitat 1 = Coniferous Woodland; Broad Habitat 2, Broadleaved Mixed and Yew Woodland = Band 2.
  - Broad Habitat 3, Broad Habitat 1 = Boundary and Linear Features; Broad Habitat 3, Broadleaved Mixed and Yew Woodland = Band 3.
  - Broad Habitat 4, Broad Habitat 1 = Arable and Horticulture; Broad Habitat 4, Broadleaved Mixed and Yew Woodland = Band 4.
  - Broad Habitat 5, Broad Habitat 1 = Improved Grassland; Broad Habitat 5, Broadleaved Mixed and Yew Woodland = Band 5.
  - Broad Habitat 6, Broad Habitat 1 = Neutral Grassland; Broad Habitat 6, Broadleaved Mixed and Yew Woodland = Band 6.
  - Broad Habitat 7, Broad Habitat 1 = Calcareous Grassland; Broad Habitat 7, Broadleaved Mixed and Yew Woodland = Band 7.
  - Broad Habitat 8, Broad Habitat 1 = Acid Grassland; Broad Habitat 8, Broadleaved Mixed and Yew Woodland = Band 8.
  - Broad Habitat 9, Broad Habitat 1 = Bracken; Broad Habitat 9, Broadleaved Mixed and Yew Woodland = Band 9.
  - Broad Habitat 10, Broad Habitat 1 = Dwarf Shrub Heath; Broad Habitat 10, Broadleaved Mixed and Yew Woodland = Band 10.
  - Broad Habitat 11, Broad Habitat 1 = Fen, Marsh, Swamp; Broad Habitat 11, Broadleaved Mixed and Yew Woodland = Band 11.
  - Broad Habitat 12, Broad Habitat 1 = Bog; Broad Habitat 12, Broadleaved Mixed and Yew Woodland = Band 12.
  - Broad Habitat 13, Broad Habitat 1 = Standing Open Waters and Canals; Broad Habitat 13, Broadleaved Mixed and Yew Woodland = Band 13.
  - Broad Habitat 14, Broad Habitat 1 = Rivers and Streams; Broad Habitat 14, Broadleaved Mixed and Yew Woodland = Band 14.
  - Broad Habitat 16, Broad Habitat 1 = Inland Rock; Broad Habitat 16, Broadleaved Mixed and Yew Woodland = Band 15.
  - Broad Habitat 17, Broad Habitat 1 = Urban; Broad Habitat 17, Broadleaved Mixed and Yew Woodland = Band 16.
- Summary: bands are interpreted per habitat class, with 1990-specific adjustments for montane absence and band-to-habitat relationships as documented.

## Data usage and interpretation
- MEAN_ESTIMATE values may be negative due to the statistical model; treat negatives as 0.
- LOWER_ESTIMATE and UPPER_ESTIMATE provide 95% confidence intervals for the estimates by land class and habitat.
- Use the stock CSV for tabular national totals by land class and habitat; use the raster for spatial distribution by 1 km pixel.

## Data licensing and acknowledgements
- All Countryside Survey data must be acknowledged.
- Acknowledgement text to be used:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## References and useful sources
- Countryside Survey project and outputs (general overview and methodologies): Countryside Survey Website.
- Key technical references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007.
  - Barr et al. (1993) Countryside Survey 1990: main report.
  - Scott (2007) CS Technical Report No.4/07: Statistical Report (national estimates from 1 km squares).
  - Bunce et al. (1996, 2007) ITE Land Classification of Great Britain.
  - Jackson (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification.
- Links to data and reports are provided in the dataset documentation.