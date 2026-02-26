# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- Purpose and scope
  - National estimates of Broad Habitat stock (Habitats 1-17) for 1984, derived using the 1998 ITE Land Classification.
  - Outputs include total areas (in thousands of hectares) by Broad Habitat and Land Class, with 95% confidence intervals.
  - Includes both a tabular stock dataset and a 1 km raster representation of habitat proportions.

- Data files and structure
  - CSV: CS1984_Broad_Habitat_Stock.csv
    - Columns and meanings:
      - YEAR: Survey year
      - LAND_CLASS: ITE Land Class
      - BROAD_HABITAT: Broad Habitat code
      - BROAD_HABITAT_NAME: Broad Habitat description
      - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
      - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
      - LOWER_ESTIMATE: Lower 95% CI for Broad Habitat area (000s ha)
      - UPPER_ESTIMATE: Upper 95% CI for Broad Habitat area (000s ha)
  - TIFF: cs1984_stock.tif
    - A 1 km pixel raster where each band corresponds to a Broad Habitat class.
    - Each pixel contains the mean percentage of that habitat within the 1 km grid cell, derived from 1 km survey squares within each Land Class strata.
    - Band-to-Habitat mapping aligns with the Broad Habitat codes described in the CSV.

- Interpretation and mapping notes
  - Broad Habitat 1 and 2 (with specific Band assignments) illustrate how bands correspond to habitat classes across Land Classs:
    - Example mappings include:
      - Band 2: Broad Habitat 2 and 1 (Coniferous Woodland)
      - Band 3: Broad Habitat 3 and 1 (Boundary and Linear Features)
      - Band 4: Broad Habitat 4 and 1 (Arable and Horticulture)
      - Band 5: Broad Habitat 5 and 1 (Improved Grassland)
      - Band 6: Broad Habitat 6 and 1 (Neutral Grassland)
      - Band 7–17: additional habitat classes and associations
  - Pixel size: 1 km; Projection: OSGB36 British National Grid (Transverse Mercator); Extent: Great Britain.

- Spatial reference and usage
  - Spatial reference: British National Grid (OSGB1936)
  - Use this data to produce national-scale habitat-area summaries by Land Class, or to map spatial distribution of Broad Habitats at 1 km resolution.
  - The raster supports analysis that combines area estimates with spatial context (e.g., overlay with other maps, integration with local planning data).

- Attribution and usage rights
  - Data owned by NERC - Centre for Ecology & Hydrology.
  - All use must acknowledge Countryside Survey data and CEH/NERC rights; include the standard acknowledgment on copies, publications, and presentations.

- Related references and methodology
  - Links to Countryside Survey technical reports, methodology papers, and supporting ITE Land Classification documentation.
  - Key sources include:
    - Scott (2007); Bunce et al. (1998, 1996) on ITE Land Classification
    - Jackson (2000) on interpretation of Biodiversity Broad Habitat Classification
    - Countryside Survey results and technical reports (2007, 2008)
  - These references describe how national estimates are generated from 1 km survey squares and how the Land Classification underpins habitat stock calculations.

- Practical considerations for data use (Data Support perspective)
  - Useful for stakeholders needing non-specialist, broad-area habitat insights (e.g., local councils, private sector planning) and for creating self-serve tools (dashboards/maps) showing Broad Habitat distribution and totals.
  - Be mindful of potential data limitations such as the 1984 baseline, reliance on the 1998 Land Classification, and confidence intervals indicating uncertainty in estimates.
  - Ensure proper data handling across formats (CSV and raster) and follow the required attribution when disseminating results.