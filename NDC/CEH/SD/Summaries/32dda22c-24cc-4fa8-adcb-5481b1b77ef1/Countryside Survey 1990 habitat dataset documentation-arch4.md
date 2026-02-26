# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Countryside Survey 1990 estimates of Broad Habitat areas in Great Britain.
- National stock estimates (Habitats 1-17) for 1990 calculated using the 2007 ITE Land Classification.
- Units are total area in thousands of hectares (000s ha) per Land Class and Broad Habitat, with lower and upper 95% confidence limits.
- Freshwater habitats analysed with a different statistical model; no separate Montane (BH15) class in 1990.

## Data files and structure

- CS1990_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
      - Note: negative values may occur due to the statistical model; treat as 0
    - LOWER_ESTIMATE: Lower 95% CI (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI (000s ha)

- cs1990_stock.tif
  - Raster: in each 1 km pixel, mean percentage value of habitat for that Broad Habitat within the Land Class strata.
  - Bands correspond to Broad Habitat classes; 1 km resolution.
  - Mapping caveat: no Montane class in 1990; Band 15 = BH16, Band 16 = BH17.

## Spatial and projection details

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB1936), Transverse Mercator
- Extent: Great Britain

## Data use, attribution, and rights

- All use of Countryside Survey data must be acknowledged.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Copyright: Countryside Survey ©, NERC-CEH. All rights reserved.
- Acknowledgement and copyright apply to copies, publications, reports, and presentations.

## Data quality, caveats, and interpretation

- MEAN_ESTIMATE values may be negative due to the statistical model; treat as 0.
- Freshwater habitats use a different model from other habitats.
- In 1990, there was no Montane (BH15) class; adjustments noted in raster band mappings.
- Band-to-habitat mappings defined for 1 km raster (e.g., Band 2 corresponds to Broad Habitat 2 for certain Land Classs).
- Confidence intervals (lower/upper) accompany the main estimates, indicating uncertainty.

## Considerations for data leaders (data strategy and governance)

- Data coverage and granularity:
  - National stock estimates by 1 km Land Class strata; total areas summarized per Broad Habitat.
  - Raster data enables spatial analyses at 1 km resolution; suitable for regional planning and landscape-scale assessments.
- Data discovery and metadata:
  - Metadata includes data source (Countryside Survey 1990), classification system (ITE Land Classification), and spatial reference details.
  - Note the absence of BH15 in 1990 and the model differences for freshwater.
- Data quality management:
  - Be mindful of potential negative mean estimates; apply rule to treat as zero where appropriate.
  - Use confidence intervals to assess uncertainty in spatial planning applications.
- Data integration:
  - Cross-walk between stock CSV and raster bands needed for combined area and spatial analyses.
  - Possible need to align with 1990 classification to other years or with more recent land classifications.
- Access and attribution:
  - Ensure proper acknowledgment in all outputs.
  - Understand licensing restrictions and rights for redistribution and publication.

## References and related publications

- Countryside Survey website and outputs (UK results 2007, methodological reports).
- Carey et al. (2008) Countryside Survey: UK Results from 2007.
- Scott (2007) CS Technical Report No. 4/07: Statistical methods for national estimates.
- Bunce et al. (1996, 2007) ITE Land Classification of Great Britain.
- Jackson (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification.
- Field handbooks and related technical documentation for 1990 Countryside Survey methodology.