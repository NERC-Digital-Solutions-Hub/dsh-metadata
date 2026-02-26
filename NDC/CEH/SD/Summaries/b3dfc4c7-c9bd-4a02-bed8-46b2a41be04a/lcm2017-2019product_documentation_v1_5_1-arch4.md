# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Aim and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map suite consists of a range of geospatial datasets describing land cover across the UK.
- Production emphasizes automatic methods (Bootstrap Training + Random Forest) to enable annual map updates; historical labour-intensive corrections are not performed in these releases.
- Purpose is to help users make informed decisions about current and future applications of UKCEH LCM data, including understanding data production decisions and validation outcomes.

## Data products and structure
- 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats, aligned with LCM2015 terminology; classes can be linked to UKCEH Aggregate Classes for generalized mapping.
- Data products are provided in multiple representations to support different use cases:
  - 20m Classified Pixels: new RF-derived per-pixel classifications with a second band indicating per-pixel classification confidence (0–100). Preserves fine details and does not generalise to land parcels.
  - Land Parcels: attributes summarising classifications within fixed land parcels using the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - 25m Rasterised Land Parcels: rasterised summary of the Land Parcels with three bands: modal class (_mode), parcel-averaged confidence (_conf), and parcel purity (_purity).
  - 1km Raster Products (gridded summaries): 
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
- Each year (LCM2017, LCM2018, LCM2019) has Great Britain (GB) and Northern Ireland (NI) datasets, yielding a total of 42 datasets per year across the product suite; full listing and metadata are provided in Appendix 5.
- Dataset extents and coordinate systems:
  - GB in British National Grid (EPSG: 27700); NI in Irish Grid (EPSG: 29903).
  - 20m pixel size for Classified Pixels; 25m for Land Parcels; 1km grids for Percent/Dominant products.
- Attribute conventions (examples):
  - 20m Classified Pixels: band 1 = predicted class; band 2 = membership probability (0–100).
  - Land Parcels: gid, _hist (histogram of pixel counts per class as tuples), _mode, _purity (percent), _conf (0–100), _stdev, _n.
  - 25m Rasterised Parcels: bands = _mode, _conf, _purity.
- Class relationships and caveats:
  - UK BAP Broad Habitats definitions are provided (Appendix 1) with notes on how they relate to UKCEH Land Cover Classes.
  - Some BAP Broad Habitat concepts are not perfectly detectable by satellite sensors; interpretations and training data are adapted accordingly.

## Production methodology
- Bootstrap Training:
  - Fully automatic training process that samples from historic UKCEH LCMs (starting with LCM2015) to create spectral training data for current classification.
  - 99% purity filter applied to select parcels from LCM2015 as training observations; bootstrap samples then bootstrap the next map.
  - Plan to update bootstrap strategy in future releases (e.g., use majority signal across multiple years for LCM2020/LCM2021).
- Random Forest classification:
  -RF classifier trained with balanced sampling: 10,000 samples per class per Classification Scene.
  - Production uses open-source tools (WEKA within PostGIS and GDAL) integrated into UKCEH’s bespoke pipeline.
- Seasonal composites and context information:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance) used to derive 20m classification scenes.
  - Nine Sentinel-2 bands (spectral) plus 10 Context Layers (e.g., terrain metrics, distance to roads, coast, freshwater, urban features) used to reduce spectral confusion.
  - Seasonal images per year: winter, spring, summer, autumn; some gaps due to cloud cover, mitigated by classifier robustness.
- Classification Scenes:
  - GB: 100x100 km tiles used to assemble 36-band Seasonal Composite Images; 74 overlapping Classification Scenes classified independently and then merged with visual inspection to select best results.
  - NI: A single 43-band (36 spectral + 7 context) Classification Scene per year, using the same approach but with NI’s smaller extent.
- UKCEH Land Parcel Spatial Framework:
  - Maintains same parcel geometries as LCM2015 with minor storage/indices changes for faster processing.
  - gid identifiers do not match LCM2015; comparison across years should use gid for 2017–2019, not LCM2015 parcel ids.
  - MMU around 0.5 ha; designed to summarise land cover into discrete, relatively homogeneous parcels; framework supports user-defined parcel structures for bespoke summarisation.

## Input data and sources
- Sentinel-2 Seasonal Composite Images (seasonal median reflectance, resampled to 20m) created via Google Earth Engine; based on TOA reflectance (SR data not yet providing improvements in this context).
- Context rasters (20m) to improve discrimination among spectrally similar classes:
  - GB: Height, Aspect, Slope; distance to buildings, roads, sea, freshwater; foreshore and tidal water masks; woodland mask.
  - NI: Height, Aspect, Slope; urban mask; distances to coast, freshwater, roads.
- Data processing and validation included visual checks and formal validation, but all maps are automatically produced without region-specific manual corrections.

## Validation and accuracy
- Validation approach:
  - UK-scale validation against GB Countryside Survey 2019 data, National Forest Inventory data, IACS, and bespoke LCM validation points (22,325 points total).
- Overall accuracy (by year):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation notes:
  - Validation points reflect cross-walked classes from different data sources; conversions introduce some subjectivity.
  - Approximately 80% correspondence across the 21-class automatic maps is considered strong for ongoing methodological improvements.

## Data interpretation and usage notes
- The 21 UKCEH Land Cover Classes are designed for broad habitat detection; some fine distinctions from BAP Broad Habitats are not achievable with remote sensing alone.
- The product set provides both detailed per-pixel classifications (20m) and aggregated parcel/grid summaries (25m and 1km) to support various analytical and reporting needs.
- Users should be aware of:
  - Changes in parcel identifiers (gid) between LCM2015 and LCM2017–2019; cross-year parcel-based comparisons should use gid rather than historical parcel IDs.
  - The difference between high-detail 20m data and generalised 1km products (potentially higher confusion in coarser products).
  - Some spectral confusion among classes (e.g., Bog vs. Heather/Acid grassland; Saltwater vs. Freshwater; variations in upland vegetation) and the role of context layers in mitigating this.

## Future plans and considerations
- UKCEH intends to release a new LCM annually moving forward, with potential expansion of input data types (e.g., Sentinel-1 SAR) and improved training data to further enhance accuracy.
- LCM2020 (planned for 2021) will likely use bootstrap from the majority signal across 2017–2019 and consider broader data inputs to improve robustness and coverage.

## Appendix highlights (for governance and standards)
- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and alignment with BAP Broad Habitats.
- Appendix 3: Recommended RGB colour recipes for display of Land Cover Classes.
- Appendix 4: Full confusion matrices and per-class accuracy from validation (by year), with producer’s and user’s accuracy details.
- Appendix 5: Full dataset inventory and naming conventions across LCM2017, LCM2018, and LCM2019 (datasets, land mass, and dataset names).