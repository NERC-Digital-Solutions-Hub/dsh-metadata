# Dataset documentation

## Overview
- Land Cover Change 1990-2015 (LCC1990_2015) is a 5-band, 25m raster dataset produced from simplified versions of LCM1990 and LCM2015.
- The product enables change mapping over 25 years and supports Land-Use and Land Cover Change (LULUCF) tracking for greenhouse gas inventories.
- GB and Northern Ireland (NI) have separate data sets due to differing projections.

## Data Product and Structure
- 5-band raster:
  - Band 1: Simplified 1990 classes (6 classes) from LCM1990.
  - Band 2: Simplified 2015 classes (6 classes) from LCM2015.
  - Band 3: Binary change layer (0 = no change, 1 = change).
  - Band 4: 'Change from' class (0-6) for areas undergoing change.
  - Band 5: 'Change to' class (0-6) for areas undergoing change.
- Two principal use modes:
  - Bands 1-2 provide complete UK coverage and can be used as model inputs; the difference between 1990 and 2015 reflects change.
  - Bands 3-5 provide partial coverage limited to changed areas, suitable for analyses of location, extent, and type of changes.
- Class structure:
  - Six simplified classes mapped from the original 21 LCM classes: Woodland, Arable, Grassland, Water (Freshwater), Built-up areas, Other.
  - Table 3 maps these six to the corresponding LCM classes; bands 1-3 use 0 for no change where appropriate.

## Corrections and Quality Assurance
- Corrections applied to mitigate known issues before change detection:
  - Inter-tidal areas: changes between inter-tidal water classes excluded from bands 3-5.
  - Rock/non-rock changes above 600m: excluded using NextMAP DEM to reduce errors.
  - River fragments and water bodies: false positives removed by using river networks and manual masking.
- Corrections applied to bands 3-5 (and to band 1 for model input consistency).
- QA checks performed, including projection validity, spatial completeness, band integrity, pixel size accuracy, and adherence to the band specifications.
- A full validation exercise was conducted against other datasets (e.g., Countryside Survey, National Forest Inventory); results to be published separately.

## Derivation and Context
- LCM1990 and LCM2015 were originally 21-class maps. They were aggregated into 6 simplified classes to improve change-mapping accuracy and support GHG inventory needs.
- The change product is designed to facilitate national-scale change analysis and aligns with GB and NI land-cover datasets used in environmental reporting.

## Data Access, Format, and Metadata
- Access: CEH Environmental Information Platform (EIP) at https://eip.ceh.ac.uk/ .
- Coverage and projections:
  - Great Britain (GB) and Northern Ireland (NI) provided as separate data sets with different projections.
- Spatial details:
  - Pixel size: 25m for both GB and NI.
  - GB: 28,000 columns × 52,000 rows; NI: 7,600 columns × 6,400 rows.
  - Lower-left coordinates: GB (0,0); NI (180,000, 300,000).
  - Data type: Unsigned, uncompressed 8-bit GeoTIFF for both GB and NI.
  - Coordinate systems: GB – British National Grid (EPSG 27700); NI – TM75 Irish Grid (EPSG 29903).
- Files are distributed as uncompressed GeoTIFFs; compressible if saved in a different format.
- References to DOIs and dataset documentation:
  - Each Land Cover Change product has a DOI for citation.
  - Queries: spatialdata@ceh.ac.uk
  - A journal paper documenting the data is in preparation.

## Usage and Citations
- DOIs provided for GB and NI datasets; include author(s) and date in text and full DOI in references when citing.
- Example DOIs:
  - GB 25m raster: Rowland et al. (2020)
  - NI 25m raster: Rowland et al. (2020)
- Data citation is encouraged to ensure methods are clear and repeatable.

## Acknowledgements and References
- Acknowledgement: Supported by NERC award NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.
- Key references:
  - Jackson, 2000 (Biodiversity Broad Habitat Definitions)
  - Rowland et al., 2017a, 2017b (LCM2015 GB and NI)
  - Rowland et al., 2020a, 2020b (LCM1990 GB and NI)
- Additional dataset documentation and DOIs are provided to enable reproducibility and proper data citation.