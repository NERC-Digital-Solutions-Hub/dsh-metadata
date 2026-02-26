# The UKCEH Land Cover Map for 2021

- The ninth UK land cover map produced by UKCEH (LCM2021) covering Great Britain and Northern Ireland.
- Produces 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats), mapped at multiple spatial resolutions.
- Core outputs:
  - 10 m Classified Pixel datasets (GB and NI): per-pixel most-likely class plus a confidence score; high spatial detail preserved (not generalised by the Land Parcel Framework).
  - Land Parcel datasets (GB and NI): attributes and statistics derived by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha) to support change detection and parcel-level analysis.
  - 25 m Rasterised Land Parcel datasets (GB and NI): three-band rasters per parcel (dominant class, confidence, purity) for compact parcel-level products.
  - 1 km raster products: dominant class and percentage cover per class/aggregate classes to enable broad-scale summaries.
- Validation and accuracy:
  - Formal validation with 35,182 reference points.
  - Overall accuracy of 82.6% (95% CI: 82.19%–82.99%).

- Production approach and data sources:
  - Automatic classification using Bootstrap Training plus Random Forest.
  - Seasonal Composite Images derived from Sentinel-2 (10-band, resampled to 10 m) across four seasons to provide temporal information.
  - 10 m Context Rasters (GB and NI) to reduce spectral confusion (terrain, proximity to roads/buildings/water, woodlands, etc.).
  - Classification Scenes: GB classified in 32 tiles (approx. 100 x 100 km each); NI classified in a single Scene.
  - Bootstrap Training: training data generated from historic LCM maps (LCM2018–LCM2020) filtered to parcels >80% pure and consistently classified across years, enabling a self-learning update loop for RF.

- Data framework and spatial details:
  - UKCEH Land Parcel Spatial Framework used to standardise parcel geometries and attributes across both GB and NI.
  - Parcel framework ensures discrete real-world units (fields, parks, urban areas, etc.) with a minimum area of ~0.5 ha.
  - Unique parcel identifiers (gid) differ from LCM2015; cross-map comparisons by parcel identifiers may require spatial overlap rather than exact IDs.
  - Coordinate systems:
    - Great Britain: British National Grid, EPSG 27700.
    - Northern Ireland: Irish Grid, EPSG 29903.
  - Extents:
    - GB: 0–700,000 m East; 0–1,300,000 m North.
    - NI: truncated Irish Grid to the NI landmass footprint.

- File structure and dataset details (highlights):
  - 10 m Classified Raster Product (GB and NI): 2 bands (class identifier and class membership probability/confidence).
  - Land Parcel Product (GB and NI): parcel-level attributes including _hist, _mode, _purity, _conf, _stdev, _agg; MMU ~0.5 ha; parcel counts: GB ~6,741,288; NI ~902,248.
  - 25 m Rasterised Land Parcel Product (GB and NI): 3-band rasters (dominant land cover _mode, _conf, _purity).
  - 1 km Raster Products: dominant class and percentile/percentage cover for both class and aggregate classifications; designed for spatial summaries across 1 km pixels.
  - Seasonal Composite Images: four-season Sentinel-2 reflectance composites; occasional cloud gaps are handled by tolerance in the classifier.
  - Context Rasters: GB includes 10 context layers (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask); NI includes analogous sets with urban mask and coastal/freshwater/road distances.
  - Data quality note: 10 m Classified Pixels are not validated against the 10 m dataset; validation was performed on the 25 m Land Parcel dataset.

- Classification methodology in brief:
  - Bootstrap Training creates training data from historic maps to train a Random Forest classifier.
  - Pixel-level classification assigns each 10 m pixel to the most probable UKCEH Land Cover Class; a confidence value accompanies each classification.
  - Sampling for RF is balanced across classes to avoid dominance by common classes.

- Relationship to biodiversity classifications:
  - 21 UKCEH Land Cover Classes are linked to UK BAP Broad Habitats but are not identical; some mappings are nuanced and often require context, hence italicised BAP names in documentation.
  - Appendices detail the mappings and considerations for specific habitat types.

- Validation and limitations:
  - Overall accuracy 82.6% with CI 82.19%–82.99%.
  - Some spectral confusions persist (e.g., certain grasslands, bracken vs acid grassland, bog vs other upland vegetation).
  - Saltwater and freshwater distinctions near coasts can be challenging; Saltwater is typically inferred via coastal context rasters.
  - The 10 m pixel data are detailed but not aligned to the Land Parcel Spatial Framework, so certain analyses should account for potential parcel-level crosswalk differences.
  - Linear features (hedgerows, walls) are not reliably classified by current spectral methods and are not separate classes.

- Display and colour guidance (for map production):
  - Appendix 5 and 6 provide recommended colour recipes for displaying UKCEH Land Cover Classes, including colour palettes that are color- and color-blind friendly.

- Practical takeaways for data use (Data Support perspective):
  - For detailed studies and change detection, use the 10 m Classified Pixel dataset complemented by the Land Parcel Framework to contextualise transitions over time.
  - Use the 25 m rasterised parcels for parcel-based analyses and to align with the MMU.
  - Use 1 km products for regional-scale summaries and rapid assessments where fine detail is less critical.
  - Leverage Context Rasters to mitigate spectral confusion and improve class separation, especially near coastlines and in urban-rural gradients.
  - When aggregating across time, the annual nature of LCM2021 plus Bootstrap Training provides a framework to distinguish real change from random classification noise.

- Appendices and supporting materials (highlights):
  - Appendix 1–2: detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats definitions.
  - Appendix 3: full list of datasets and official dataset names for LCM2021.
  - Appendix 4: comprehensive confusion matrices and class-level validation metrics (Producer’s and User’s Accuracy).
  - Appendices 5–6: colour recipes for display, including color-blind friendly options.