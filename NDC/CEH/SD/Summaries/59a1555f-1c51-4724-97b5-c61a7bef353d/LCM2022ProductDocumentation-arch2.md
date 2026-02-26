# The UKCEH Land Cover Map for 2022

- Purpose: A user guide for LCM2022, detailing its seven datasets (GB and NI) and a 1 km summary raster. Describes data production, validation, and accuracy to help users apply UKCEH LCM data effectively and understand limitations.

## Datasets and Product Suite

- Seven geospatial datasets (GB and NI):
  - 10 m Classified Pixel datasets (GB and NI)
  - 10 m Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
  - 1 km Summary Raster products (GB and NI)
- Appendix 3 lists official dataset names; Table 2 summarises product details (coordinate systems, pixel resolution, bands).
- 1 km products provide dominant class and percentage cover (for both classes and aggregates); percentage values are integer-rounded and may not sum exactly to 100 due to rounding and coastal area handling.
- GB uses 32 Classification Scenes (tile-based) for full GB coverage; NI uses a single 49-band Classification Scene (40 Sentinel-2 bands plus Context rasters).
- Output layers include:
  - 10 m Classified Pixels: two bands per pixel (land cover class identifier and associated confidence)
  - 25 m Rasterised Land Parcels: three bands (dominant land cover class, mean confidence, and purity)
  - 1 km summaries: dominant class, aggregate dominance, and percentage cover per class/aggregate

## Data Production: Methods and Features

- Bootstrap Training and Random Forest:
  - Bootstrap Training automatically builds training data from historic maps (LCM2019–LCM2021) with >80% probability and consistent class across years.
  - Random Forest classifier assigns the most probable UKCEH Land Cover Class per pixel.
- Seasonal Composite Images:
  - Derived from Google Earth Engine; Sentinel-2 data resampled to 10 m with four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Ten Sentinel-2 bands (2, 3, 4, 5, 6, 7, 8, 8A, 11, 12); occasional cloud gaps are handled without manual gap-filling.
- Context Rasters:
  - 10 m context layers to reduce spectral confusion (GB: height, aspect, slope; distance to buildings/roads/tidal water/freshwater; foreshore, woodlands, saltmarsh).
  - NI adds urban mask, coast and freshwater distances, roads, foreshore, tidal indicators.
- Classification Scenes:
  - GB: 32 tiles (100 x 100 km equivalents) classified independently; occasional overlaps at tile boundaries.
  - NI: single Classification Scene covering the full land mass of Northern Ireland.
- UK Land Parcel Spatial Framework:
  - Defines ~0.5 ha minimum mapped parcels; parcels are used to aggregate 10 m pixels and to support change detection.
- Bootstrap Training Dataset Sources:
  - Uses LCM2019/2020/2021 classified pixels; estimated to reduce need for new field data.
- Software:
  - Bespoke UKCEH tools integrating Weka, PostGIS, and GDAL (open source).

## Validation, Accuracy, and Known Issues

- Validation:
  - 33,107 validation points across all 21 LCM classes; compiled from GB countryside surveys, National Forest Inventory, Rural Payments data, and bespoke validation points.
  - Overall accuracy: 86.1% for full thematic detail (LCM2022).
- Known Issues:
  - Some polygons missing from the vector Land Parcel products; corresponding nodata areas in the 25 m rasterised land parcels. Impact considered negligible for 1 km products; 10 m classified pixels are unaffected.
- Citing and reproducibility:
  - Each LCM2022 dataset has a DOI; recommended citations provided (Marston et al. 2024 and related works).
  - Disclaimer notes that annual maps use slightly different methods; observed changes may reflect real change or methodological differences.

## UKCEH Land Cover Classes and BAP Relationships

- UKCEH Land Cover Classes: 21 classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, but not identical to BAP Broad Habitats.
- Relationship notes:
  - Generally one-to-one with BAP Broad Habitats; some exceptions and splits (e.g., Heather vs Heather grassland; Urban vs Suburban; Freshwater vs Rivers/Canals vs Standing Open Water).
  - Appendices 1–2 provide definitions and nuances; italicization used to distinguish UKCEH classes from BAP Broad Habitats when necessary.
  - Saltwater is treated separately where possible; coastal water features have lower priority in mapping accuracy due to spectral similarity with land features.
- Examples of mapping decisions:
  - Arable vs Improved Grassland: spectral similarity leads to potential confusion; context rasters help.
  - Fen, Marsh, Swamp vs Bog: spectral and patch-size complexity can lead to inter-class confusion; classifier learns from training data to reflect these challenges.
  - Built-up Areas and Gardens: Urban vs Suburban differentiated; some confusion expected due to mixed signatures.

## Data Access, Usage, and Citations

- Data access:
  - Data products have DOIs and are archived in NERC EDS Environmental Information Data Centre (EIDC).
  - Appendix 3 lists dataset-specific DOIs and citations.
- Guidance for users:
  - 10 m Classified Pixels preserve detailed landscape features; 25 m Parcel rasterises offer standardized parcel-based comparisons and change detection compatibility.
  1 km rasters provide broad-scale summaries suitable for regional analyses and integration with other datasets.
- Class color schemes:
  - Appendix 5: recommended color recipe for displaying UKCEH Land Cover Classes (standard palette).
  - Appendix 6: color-blind friendly version of the palette.
  - QGIS symbology files accompanying data products to implement the palettes.

## Practical Implications for Analysts Monitoring the Environment

- Standardised, time-series-ready data:
  - LCM2022 supports monitoring state and change of the UK countryside with annual updates, enabling differentiation between random errors and real changes over time.
- Data integration and re-use:
  - The underlying datasets (especially 10 m pixels and Land Parcel framework) are designed for further integration with other environmental data sources, supporting broader analyses and policy performance evaluation.
- Temporal and methodological transparency:
  - Clear notes on validation, accuracy, and methodological evolution help analysts interpret changes across map versions and plan for future data integration and methodological refinements.
- Suitability for environmental health indicators:
  - Outputs can be used to derive indicators of habitat extent, fragmentation, and land cover change, aiding policy performance assessments and environmental monitoring programs.