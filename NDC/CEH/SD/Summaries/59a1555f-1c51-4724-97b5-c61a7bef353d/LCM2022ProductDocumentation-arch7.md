# The UKCEH Land Cover Map for 2022

- Overview of LCM2022
  - UKCEH’s annual land cover map, building on 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats, BAP).
  - Produced from Classification Scenes combining Sentinel-2 Seasonal Composite Images with Context Rasters; classification uses Bootstrap Training and Random Forest.
  - Seven datasets: three per region (Great Britain and Northern Ireland) of 10 m Classified Pixels, Land Parcel Datasets, and 25 m Rasterised Land Parcels, plus a 1 km summary raster product covering GB and NI.
  - Formal validation reports overall accuracy of 86.1% at full thematic detail.

- Datasets and formats
  - 10 m Classified Pixel datasets (GB and NI)
    - Mosaic of Classification Scenes; each pixel’s class (UKCEH Land Cover Class) plus a confidence/probability band.
    - 10 m pixels are not generalized by the UKCEH Land Parcel Spatial Framework to preserve fine landscape features.
  - Land Parcel datasets (GB and NI)
    - Created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterized representation of parcels with three bands: dominant land cover (mode), mean confidence, and parcel purity.
  - 1 km Summary rasters (GB and NI)
    - Dominant class per 1 km pixel (21 class data) and percentage cover per class (21 bands for classes, 10 bands for aggregates).
    - Rounding can cause the 1 km totals to drift around 100%.
  - Coordinate systems
    - GB: British National Grid (EPSG: 27700)
    - NI: Irish Grid TM75 (EPSG: 29903)

- Classification methodology
  - Seasonal Composite Images and Context Rasters
    - Seasonal imagery: four 3-month periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) from Sentinel-2 at ~10 m resolution; four-season median reflectance.
    - Context Rasters: GB uses height, aspect, slope, distances to buildings/roads/tidal water/freshwater, foreshore and woodland masks; NI uses height, aspect, slope, urban mask, coast/freshwater/road distances, foreshore and tidal masks.
  - Bootstrap Training and Random Forest
    - Bootstrap Training automatically derives training data from historic land cover maps without new field data.
    - Training pixels drawn from LCM2019, LCM2020, LCM2021 with >80% probability and consistent class across three years.
    - RF classifier trained with balanced sampling to avoid dominance by common classes.
    - Processing environment uses bespoke UKCEH software integrating WEKA, PostGIS, and GDAL.
  - 32 GB GB Classification Scenes; NI uses a single 49-band Classification Scene (40-band Sentinel-2 + NI Context Rasters).

- UKCEH Land Parcel Spatial Framework
  - Framework derived from generalising national cartography; designed to represent discrete real-world units (fields, parks, etc.) and reduce noise.
  - MMU ~0.5 ha; parcels may be dominated by a single land cover type.
  - gid identifiers in this framework do not match LCM2015 parcel IDs; affects cross-version parcel comparison.

- Data quality and validation
  - Validation dataset: 33,107 reference points across all 21 classes.
  - Overall accuracy: 86.1% (thematic detail).
  - Known issues: a small number of polygons missing from vector land parcel products; negligible effect on 1 km products; 10 m classified pixels remain unaffected.

- Class relationships and nomenclature
  - 21 UKCEH Land Cover Classes described in Appendix 1, linked to UK BAP Broad Habitats (Appendix 2) with nuanced mapping.
  - Some BAP Broad Habitat definitions are retained for comparability with earlier products; UKCEH classes may differ in granularity or interpretation.
  - Special notes on key classes (e.g., Saltwater vs Freshwater, Inland Rock, Bracken, Heather) and typical spectral/confidence behaviors.

- Production notes and updates
  - LCM2022 is the tenth UK land cover map; aims for annual updates to improve temporal consistency and enable change detection.
  - If new methods yield accuracy gains, methods may be reapplied across the catalogue.
  - Disclaimer: method changes between years mean some observed differences reflect methodology, not only real change.

- Validation and citations
  - Primary dataset DOIs provided for each product (10 m Classified Pixels GB/NI, 25 m Rasterised Land Parcels GB/NI, Land Parcel products GB/NI, 1 km summary rasters, etc.).
  - Key references: Marston et al. (2024a–g) for various LCM2022 data products; broader production methodology in Marston et al. (2023/2024).
  - Formal glossary and appendices provide detailed class definitions, mapping to BAP, and colour recipes for map display.

- Practical guidance for GIS use
  - Use 10 m Classified Pixels for detailed mapping of landscape features; data include a confidence band per pixel.
  - Use Land Parcel datasets to analyze and compare land cover over time with a fixed spatial framework; MMU of ~0.5 ha ensures discrete parcels.
  - Use 25 m Rasterised Parcel data for efficient parcel-level analyses; monitor conf and purity values for quality checks.
  - Use 1 km summary rasters for coarse-grain regional analyses and change detection; be mindful of rounding effects in percentage totals.
  - Seasonal and Context Raster layers help resolve spectral confusion (e.g., distinguishing vegetation from bare ground, urban features).
  - For display, use the provided colour recipes or unit-specific QGIS symbology files; also available are color-blind friendly options.