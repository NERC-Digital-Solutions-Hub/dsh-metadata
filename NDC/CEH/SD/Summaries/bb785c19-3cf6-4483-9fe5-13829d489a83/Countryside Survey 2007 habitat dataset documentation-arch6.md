# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 2007, calculated using the 2007 ITE Land Classification.
- Outputs provided as total area in 000s ha per Broad Habitat and Land Class, with 95% confidence intervals (lower/upper estimates).
- Note: freshwater habitats were analyzed using a different statistical model than the other habitats.
- Data formats include a CSV dataset and a 1 km resolution raster dataset for spatial representation.

## Datasets and file details

- CS007_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Year of Survey (2007)
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha)
      - Note: negative MEAN_ESTIMATES may occur due to the statistical model; treat as 0
    - LOWER_ESTIMATE: Lower bound of 95% confidence interval (000s ha)
    - UPPER_ESTIMATE: Upper bound of 95% confidence interval (000s ha)

- CS2007_Stock.tif
  - Spatial raster with 1 km pixel size; British National Grid
  - Each band represents a Broad Habitat class (as mapped to Land Class strata)
  - Pixel values denote the mean percentage of habitat in that 1 km pixel
  - Coverage is based on 1 km survey squares sampled within Land Class strata
  - Band-to-habitat mappings are provided in the accompanying documentation (e.g., Band 17 corresponds to Urban for Broad Habitat 1)

## Spatial reference and resolution
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator, Great Britain
- Extent: Great Britain

## How to use and interpret

- Data products enable self-serve analyses of habitat distribution by land class:
  - Use the CSV for aggregated totals and confidence intervals by Land Class and Broad Habitat (2007).
  - Use the 1 km raster to map and visualize spatial patterns of habitat presence/cover across Great Britain.
- Important notes:
  - MEAN_ESTIMATE values may be negative; treat negatives as zero.
  - Freshwater habitats were modeled differently; consider this when integrating with other habitat types.
- Potential use cases:
  - Dashboards and maps showing habitat distribution by land class.
  - Derived statistics by region, land class, or habitat type.
  - Temporal comparisons if additional years are available.

## Data quality and caveats
- Negative mean estimates arise from the statistical modeling approach; require conversion to zero where appropriate.
- Freshwater habitat estimates use a different statistical approach; ensure consistent methodology when combining with terrestrial habitats.
- Data are produced from the Countryside Survey 2007; users should consult the referenced technical reports for methodological details.

## Acknowledgement and licensing
- All Countryside Survey data must be acknowledged.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Acknowledgement and copyright information should be used on all copies, publications, and presentations.

## References and publications
- Countryside Survey: UK Results from 2007 (Carey et al., 2008) – overview and methodology.
- Countryside Survey technical reports:
  - CS UK Results 2007 (Technical reports and summaries)
  - CS Technical Report No.4/07: Statistical Report (how national estimates are generated from 1 km survey squares)
  - CS Technical Report No.1/07: Field Mapping Handbook (habitat mapping methodology)
- Land Classification references:
  - ITE Merlewood Land Classification (Bunce et al., 1996; 1981)
- Guidance and interpretation documents for Biodiversity Broad Habitat Classification (Jackson, 2000)