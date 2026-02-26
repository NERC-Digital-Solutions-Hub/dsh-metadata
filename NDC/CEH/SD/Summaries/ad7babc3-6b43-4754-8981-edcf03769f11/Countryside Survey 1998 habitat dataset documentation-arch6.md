# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Data overview
- National estimates of Broad Habitat stock (Habitats 1-17) for 1998 computed using the 2007 ITE Land Classification.
- Estimates are given as total areas in thousands of hectares (000s ha) per Broad Habitat and Land Class, including lower and upper 95% confidence limits.
- Freshwater habitats were analyzed with a different statistical model from other habitats.
- Field survey conducted in 1998 (with a few sites in 1999); commonly referred to as Countryside Survey 2000.

## Data files and structure
- CS1998_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
- CS1998_stock.tif
  - A 1 km pixel raster where each band represents a Broad Habitat class and contains the mean percentage estimate of habitat presence in that square.
  - The band-to-habitat mapping is defined in the dataset documentation (e.g., Band 1/2 mapping to Coniferous/Deciduous woodlands, etc.).

## Column details (CSV)
- YEAR: Year of survey.
- LAND_CLASS: ITE Land Classification code (e.g., Bunce et al. references).
- BROAD_HABITAT: Broad Habitat code.
- BROAD_HABITAT_NAME: Description of Broad Habitat.
- LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha).
- MEAN_ESTIMATE: Mean area estimate for the Broad Habitat within the Land Class (000s ha).
- LOWER_ESTIMATE / UPPER_ESTIMATE: 95% confidence interval bounds (000s ha).

## Spatial and technical details
- CS1998_stock.tif uses 1 km resolution (pixel size 1000 m).
- Coordinate system: British National Grid (OSGB36); Projection: Transverse Mercator.
- Extent: Great Britain.

## Data use and rights
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey copyright and database rights apply; all rights reserved.

## Data interpretation notes
- Negative MEAN_ESTIMATE values should be treated as 0.
- The 1998 field survey results are sometimes referred to as Countryside Survey 2000.
- Freshwater habitat estimates use a different statistical model, affecting comparability with other habitat types.
- Data outputs may be subject to the ITE Land Classification (2007) framework; cross-year or cross-class comparisons should consider methodological differences.

## References and further reading
- Countryside Survey technical reports and publications (e.g., CS 2007 UK Results; Statistical Report No. 4/07 by Scott, W.A.).
- ITE Land Classification of Great Britain (Bunce et al., 2007) and earlier classification descriptions (Bunce et al., 1996; 1981; Barr et al., 1998/3rd Draft Handbooks).
- Related guidance on interpretation of Biodiversity Broad Habitat Classification (Jackson 2000) and supporting background documents from Haines-Young et al. (2000).