# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- Release and description of three national UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- Each map uses 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) and matches the LCM2015 class structure for comparability.
- All three maps are produced automatically using Bootstrap Training with a Random Forest classifier; no manual corrections were applied this release.
- Annual updates are planned; visual checks and formal validation indicate map quality is similar to LCM2015.
- A glossary explains UKCEH-specific terms and capitalisation conventions; Appendix materials provide additional context and validation details.

## Data products and structure
- For each year, data are provided at multiple spatial products and resolutions, with GB and NI versions:
  - 20m Classified Pixels (2-band, 8-bit): per-pixel class and per-pixel confidence.
  - Land Parcels: parcel-level attributes derived from the UKCEH Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels: 3-band rasters (mode, conf, purity) summarising parcels.
  - 1km Raster datasets (intermediate aggregations):
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (1-band)
    - 1km Dominant Aggregate Cover (1-band)
- Total of 42 datasets across GB and NI for three years (21 classes in each product).

## Production methodology and workflow
- Bootstrap Training: automatic, self-starting training using historic land cover observations to generate spectral training data for the RF classifier. The Bootstrap Training for 2017–2019 derives from LCM2015, which itself used stable historic observations (1990–2007) plus manual observations.
- Random Forest classification: RF classifier trained with balanced sampling (10,000 samples per class per Classification Scene) to produce the 20m Classified Pixels. Produced with a bespoke pipeline integrating Weka, PostGIS, and GDAL.
- Seasonal inputs and classification scenes:
  - Seasonal Composite Images: Sentinel-2 TOA reflectance, median per season (winter, spring, summer, autumn) at 20m, using bands 2,3,4,5,6,7,8,11,12.
  - Context Rasters (20m): terrain (Height, Aspect, Slope), proximity masks (buildings, roads, sea, freshwater), foreshore, tidal water, and woodland context.
  - Seasonal gaps may occur due to cloud; the classifier tolerates missing data with partial-season information.
  - Classification Scenes: GB produced as overlapping 100x100 km tiles (36-band seasonal + 10 context bands = 46 bands per scene); NI uses a single 43-band scene (36 spectral + 7 context).
- UKCEH Land Parcel Spatial Framework:
  - Parcels are ~0.5 ha minimum mappable unit, generalized from national cartography, designed to reduce noise and provide stable time-series units.
  - Land Parcel identifiers (gid) differ from LCM2015; comparisons between 2017–2019 should use gid-based matching.
  - Framework supports summarizing 20m Classified Pixels into parcel-level attributes.

## Context, seasonality, and inputs
- Sentinel-2 bands and resolutions (relevant bands and spatial details provided for reproducibility).
- Choice of TOA reflectance over SR (though SR was available via Google Earth Engine, TOA performed similarly or better for current LCM classes; potential future refinement with more input types).
- Context rasters are crucial to reduce spectral confusion (e.g., distinguishing vegetation types by proximity to roads, water, elevation, and landforms).

## Dataset details and attributes
- 20m Classified Pixels:
  - 2-band raster: band 1 = most likely UKCEH Land Cover Class; band 2 = membership probability (0–100) for that class.
  - Maintains high-detail features, including narrow patches below 0.5 ha MMU.
- Land Parcels:
  - Attributes (Table 5): gid, _hist (list of class-frequency tuples), _mode (dominant class), _purity (percent of modal class), _conf (mean class membership probability), _stdev (uncertainty), _n (npix).
  - Note: some attribute names differ from LCM2015; descriptions aligned to current production conventions.
- 25m Rasterised Land Parcels:
  - 3-band rasters: band 1 = _mode; band 2 = _conf; band 3 = _purity.
- 1km rasters (summary products):
  - 1km Percent Cover: 21-band raster giving per-class percentage cover per 1km cell.
  - 1km Percent Aggregate Cover: 10-band raster for aggregated classes.
  - 1km Dominant Cover: single-band raster of dominant class per 1km cell.
  - 1km Dominant Aggregate Cover: single-band raster for dominant aggregate class per 1km cell.
- Georeferencing and extents:
  - Great Britain: GB British National Grid (EPSG:27700), extents defined; NI uses Irish Grid (EPSG:29903).
  - Pixel/grid specifics and band counts are documented in the data guide.
- Dataset count per year: 42 datasets total (GB and NI, across the five product types).

## Validation and accuracy
- Validation dataset: GB countryside survey 2019 data, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points total).
- Reported overall accuracy (UK scale) for the three products:
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Validation points originate from sources with different purposes; class mappings required transformations.
  - Accuracy figures reflect best available indicators; some misclassifications are expected.
  - Approximately 80% correspondence is considered impressive for automatically produced 21-class maps; ongoing improvements anticipated.

## Outputs, visualization, and usage notes for GIS work
- The suite provides multi-resolution data suitable for map-based visualization, change detection, and policy/public-facing products.
- The 20m Classified Pixels preserve fine-scale features for detailed mapping; higher-level 1km products enable broad-scale planning and summary analyses.
- For cross-year analysis, use gid-based comparisons for Land Parcels; note that parcel identifiers changed from LCM2015.
- The 21-class framework aligns with UKCEH Land Cover Classes and UK BAP Broad Habitats; the tables and appendices document class derivations and detection considerations.

## Timeliness, updates, and future plans
- UKCEH aims to release a new LCM annually, building on Bootstrap Training and RF classification.
- Future work includes exploring additional data sources (e.g., Sentinel-1 SAR), potential gap-filling approaches for complete seasonal data, and refining training data as new observations become available.
- The production framework anticipates evolving Bootstrap Training strategies, with planned shifts toward using multi-year majority signals for training (e.g., 2020 bootstrap from 2017–2019).

## References and supporting context
- Core methods: Bootstrap Training, Random Forest classification, use of Google Earth Engine for Sentinel-2 seasonal composites, and context rasters to improve classification accuracy.
- Appendix materials include detailed class definitions and relationships between UKCEH Land Cover Classes and BAP Broad Habitats, as well as color mapping and confusion matrices to support interpretation.