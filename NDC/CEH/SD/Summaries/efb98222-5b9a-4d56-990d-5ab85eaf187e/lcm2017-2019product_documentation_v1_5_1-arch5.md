# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Three new UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019
- Built from 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with an automatic production workflow
- Aimed at rapid, annual UK-wide mapping with ongoing validation and future improvements

## Purpose and scope

- Provides a user guide for the three products, detailing content, structure, production decisions and validation
- Data produced automatically using Bootstrap Training and Random Forest classifiers
- Sentinel-2 Seasonal Composite Images (TOA) at 20 m resolution combined with Context Rasters to create Classification Scenes
- Emphasizes understanding production choices to support informed use and future planning

## Data content and structure

- Dataset suite duplicated for each year and region, totaling 42 datasets (GB and NI across three years)
  - 20 m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25 m Rasterised Land Parcels (GB and NI)
  - 1 km Dominant Cover (GB and NI)
  - 1 km Percent Cover (GB and NI)
  - 1 km Percent Aggregate Cover (GB and NI)
  - 1 km Dominant Aggregate Cover (GB and NI)
- Coordinate systems
  - Great Britain: GB National Grid (EPSG: 27700)
  - Northern Ireland: Irish Grid (EPSG: 29903)
- Pixel and raster details
  - Classified Pixels: 20 m, 2-band raster (class, membership probability 0–100)
  - Land Parcels: attributes with 20 m to 25 m aggregation; detailed histograms, mode, purity, uncertainty
  - 25 m Rasterised Land Parcels: 3 bands (mode, conf, purity)
  - 1 km rasters: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant/Dominant Aggregate (1 band each)
- Dataset relationships and lineage
  - Datasets follow the 2015 structure with an added 20 m Classified Pixels dataset
  - Land Parcel Spatial Framework used to summarize 20 m pixels into parcels
- Visual and descriptive guidance
  - Appendix figures and color recipes provided for consistent display
  - Detailed cross-year and cross-class relationships described to aid interpretation

## Production approach and methodology

- Bootstrap Training
  - Automatic training set built from historic UKCEH LCMs (not requiring new field data)
  - Uses majority signal across time; selects parcels with high purity (>= 99%) from LCM2015 as training seeds
  - Plans to bootstrap future maps from majority signals across recent years
- Random Forest classification
  - 10,000 samples per land cover class drawn with replacement for balanced training
  - Training data derived from Bootstrap Training, classification scenes created from 36-band Seasonal Composite Images plus 20 m Context Rasters
  - GB production uses 74 overlapping 100 x 100 km tiles; NI uses a single 43-band classification scene
- Context rasters
  - 20 m rasters providing terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal water, and woodland
  - Aids disambiguation of spectrally similar land-cover classes
- Seasonal Composite Images
  - Sentinel-2 bands used to generate four-season composites (winter, spring, summer, autumn)
  - TOA reflectance chosen over surface reflectance (SR) based on evaluation during production
  - Some seasonal gaps may occur due to cloud; future plans to test alternative inputs (e.g., Sentinel-1)
- Classification Scenes and tile strategy
  - GB: overlapping 100 x 100 km tiles to ensure diverse training and manageable processing
  - NI: single tile per year for efficiency
- Land Parcel Spatial Framework
  - Maintains 0.5 ha minimum parcel size; unchanged geometry from LCM2015 but reindexed for faster processing
  - gid identifiers differ from LCM2015; use gid for cross-year comparisons

## Data quality, validation and accuracy

- Validation approach
  - UK-scale validation using GB countryside survey 2019, National Forest Inventory, IACS, plus bespoke LCM validation points
  - Total validation points: 22,325
- Reported overall accuracy (UK scale, 21 classes)
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes
  - Validation dataset is not a guaranteed truth; conversions between class schemes introduce subjectivity
  - The same validation points were used across the three products, so accuracy relative to each product varies
  - Appendix 4 contains full correspondence tables and validation details
- Product consistency
  - Approximately 80% overall correspondence across products is considered impressive for an automatic 21-class map

## Production decisions and limitations

- Automated production yields rapid, coast-to-coast UK maps but with typical classification errors
- No manual corrections were performed this time to enable annual updates
- Some class delineations reflect the limitations of remotely sensed data and the breadth of BAP Broad Habitat categories
- Future improvements anticipated through additional data sources and training data refinement

## Practical considerations for data stewards and users

- Data governance and versioning
  - Clear versioning (v1.5.1) and year-specific datasets enable traceability and reproducibility
  - gid and parcel-based identifiers are not directly comparable year-to-year; use gid for cross-year parcel comparisons
- Interoperability and metadata
  - Comprehensive metadata across datasets (extents, pixel sizes, bands, and class definitions) provided
  - Appendix 1–3 offer class definitions, legends, and color schemes to support consistent visualization
- Change management and future planning
  - Annual update cycle with planned enhancements to Bootstrap Training and input data (e.g., exploring SAR or expanded SR usage)
  - Ongoing validation and alignment with evolving biodiversity and land-cover class definitions
- End-user guidance
  - Users should be aware of potential spectral confusion among grassland, arable, and various habitat types
  - Context rasters and seasonal data improve classification in ambiguous regions; usage should consider these ancillary layers

## Appendices and supplementary context (highlights)

- Appendix 1–2: UKCEH Land Cover Classes and Biodiversity Action Plan Broad Habitats definitions and mappings
- Appendix 3: Recommended RGB color mappings for display
- Appendix 4: Detailed validation results and confusion matrices
- Appendix 5: Full list of datasets by year, region, and product
- References: foundational works on bootstrap training, random forests, and prior UKCEH LCM reports