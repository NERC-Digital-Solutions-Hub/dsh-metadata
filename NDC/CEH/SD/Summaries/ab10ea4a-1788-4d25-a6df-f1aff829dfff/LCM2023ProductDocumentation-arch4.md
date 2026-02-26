# The UKCEH Land Cover Map for 2023

- The LCM2023 is the UKCEH annual land cover map, the eleventh in the series, mapping 21 UKCEH Land Cover Classes aligned to Biodiversity Broad Habitats (BAP) definitions. It combines Sentinel-2 Seasonal Composite Images with Context Rasters and uses Bootstrap Training with a Random Forest classifier. Formal validation reports an overall accuracy of 83% at full thematic detail.
- Product goal: enable rapid monitoring of state and change in the UK countryside, supporting change detection and a consistent time series to differentiate real changes from classification error.

## Data Products and Structure

- 10 m Classified Pixel datasets
  - Separate for Great Britain (GB) and Northern Ireland (NI).
  - Each pixel has two bands: the most likely UKCEH Land Cover Class (integer) and the associated confidence (probability).
  - Not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail (e.g., small patches, narrow features).

- Land Parcel datasets
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha, MMU).
  - Parcel-level attributes included (e.g., hist, mode, purity, conf, n, etc.), enabling change detection at parcel scale.
  - Gaps: a small number of polygons missing from vector land parcel products (minimal impact on 1 km products).

- 25 m Pixel Rasterised Land Parcel datasets
  - Rasterised version of land parcels at 25 m resolution, GB and NI.
  - Three bands: per-parcel dominant land cover (mode), mean confidence (conf), and purity.

- 1 km raster products
  - Summary rasters for GB and NI derived from the 25 m data.
  - Products include dominant cover (1 band for classes, 1 band for aggregates) and percentage cover (21 bands for classes, 10 bands for aggregates).
  - Integer-valued percentages; totals may not sum exactly to 100 due to rounding and coastal Polygon considerations.

- Seasonal Composite Images
  - Four-season Sentinel-2-based composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) used to generate Classification Scenes.
  - 10 m resolution bands; occasional cloud gaps are handled by the classifier’s tolerance to partial spectral information.

- Context Rasters
  - 10 m context layers to reduce spectral confusion (GB and NI differ slightly).
  - GB examples: height, aspect, slope, distance to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, saltmarsh mask.
  - NI examples: height, aspect, slope, urban mask, distance to coast, freshwater, roads, foreshore, tidal water.

- Classification Scenes
  - GB: grid of ~32 tiles (100 x 100 km each) used to train and classify independently; some edge-tile adjustments for small islands.
  - NI: a single 49-band Classification Scene (40 Sentinel-2 bands + 9 context bands) covering Northern Ireland.

- UKCEH Land Parcel Spatial Framework
  - Framework used to generalise national cartography into discrete land parcels for stable, repeatable comparisons over time.
  - Changes from prior datasets mean parcel identifiers (gid) do not match LCM2015, affecting direct cross-year parcel ID comparisons.

- Bootstrap Training
  - Automatic training data derived from historic LCMs (LCM2020–2022) with >80% probability and consistent class across years.
  - Provides abundant training observations without costly field data; limitations noted for arable and improved grassland transitions.

- Random Forest Classification
  - RF classifier trained on Bootstrap Training pixels; 10,000 samples per bag, with balanced class representation to reduce bias toward common classes.
  - Custom, UKCEH-developed software integrating Weka, PostGIS, and GDAL.

## Data Production and Methodology

- Data sources
  - Sentinel-2 Seasonal Composite Images (4-season temporal signals).
  - Context rasters from public/open datasets (terrain, urban areas, distances to features, shorelines).
  - Historic LCM maps used for Bootstrap Training.
- Processing workflow
  - Build Classification Scenes from seasonal + context rasters.
  - Train RF via Bootstrap Training data, generate 10 m classified pixels mosaic.
  - Derive Land Parcel datasets by overlaying classified pixels with the Land Parcel Spatial Framework.
  - Create 25 m rasterised land parcels from parcel data.
  - Generate 1 km summary rasters by aggregating 25 m data.
- Validation and accuracy
  - Validation dataset: 33,107 points across all 21 classes, using GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke points.
  - Overall accuracy: 83% at full thematic detail (LCM2023 validation).

## Product Details and Metadata

- Coordinate systems
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid TM75 (EPSG 29903)
- Extents and parcels
  - GB land parcels: ~6,741,294 parcels
  - NI land parcels: ~902,252 parcels
  - 10 m and 25 m products cover GB and NI with respective extents and origins aligned to national grids.
- Dataset documentation
  - Each LCM2023 dataset has a DOI; accompanying references and methodological descriptions are provided for replication and citation.
  - 1 km summary rasters, 25 m rasterised land parcels, land parcels (vector), and 10 m classified pixels each have dedicated DOIs and citations.

## Considerations for Data Leaders

- Data system and ecosystem
  - LCM2023 provides an annual, coherent data lineage with clear dependencies among seasonal composites, context rasters, classification scenes, land parcel framework, and parcel-level products.
  - The time-series nature supports change detection and differentiation between real land cover changes and random classification errors.
- Data quality, standards, and usability
  - 83% overall accuracy at full thematic detail; validation focused on 25 m rasterised parcels, with some minor vector parcel gaps.
  - Detailed metadata enables discoverability, provenance tracking, and reproducibility across GB and NI.
- Access, use, and governance
  - DOIs and citations provided for all data products; users should cite the appropriate dataset when reusing.
  - Acknowledge potential annual methodological changes; “Disclaimer” notes indicate shifts in methods can yield year-to-year differences beyond actual land cover change.
- Gaps and improving areas
  - Some cross-year parcel ID comparability challenges due to updates in the Land Parcel Spatial Framework.
  - Instances of spectral confusion across habitat types (notably among bog, heath, fen, and related classes) despite context layers.
  - Small polygons missing in vector land parcel products; minimal impact on 1 km products.

## Known Issues and Limitations

- Minor missing polygons in vector land parcel products; negligible effect on 1 km products; 10 m classified pixel data unaffected.
- Periodic methodological changes may introduce differences between years beyond actual land-cover changes.

## References and Access

- Dataset DOIs and citations are provided for all products (10 m classified pixels GB/NI, 25 m rasterised land parcels GB/NI, land parcels (vector), and 1 km summary rasters).
- Primary production and validation references include Marston et al. (2023–2024) and related methodological papers on LCM2007–LCM2021 series.