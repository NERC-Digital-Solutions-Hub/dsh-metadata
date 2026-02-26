# Broad Habitat Area Estimates by Land Class for Great Britain 1990

- Purpose and scope
  - Provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain in 1990.
  - Uses the 2007 ITE Land Classification to enable consistent monitoring of environmental health and policy performance over time.
  - Outputs are supplied as total areas (in 000s ha) by Broad Habitat and Land Class, with associated confidence intervals; intended for scrutiny and comparison across time.

- Data files and formats
  - CS1990_Broad_Habitat_Stock.csv
    - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE
    - MEAN_ESTIMATE: mean area (000s ha); may be negative due to the statistical model (treat as 0)
    - LOWER_ESTIMATE / UPPER_ESTIMATE: 95% confidence interval bounds
    - Note: freshwater habitats were modeled differently; no separate Montane (BH15) class in 1990
  - cs1990_stock.tif
    - Raster with 1 km pixel resolution; each band represents a Broad Habitat class
    - Pixel values indicate mean percentage habitat within that 1 km square
    - Mapping of bands to habitats (e.g., Band 1/2 correspond to Broad Habitat 1/2 as described)
    - No Montane class in 1990; Band 15 corresponds to BH16, Band 16 to BH17

- Land Classification and references
  - Based on the ITE Land Classification framework (Bunce et al. 1996; Bunce et al. 1981; Bunce et al. 2007)
  - Land Class areas are provided in 000s ha for each Broad Habitat and Land Class
  - Key publications and methodologies cited for context and reproducibility (e.g., Scott 2007; Jackson 2000)

- Spatial information
  - Spatial reference: British National Grid (OSGB36)
  - Pixel size: 1 km; Extent: Great Britain; Projection: Transverse Mercator
  - Useful for creating standardized maps and integrating with other GIS layers for monitoring

- Data usage, access, and acknowledgments
  - All CS data must be acknowledged as Countryside Survey data owned by NERC - CEH
  - Countryside Survey © CEH; data rights reserved
  - Referenced outputs and websites provide background, methodologies, and further documentation (e.g., CS reports and technical notes)

- Practical considerations for analysts
  - Use standardized methods to compare broad habitat extents over time
  - Apply caution with negative MEAN_ESTIMATE values (treat as zero)
  - For 1990, note absence of Montane habitat (BH15) and special treatment of freshwater modeling
  - Ensure linkage between CSV (stock) data and TIFF (raster) data when integrating area estimates with spatial analyses
  - Store and, where appropriate, upload datasets to monitoring portals to enable wider access and reuse

- References and related resources
  - Countryside Survey website and outputs (general overview and 2007 UK results)
  - Technical reports on statistical methods and ITE Land Classification
  - Key bibliographic sources: Scott (2007), Bunce et al. (1996, 2007), Jackson (2000), Barr et al. (1993, 1991), etc.