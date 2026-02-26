# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Provides national estimates of Broad Habitat stock (Habitats 1–17) for 1990 using the 2007 ITE Land Classification.
- Two data products available:
  - CSV stock data (CS1990_Broad_Habitat_Stock.csv): national estimates by land class, with 95% confidence intervals.
  - Raster stock data (cs1990_stock.tif): 1 km resolution grid of mean percentage habitat per square, by Broad Habitat band.
- Notes that freshwater habitats were modeled differently and there was no Montane (BH15) class in 1990.

## Data products and key variables

- CS1990_Broad_Habitat_Stock.csv
  - YEAR: Year of survey
  - LAND_CLASS: ITE Land Class (classification scheme references Bunce et al. 1996; 1981; 2007)
  - BROAD_HABITAT: Broad Habitat code (BH1–BH17)
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
    - Note: negative values may occur due to the statistical model; treat as 0
  - LOWER_ESTIMATE: Lower 95% CI (000s ha)
  - UPPER_ESTIMATE: Upper 95% CI (000s ha)

- cs1990_stock.tif
  - 1 km grid; each pixel contains a mean percentage estimate of habitat presence for the corresponding Broad Habitat band
  - Bands correspond to Broad Habitat classes (see band-to-habitat mapping below)
  - Note: Band 15 corresponds to BH16 and Band 16 to BH17 because Montane BH15 was not present in 1990

## Raster band to Broad Habitat mapping notes
- Bands are organized such that each band represents a Broad Habitat class context in the 1 km pixel data.
- Example mappings (as described in the dataset notes):
  - Broad Habitat 2, Broad Habitat 1 = Coniferous Woodland
  - Broad Habitat 2, Broadleaved Mixed and Yew Woodland = Band 2
  - Broad Habitat 3, Broad Habitat 1 = Boundary and Linear Features
  - Broad Habitat 3, Broadleaved Mixed and Yew Woodland = Band 3
  - Broad Habitat 4, Broad Habitat 1 = Arable and Horticulture
  - Broad Habitat 4, Broadleaved Mixed and Yew Woodland = Band 4
  - Broad Habitat 5, Broad Habitat 1 = Improved Grassland
  - Broad Habitat 5, Broadleaved Mixed and Yew Woodland = Band 5
  - Broad Habitat 6, Broad Habitat 1 = Neutral Grassland
  - Broad Habitat 6, Broadleaved Mixed and Yew Woodland = Band 6
  - Broad Habitat 7, Broad Habitat 1 = Calcareous Grassland
  - Broad Habitat 7, Broadleaved Mixed and Yew Woodland = Band 7
  - Broad Habitat 8, Broad Habitat 1 = Acid Grassland
  - Broad Habitat 8, Broadleaved Mixed and Yew Woodland = Band 8
  - Broad Habitat 9, Broad Habitat 1 = Bracken
  - Broad Habitat 9, Broadleaved Mixed and Yew Woodland = Band 9
  - Broad Habitat 10, Broad Habitat 1 = Dwarf Shrub Heath
  - Broad Habitat 10, Broadleaved Mixed and Yew Woodland = Band 10
  - Broad Habitat 11, Broad Habitat 1 = Fen, Marsh, Swamp
  - Broad Habitat 11, Broadleaved Mixed and Yew Woodland = Band 11
  - Broad Habitat 12, Broad Habitat 1 = Bog
  - Broad Habitat 12, Broadleaved Mixed and Yew Woodland = Band 12
  - Broad Habitat 13, Broad Habitat 1 = Standing Open Waters and Canals
  - Broad Habitat 13, Broadleaved Mixed and Yew Woodland = Band 13
  - Broad Habitat 14, Broad Habitat 1 = Rivers and Streams
  - Broad Habitat 14, Broadleaved Mixed and Yew Woodland = Band 14
  - Broad Habitat 16, Broad Habitat 1 = Inland Rock
  - Broad Habitat 16, Broadleaved Mixed and Yew Woodland = Band 15
  - Broad Habitat 17, Broad Habitat 1 = Urban
  - Broad Habitat 17, Broadleaved Mixed and Yew Woodland = Band 16
- Important note: There was no Montane (BH15) class in 1990; Band 15 is used for BH16, and Band 16 for BH17.

## Spatial and technical details

- Spatial resolution: 1 km pixel size
- Pixel size (m): 1000 m
- Coordinate system: British National Grid (OSGB1936)
- Projection: Transverse Mercator
- Extent: Great Britain
- Data ownership and rights: Countryside Survey data owned by NERC - CEH; all outputs require acknowledgement
- Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © NERC- CEH. All rights reserved.”

## Data provenance and references

- Based on Countryside Survey 1990; methods linked to 2007 ITE Land Classification (Bunce et al. and Scott 2007)
- Key references and publications include:
  - Countryside Survey: UK results from 2007 (Carey et al., 2008)
  - Countryside Survey 1990: main report (Barr et al., 1993)
  - ITE Land Classification of Great Britain (Bunce et al., 1996; 2007)
  - Guidance on interpretation of the Biodiversity Broad Habitat Classification (Jackson, 2000)
- Useful links and metadata are provided in the dataset documentation and related technical reports (e.g., CS Technical Report No. 4/07)

## Practical considerations for data use

- MEAN_ESTIMATE values may be negative due to the modeling approach; treat negative MEAN_ESTIMATE as zero
- 95% confidence intervals (LOWER_ESTIMATE, UPPER_ESTIMATE) accompany mean estimates for uncertainty
- Some data formats and the presence of patchy data across land classes may require careful harmonization when combining CSV and raster outputs
- Data usage should include proper attribution to Countryside Survey and CEH; consult linked references for methodology and classification details
- Freshwater habitat estimates used a different statistical model; note this when aggregating or comparing with terrestrial habitats

## Summary of purpose

- Enables national and spatial assessment of Broad Habitat distribution across Great Britain for 1990
- Supports data exploration, cross-classification with land class, and creation of data products (tables and maps) for end users to interpret habitat extents and uncertainties
- Facilitates integration with broader Countryside Survey datasets and longitudinal analyses when combined with later survey years