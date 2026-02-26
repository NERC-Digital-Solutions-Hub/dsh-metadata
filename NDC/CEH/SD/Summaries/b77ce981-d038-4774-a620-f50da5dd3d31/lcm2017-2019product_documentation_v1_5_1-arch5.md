# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Overview
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Outputs consist of 21 UKCEH Land Cover Classes (based on UK BAP Broad Habitats) with annual production aims.
- Production approach: automatic Bootstrap Training plus Random Forest (RF) classifier; seasonal Sentinel-2 data processed via Google Earth Engine.
- Release scope: UK-wide maps with Great Britain (GB) and Northern Ireland (NI) versions for each year, totaling 42 datasets.
- Validation indicates maps are of similar quality to the latest predecessor (LCM2015); typical overall accuracy around 78–79% at UK scale.

## Data and Production Methods
- Bootstrap Training
  - Uses historic LCM2015 data (bootstrap majority from 1990–2007) to generate spectral training observations for 2017–2019.
  - Training set built from UKCEH LCM2015 parcels with purity ≥ 99%.
  - Goal: leverage majority signal over short update intervals to train robust RF classifiers.
- Random Forest Classification
  - Balanced sampling: 10,000 samples per land-cover class for RF training.
  - Production software integrates WEKA with PostGIS and GDAL (open-source tools).
  - Classification yields the 20m Classified Pixels product, with a per-pixel probability (Band 2) indicating confidence (0–100).
- Data Inputs
  - Seasonal Composite Images: four-season median TOA reflectance from Sentinel-2, generated in Google Earth Engine (TOA chosen over SR after evaluation).
  - Context Rasters (20m): terrain (Height, Aspect, Slope), proximity masks (building, road, sea, freshwater), foreshore, tidal water, woodland masks.
  - Classification Scenes: GB uses 100x100 km tiles (36-band Seasonal Composites + 10 Context layers; total 46 bands) across 74 overlapping GB scenes; NI uses a single 43-band scene per year.
- Land Cover Classes and Mapping
  - 21 UKCEH Land Cover Classes aligned with UKCEH LCM2015 lineage; closely matched to BAP Broad Habitats (with careful terminology distinctions).
  - Appendix 1–2 describe class derivations and the relationship to BAP Broad Habitats.
- UKCEH Land Parcel Spatial Framework
  - Fixed framework (0.5 ha MMU) used to summarise 20m Classified Pixels into Land Parcels with consistent geometry across years.
  - GID serves as parcel identifier; parcel IDs do not match LCM2015, but GID enables time-series comparisons.
- Datasets and Extents
  - 20m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Raster datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band)
  - 42 total datasets (GB and NI for each year)
- Coordinate Systems
  - GB: EPSG: 27700 (British National Grid)
  - NI: EPSG: 29903 (TM 75 Irish Grid)

## Dataset Descriptions and Differences from LCM2015
- 20m Classified Pixels
  - New addition for LCM2017–2019; RF classification results with per-pixel confidence (Band 2 0–100).
  - Preserves fine landscape detail (no land parcel generalisation).
- Land Parcels
  - Attributes refined: gid (unique parcel id), hist (per-class pixel counts), mode, purity, conf, stdev, n.
  - Several attribute name changes (align with production software); enhanced histogram presentation.
  - The “Composite” attribute from LCM2015 is removed.
  - Parcel gid values do not match LCM2015; use gid for cross-year comparisons.
- 25m Rasterised Land Parcels
  - 3-band raster: band 1 (mode), band 2 (conf), band 3 (purity).
  - Purity and confidence representations updated from floating to percentage scale (0–100).
- 1km rasters
  - 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), 1km Dominant Aggregate Cover (1 band).
- Seasonal Composite Images
  - Sentinel-2 bands and resolutions listed; 4-season coverage with gaps due to cloud, handled by RF tolerance.
  - Decision to use TOA rather than SR data based on current performance.
- UKCEH Land Parcel Spatial Framework
  - Framework retained from LCM2007/LCM2015 lineage; minor storage/index changes; GB NI parcel counts remain large (GB ~6.7M parcels, NI ~0.9M).
- Context Rasters
  - GB and NI context layers differ slightly (GB uses urban, coast, freshwater, etc.; NI uses urban mask, coast, freshwater, road).
- Data Quality and Validation
  - Validation set: 22,325 points from GB countryside survey 2019, open forest inventory, IACS, and interpretation points.
  - Accuracy at UK scale: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation caveats: crosswalks between legacy and current class definitions; validation points may not perfectly match UKCEH classes.
- Appendices and Documentation
  - Appendix 1–2 provide detailed notes on UKCEH Land Cover Classes and their relation to BAP Broad Habitats.
  - Appendix 3 provides a recommended RGB color recipe for displaying classes.
  - Appendix 4 includes comprehensive confusion matrices and producer/user accuracy assessments by year.
  - Appendix 5 lists the full dataset catalog for LCM2017–LCM2019.

## Practical Considerations for Data Stewardship
- Data Provenance and Lineage
  - Bootstrap Training derives training data from 2015 maps for all three years; transparency on sampling with ≥99% purity parcels.
  - RF classifier training is balanced to ensure rare classes are represented.
  - All inputs (Sentinel-2 seasonal composites, context rasters) documented for reproducibility.
- Time-series and Comparability
  - GIDs do not match across LCM2015 vs LCM2017–2019; cross-year comparisons should use the Land Parcel Spatial Framework identifiers (gid) rather than older parcel IDs.
  - The 20m Classified Pixels layer preserves fine detail and supports custom aggregation schemes beyond the provided Land Parcels framework.
- Limitations and Uncertainty
  - No manual accuracy corrections were applied to LCM2017–2019 (contrast with earlier maps); classification errors are expected to be randomly distributed but persist in some regions.
  - Some land cover classes (e.g., Neutral Grassland, Peat-related uplands) show notable confusion in spectral separation; context rasters help mitigate this.
  - Future enhancements may include gap filling with alternative optical sources or radar data (Sentinel-1) to address seasonal gaps.
- Update and Accessibility
  - Goal to release a new LCM annually; 4-season approach enables timely mapping of land cover change.
  - Datasets designed for discovery and reuse via UKCEH data portals; metadata alignment with production processes to aid governance.
- Metadata and Classification Standards
  - Clear mappings between UKCEH Land Cover Classes and UK BAP Broad Habitats; careful terminology to avoid ambiguity.
  - Color coding and documentation (Appendix 3) to support consistent visualization across platforms.

## References and Key Resources
- Core methodological references: Breiman (Random Forest), Carrasco et al. (Sentinel data combinations), Jackson (BAP Broad Habitats), Morton et al. (LCM2007/LCM2011 lineage).
- Appendices provide detailed class definitions, classification notes, and validation tables to support auditability and reproducibility.