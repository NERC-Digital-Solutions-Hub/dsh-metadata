# The UKCEH Land Cover Map for 2020

- Purpose: User guide for LCM2020, a set of land cover maps produced annually. The product comprises six datasets (three for Great Britain and Northern Ireland), including 10 m classified pixel data, 25 m rasterised land parcels, and corresponding land parcel datasets. The aim is to help users make informed decisions about applying UKCEH LCM data, with an emphasis on data production, validation, and accuracy. Overall accuracy is just over 79%.

## What the data includes

- Land cover classes: 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats (with careful notes on equivalences and differences).
- Datasets and resolutions:
  - 10 m Classified Pixel datasets (GB and NI): classified pixels with two bands per pixel — the most likely UKCEH Land Cover Class and the associated probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised parcels carrying per-parcel attributes (mode, confidence, purity) across three bands.
  - Land Parcel Product datasets (GB and NI): parcel metadata and spatial framework information (EPSG codes and extents).
  - Additional: 8-bit Raster Products; for Northern Ireland, a 20 m Classified Raster Product is also available (as per Appendix 5).
- Spatial framework: UKCEH Land Parcel Spatial Framework with a minimum mapped unit of ~0.5 ha; parcels generalise national cartography to reduce noise and support change detection.

## How LCM2020 was produced

- Mapping approach:
  - Land cover is mapped from Classification Scenes composed of Sentinel-2 Seasonal Composite Images plus 10 Context Rasters to reduce spectral confusion.
  - Bootstrap Training (automatic training data from historic maps) is used with a Random Forest classifier to derive land cover classifications.
- Seasonal and contextual data:
  - Seasonal Composite Images: Sentinel-2 reflectance data for four seasons (winter, spring, summer, autumn) derived via Google Earth Engine; some gaps due to cloud cover, but the classifier tolerates partial data.
  - Context Rasters (GB and NI): features such as height, aspect, slope, and distances to buildings, roads, sea, freshwater, with region-specific masks (e.g., urban masks for NI, foreshore, tidal water, woodland).
- Classification Scenes and training:
  - GB: 100x100 km tiles yielding 74 overlapping Classification Scenes (36-band Sentinel-2 scenes + 10 context rasters; some regions classified multiple times due to overlaps; a manual precedence step selects final results).
  - NI: a single Classification Scene per year using a 36-band Sentinel-2 image set plus NI context rasters.
- Bootstrap Training data:
  - Derived from LCM2017–2019, filtered to parcels with >99% purity across three years, resulting in about 941,027 GB and 214,833 NI training objects.
- Random Forest classifier:
  - Balanced learning by drawing 10,000 samples per class with replacement from labelled parcels; produces the 10 m Classified Pixel product.
- Validation:
  - Validated against countryside survey data (2019–2020), National Forest Inventory, IACS, and bespoke validation points (n = 34,715); overall accuracy ~79.2% at full thematic detail (Appendix 4).

## Data quality, accuracy and change detection

- Annual maps enable distinguishing random classification noise from real change; most classification errors are random in space/time and should not recur at the same location year after year.
- Validation indicates 79.2% producer/user accuracy at full detail; Appendix 4 provides class-by-class performance and confusion matrices.
- Validation caveats: validation points intersect Land Parcel datasets; accuracy metrics are reported for the product as a whole and by class.

## Relationship to BAP Broad Habitats

- The 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical; BAP definitions are referenced and italicised when used.
- Several mappings and occasional splits:
  - Examples: Broadleaved vs Deciduous woodland; Dwarf Shrub Heath split into Heather and Heather Grassland; Built-up Areas split into Urban and Suburban; Freshwater aggregates Rivers/Standing Water.
- Appendices provide detailed notes on how classes map to BAP habitats and the implications for interpretation and validation.

## UKCEH Land Parcel Spatial Framework

- Parcels are designed to represent discrete land units (minimum ~0.5 ha) to support change detection and reduce noise.
- The parcel framework was updated from LCM2015; thus, unique parcel identifiers (gid) may not align year-to-year for direct comparisons, which can affect longitudinal parcel-based analyses.

## Practical use and limitations for data users

- Pixel vs parcel data:
  - 10 m Classified Pixels: two-band output (class ID, class probability). Not generalised by the Land Parcel Spatial Framework to preserve fine-scale features.
  - 25 m Rasterised Land Parcels: per-parcel attributes (mode, conf, purity) and a 3-band raster representation.
- Data access and metadata:
  - Appendix 5 lists official dataset names and extents for GB and NI, including EPSG codes and pixel resolutions (10 m, 20 m, 25 m) and the number of bands.
- Display and interpretation:
  - Appendix 3 provides a recommended color scheme for displaying the 21 UKCEH Land Cover Classes.

## Summary of key takeaways for data use

- LCM2020 offers annually produced, high-resolution land cover data for the UK with robust validation (~79% accuracy) and a strong emphasis on time-series change detection.
- Production relies on Bootstrap Training and Random Forest classification applied to 36-band Sentinel-2 scenes augmented with 10 Context Rasters; GB uses tiled classification scenes, NI uses a single scene per year.
- Outputs include detailed 10 m classified pixel maps and 25 m rasterised land parcel maps, plus corresponding parcel metadata, enabling both pixel-level analyses and parcel-based change detection.
- Users should be aware of the parcel framework’s MMU (0.5 ha) and potential year-over-year id mismatches when performing longitudinal comparisons.
- The data are integrated with BAP Broad Habitats for consistency with earlier products, but users should consult Appendices for precise class definitions and crosswalks.