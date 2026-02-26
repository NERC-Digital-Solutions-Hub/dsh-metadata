# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- UKCEH released three new national land cover maps: LCM2017, LCM2018 and LCM2019, each representing 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and aligned with the 2015 map for comparability.
- All three maps were produced automatically using Bootstrap Training combined with a Random Forest classifier, enabling near-annual updates without manual corrections.
- The dataset suite is provided for Great Britain (GB) and Northern Ireland (NI), with 42 datasets in total (3 years × 2 regions × multiple products).

## Data content and structure

- UKCEH Land Cover Classes and Aggregates
  - 21 UKCEH Land Cover Classes (GB/NB) derived from BAP Broad Habitats; 10 UKCEH Aggregate Classes.
  - Table relationships describe how classes map to BAP Broad Habitats and include notes on specific splits (e.g., Urban vs Suburban; Saltwater vs Freshwater).

- Core dataset products (per year and region)
  - 20m Classified Pixels (GB and NI)
    - 2-band, 8-bit rasters: Band 1 = most likely UKCEH class; Band 2 = class membership probability (0–100).
    - Preserves fine detail (no generalisation by land parcels).
  - Land Parcels
    - Attributes derived from intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Key attributes: gid, _hist (histogram of class occurrences per parcel), _mode (dominant class), _purity (percentage of modal class), _conf (mean class-membership probability), _stdev, _n (count of pixels).
    - Gid values differ from LCM2015; useful for cross-year comparison via gid only between LCM2017–2019.
  - 25m Rasterised Land Parcels
    - 3-band raster (band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km Raster Datasets (intermediate generalisation)
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)

- Spatial extents and grids
  - Great Britain uses GB British National Grid (EPSG:27700).
  - Northern Ireland uses Irish Grid (EPSG:29903).
  - 20m Classified Pixels are provided for GB; 25m Land Parcels and 1km rasters are provided for both GB and NI where applicable.
  - Datasets are duplicated per year, yielding 42 main datasets (GB/NI × 3 years × products).

## Production methodology

- Sentinel-2 seasonal data
  - Seasonal Composite Images per season (winter, spring, summer, autumn) created from Sentinel-2 reflectance (TOA used; SR did not improve classification in this study).
  - Seasonal data are combined with 10 Context Rasters to form Classification Scenes.

- Bootstrap Training
  - Bootstrap Training generates training data automatically from historic maps (starting from LCM2015) to train a Random Forest classifier.
  - For LCM2017–2019, parcels with >= 99% purity from LCM2015 were used to bootstrap the training set; future bootstraps planned from majority signals across several years.

- Random Forest classification
  - Training uses balanced sampling: 10,000 samples per class from each training scene.
  - The classification yields the 20m Classified Pixels product, which then informs the higher-level parcel-based products.

- Classification Scenes and geographic tiling
  - GB: Overlapping 100x100 km tiles used to extract 36-band Seasonal Composite Images; combined with Context Rasters to create 46-band GB Classification Scenes; 74 overlapping scenes classified independently and visually reconciled to produce final results.
  - NI: A single 43-band Classification Scene per year based on the minimum bounding rectangle around NI land mass.

- UKCEH Land Parcel Spatial Framework
  - The framework (0.5 ha MMU) is unchanged in geometry from LCM2015, but storage order and indices were updated for speed.
  - The gid values differ from LCM2015; parcel-level comparisons between 2017–2019 should use gid or spatial overlap, not direct gid matching.
  - The framework supports summarising 20m Classified Pixels into parcels, enabling robust change detection while preserving parcel-level context.

- Validation
  - UK-scale validation used 22,325 points from various sources (Countryside Survey, NFI, IACS, manual interpretation).
  - Reported overall accuracy:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation notes emphasize that accuracy is an informative indicator, not absolute truth, and conversions between class schemes can introduce subjectivity.

## Practical notes for GIS specialists

- Class and parcel relationships
  - 21 UKCEH Land Cover Classes correspond to UK BAP Broad Habitats; tables provide mapping and nuances (e.g., Saltwater vs Freshwater, Urban vs Suburban).
  - Appendix material explains class definitions and detection considerations, including common spectral confusions and the role of context rasters.

- Data usage and cautions
  - No manual corrections were applied this release; results rely on automated classification plus visual validation.
  - Gid-based parcel comparisons across 2017–2019 are not direct year-to-year parcel-id matches; use gid for cross-year parcel comparisons or spatial overlap for change assessment.
  The 20m Classified Pixels dataset preserves detailed landscape patterns but is not generalised, which may affect downstream analyses that rely on aggregation.

- Future and planning notes
  - The production approach removes manual pre-processing steps, enabling annual updates; future years may expand to include additional data sources (e.g., radar) or different signal processing.
  - The methodology anticipates improving gap filling in seasons with cloud cover (e.g., via additional optical sources or Sentinel-1 SAR).

## Appendices and references (highlights)

- Appendix 1 and 2: Detailed notes on UKCEH Land Cover Classes and UK BAP Broad Habitats; guidance on interpretation, detection limitations, and class derivations.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes (optional for visualization).
- Appendix 4: Validation tables and confusion matrices illustrating class-wise performance and overall accuracy.
- Appendix 5: Full dataset list and metadata per LCM2017, LCM2018, and LCM2019 (dataset names, regions, and holdings).