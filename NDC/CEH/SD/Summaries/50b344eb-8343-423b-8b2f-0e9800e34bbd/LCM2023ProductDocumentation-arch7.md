# The UKCEH Land Cover Map for 2023

## Product overview
- UKCEH LCM2023 comprises seven datasets: three for Great Britain (GB) and three for Northern Ireland (NI) plus a 1 km summary raster that covers both GB and NI.
- Datasets include a 10 m dataset of classified pixels, a dataset of classified land parcels, and a 25 m pixel rasterised land parcels dataset; plus a 1 km summary raster product.
- Land cover is defined via 21 UKCEH Land Cover Classes, linked to Biodiversity Action Plan (BAP) Broad Habitats; annual maps aim to enable change detection and temporal comparability.
- Overall validation accuracy reported at 83% for full thematic detail.

## Key concepts and data structure
- UKCEH Land Cover Classes and BAP links
  - 21 UKCEH Land Cover Classes aligned (with some differences) to BAP Broad Habitats; distinctions explained to avoid ambiguity.
- 10 m Classified Pixel datasets
  - Created from multiple Classification Scenes; each pixel gets a most-likely class and a confidence probability.
  - First band: UKCEH Land Cover Class; Second band: class membership probability.
  - Not generalised with the UKCEH Land Parcel Spatial Framework to preserve fine-scale features.
- Land Parcel datasets
  - Result from overlaying the 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to generate parcel attributes.
  - MMU (minimum mapping unit) ~ 0.5 ha; parcels typically dominated by a single land cover type; supports change detection.
- 25 m Rasterised Land Parcels
  - Raster version of Land Parcel data; three bands per parcel: dominant land cover (mode), confidence, and purity.
  - GB and NI coordinate systems and extents specified (GB EPSG 27700; NI EPSG 29903).
- 1 km summary rasters
  - Summary products derived from 25 m rasters: dominant class per 1 km pixel, and percentage cover for each class/aggregate class.
  - Rounding can cause the 21-class total to deviate from 100%; coastal pixels may sum to less than 100.
- Seasonal Composite Images and Context Rasters
  - Seasonal Composites derived from Sentinel-2 at 10 m, four seasons; four bands per season used; occasional cloud gaps but classification robust to gaps.
  - 10 m Context Rasters used to reduce spectral confusion (GB and NI have different sets of context layers such as height, aspect, slope, proximity to roads/buildings, foreshore/woodland masks, etc.).
- Classification Scenes
  - GB: 32 Classification Scenes (~100 x 100 km tiles) classified independently; NI: a single 49-band Classification Scene combining a 40-band Sentinel-2 Seasonal Composite with NI Context Rasters.
  - Scene design aims to manage phenological variation and data volume; some intentional tile extent adjustments to accommodate sea coverage.
- UKCEH Land Parcel Spatial Framework
  - Established framework for parcel geometry since LCM2007; minor changes since LCM2015; unique parcel IDs (gid) may not align exactly with LCM2015 for cross-map comparisons.
- Bootstrap Training and Random Forest
  - Bootstrap Training uses historic LCM observations to automatically sample training data from current imagery, reducing the need for new field data.
  - Random Forest classifier trained on balanced Bootstrap Training samples (10,000 per bag) to derive the 10 m classified pixels.
  - Software stack combines WEKA, PostGIS, and GDAL (open source).

## Data access, formats, and metadata
- Projections and extents
  - GB: EPSG 27700; NI: EPSG 29903; 10 m and 25 m raster products; vector land parcel products with corresponding metadata.
- File formats
  - 10 m Classified Pixels: multi-band raster (class ID + confidence).
  - 25 m Rasterised Land Parcels: 3-band raster (mode, conf, purity).
  - Land Parcel Vector: parcel geometries with attributes including gid and other parcel-level stats.
  - 1 km Summary Rasters: single-band and multi-band rasters for class/aggregate class data.
- Data sources and validation
  - Validation uses 33,107 reference points from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke points; overall accuracy 83%.
- DOIs and citations
  - Each dataset has a DOI; recommended citations include Marston et al. (2024a–g) and Morton et al. (2011; 2007); overview in Marston et al. (2023/2024).
- Display and usage aids
  - Appendix 5 and 6 provide recommended color schemes (including color-blind friendly versions) and accompanying QGIS symbol files (lcm_raster*.qml).

## Production methodology in brief
- Seasonal spectral information
  - Sentinel-2 four-season composites (10 m) combined with Context Rasters to form Classification Scenes.
- Bootstrap Training and RF classification
  - Historical LCM observations sampled to train RF, ensuring ample representation of each class; balanced sampling mitigates dominance by common classes.
- Data processing framework
  - Custom UKCEH pipeline integrating WEKA, PostGIS, and GDAL; transparent methodology with ongoing improvements.

## Data quality, issues, and limitations
- Known issues
  - A small number of polygons missing from vector land parcel products; 25 m rasterised parcels and 10 m pixel datasets are otherwise unaffected; 1 km rasters remain valid.
  - Some classification confusions persist (e.g., Saltwater vs Freshwater near coasts; bog vs heath-related upland classes) despite context rasters.
  - Annual method changes can produce real changes plus methodological differences; users should consider method updates when comparing across years.
- Scale and accuracy notes
  - 83% overall accuracy at full thematic detail; class-level producer and user accuracies vary (confusion matrices provided in Appendix 4).

## Practical guidance for GIS specialists
- Data use
  - 10 m Classified Pixels: high-detail mapping; suitable for fine-scale analyses and feature-level mapping; not generalised by Land Parcel Framework to preserve detail.
  - 25 m Rasterised Land Parcels: suitable for parcel-based analyses, change detection, and integration with the Land Parcel Spatial Framework.
  - Land Parcel Vector: enables vector-based analyses and integration with GIS workflows; note potential gid mismatches with older datasets.
  - 1 km Summary Rasters: suitable for regional/broad-scale analyses and quick overviews; percentage sums may not equal 100 due to rounding.
- Visualization
  - Appendix 5 and 6 provide recommended color recipes; QGIS symbol files are included to support consistent visualization across platforms.
- Temporal considerations
  - LCM2023 is part of an annual series; automated Bootstrap Training and ongoing refinement aim to enhance comparability over time and support change detection.

## Appendices (high-level)
- Appendix 1: Notes on UKCEH Land Cover Classes (and nuances relative to UK BAP Broad Habitats).
- Appendix 2: Summary of Biodiversity Action Plan (BAP) Broad Habitats definitions.
- Appendix 3: Full list of LCM2023 datasets with DOIs.
- Appendix 4: Correspondence matrices (confusion/accuracy details by class).
- Appendix 5–6: Colour recipes for display (standard and color-blind friendly) and associated QGIS symbology files.