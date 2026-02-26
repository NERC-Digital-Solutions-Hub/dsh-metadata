# Dataset documentation

- A UK parcel-based land cover map (LCM2015) with 21 classes, aligned to UK Biodiversity Action Plan Broad Habitats; produced from two-date Landsat-8 (30 m) and AWIFS (60 m) composites; designed to support monitoring, policy scrutiny, and future decision-making; updated from LCM2007 to enable change mapping; notes that differences between maps reflect both real changes and classification differences.

## What LCM2015 is and how it’s structured

- Land cover mapping, not land use; produced as a suite of data products to serve diverse monitoring needs.
- Spatial framework built on real-world boundaries (polygons) to aid interpretation and interoperability with other geospatial datasets.
- Core data formats include:
  - Vector data set (GB and NI): polygons with rich attributes; ~6.7 million polygons for GB and ~0.9 million for NI.
  - 25 m raster: two-band product per polygon (band 1 = dominant class, band 2 = mean per-polygon probability).
  - 1 km raster products: aggregate dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
- Minimum mapping unit: parcels >0.5 ha; small parcels (<0.5 ha) and short features (<20 m) dissolved into surrounding area.
- Projects supported by DOIs for all products to enable repeatable citation and tracking of usage.

## Key differences from LCM2007 (highlights for monitoring work)

- Output data changes
  - Montane class removed; distribution reclassified as Inland Rock or other upland habitats using spectral data (not altitude thresholds).
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitat types; no soil data used in LCM2015 classification.
  - 25 m raster becomes a two-band image (classification band + mean probability in band 2); probability data simplified (vector stores per-polygon mean probability; 25 m raster band 2 holds this value).
  - Probability data for 1 km products not provided; spectral sub-classes removed (no per-subclass probabilities).
  - Spatial framework eliminated segmentation; per-pixel (not segmentation-based) classification for improved consistency and change detection suitability, particularly in uplands.
  - Mixed woodland training now uses pure stands for Coniferous/Broadleaf training; final polygon label is the modal class of the pixel-level classifications.
- Methodology shifts
  - New Random Forest classifier replaces Maximum Likelihood; handles multi-model data without sub-class grouping; typically improved performance.
  - Ancillary data (e.g., altitude, soil) are inputs to the classification rather than post-classification rules; enhances objectivity and integration of contextual information.
  - Stable training areas approach (initially from 2000/2007 overlap) extended with coastal and difficult classes; inter-tidal areas removed from stable data; coastal/coarse areas addressed through supplemental training data.
- Scope and outputs
  - LCM2015 maps land cover and provides extensive metadata and uncertainty information at polygon level.
  - 21 target classes (with some groupings, e.g., Urban/Suburban under Built-up Areas and Gardens) and 10 aggregate classes for 1 km products.
  - Labelling uses unique geometry identifiers (gid) to enable unambiguous data communication.

## Data products in detail

- Vector data set
  - 9 attributes per polygon, including:
    - gid: unique parcel identifier
    - BHAB: dominant Broad Habitat class (text and integer)
    - Pix_dist: list of pixel counts for all 21 classes plus total and modal class
    - unc: mean per-polygon probability from Random Forest (0–255 scale)
    - unc_stdev: standard deviation of uncertainty
    - npix: number of pixels in the polygon
    - Modal_class: recommended class for display (1–21)
    - Modal_prop: proportion of polygon classified as dominant class
    - Composite: composite image identifier used for the classification
- Raster data sets
  - 25 m raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability
  - 1 km raster: dominant class and percentage cover for both 21 classes and 10 aggregate classes
- Class structure
  - 21 target classes mapped to Broad Habitats; some broad habitats are subdivided (e.g., Urban vs Suburban, Heather vs Heather grassland)
  - Tables and appendices define detailed mappings and colour conventions for data visualization

## Metadata, uncertainty, and data governance

- Rich metadata at the polygon level; includes dominant class details, per-polygon breakdown, and mean probabilities from the classifier.
- Uncertainty information is explicitly provided via the per-polygon probability (Random Forest output).
- Each data product has a Digital Object Identifier (DOI) to support precise citation and reproducibility.
- Data are available in two GB/NI geographic contexts (British National Grid for GB; Irish National Grid for NI); coordinate systems and extents are specified.

## Access, usage, and citations

- Data access
  - 1 km raster data accessible via the CEH Environmental Information Platform (EIP).
  - Full vector and 25 m raster products available on request under licence; online application process described by CEH.
  - Licence fees may apply for some users and applications.
- Citing LCM2015
  - Each product has its own DOI; references should include authors and year in text and full DOI in references.
  - Example DOIs are provided for GB and NI vector, 25 m, 1 km dominant/percentage products, and aggregate products.
- Practical notes for users
  - The vector dataset is large; the 25 m raster offers a lighter-weight alternative with the same classification detail but less metadata overhead.
  - The 1 km products are intended for national-scale modelling and cross-dataset integration (e.g., with meteorology or species distributions).

## Practical implications for monitoring frameworks

- Provides multi-scale data suitable for policy evaluation and long-term trend analysis:
  - Fine-scale per-polygon data with explicit uncertainty supports robust uncertainty analyses in environmental health monitoring.
  - Per-polygon gid and rich metadata enable reproducible reporting and traceability of results.
  - Availability of DOIs enhances transparency and citability of dataset-derived indicators.
- Clear documentation of methodological changes and data governance facilitates transparent interpretation of changes across monitoring periods.
- Limitations and cautions are acknowledged (e.g., not all maps are ideal for change mapping in their current state; differences arise from both real change and classification updates).

## Appendix highlights (classification framework)

- Detailed descriptions and definitions of the 21 LCM2015 classes mapped to Broad Habitats.
- Notes on specific classes (e.g., Broadleaved Woodland, Coniferous Woodland, Arable and Horticulture, various Grasslands, Bracken, Bog, Wetlands, Inland Rock, Urban/Suburban, Littoral and Supralittoral habitats, etc.).
- Colour-mapping conventions and class labelling guidance to support consistent visualization and reporting.