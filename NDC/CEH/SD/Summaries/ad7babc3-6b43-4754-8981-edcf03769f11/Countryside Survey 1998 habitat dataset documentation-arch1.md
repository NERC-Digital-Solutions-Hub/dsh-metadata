# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1-17) for 1998, calculated using the 2007 ITE Land Classification; results expressed as total area in thousands of hectares with lower and upper 95% confidence intervals. Freshwater habitats were modeled separately.
- Field survey conducted in 1998 (with a few sites in 1999); often referred to as Countryside Survey 2000.
- Land Class basis: ITE Merlewood Land Classification (Bunce et al. updates) used to derive habitat stock; Broad Habitat names aligned with Jackson (2000) guidance.
- Data intended for national-scale analysis and reporting; suitable for identifying patterns, trends, and informing policy or research at broader scales.

## Data Files
- CS1998_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS (ITE text), BROAD_HABITAT (code), BROAD_HABITAT_NAME (description), LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).
  - Notes: MEAN_ESTIMATE can be negative due to the statistical model; treat negative values as 0 in analyses.
- CS1998_stock.tif
  - A 1 km resolution raster where each band represents a Broad Habitat class; each 1 km pixel contains a mean percentage estimate of that habitat within the square.
  - The document provides a band-to-habitat crosswalk (mapping between bands and Broad Habitat classes); consult the metadata for the exact band mappings.

## Data Structure and Mapping
- Raster bands capture habitat distribution across Great Britain at 1 km resolution, derived from 1 km survey squares within each Land Class stratum.
- Each band corresponds to a Broad Habitat class; the accompanying documentation lists the precise crosswalk between bands and habitat names.

## Spatial Reference and Extent
- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain

## Usage Notes and Quality Considerations
- The dataset provides national-level estimates; applicability to local or finer-scale analyses may be limited by scale and reporting units.
- Negative MEAN_ESTIMATE values are possible due to the statistical modeling approach; convert to zero for analysis purposes.
- Freshwater habitats were modeled with a different statistical approach than terrestrial and other habitat types; consider this in cross-habitat comparisons.
- Data sources and classification schemes come from the ITE Land Classification and related Countryside Survey methodologies; ensure consistent use of classifications when combining with other datasets.

## Access and Acknowledgement
- All use of Countryside Survey data must include the following acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC-CEH. All rights reserved.

## References and Related Work
- Countryside Survey project overview and methodologies: Countryside Survey website and outputs
- Key technical references on methods and classifications:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
  - Scott (2007) CS Technical Report No. 4/07: Statistical methods for national estimates
  - Bunce et al. (1996, 1981, 2007): ITE Land Classification of Great Britain
  - Jackson (2000) Guidance on interpretation of the Biodiversity Broad Habitat Classification
- Data access and identifiers can be found through the Countryside Survey and CEH data portals.