# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- User guide accompanying the release of three UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Explains content, production decisions, validation, and future plans to help users apply the data appropriately.
- Emphasizes reliance on automated production methods to enable annual updates and to understand limitations.

## Production approach and data lineage
- LCMs produced automatically using Bootstrap Training with a Random Forest (RF) classifier.
- Training data drawn from historic UKCEH LCMs (Bootstrap Training) to sample current satellite scenes; aims to leverage majority signal across time.
- Sentinel-2 Seasonal Composite Images (TOA reflectance) per season (winter, spring, summer, autumn) used to generate Classification Scenes with 20m internal context rasters.
- 20m Classified Pixels form the core, with subsequent summaries to Land Parcels, 25m Rasterised Land Parcels, and 1km raster products.
- Global validation performed at UK scale against multiple data sources; manual corrections were not applied this release to enable annual production without labour-intensive pre-processing.

## Datasets and data products
- 20m Classified Pixels (new): per-pixel RF classification with class label and a second band indicating classification confidence (0–100). Keeps high-detail where features fall below MMU.
- Land Parcels: parcel-level attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework; includes _hist, _mode, _purity, _conf, _stdev, _n, with notes on attribute naming changes since 2015.
- 25m Rasterised Land Parcels: three-band raster for each parcel (dominant class, confidence, and purity).
- 1km Raster datasets:
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (1-band)
  - 1km Dominant Aggregate Cover (1-band)
- Geographic coverage and formats:
  - Separate GB and Northern Ireland editions; GB uses Great Britain grid (EPSG:27700) and NI uses Irish grid (EPSG:29903).
  - 42 total datasets released (per year across GB and NI).

## Classification framework and scenes
- Classification Scenes:
  - GB: 74 overlapping 100x100 km tiles, each producing a 46-band classification scene (spectral bands plus context layers).
  - NI: single 43-band scene per year per year determined by the bounding rectangle of NI land mass.
- Context Rasters (20m): include terrain (Height, Aspect, Slope) and proximity masks (buildings, roads, coast, freshwater, urban, etc.) to reduce spectral confusion.
- Seasonal Composite Images: derived from Google Earth Engine using median TOA reflectance for four seasons; some seasonal gaps due to cloud are allowed and RF tolerates partial spectral information.
- Bootstrap Training and RF:
  - Bootstrap Training sources via majority signal from 2015 maps; RF classifier trained with balanced sampling across classes to avoid dominance by common classes.
  - Training data drawn from 2015 LCM parcels (purity >= 99%), with plans to boost future bootstraps using 3-year or multi-year signals.

## UKCEH Land Parcel Spatial Framework
- Framework maps land parcels (~0.5 ha MMU) to reduce classification noise and support change detection.
- gid is a stable parcel identifier, but new LCM2017–2019 gids do not match LCM2015 gid values; comparisons across years should use gid overlaps rather than direct parcel id matches.
- Users can summarize 20m Classified Pixels with their own parcel structures if desired; future refinements may adjust MMU and parcel frameworks.

## Data quality, validation, and limitations
- Validation:
  - UK scale validation using GB Countryside Survey 2019 data, National Forest Inventory, IACS, and bespoke validation points (22,325 in total).
  - Reported overall accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  Note: Validation points are not absolute truth; class mappings required interpretation and could introduce subjectivity.
- Per-class and producer/user accuracies provided in detailed confusion matrices (Appendix 4), illustrating strengths and confusions across UKCEH Land Cover Classes.
- Known limitations and challenges:
  - Some data gaps and metadata issues addressed via direct liaison with data originators.
  - Siloed data and data-sharing considerations noted as potential barriers in monitoring frameworks.
  - Spectral similarity and landscape heterogeneity can cause misclassification in certain habitats (e.g., upland peatland, bracken in acid grassland; coastal Saltmarsh vs. Saltmarsh misattribution risk).

## Metadata, standards, and governance
- The dataset suite includes extensive metadata tables (Tables 2–4) detailing coordinate systems, extents, pixel sizes, and class counts.
- 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with careful mapping to ensure consistency with earlier products (LCM2000, LCM2007, LCM2015).
- Appendices provide guidance on class definitions (Appendix 1), BAP Broad Habitats (Appendix 2), color mapping (Appendix 3), and detailed validation outputs (Appendix 4) and dataset lists (Appendix 5).

## Use considerations for monitoring and decision-making
- Appropriate use requires understanding of automated production decisions (no manual corrections) and the impact on accuracy at high thematic detail.
- The 20m Classified Pixels are ideal for detailed habitat detection and fine-scale monitoring, while 1km products offer more generalized, stable summaries for broader trend analysis.
- The UKCEH Land Parcel Spatial Framework enables consistent time-series comparison within the MMU constraints; cross-year parcel-id matching is limited, but gid-based comparisons are robust.
- The annual production approach supports near-term monitoring and decision-making, with continuous evaluation and potential incorporation of additional data sources to improve gaps and accuracy.

## Future plans and ongoing development
- Aim to release a new LCM annually; exploration of additional data sources (e.g., Sentinel-1 SAR) to fill cloud gaps and potentially improve seasonal completeness.
- Plans to refine training data approaches (e.g., using multi-year majority signals) and to adapt the Land Parcel Framework to evolving resolutions and monitoring needs.
- Ongoing validation resource development and potential improvements to improve per-class accuracies and reduce specific confusions.

## Appendices and ancillary material
- Appendix 1: Notes on UKCEH Land Cover Classes (class definitions, detection notes, potential confusions).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (descriptions and classifications).
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
- Appendix 4: Comprehensive confusion matrices for LCM2017, LCM2018, LCM2019 (per-class and total accuracies; producer and user accuracies).
- Appendix 5: Full list of datasets for LCM2017, LCM2018, and LCM2019 (dataset names, geography, and status).