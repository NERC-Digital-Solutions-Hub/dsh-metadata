# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- Purpose and scope
  - Provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain for the year 1984.
  - Estimates are calculated using the 1998 ITE Land Classification and presented as total areas in thousands of hectares (000s ha) for each Broad Habitat per Land Class, including 95% confidence intervals (lower and upper estimates).

- Data files and what they contain
  - CS1984_Broad_Habitat_Stock.csv
    - Contains nationwide Broad Habitat stock estimates by Land Class for 1984.
    - Key columns:
      - YEAR: survey year (1984)
      - LAND_CLASS: ITE Land Class (Bunce et al. references)
      - BROAD_HABITAT: Broad Habitat code
      - BROAD_HABITAT_NAME: Broad Habitat description
      - LAND_CLASS_AREA: total area of the relevant Land Class (000s ha)
      - MEAN_ESTIMATE: mean area of Broad Habitat for the Land Class (000s ha)
      - LOWER_ESTIMATE: lower 95% CI (000s ha)
      - UPPER_ESTIMATE: upper 95% CI (000s ha)
  - cs1984_stock.tif
    - Raster (1 km pixel resolution) where each band corresponds to a Broad Habitat class.
    - Each 1 km pixel contains a mean percentage estimate of habitat amount within that square, based on means from 1 km survey squares sampled within each Land Class strata.
    - Band-to-Broad Habitat mapping aligns with the Broad Habitat 1–17 structure described in the dataset documentation.

- Classification and methodology
  - Uses the 1998 ITE Land Classification (Bunce et al., 1996; 1981; 1998) to derive national Broad Habitat stock for 1984.
  - Broad Habitat names and definitions reference Jackson (2000) guidance on interpretation of the Biodiversity Broad Habitat Classification.

- Spatial and technical details
  - Spatial resolution and extent: 1 km pixel size; covers Great Britain; British National Grid (OSGB1936), Transverse Mercator projection.
  - Data format considerations: csv for tabular national estimates; tif raster for spatially explicit estimates by land class and habitat band.

- Acknowledgement and usage rights
  - All Countryside Survey data must be acknowledged.
  - Data copyrighted by NERC - Centre for Ecology & Hydrology; Countryside Survey material is © NERC-CEH. All rights reserved.
  - Acknowledgement example included in the documentation: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”

- References and related materials
  - Key methodological and background references include:
    - Bunce et al. (1996, 1981, 1998) on ITE Merlewood Land Classification and its evolution.
    - Jackson (2000) guidance on interpretation of the Biodiversity Broad Habitat Classification.
    - Scott (2007); Carey et al. (2008) Countryside Survey reports and technical materials.
  - Links and further metadata are provided in the documentation and Countryside Survey website.