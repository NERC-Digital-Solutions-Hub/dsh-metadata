# The UKCEH Land Cover Map for 2022

- Overview
  - UKCEH's tenth land cover map (LCM2022) producing 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP) definitions.
  - Product consists of seven geospatial datasets: three per region (Great Britain and Northern Ireland) plus a 1 km summary raster.
  - Datasets include a 10 m classified pixel product, a land parcel dataset, and a 25 m rasterised land parcel product; plus a cross-region 1 km summary raster.
  - Classification is automatic, using Bootstrap Training and a Random Forest classifier; aims for annual, comparable maps with validation-backed accuracy (86.1% overall at full thematic detail).

- Datasets and data structure
  - 10 m Classified Pixel datasets
    - Generated from multiple Classification Scenes; produce a mosaic of national land cover.
    - Each pixel has two bands: the most likely UKCEH Land Cover Class and the associated class probability/confidence.
    - 10 m pixels are not generalised by the Land Parcel Spatial Framework to preserve fine features (e.g., narrow habitats).
  - Land Parcel datasets
    - Result from intersecting the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to create parcel-level attributes.
  - 25 m Rasterised Land Parcel datasets
    - Rasterised version of land parcels (GB and NI) at 25 m resolution; bands carry per-parcel mode, conf, and purity values.
  - Vector Land Parcel Product
    - A separate vector representation of land parcels with attributes suitable for change detection and parcel-level analyses.
  - 1 km Summary rasters
    - Across GB and NI, summarise 25 m rasters to 1 km cells: dominant class, dominant aggregate class, and percentage cover per class/aggregate.
    - Percentage rasters are integer-valued; sums may slightly diverge from 100 due to rounding and coastal edge effects.
  - Seasonal Composite Images
    - Sentinel-2-based seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m, with spectral bands from Sentinel-2.
    - Some gaps due to cloud are tolerated; the classifier remains robust to partial spectral information.
  - Context Rasters
    - 10 m context rasters used to reduce spectral confusion (e.g., terrain, proximity to buildings/roads, water, coastal features, land/water masks).
    - GB and NI variants include different combinations of terrain, urban, coastal, water, and binary masks.
  - Classification Scenes and Tiles
    - GB: 32 Classification Scenes (approx. 100 x 100 km tiles) to cover the GB land surface; overlapping at tile edges where extents are adjusted.
    - NI: a single Classification Scene covering all NI land mass; a 49-band single Classification Scene combining a 40-band Sentinel-2 Seasonal Composite with NI context rasters.
  - UK Land Parcel Spatial Framework and MMU
    - Framework with ~0.5 ha minimum mapping unit (MMU); generalised to remove detail and create discrete parcels representing real-world units (fields, parks, urban areas, etc.).
    - 10 m pixels are later grouped into parcels to reduce noise and enable time-based change detection.
    - Note: gid identifiers in the spatial framework may not match LCM2015 parcel identifiers due to framework reordering and indexing changes.

- Methods and training
  - Bootstrap Training
    - Automatic training data selection using historic LCM data without field-collected inputs.
    - Training pixels are drawn from LCM2019–LCM2021, selecting pixels with >80% probability and the same land cover class across all three years.
    - Helps to exploit a large, wall-to-wall training set; reduces the impact of minor changes since the refresh interval is short relative to dynamics.
  - Random Forest classification
    - 10,000 samples per class per bag, with replacement to balance class representation during training.
    - Classifier implemented with bespoke UKCEH software integrating Weka, PostGIS, and GDAL (open-source stack).
  - Validation
    - 33,107 validation points across all 21 classes.
    - Overall accuracy: 86.1% (full thematic detail).

- Known issues and caveats
  - Some polygons missing from the vector Land Parcel Product; corresponding NODATA areas in the 25 m rasterised parcels. Minimal impact on 1 km products; 10 m classified pixels unaffected.
  - Methods evolve over time; small differences between LCM2022 and earlier years reflect methodological updates.

- Data accessibility and citations
  - Each LCM2022 dataset has its own DOI; detailed citations provided for all products (10 m classified pixels GB/NI; 25 m rasterised land parcels GB/NI; land parcel products GB/NI; 1 km rasters).
  - For production-method overview, see Marston et al. (2023) and related 2024 datasets.
  - Disclaimer: annual methodological refinements mean some changes reflect both real change and method updates.

- Classification detail and class definitions
  - 21 UKCEH Land Cover Classes aligned with BAP Broad Habitats; definitions and mappings described in Appendices 1–3.
  - Relationships between UKCEH classes and BAP Broad Habitats documented; some BAP classes are represented by aggregated UKCEH classes in the Land Parcel product.
  - Appendix 5 and 6 provide color recipes (including color-blind friendly options) for displaying UKCEH Land Cover Classes; accompanying QGIS symbology files are provided.

- Coordinate systems and extents
  - Great Britain: British National Grid, EPSG 27700; extent 0–700,000 E, 0–1,300,000 N.
  - Northern Ireland: Irish Grid TM75, EPSG 29903; extent truncated to NI landmass (approx. 180,000–400,000 E, 300,000–500,000 N for the NI frame).
  - Pixel resolutions: 10 m (classified pixels, context rasters, seasonal composites); 25 m (land parcel rasters); 1 km summary rasters aggregate from 25 m data.
  - Parcel counts: GB ~6,741,294 parcels; NI ~902,252 parcels; per-parcel attributes and per-pixel statistics are included in respective datasets.

- Practical notes for GIS use
  - 10 m classified pixels provide fine detail but are not generalised by the Land Parcel framework; useful for detailed habitat mapping and change detection with high spatial fidelity.
  - 25 m rasterised land parcels and vector land parcels enable efficient analysis at parcel level and robust time-series comparisons.
  - 1 km rasters offer a coarser, region-wide summary suitable for broad-scale policy and environmental monitoring.
  - Context rasters and Seasonal Composites improve discrimination of spectrally similar land cover types (e.g., various grasslands, inland water, coastal features).
  - Validation expectations and accuracy should be considered when interpreting fine-scale changes, particularly for classes with lower producer's/user accuracies.

- Summary of purpose for GIS specialists
  - Provides a multi-resolution, temporally consistent UK land cover dataset (LCM2022) optimized for map-based visualization and analysis.
  - Enables detailed mapping (10 m) and scalable analyses (25 m parcels, 1 km summaries) across GB and NI, with thorough documentation on production, validation, and data quality.