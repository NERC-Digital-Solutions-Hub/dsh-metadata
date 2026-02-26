# The UKCEH Land Cover Map for 2021

## Overview and purpose
- UKCEH LCM2021 is the ninth UK land cover map, produced annually using automated methods.
- Product consists of six datasets: three datasets for Great Britain and Northern Ireland (GB and NI) each containing a 10 m classified-pixel dataset, a dataset of classified land parcels, and a 25 m pixel (rasterised) land parcels dataset.
- Aims to provide a consistent, auditable data product to monitor environmental state and change, with validation and guidance to support informed use.

## Data products and structure
- 10 m Classified Pixel datasets (GB and NI)
  - Derived from multiple classified Classification Scenes; RF classifier assigns a most-likely class and a confidence probability.
  - Band 1: UKCEH Land Cover Class identifier; Band 2: class membership probability.
  - 10 m pixels retain full spatial detail (not generalised by the Land Parcel Spatial Framework) to preserve fine features.
- Land Parcel datasets (GB and NI)
  - Result from intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - Land Parcel attributes include: gid, _hist (histogram of class frequencies), _mode (dominant class), _conf (mean class membership probability), _stdev, _agg (aggregate class), _n (number of pixels).
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - 3-band rasters per parcel: dominant land cover (_mode), confidence (_conf), and purity (_purity).
- 1 km raster products
  - Summary products from 25 m rasters: dominant class at 1 km, percentage cover by class (and by aggregate class).
  - Percentage values are integer-based and may not sum exactly to 100 due to rounding.
- Spatial references
  - GB: OSGB 27700 (British National Grid)
  - NI: Irish Grid TM75 (EPSG 29903)
- Land mass coverage and parcel counts
  - GB parcels: ~6.74 million
  - NI parcels: ~0.90 million
- Extents and resolutions
  - 10 m and 25 m products; 1 km summary products built from 25 m data.

## Data production methodology
- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 reflectance, resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with median reflectance across bands 2,3,4,5,6,7,8,8a,11,12.
  - Occasional cloud gaps; classifier tolerates partial spectral information to produce national coverage.
- Context Rasters
  - 10 m context layers included to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, coast, water, woodland).
  - GB and NI have different sets of context rasters appropriate to each region.
- Classification Scenes and tiles
  - GB classified using 32 Classification Scenes (tiles ~100 x 100 km); NI uses a single Classification Scene.
  - Each Classification Scene is trained and classified independently to manage regional phenology and data processing.
- Training: Bootstrap Training and Random Forest
  - Bootstrap Training uses historical LCM data (LCM2018–LCM2020) filtered for >80% purity and consistent class across years to generate training samples.
  - Training samples are balanced across classes; Random Forest classifier yields the 10 m Classified Pixel product.
  - The process aims to maximize temporal consistency and facilitate change detection.
- Validation and accuracy
  - Formal validation used 35,182 reference points across all 21 classes.
  - Overall accuracy: 82.6% (95% CI: 82.19%–82.99%) on the 25 m rasterised land parcel dataset.
- Data quality and limitations
  - Validation performed against the 25 m Land Parcel dataset; 10 m Classified Pixels were not independently validated against the same spatial framework.
  - Some spectral confusions persist between certain land cover types (see Appendix notes on class relationships and confusions).
  - Saltwater and Freshwater distinctions can be challenging in coastal/estuarine zones; some miscoding possible in tidal areas.

## The UKCEH Land Parcel Spatial Framework and MMU
- Land parcels are generalised units (~0.5 ha minimum MMU) derived from generalising national cartography.
- The parcel framework provides a stable basis for time-series change detection, while 10 m pixels preserve fine landscape features.
- Parcel identifiers (gid) have changed from LCM2015; cross-map comparisons by parcel ID may require spatial overlap rather than direct ID matching.

## Relationship to BAP Broad Habitats (Appendices overview)
- UKCEH Land Cover Classes (21) are linked to UK BAP Broad Habitats but are not a one-to-one match.
- Some mappings are altered for spectral mapping purposes; Appendix 1 and 2 provide details and caution on ambiguities.
- Certain broad habitats are split into multiple UKCEH classes (e.g., Heather vs. Heather Grassland; Urban vs. Suburban) to improve spectral discrimination.

## Use cases for environmental monitoring and policy performance
- Time-series monitoring: annual maps enable differentiation between random classification errors and persistent real-world change (errors tend to flicker year-to-year).
- Change detection: robust for tracking habitat transitions and land cover dynamics, supporting environmental objectives and reporting needs.
- Data integration: rich suite of outputs (10 m pixels, land parcels, 25 m rasters, and 1 km summaries) supports various analytic scales and integration with other datasets.
- Decision support: standardized outputs with accompanying metadata and validation support reproducible analyses and policy evaluation.

## Practical considerations for analysts
- Use 10 m Classified Pixel data for fine-scale mapping and landscape detail; be aware that these are not generalised by the parcel framework.
- Use Land Parcel datasets for structured, change-detection-ready analysis; leverage _hist, _mode, _conf, _purity, and _agg attributes to interpret classifications.
- For summary assessments, employ 1 km products to analyze broad-scale land cover patterns, while acknowledging rounding in percentage calculations.
- Account for potential confusions and region-specific limitations outlined in Appendices (e.g., between certain grassland types, Bog vs. Peat-influenced classes, coastal Saltwater vs. Freshwater near tidal zones).
- When visualizing, refer to Appendix 5/6 color recipes to ensure consistent, interpretable displays; color-blind friendly options are provided.

## Appendices: key references for interpretation and display
- Appendix 1: Notes on UKCEH Land Cover Classes (and their relation to UK BAP Broad Habitats; differences and labeling conventions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats—definitions and how they map to UKCEH classes.
- Appendix 3: Full list of LCM2021 datasets by region and product name.
- Appendix 4: Correspondence matrices and accuracy metrics from validation (class-by-class producer/user accuracies and confusion patterns).
- Appendix 5 & 6: Recommended color recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly variants).