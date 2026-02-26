# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock for 1978 by Land Class, calculated using the 1990 ITE Land Classification (as described in Scott, 2007).
- Excludes Broad Habitat codes 15 and 20.
- Units are 000s hectares (000s ha).
- Based on Countryside Survey data (CS) and the 1 km survey square methodology; used to understand habitat distribution and changes over time (contextualized by related Countryside Survey reports).

## Data files and structure

- CS1978_Estimates_by_LC.csv
  - Purpose: National estimates of Broad Habitat by Land Class for 1978.
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class code
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat name
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area estimate of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI bound (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI bound (000s ha)
- CS78_BH1_17.tif
  - Raster data derived from Land Class totals for each Broad Habitat (1–17, excluding 15).
  - Represents percentage of each Land Class area occupied by a Broad Habitat per 1 km pixel.
  - Bands correspond to Broad Habitat classes:
    - Band 1: Broadleaved Mixed and Yew Woodland
    - Band 2: Coniferous Woodland
    - Band 3: Boundary and Linear Features
    - Band 4: Arable and Horticulture
    - Band 5: Improved Grassland
    - Band 6: Neutral Grassland
    - Band 7: Calcareous Grassland
    - Band 8: Acid Grassland
    - Band 9: Bracken
    - Band 10: Dwarf Shrub Heath
    - Band 11: Fen, Marsh, Swamp
    - Band 12: Bog
    - Band 13: Standing Open Waters and Canals
    - Band 14: Rivers and Streams
    - Band 15: Inland Rock
    - Band 16: Urban
- Pixel size: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator GB; Extent: GB

## Data provenance and methodology

- Data origin: Countryside Survey (CS) data, owned by NERC - Centre for Ecology & Hydrology (CEH).
- Classification framework: Derived from the 1990 ITE Land Classification (Bunce et al., 1996; Bunce et al., 1981).
- Methodology references:
  - Scott, W.A. (2007): Technical Report describing how national estimates are generated from 1 km survey squares.
  - Wood et al. (2012): Countryside Survey: Measuring Habitat Change Over 30 Years (1978 Data Rescue – Final Report).
  - CS Technical Reports on habitat mapping and classification (TR1/07; field mapping handbook).
  - Jackson, D.L. (2000): Guidance on interpretation of Biodiversity Broad Habitat Classification.
- Data handling: Data are provided with associated metadata and require acknowledgement; datasets may be used to support habitat-change analyses and crosswalks with other classifications.

## Usage notes and attribution

- All CS data usage requires acknowledgement:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Countryside Survey ©; Database Right/Copyright CEH. All rights reserved.
- Practical considerations for analysts:
  - The 1978 estimates use an older land classification (ITE) and may require cross-walking with newer classifications for temporal comparisons.
  - The TIFF provides pixel-level composition that can be aggregated to produce area estimates or maps at requested scales, with careful handling of overlapping or excluded Broad Habitats (codes 15 and 20 not included in the 1978 CSV).

## References (selected)

- Countryside Survey project overview and methodologies (CS Website).
- Wood, C.M., Howard, D.C., Henrys, P.A., Bunce, R.G.H., Smart, S.M. (2012). Countryside Survey: Measuring Habitat Change Over 30 Years. 1978 Data Rescue – Final Report.
- Scott, W.A. (2007). CS Technical Report No. 4/07: Statistical methods for generating national estimates from 1 km survey squares.
- Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Lane, A.M.J. (1996). ITE Merlewood Land Classification of Great Britain.
- Bunce, R.G.H., Barr, C.J., Whittaker, H.A. (1981). Land Classes in Great Britain: Preliminary Descriptions for Users of the Merlewood Method of Land Classification.
- Jackson, D.L. (2000). Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).