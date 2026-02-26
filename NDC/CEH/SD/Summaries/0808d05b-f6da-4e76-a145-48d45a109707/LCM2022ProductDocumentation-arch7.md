# The UKCEH Land Cover Map for 2022

- The LCM2022 is UKCEH’s 10th national land cover map, produced annually using automated methods. It provides 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan Broad Habitats (BAP) and is produced by classifying Classification Scenes that combine Sentinel-2 Seasonal Composite Images with Context Rasters.
- The product suite comprises seven geospatial datasets for Great Britain (GB) and Northern Ireland (NI): three datasets per region (10 m classified pixels, land parcel datasets, and 25 m rasterised land parcels), plus a 1 km summary raster that covers both GB and NI.
- Accuracy: formal validation reports an overall accuracy of 86.1% at full thematic detail.

## Data products and formats

- 10 m Classified Pixel datasets
  - GB and NI separately.
  - Derived from a mosaic of Classification Scenes; each pixel has:
    - Band 1: UKCEH Land Cover Class identifier (integer).
    - Band 2 (GB) or Band 3 (NI): classification confidence/probability.
  - 10 m pixels are not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine landscape details (e.g., narrow features). Validation was conducted against the 25 m rasterised land parcel dataset, not the 10 m pixels.
- Land Parcel datasets
  - Result from intersecting the 10 m Classified Pixel datasets with the UKCEH Land Parcel Spatial Framework.
  - Provide parcel-level attributes and support change detection.
- 25 m Rasterised Land Parcel datasets
  - GB and NI separately.
  - Three-band rasters per parcel: mode (dominant class), conf (mean confidence across pixels in parcel), and purity (dominance of the modal class).
- Land Parcel Vector product
  - Vector representation of land parcels with parcel-level identifiers and attributes (gid, hist, mode, conf, stdev, agg, n, ogc_fid) to assist spatial analysis and data management.
- 1 km Summary rasters
  - GB and NI combined.
  - Dominant class per 1 km cell (21 classes) plus percentage cover per class (21 bands) and corresponding aggregate classes (10 bands).
  - Percentage values are integers with rounding; coastal areas may sum to slightly less than 100% due to area within the 1 km pixel.
- Coordinate systems and extents
  - GB: British National Grid (EPSG: 27700); extent roughly 0–700000 E, 0–1300000 N.
  - NI: Irish Grid (TM75; EPSG: 29903); extent truncated to NI landmass.
- Seasonality and spectral data
  - Seasonal Composite Images created from Sentinel-2: four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with bands 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12.
  - Context Rasters (10 m) used to reduce spectral confusion (GB: terrain, distance to buildings/roads/water, foreshore, woodland and saltmarsh masks; NI: terrain, urban mask, distances to coast/roads/freshwater, foreshore, tidal water).

## How LCM2022 was produced

- Bootstrap Training
  - Automatic training data generation from historical LCM maps (LCM2019–LCM2021) with >80% probability that agreed on the same land cover class, providing a rich training set without new field data.
  - Helps bootstrap the classifier for the current map, enabling annual production.
- Random Forest classification
  - Balanced training by drawing 10,000 samples per class (with replacement) to train the RF classifier.
  - Produces the 10 m Classified Pixel product and associated class probabilities.
- Software and workflow
  - Custom pipeline combining WEKA, PostGIS, and GDAL; open-source components underpin the workflow.
- Classification Scene strategy
  - GB uses 32 Classification Scenes (tiles ~100 x 100 km each) to cover the land surface; NI uses a single Classification Scene due to smaller extent.
  - Each scene is trained and classified independently to manage regional phenology and data variability.

## Data interpretation and validation

- Validation
  - 33,107 validation points across all 21 classes; overall accuracy 86.1%.
  - Validation data derived from GB countryside surveys, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Known issues
  - A small number of polygons missing from the vector Land Parcel Product, causing nodata gaps in the 25 m rasterised land parcels. Effects are negligible for the 1 km summary rasters; 10 m classified pixels remain unaffected.

## Dataset specifics and key attributes

- Class definitions and relationships
  - UKCEH Land Cover Classes (21) are aligned with but not identical to UK BAP Broad Habitats. Appendices provide mapping notes and how certain classes are split or combined (e.g., Urban vs Suburban; Heather vs Heather grassland; Freshwater vs Saltwater handling).
- Parcel-based attributes (LCM Land Parcel Product)
  - gid: unique parcel identifier
  - _hist: frequency distribution of classes within the parcel
  - _mode: most frequent class within parcel
  - _conf: mean class membership probability (0–100 scale)
  - _stdev: standard deviation of _conf
  - _agg: aggregate class mapping (Table 1 relationships)
  - _n: number of 10 m pixels intersecting parcel
  - ogc_fid: GIS feature identifier
- 25 m parcel rasters
  - Band 1: dominant land cover class (mode)
  - Band 2: conf (mean parcel confidence)
  - Band 3: purity (per-parcel pixel purity)
- 1 km rasters
  - Dominant class in each 1 km cell (1 band)
  - Percentage cover per class (21 bands) and per-aggregate class (10 bands)
  - Note: rounding can cause sums to diverge from 100; coastal pixels may sum to less than 100 due to coastal mapping dynamics

## Practical notes for GIS usage

- Data access and citation
  - Each LCM2022 dataset has a DOI; see Table 5 for exact citations. Reference Marston et al. (2023) for prior production methods and Marston et al. (2024a–g) for LCM2022 data products.
- Colour and styling
  - Appendix 5 and 6 provide recommended colour recipes (including color-blind friendly options) for visualising UKCEH Land Cover Classes in GIS platforms (e.g., QGIS), with accompanying QGIS style files (lcm_raster.qml and lcm_raster_cb_friendly.qml).
- Data interpretation guidance
  - The annual map series supports change detection by differentiating real land cover changes from random classification errors that tend to flicker over time.
  - Users should be aware that method changes across years can introduce minor differences beyond actual land cover change.

## Appendices (highlights)

- Appendix 1: Notes on UKCEH Land Cover Classes (class-specific considerations, potential spectral confusions, and training data caveats)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and relationships to UKCEH classes
- Appendix 3: Full list of LCM2022 datasets and DOIs
- Appendix 4: Correspondence matrices and accuracy metrics by class (user’s and producer’s accuracy)
- Appendix 5: Recommended colour recipe for displaying UKCEH Land Cover Classes
- Appendix 6: Colour-blind friendly colour recipe
- Appendix 7: QGIS style files for standard and colour-blind friendly displays

## What this means for GIS specialists

- Access to high-resolution, year-on-year comparable land cover data for GB and NI, with both pixel-level (10 m) and parcel-level (0.5 ha MMU) representations and a 1 km summary layer for broad-scale analyses.
- Robust classification framework (Bootstrap Training + Random Forest) with detailed context rasters to reduce spectral confusion.
- Clear metadata, validation results, and longitudinal consistency aids change detection, policy reporting, environmental monitoring, and map-based storytelling.
- Ready-to-use visualization assets (colour palettes and QGIS styles) to produce publication-ready maps.