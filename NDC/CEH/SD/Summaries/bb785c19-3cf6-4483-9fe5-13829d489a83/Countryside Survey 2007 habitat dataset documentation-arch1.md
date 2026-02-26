# Broad Habitat Area Estimates by Land Class for Great Britain

- Purpose: Presents national 2007 estimates of Broad Habitat stock (Habitats 1–17) derived from the 2007 ITE Land Classification; includes mean estimates with 95% confidence intervals; notes that freshwater habitats used a different statistical model.

- Data file: CS007_Broad_Habitat_Stock.csv
  - YEAR (numeric): Year of survey
  - LAND_CLASS (text): ITE Land Class (references Bunce et al. 1996; 1981; 2007)
  - BROAD_HABITAT (numeric): Broad Habitat code
  - BROAD_HABITAT_NAME (text): Broad Habitat description (Jackson, 2000)
  - LAND_CLASS_AREA (numeric): Total Area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE (numeric): Mean area of Broad Habitat for the Land Class (000s ha); may be negative due to the statistical model; treat as 0
  - LOWER_ESTIMATE (numeric): Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE (numeric): Upper 95% confidence limit (000s ha)
  - Notes: Freshwater habitats analyzed with a different model; data enabling national-level habitat stock assessment by Land Class.

- Raster data: CS2007_Stock.tif
  - 1 km resolution raster where each band represents a Broad Habitat class.
  - Each 1 km pixel contains a mean estimate of the percentage of habitat in that square, derived from 1 km survey squares sampled within each Land Class strata.
  - Mapping details (examples):
    - Broad Habitat 2, Broad Habitat 1 = Coniferous Woodland; Broad Habitat 2, Broadleaved Mixed and Yew Woodland = Band 2
    - Broad Habitat 3, Broad Habitat 1 = Boundary and Linear Features; Broad Habitat 3, Broadleaved Mixed and Yew Woodland = Band 3
    - Broad Habitat 4, Broad Habitat 1 = Arable and Horticulture; Broad Habitat 4, Broadleaved Mixed and Yew Woodland = Band 4
    - Broad Habitat 5, Broad Habitat 1 = Improved Grassland; Broad Habitat 5, Broadleaved Mixed and Yew Woodland = Band 5
    - Broad Habitat 6, Broad Habitat 1 = Neutral Grassland; Broad Habitat 6, Broadleaved Mixed and Yew Woodland = Band 6
    - Broad Habitat 7, Broad Habitat 1 = Calcareous Grassland; Broad Habitat 7, Broadleaved Mixed and Yew Woodland = Band 7
    - Broad Habitat 8, Broad Habitat 1 = Acid Grassland; Broad Habitat 8, Broadleaved Mixed and Yew Woodland = Band 8
    - Broad Habitat 9, Broad Habitat 1 = Bracken; Broad Habitat 9, Broadleaved Mixed and Yew Woodland = Band 9
    - Broad Habitat 10, Broad Habitat 1 = Dwarf Shrub Heath; Broad Habitat 10, Broadleaved Mixed and Yew Woodland = Band 10
    - Broad Habitat 11, Broad Habitat 1 = Fen, Marsh, Swamp; Broad Habitat 11, Broadleaved Mixed and Yew Woodland = Band 11
    - Broad Habitat 12, Broad Habitat 1 = Bog; Broad Habitat 12, Broadleaved Mixed and Yew Woodland = Band 12
    - Broad Habitat 13, Broad Habitat 1 = Standing Open Waters and Canals; Broad Habitat 13, Broadleaved Mixed and Yew Woodland = Band 13
    - Broad Habitat 14, Broad Habitat 1 = Rivers and Streams; Broad Habitat 14, Broadleaved Mixed and Yew Woodland = Band 14
    - Broad Habitat 15, Broad Habitat 1 = Montane; Broad Habitat 15, Broadleaved Mixed and Yew Woodland = Band 15
    - Broad Habitat 16, Broad Habitat 1 = Inland Rock; Broad Habitat 16, Broadleaved Mixed and Yew Woodland = Band 16
    - Broad Habitat 17, Broad Habitat 1 = Urban; Broad Habitat 17, Broadleaved Mixed and Yew Woodland = Band 17

- Spatial and technical details
  - Pixel size: 1 km (1000 m)
  - Coordinate system: British National Grid (OSGB36)
  - Projection: Transverse Mercator Great Britain
  - Extent applies to Great Britain

- Acknowledgement and usage
  - All CS data usage requires acknowledgment of Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Copyright: Countryside Survey © NERC-CEH; All rights reserved

- References and context
  - Countryside Survey project website and UK results from 2007 (Carey et al. 2008)
  - Statistical methodologies: CS Technical Report No.4/07 (Scott 2007)
  - Land Classification basis: ITE Merlewood Land Classification (Bunce et al. 1996; 1981)
  - Field mapping methodology: CS Technical Report No.1/07
  - Guidance on Broad Habitat Classification (Jackson, 2000; JNCC Report 307)

- Potential uses for analysis
  - Quantify habitat stock by Land Class and Broad Habitat across Great Britain
  - Assess spatial patterns and regional differences using the 1 km raster
  - Compare 2007 estimates to other years or to alternative classifications
  - Incorporate uncertainty bounds (lower/upper estimates) into predictive models
  - Integrate with other environmental datasets to examine drivers of habitat change
  - Support planning and policy decisions by providing nationally consistent habitat extents