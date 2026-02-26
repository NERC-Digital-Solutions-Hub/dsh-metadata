# Broad Habitat Area Estimates by Land Class for Great Britain

## Aim and scope
- Provides national estimates of Broad Habitat stock (Habitats 1-17) for 2007 using the 2007 ITE Land Classification.
- Outputs include total area by Land Class with lower and upper 95% confidence limits; freshwater habitats use a different statistical model.
- Suitable for monitoring environmental health and policy performance over time, in line with standardised datasets.

## Data products and formats
- CS007_Broad_Habitat_Stock.csv
  - Year (YEAR): Year of Survey
  - Land class (LAND_CLASS): ITE Land Classification
  - Broad Habitat code (BROAD_HABITAT)
  - Broad Habitat name (BROAD_HABITAT_NAME)
  - Land class area (LAND_CLASS_AREA): total area of relevant Land Class (000s ha)
  - Mean estimate (MEAN_ESTIMATE): mean area of Broad Habitat for the Land Class (000s ha); may be negative due to model; treat as 0
  - Lower estimate (LOWER_ESTIMATE): lower 95% confidence limit (000s ha)
  - Upper estimate (UPPER_ESTIMATE): upper 95% confidence limit (000s ha)

- CS2007_Stock.tif (raster)
  - 1 km pixel bands; each band corresponds to a Broad Habitat class
  - Pixel values represent mean percentage of habitat within each 1 km square, based on 1 km survey squares within each Land Class stratum
  - Band-to-habitat mappings described (e.g., Band 2 = Broad Habitat 2/Coniferous Woodland, etc.)

## Data content details
- Broad Habitat coverage includes Habitats 1-17, with mapping between habitat codes and descriptive names (as defined in Jackson 2000 and related references).
- The dataset integrates information from the Countryside Survey 2007 and the ITE Merlewood Land Classification system.

## Spatial reference and technical details
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator Great Britain
- Extent: Great Britain

## Data quality, caveats and interpretation
- MEAN_ESTIMATE may be negative due to statistical modeling; interpret negative values as zero.
- Freshwater habitats are modeled separately from other habitats.
- Spatial raster provides mean percentages per 1 km pixel within Land Class strata, requiring careful aggregation to national totals.

## Usage, access and attribution
- Data must be acknowledged as Countryside Survey data owned by NERC - CEH.
- Full provenance notes and references provided for methodologies and classification schemes (ITE Land Classification; Countryside Survey reports; statistical methodology).

## Relevance for monitoring and transparency
- Supports standardized, reproducible monitoring of environmental habitat extent and change over time.
- Facilitates cross-comparison with policy performance and other environmental health indicators.
- Aligns with the goals of making underlying data accessible to others and enhancing dataset reuse.