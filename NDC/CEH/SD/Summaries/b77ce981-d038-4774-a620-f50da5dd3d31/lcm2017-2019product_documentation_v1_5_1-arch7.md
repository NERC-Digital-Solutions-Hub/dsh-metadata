# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- Purpose and scope
  - User guide accompanying LCM2017, LCM2018, and LCM2019.
  - 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with near-continuity to earlier maps (LCM2015, LCM2007, LCM2000).
  - Automatic production workflow (Bootstrap Training + Random Forest); no manual corrections this release.
  - Aim: help GIS users understand data structure, production decisions, validation, and future plans to enable informed use.

- Key concepts and terminology
  - 21 UKCEH Land Cover Classes and 10 UKCEH Aggregate Classes; mappings to UK BAP Broad Habitats described in appendices.
  - Bootstrap Training: automatic selection of training observations from historic maps to train classifiers.
  - Classification Scene: multi-layer input (Seasonal Composite + Context Rasters) used for classification.
  - Seasonal Composite Image: Sentinel-2-based seasonal reflectance, per season, resampled to 20 m.
  - Context Rasters: 20 m layers adding terrain, distance to features, etc., to reduce spectral confusion.
  - Land Parcel Spatial Framework: fixed parcel-based schema (0.5 ha MMU) used to summarise 20 m classified pixels into parcels.

- Product structure and datasets
  - 20 m Classified Pixels (GB and NI versions)
    - New addition in 2017–2019 suite; RF results with per-pixel class probability.
    - Band 1: most likely UKCEH Land Cover Class; Band 2: confidence (0–100).
    - Preserves fine detail (narrow features) not generalised by parcels.
  - Land Parcels
    - Derived by intersecting 20 m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Attributes include: gid, hist (frequency of classes within parcel), mode, purity, conf, stdev, n.
    - Some attribute names differ from LCM2015; descriptions clarified in Appendix.
  - 25 m Rasterised Land Parcels
    - Rasterised from Land Parcels (3-band: mode, conf, purity).
  - 1 km Raster datasets (GB and NI)
    - 1 km Percent Cover (21 bands; % cover of each class per 1 km cell).
    - 1 km Percent Aggregate Cover (10 bands; aggregate class percentages).
    - 1 km Dominant Cover (single-band dominant class per 1 km cell).
    - 1 km Dominant Aggregate Cover (single-band dominant aggregate class per 1 km cell).

- Production workflow and inputs
  - Sentinel-2 Seasonal Composite Images produced via Google Earth Engine (GEE):
    - Seasonal TOA reflectance (winter, spring, summer, autumn) per 20 m pixel.
    - 9 Sentinel-2 bands used; some seasonal gaps due to cloud are left as nulls.
    - TOA used in this release; SR did not improve classification in these products.
  - Context Rasters (GB and NI)
    - GB: height, aspect, slope, distance to buildings/roads/coast/freshwater, foreshore, tidal water, woodland.
    - NI: height, aspect, slope, urban mask, distance to coast, freshwater, road.
  - Classification Scenes
    - GB classified in 100x100 km tiles (74 overlapping scenes); NI uses a single 43-band scene per year.
    - Overlaps allow balancing training observations; visual checks used to select preferred results.
  - UKCEH Land Parcel Spatial Framework
    - Maintains 0.5 ha MMU; parcel identifiers (gid) do not match LCM2015, complicating cross-year parcel ID comparisons.
  - Bootstrap Training and Random Forest
    - Training data drawn from LCM2015 bootstrap; 99% purity parcels selected as training inputs.
    - RF classifier: 10,000 samples per class, balanced via sampling with replacement.
    - Production software uses Weka within PostGIS and GDAL tools (open source).
  - Validation and quality assurance
    - UK-scale validation against GB countryside survey 2019, open data inventories, and bespoke validation points (22,325 total points).
    - Overall accuracy: LCM2017 ~78.6%, LCM2018 ~79.6%, LCM2019 ~79.4%.
    - Validation points are not absolute truth; conversions from other classifications are involved; still a strong indicator of performance.

- Data quality, limitations, and notes
  - No manual corrections applied to the new maps; all classification is automatic.
  - Classification errors are expected to be spatially random, but persistent changes will stand out over time.
  - Land Parcel identifiers (gid) differ from LCM2015; cross-year parcel-based comparisons require gid-based overlap rather than parcel IDs.
  - Context rasters and seasonal spectra reduce spectral confusion but some classes remain spectrally similar (e.g., various grasslands, peat-related habitats).
  - Seasonal gaps may occur in future years; potential gap-filling considered using Sentinel-1 SAR and alternative sources.

- Appendices and reference material
  - Appendix 1 & 2: UKCEH Land Cover Classes and UK BAP Broad Habitats; notes on confusion and detection limits.
  - Appendix 3: Recommended RGB color recipes for displaying UKCEH classes.
  - Appendix 4: Validation results by class (confusion matrices, user and producer accuracy summaries) and table mappings.
  - Appendix 5: Full list of datasets per year, including GB and NI products (total of 42 datasets across three years; 20 m, 25 m, and 1 km products).
  - References: key literature on RF, bootstrap training, and habitat classifications.

- Practical implications for GIS specialists
  - Access to consistent, automated, annual UK-wide land cover products (LCM2017–2019) at multiple thematic resolutions (20 m, 25 m, 1 km).
  - Use 20 m Classified Pixels for maximum detail and bespoke summarisation; use Land Parcels or 1 km rasters for broader analyses.
  - When linking across years, rely on gid for parcel-based comparisons; avoid cross-year parcel ID matching.
  - Colors and class definitions aligned with UKCEH guidance; refer to appendices for detailed class meanings and mapping to BAP habitats.
  - Validation indicates robust performance (around 79% overall accuracy) suitable for monitoring changes and baseline mapping, with ongoing plans to evolve methods and inputs.

- Future plans and outlook
  - Annual release of a new LCM to better capture land cover change dynamics (as opposed to multi-year gaps).
  - Potential inclusion of additional data sources (e.g., Sentinel-1 SAR) to handle cloud gaps and improve classifications.
  - Continued refinement of Bootstrap Training strategies and possible updates to parcel frameworks as higher-resolution data become more routine.