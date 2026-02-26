# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 2007, derived using the 2007 ITE Land Classification. Data correspond to total area in 000s hectares per Land Class and Broad Habitat, with lower and upper 95% confidence intervals. Freshwater habitats were modeled differently from other habitats.
- Includes both a tabular stock dataset and a corresponding raster product for spatial distribution.

## Data assets

- CS007_Broad_Habitat_Stock.csv
  - YEAR: Survey year
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha); may be negative due to the statistical model (treat negatives as 0)
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

- CS2007_Stock.tif
  - 1 km pixel raster; each pixel band represents a Broad Habitat class, with mean percentage estimates of habitat presence within 1 km survey squares sampled across Land Class strata.
  - Band mappings (examples):
    - Broad Habitat 2, Broad Habitat 1 -> Coniferous Woodland (Band 2)
    - Broad Habitat 3, Broad Habitat 1 -> Boundary and Linear Features (Band 3)
    - Broad Habitat 4, Broad Habitat 1 -> Arable and Horticulture (Band 4)
    - Broad Habitat 5, Broad Habitat 1 -> Improved Grassland (Band 5)
    - …and so on through Band 17 (Urban, etc.)

## Spatial and technical details

- Spatial reference
  - Pixel size: 1 km (1000 m)
  - Coordinate system: British National Grid (OSGB36, Transverse Mercator)
- Extent
  - Great Britain
- Data provenance
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data © CEH
- Usage and attribution
  - All CS data must be acknowledged in copies, publications, and presentations
  - Countryside Survey ©; All rights reserved

## Data governance, licensing, and attribution

- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Copyright: Countryside Survey ©; Database Right/Copyright NERC-CEH; All rights reserved

## Data quality, limitations, and caveats

- MEAN_ESTIMATE values may be negative due to the statistical model; treat negative values as zero
- Freshwater habitats were analyzed using a different statistical model than other habitats; cross-comparison should consider this
- Data availability is presented at national (2007) level and 1 km raster resolution; granularity may limit finer-scale analyses
- Data discovery and integration may require cross-referencing Land Class classifications (ITE Bunce et al. series) and corresponding bibliographic sources

## References and provenance

- Countryside Survey project context and UK results (Carey et al., 2008)
- Technical background on generation of national estimates (Scott, 2007; CS Technical Reports No. 4/07)
- Land Classification framework (Bunce et al.; Merlewood Land Classification)
- Habitat interpretation guidance (Jackson, 2000)
- Key sources and methodologies available via Countryside Survey website and associated publications

## Practical implications for Data Leaders

- Data inventory and strategy
  - Catalogue and track this dataset as a national baseline for Broad Habitat stocks by Land Class
  - Use both the CSV stock data and the raster product for cross-validation and spatial analyses
- Data discovery and metadata
  - Ensure robust metadata alignment (columns, units, spatial reference, year, classifications, and model caveats)
  - Maintain clear provenance links to underlying land classification schemes and referenced publications
- Data quality and stewardship
  - Monitor and document treatment of negative MEAN_ESTIMATE values
  - Acknowledge the distinct modeling approach for freshwater habitats when integrating with other habitat datasets
- Access, governance, and collaboration
  - Acknowledge licensing requirements in all outputs
  - Coordinate with data stewards (CEH/NERC) for updates, extensions, or cross-partner data sharing
  - Leverage the 1 km raster for scalable analyses (e.g., policy evaluation, land-use planning) while using the CSV for tabular summaries and uncertainty ranges
- Application and decision support
  - Integrate stock estimates with user needs and policy contexts to prioritize data gathering, gap analysis, and data-product development
  - Consider establishing communities of practice around land-class–habitat data products to enhance coordination and reduce duplication