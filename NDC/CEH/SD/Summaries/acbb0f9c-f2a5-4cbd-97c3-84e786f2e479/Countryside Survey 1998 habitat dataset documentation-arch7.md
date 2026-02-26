# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 1998, calculated using the 2007 ITE Land Classification.
- Estimates provided as total area (in 000s hectares) per Broad Habitat per Land Class, with lower and upper 95% confidence intervals.
- Freshwater habitats were analyzed with a different statistical model from other habitats.
- Field survey conducted in 1998 (with a few sites in 1999); commonly referred to as the Countryside Survey 2000.

## Data Files

- CS1998_Broad_Habitat_Stock.csv
  - Contains: YEAR, LAND_CLASS (ITE Land Class), BROAD_HABITAT (Broad Habitat code), BROAD_HABITAT_NAME (description), LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).
  - Notes:
    - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
    - Year indicates the survey year; the dataset refers to 1998 (some sites 1999) but is often cited as Countryside Survey 2000.

- CS1998_stock.tif
  - A 1 km resolution raster (.tif) where each band represents a Broad Habitat class.
  - Each 1 km pixel contains a mean percentage estimate of the amount of that habitat within the pixel, derived from 1 km survey squares within each Land Class strata.
  - Bands are mapped to Broad Habitat classes (detailed mapping provided in accompanying documentation).
  - Spatial Reference: 1 km pixels; Coordinate system: British National Grid (OSGB36); Projection: Transverse Mercator; Extent: Great Britain.

## Data Details and Interpretation

- Habitat and land-class linkage
  - Estimates are presented per Land Class (ITE Land Classification) and Broad Habitat (1–17).
  - The dataset integrates data across land classes to produce national habitat area estimates for each Broad Habitat.

- Raster data interpretation
  - The CS1998_stock.tif raster consists of 17 bands (one per Broad Habitat class), with each pixel value representing the mean percentage of that habitat in the corresponding 1 km cell.
  - A detailed band-to-habitat mapping guide is provided in the accompanying materials.

- Coverage and scope
  - Spatial extents cover Great Britain.
  - Data are rooted in Countryside Survey 1998 methodology and the 2007 ITE Land Classification framework.

## Spatial Reference and Technical Details

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB1936)
- Projection: Transverse Mercator
- Extent: Great Britain
- Data use requires acknowledgment to NERC - Centre for Ecology & Hydrology

## Usage Notes and Considerations for GIS Work

- Data quality and preparation
  - Be aware that some MEAN_ESTIMATE values may be negative due to the statistical model; convert negatives to zero for practical map display.
  - Freshwater habitat estimates were produced with a different statistical approach; consider this when integrating with other habitat layers.

- Time and classification context
  - The data reflect 1998 field survey results; classifications are based on the 2007 ITE Land Classification framework.
  - The Countryside Survey 1998 dataset is frequently cited as Countryside Survey 2000 in literature and metadata.

- Acknowledgment and rights
  - All CS data must be acknowledged in publications, maps, and presentations.
  - Acknowledgement language: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © NERC- Centre for Ecology & Hydrology.”

## Provenance, References, and Useful Links

- Primary source: Countryside Survey data (1998) for Broad Habitat stock and 1 km raster.
- Related publications and references include technical reports and methodology documents detailing:
  - Statistical methods for deriving national estimates from 1 km squares
  - ITE Land Classification of Great Britain 2007
  - Guidance on interpretation of Biodiversity Broad Habitats
- Relevant sources and project pages:
  - Countryside Survey website and outputs
  - Listed reports and datasets in the accompanying references section

## Practical GIS Actions

- Load CS1998_Broad_Habitat_Stock.csv to review per-Land-Class, per-Broad-Habitat areas and confidence intervals.
- Load CS1998_stock.tif to visualize 17-band habitat masks; use band mapping to display each Broad Habitat as a separate layer or composite with appropriate transparency.
- Prepare a map showing national Broad Habitat distribution by Land Class, ensuring proper handling of negative MEAN_ESTIMATE values and applying 0 lower bounds where needed.
- Include proper attribution to Countryside Survey (NERC-CEH) on all outputs.