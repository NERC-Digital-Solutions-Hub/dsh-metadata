# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Document context
- Version: 1: 22-1-2014
- Author: C.M. Wood, CEH Lancaster
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Purpose and scope
- Provides national estimates of Broad Habitat stock (Habitats 1–17) for 1998.
- Estimates are expressed as total area (000s ha) by Land Class, with lower and upper 95% confidence intervals.
- Freshwater habitats analyzed with a different statistical model from other habitats.
- Based on the 2007 ITE Land Classification (Bunce et al., 1996; 1981; 2007) and field data collected mainly in 1998 (with some sites in 1999; often referred to as Countryside Survey 2000).

## Data products and formats
- CS1998_Broad_Habitat_Stock.csv
  - Columns include YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - MEAN_ESTIMATE is the mean area for the Broad Habitat within a Land Class (000s ha); negative MEAN_ESTIMATE values should be treated as 0.
- CS1998_stock.tif
  - A 1 km resolution raster with multiple bands; each band represents a Broad Habitat class within Land Class strata.
  - Band-to-habitat mappings indicate how Broad Habitat codes relate to raster bands (e.g., Band 2 generally corresponds to Coniferous/ Broadleaved Woodland in various combinations).

## Data interpretation and methodology
- Land Classification context: ITE Land Classification (GB) as described by Bunce et al. (1996, 1981, 2007); classifications underpin habitat assignments.
- Spatial and statistical approach:
  - 1 km survey squares sampled within each Land Class to derive mean habitat proportions (for CS1998_stock.tif).
  - National estimates derived from the 1 km sample data (CS1998_Broad_Habitat_Stock.csv) using the specified statistical framework.
- Notes on data values:
  - Some MEAN_ESTIMATE values may be negative due to the statistical model; these should be treated as zero.
  - Freshwater habitats use a different statistical model than terrestrial habitats.

## Spatial reference and extent
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain

## Data usage, attribution, and rights
- All CS data must be acknowledged.
- Acknowledgement language (to be used on copies, publications, and presentations):
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Related references and resources
- Countryside Survey project overview and methodologies (website and various reports)
- Key publications including:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
  - Scott (2007) CS Technical Report No.4/07: Statistical methodology for national estimates from 1 km squares
  - Bunce et al. (1996, 1981, 2007) ITE Land Classification of Great Britain
  - Jackson (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification

## Relevance to environmental monitoring and policy
- Illustrates standardised, verifiable data processes for assessing environmental health over time.
- Demonstrates aggregation of field data into national habitat stock estimates by land class.
- Provides spatially explicit outputs (maps and raster bands) suitable for reporting, monitoring policy performance, and enabling data access for reuse.