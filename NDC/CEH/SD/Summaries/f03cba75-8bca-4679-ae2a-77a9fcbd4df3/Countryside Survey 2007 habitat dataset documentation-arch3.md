# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- Provides national estimates of Broad Habitat stock (Habitats 1-17) for 2007, derived from the 2007 ITE Land Classification.
- Outputs include total area per Land Class in 000s hectares and mean estimates with 95% confidence intervals (lower and upper), noting that freshwater habitats used a different statistical model.
- Notes that some mean estimates may be negative due to the statistical model; these should be treated as zero.
- Includes mapped estimates from Countryside Survey 2007 as a 1 km pixel raster (CS2007_Stock.tif), with per-pixel mean percentage estimates for each Broad Habitat band.

## Data Files and Contents
- CS007_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE
  - Purpose: National estimates of Broad Habitat stock by Land Class for 2007 (Habitat 1–17) using the 2007 ITE Land Classification.
  - Notes: Freshwater habitats analyzed with a different model; negative MEAN_ESTIMATE values should be treated as 0.
- CS2007_Stock.tif
  - Spatial raster (1 km pixel size, OSGB36 / British National Grid)
  - Bands: Each band corresponds to a Broad Habitat class; values represent mean percentage of habitat within each 1 km square.
  - Band-to-habitat mapping is provided (e.g., Band 2 corresponds to Broad Habitat 2 in conjunction with specific Land Class strata; detailed pairings listed in the file notes).

## Spatial Reference and Format
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent and band assignments align with the 1 km survey squares within Land Class strata

## Usage, Interpretation and Scope
- Used to quantify habitat stock and inform monitoring frameworks at national and land-class levels.
- Enables spatially explicit assessment of habitat distribution (via the raster) and aggregated area estimates (via the CSV).
- Provides a baseline for 2007 Countryside Survey results and supports trend analysis when paired with comparable data from other years or studies.
- Data should be cited and acknowledged as Countryside Survey data owned by NERC-Centre for Ecology & Hydrology.

## Metadata, Quality and caveats
- Freshwater habitats are modeled using a different statistical approach than other Broad Habitats.
- Some mean estimates may be negative; policy: treat as zero.
- Completeness and compatibility of metadata can affect verification; cross-reference with associated technical reports for methodology.
- Data governance considerations apply to sharing and reuse of underlying datasets and derived outputs.

## Access, Licensing and References
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; data © CS
- Relevant publications and references include:
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - CS Technical Report No.4/07: Statistical methods for national estimates (Scott, 2007)
  - ITE Merlewood Land Classification background (Bunce et al., 1996; 1981)
  - Countryside Survey Field Mapping Handbook (CS Technical Report No.1/07)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)

## Practical Considerations for Monitoring Frameworks
- Uses:
  - Derive policy-relevant habitat stocks by land class for 2007 as a baseline.
  - Support spatially explicit monitoring with 1 km raster data to identify regional patterns and priority areas.
  - Inform governance decisions on data collection, reporting, and open data practices.
- Data gaps and barriers:
  - Potential lack of up-to-date data and metadata gaps; reliance on party-provided metadata and methodology reports.
  - Public sharing of underlying data can pose barriers; explicit data governance and openness standards are essential at the source.