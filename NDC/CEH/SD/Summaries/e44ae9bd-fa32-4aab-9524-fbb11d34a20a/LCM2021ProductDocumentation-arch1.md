# The UKCEH Land Cover Map for 2021

## Purpose and scope
- UKCEH Land Cover Map 2021 (LCM2021) is the ninth UK land cover map, produced annually.
- Product comprises six geospatial datasets: three for Great Britain (GB) and three for Northern Ireland (NI).
- Datasets include: 10 m Classified Pixel dataset, Land Parcel dataset, and 25 m Rasterised Land Parcel dataset; plus 1 km summary products.
- Aim is to support informed decision-making in environmental monitoring and change detection through consistent, traceable data.

## Data structure and outputs
- 10 m Classified Pixel dataset: mosaic of Classification Scenes; each pixel has a most-likely UKCEH Land Cover Class and a confidence/probability value.
- Land Parcel dataset: results from intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework to derive parcel attributes.
- 25 m Rasterised Land Parcel dataset: 3-band raster (dominant land cover, mean confidence, and parcel purity) derived from parcel data.
- 1 km products: dominant cover per 1 km pixel and percentage cover per class (21 UKCEH classes; 10 Aggregate classes) with rounding, noting coastal areas may sum to <100 due to mapping resolution.
- Coordinate systems: GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (TM75, EPSG: 29903).

## Datasets and metadata
- Dataset suite includes: 10 m Classified Raster (GB and NI), Land Parcel Product (GB and NI), 25 m Rasterised Land Parcel Product (GB and NI), plus 1 km summary products.
- Appendix 3 lists official dataset names; Appendix 5/6 provide color recipes for display.
- Number of land parcels: GB ~6.7 million; NI ~0.9 million.
- The 10 m and 25 m products differ in resolution and generalisation status; 10 m pixels preserve fine detail, while parcel-based products use the Land Parcel Spatial Framework (MMU ~0.5 ha).

## Classification method and production
- Classification scenes: for GB, 32 tiles (based on modified OS 100 km grid) covering GB land surface; NI uses a single 49-band Classification Scene (40 Sentinel-2 bands plus NI context rasters).
- Seasonal data: Sentinel-2 Seasonal Composite Images (10 bands) resampled to 10 m, with four seasons to capture phenology.
- Context rasters (10 m): terrain (height, aspect, slope) and proximity rasters (distance to buildings, roads, sea, freshwater, etc.), plus foreshore and tidal masks; NI includes an urban mask.
- Bootstrap Training: automatic, hardware-intensive training using historic LCM data (LCM2018–LCM2020). Training samples are parcels with >80% purity and consistent class across three years.
- Random Forest: to classify Classification Scenes; sampling with replacement to balance class representation; 10,000 samples per bag; RF-based output is the 10 m classified pixel product.
- Software: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open-source components).

## Bootstrap Training and validation
- Bootstrap Training leverages wall-to-wall historic maps to generate large training sets for next maps, enabling annual updates.
- Validation: 35,182 reference points across all 21 classes; data sources include GB countryside survey, National Forest Inventory, Rural Payments Agency, and bespoke validation points.
- Overall accuracy: 82.6% with a 95% confidence interval of 82.19%–82.99%.
- Validation for the 25 m rasterised land parcel dataset (not the 10 m pixel product) informs accuracy assessments; Appendix 4 provides detailed confusion matrices and per-class accuracy.

## The UKCEH Land Parcel Spatial Framework
- Land Parcel Spatial Framework originated for LCM2007 and updated for LCM2015; minor changes since then (storage ordering and new indices).
- Parcels typically ~0.5 ha minimum; designed to represent discrete real-world units (fields, parks, urban areas, etc.).
- 10 m pixels are aggregated into parcels to reduce noise and enable change detection over time.
- Parcel identifiers (gid) do not match LCM2015 when comparing by parcels due to framework updates.

## Seasonal imagery and context rasters details
- Seasonal Composite Images (GB): four 3-month periods; occasionally cloud gaps, but classifier tolerates partial spectral data.
- Context rasters (GB NI differences summarized above) are used to resolve spectral confusion (e.g., bare rocks vs. urban surfaces, coastal vs. inland features).

## Classification Scenes and processing extent
- GB classification Scenes: 32 tiles; each trained and classified independently; tile size chosen to limit regional phenological variation.
- NI classification Scene: single 49-band Scene; designed to accommodate NI’s smaller land area.
- Output resolution and metadata: detailed in Tables and Appendices; dataset extents and naming follow official documentation.

## Biodiversity Action Plan (BAP) alignment
- UKCEH Land Cover Classes (21) are closely related to BAP Broad Habitats but not identical.
- Appendices explain how certain BAP Broad Habitats map to UKCEH classes and note areas of potential spectral confusion or classification trade-offs.
- Some BAP classes are split or combined to reflect remote-sensing capabilities and training data constraints.

## Data quality, caveats, and guidance for users
- 10 m Classified Pixels: not generalised with the Land Parcel Spatial Framework; suitable for specialists who understand the implications of higher detail and potential parcel-level smoothing in other products.
- Validation baseline: accuracy figures apply to 25 m rasterised parcels; 10 m products have independent considerations due to the lack of parcel-level validation.
- Methodology is evolving; annual updates enable better change detection and temporal consistency, helping to separate true land cover change from random errors.
- Users seeking cross-map comparison should note parcel ID changes between LCM2015 and LCM2021; spatial overlap may be required for matching.

## Practical implications for analysts
- The six-dataset product suite provides both pixel-level (10 m) detail and parcel-based (25 m) summaries, plus coarser 1 km summaries for broad-scale analyses.
- Bootstrap Training and RF classification offer a scalable path to annual updates with a consistent training base, improving comparability over time.
- Context rasters and seasonal composites are central to reducing spectral confusion and improving classification accuracy.
- The documentation emphasizes metadata, data provenance, and dataset discoverability to support reproducible analyses.

## Appendices (highlights)
- Appendix 1 & 2: Notes on UKCEH Land Cover Classes and UK BAP Broad Habitats – definitions and relationships.
- Appendix 3: Full list of LCM2021 datasets by mass and region.
- Appendix 4: Correspondence matrices (confusion matrices) and per-class accuracy metrics.
- Appendix 5 & 6: Display color recipes for UKCEH Land Cover Classes (including color-blind friendly options).
- References: foundational sources for methods and prior LCM work.