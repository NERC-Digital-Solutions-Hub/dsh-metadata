# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- UKCEH released three new national land cover maps (LCMs): LCM2017, LCM2018 and LCM2019.
- All maps use 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats and align with previous UKCEH classes (LCM2015, LCM2007, LCM2000).
- Production is automated using Bootstrap Training plus Random Forest (RF) classification, enabling annual updates.
- Classification is based on Sentinel-2 Seasonal Composite Images (TOA reflectance) plus 20m Context Rasters; aim is rapid production while maintaining quality.

## Purpose and Scope

- Provide a rapid, UK-wide land cover product with 21 defined classes, offering change-tracking capabilities and compatibility with existing UKCEH/classification schemes.
- Emphasise data production decisions, validation, and future plans to help users make informed usage choices.

## Data Products and Structure

- For each year (2017, 2018, 2019), 42 datasets are produced (GB and NI versions across products):
  - 20m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Dominant Cover (GB and NI)
  - 1km Dominant Aggregate Cover (GB and NI)
  - 1km Percent Cover (GB and NI)
  - 1km Percent Aggregate Cover (GB and NI)
- 20m Classified Pixels: two-band rasters (band1 = most likely class, band2 = confidence 0–100). This dataset preserves detailed landscape features (no MMU generalisation).
- Land Parcels: attributes include gid, _hist (per-class pixel counts per parcel as tuples), _mode, _purity, _conf, _stdev, _n. Gid values differ from LCM2015 to reflect the UKCEH Land Parcel Spatial Framework changes.
- 25m Rasterised Land Parcels: three bands for each parcel (band1 = modal class _mode, band2 = confidence _conf, band3 = purity _purity).
- 1km datasets: 
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- GB and NI extents: GB uses British National Grid (EPSG:27700) and NI uses Irish Grid (EPSG:29903). Each dataset includes GB and NI versions where applicable.

## Data Production and Methodology

- Bootstrap Training: automatically samples historical land cover maps to create training datasets (from LCM2015 for LCM2017–2019). Parcels with ≥99% purity from LCM2015 were used to build bootstrap training sets.
- Random Forest (RF) Classification: balanced training (10,000 samples per class per training set) to classify all pixels in Classification Scenes.
- Training data lineage: Bootstrap Training relies on majority signals over time; the system is designed to bootstrap the next map from the current map’s dominant signal.
- Datasets and software: production uses a bespoke RF classifier integrating WEKA with PostGIS and GDAL tools.
- Seasonal inputs: Sentinel-2 Seasonal Composite Images (TOA reflectance) created per season (winter, spring, summer, autumn) at 20m resolution; seasons may have gaps due to cloud, but the classifier tolerates partial data.
- Context information: 20m Context Rasters (terrain, proximity to buildings, roads, sea, freshwater, foreshore, tidal water, woodland) to reduce spectral confusion.
- Classification Scenes: 
  - GB: 100x100 km tiles (74 overlapping GB Classification Scenes) to ensure balanced training across phenology and geography; multiple classifications may exist for overlaps; visual inspection determines the final cut.
  - NI: a single 43-band (36 spectral + 7 context) Classification Scene per year determined by NI’s minimum bounding rectangle.
- UKCEH Land Parcel Spatial Framework: maintains ~0.5 ha MMU; parcels are used to structure 20m Classified Pixels; framework adjusted for performance; gid changes mean cross-year parcel comparisons require spatial overlap rather than parcel-id matches (gid differences acknowledged).
- Change detection and time series: intended to enable annual change understanding; however, parcel identifiers do not match exactly year-to-year due to spatial framework changes.
  
## Classification Inputs and Data Realisation

- Seasonal Composite Images: Sentinel-2 bands 2,3,4,5,6,7,8,11,12 used; 4-season composites designed to capture phenology; Google Earth Engine provides TOA (SR data considered but not adopted for these products).
- Context Rasters: GB (10+ context rasters including height, aspect, slope, urban/road/flood proximities, foreshore, tidal, woodland masks); NI context rasters include height, aspect, slope plus NI-specific urban and proximity layers.
- Classification Scenes and Output: GB uses multiple overlapping scenes to ensure robust training data coverage; NI uses a single scene per year.

## Validation, Accuracy, and Caveats

- Product validation: UK-scale validation using GB countryside survey (2019), National Forest Inventory, IACS data, and bespoke validation points (22,325 points total).
- Reported overall accuracy (producer's/user’s accuracy oriented) for the three years:
  - LCM2017: about 78.6% overall
  - LCM2018: about 79.6% overall
  - LCM2019: about 79.4% overall
- Validation notes:
  - Validation data sources differ from actual class definitions; conversions between schemes involved subjectivity.
  - The validation sample is not an absolute truth but the best available indicator; accuracy is expected to improve as methods mature.
- Output guidance: outputs are intended for broad-scale application and change detection; outputs include detailed per-class confusion matrices and user/producer accuracies (Appendix 4 contains full confusion matrices and validation details).

## Class Definitions and Colour Encoding

- 21 UKCEH Land Cover Classes (aligned with LCM2015/LCM2007/LCM2000 lineage; not exactly UK BAP Broad Habitats but linked for interpretation).
- Appendix 1 and 2 provide notes on class definitions and the relationship with BAP Broad Habitats; Appendix 3 includes a recommended RGB color recipe for displaying the 21 classes.
- Acknowledges limitations in spectral separation for some habitat types (e.g., Bracken vs Acid Grassland; peatland vegetation) and the role of contextual layers in improving separation for several classes.

## Data Accessibility and Appendix References

- Appendix 5 lists the full set of datasets per year (LCM2017, LCM2018, LCM2019) and dataset naming conventions; includes GB/NI data, and the named products (e.g., 20m Classified Pixels, Land Parcels, etc.).
- The document also details formatting changes, dataset attribute changes (e.g., _hist representation, _conf scaling from 0–255 to 0–100), and the rationale for aligning attribute naming with production software.

## Practical Takeaways for Data Support and Usage

- If you need fine-scale detail and parcel-level summarisation, use 20m Classified Pixels or 25m Rasterised Land Parcels; for broader area analyses, use 1km Percent/Dominant products.
- When combining with other datasets, be mindful of the gid changes and cross-year parcel comparisons; use spatial overlap for temporal comparisons.
- Take into account the 21-class structure and consider using the 1km Percent/Percent Aggregate products for multi-class composition analyses.
- For mapping and visualization, apply the Appendix 3 color scheme to maintain consistency with the UKCEH palette.
- Expect ongoing improvements in future LCMs as Bootstrap Training and RF methods evolve and more training data become available.