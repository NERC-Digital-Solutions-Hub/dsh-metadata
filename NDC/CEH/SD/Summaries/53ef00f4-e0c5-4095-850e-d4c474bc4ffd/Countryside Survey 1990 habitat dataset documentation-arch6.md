# Broad Habitat Area Estimates by Land Class for Great Britain 1990

- Purpose and scope
  - Provides national estimates of Broad Habitat stock (Habitats 1–17) for 1990, derived using the 2007 ITE Land Classification.
  - Outputs include total areas by Land Class and Broad Habitat, with uncertainty bounds, plus spatially explicit 1 km raster estimates.

- Data products

  - CS1990_Broad_Habitat_Stock.csv
    - Columns:
      - YEAR: Year of Survey
      - LAND_CLASS: ITE Land Class
      - BROAD_HABITAT: Broad Habitat code
      - BROAD_HABITAT_NAME: Broad Habitat description
      - LAND_CLASS_AREA: Total area of relevant Land Class (000s ha)
      - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha); may be negative (treat as 0)
      - LOWER_ESTIMATE: Lower 95% CI
      - UPPER_ESTIMATE: Upper 95% CI
    - Notes:
      - Freshwater habitats analysed with a different statistical model.
      - No Montane (BH15) class in 1990.

  - cs1990_stock.tif
    - 1 km resolution raster; each band corresponds to a Broad Habitat class.
    - For each 1 km survey square, band value represents mean percentage habitat within that square.
    - Mapping of bands to Broad Habitats (e.g., Band 1/2 associations outlined; no Montane class in 1990 means Band 15=BH16, Band 16=BH17).
    - Spatial reference: 1 km pixel, British National Grid (OSGB36), Transverse Mercator, extent: Great Britain.

- Technical and spatial details

  - Pixel size: 1000 m
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator
  - Extent: Great Britain
  - Both data products require acknowledgement of Countryside Survey data owned by NERC-CEH

- Usage notes and data quality

  - MEAN_ESTIMATE values may be negative due to the statistical model; treat negative values as 0
  - 1990 estimates assume the 2007 ITE Land Classification; interpret in the context of that framework
  - No Montane BH15 class in 1990; raster bands reflect available habitat classes for that year
  - Data are suitable for national-scale stock assessments and for creating self-serve exploration maps; can be combined with other datasets (e.g., other years, other habitat classifications) with careful cross-walking

- Access, rights, and references

  - Acknowledgement required: Countryside Survey data owned by NERC-Centre for Ecology & Hydrology; data © NERC
  - Key references and related resources:
    - Scott, W.A. (2007) CS Technical Report No.4/07 Statistical Report
    - Bunce et al. (1996, 2007) ITE Land Classification guidance and updates
    - Jackson (2000) Guidance on Broad Habitat Classification interpretation
    - Countryside Survey project outputs and main reports (2007 UK results, etc.)

- Practical data-product ideas for a Data Support perspective

  - Build dashboards that show Broad Habitat stock by Land Class for 1990, with uncertainty bands
  - Create map visualizations from cs1990_stock.tif to explore spatial distribution of Broad Habitats across GB
  - Develop data pipelines to combine the stock CSV with additional years or with other classifications, enabling trend analyses
  - Produce user-friendly reports or charts summarizing the proportion of land by habitat type per Land Class, using MEAN_ESTIMATE and confidence intervals
  - Document data lineage and data quality checks (handling negative MEAN_ESTIMATE, band-to-habitat mappings, and Montane/class omissions) for transparency and reuse