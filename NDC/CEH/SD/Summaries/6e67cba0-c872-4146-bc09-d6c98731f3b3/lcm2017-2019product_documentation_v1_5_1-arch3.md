# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Aim
- Provide a user guide for three UKCEH Land Cover Maps (LCMs): LCM2017, LCM2018 and LCM2019.
- Describe content, structure, production decisions, validation, and future plans to help users apply the data for monitoring environmental health, policy scrutiny, and decision-making.

## What the maps are and what they contain
- 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, aligned with prior LCMs for consistency.
- Data products released for each year (2017, 2018, 2019) and for two regions (Great Britain and Northern Ireland), totaling 42 datasets per year.

- Datasets and formats
  - 20m Classified Pixels (new in 2017-2019): RF classification results with per-pixel class (Band 1) and per-pixel confidence (Band 2), preserving fine landscape detail.
  - Land Parcels: parcel-level attributes derived from the 20m classified pixels, including hist, mode, purity, conf, stdev, and n.
  - 25m Rasterised Land Parcels: rasterised representation (3 bands: mode, conf, purity) of Land Parcels.
  - 1km Raster datasets:
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)

- Spatial and grid framework
  - Great Britain: GB National Grid (EPSG:27700)
  - Northern Ireland: Irish Grid (EPSG:29903)
  - Land Parcels have a minimum mapped unit of ~0.5 hectares (MMU); gid identifiers exist, but gid values do not match those from LCM2015 for cross-year parcel comparisons; use gid for year-to-year comparisons within this release.

## Production methods and data structure
- Bootstrap Training
  - Fully automatic training using historic LCM observations (LCM2015) to bootstrap classifier.
  - Uses 99% purity parcels from LCM2015 to build training samples, enabling annual updates with minimal new field data.
  - Future plans envisage bootstraps based on majority signals across multiple years (e.g., 2017–2019 for 2020 map).

- Random Forest classification
  - Training data drawn from Bootstrap Training; 10,000 samples per class with replacement to balance the dataset.
  - Processing uses bespoke UKCEH software integrating WEKA, PostGIS, and GDAL (open source).

- Classification Scenes and tiling
  - Great Britain: overlapping 100x100 km tiles, resulting in 36-band Seasonal Composite Images combined with 20m Context Rasters to create 46-band GB Classification Scenes; 74 overlapping scenes classified independently with manual precedence for final selection.
  - Northern Ireland: a single 43-band Classification Scene per year.

- Seasonal Composite Images and input data
  - Seasonal composites derived from Google Earth Engine using Sentinel-2 TOA reflectance (20m resolution) for four seasons (winter, spring, summer, autumn).
  - Nine Sentinel-2 bands used; some seasonal gaps due to cloud, represented as nulls. Classifier tolerates partial data; gaps may be filled in future with alternative sources (e.g., Sentinel-1 SAR).
  - TOA data chosen over surface reflectance (SR) after evaluation.

- Context rasters (20m)
  - GB: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask.
  - NI: height, aspect, slope, urban mask, distance to coast, freshwater, road networks, etc.

- UKCEH Land Parcel Spatial Framework
  - Framework unchanged in geometry from LCM2015 but with reordering and new indices to speed processing.
  - Parcels predominantly 0.5 ha MMU; used to aggregate 20m Classified Pixels into meaningful real-world units.
  - Provides fixed structure for change detection; supports user-defined parcel structures if preferred (e.g., hydrological catchments, administrative boundaries).

- Validation and quality assurance
  - UK-wide validation against GB countryside survey data (2019), National Forest Inventory data, IACS data, and bespoke validation points (22,325 total).
  - Reported accuracies at national scale:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes acknowledge differences between validation data and product classifications and emphasize that figures are indicators rather than absolute truth.

## How the data are described and presented
- Dataset descriptions and appendices
  - Appendix 1 and 2: notes on UKCEH Land Cover Classes and Biodiversity Action Plan Broad Habitats; guidance on interpretation and detection limitations, including upland and coastal vegetation complexities.
  - Appendix 3: recommended RGB color recipe for displaying the 21 land cover classes.
  - Appendix 4: full validation tables and confusion matrices (UKCEH LCM2017, LCM2018, LCM2019).
  - Appendix 5: full list of datasets by year and region.

- Visual and reporting guidance
  - Figures illustrate data structure and example datasets (20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels) and the generalization effect of 1km products versus 20m detail.

- Data governance and openness
  - Outputs are shared publicly (internal data governance in place for the datasets). Metadata and underlying data are described; some metadata gaps were addressed through originator contact and documentation.

## Applications for monitoring and policy
- Designed to support environmental health monitoring, policy scrutiny, and future decision-making with regularly updated national-scale land cover information.
- The framework emphasizes repeatability, openness, and governance, enabling stakeholders to:
  - Assess land cover change over time at multiple spatial scales (20m, 25m parcel-level, and 1km summaries).
  - Compare current maps with previous UKCEH LCMs for trend analysis, while noting caveats about parcel identifiers across years.
  - Use 20m Classified Pixels and Land Parcels for detailed change detection; 1km products for broader regional assessments.

## Limitations and future plans
- Limitations
  - No manual corrections in this release; classification errors are randomly distributed but persist where data quality varies.
  - Some misclassification remains inevitable due to spectral similarity among land cover types and the inherent challenge of mapping certain BAP Broad Habitats spectrally (e.g., upland peatland vegetation, bracken).
  - Parcel-level cross-year comparisons are hampered by gid changes; cross-year comparisons should use gid within the same release rather than Parcel IDs from prior maps.

- Future directions
  - Annual release cadence to track land cover change (intended going forward beyond 2019).
  - Potential enhancement of gap filling using alternative optical sources and radar data (e.g., Sentinel-1) to address cloud gaps.
  - Exploration of finer parcel frameworks as higher-resolution data become more available; potential reduction of the MMU.
  - Continued refinement of Bootstrap Training strategies, potentially using multi-year majority signals for training data.

## References and related resources
- Foundational references to Random Forests, WEKA, and land cover methodological literature.
- Appendix materials provide detailed descriptions of class definitions, validation, and color schemes to support application and interpretation.