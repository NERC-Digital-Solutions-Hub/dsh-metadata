# Dataset documentation

- Land Cover Map 1990 (LCM1990) is documented as a complex data set with multiple products designed for UK land cover monitoring and long-term change analysis.
- This document explains data products, provenance, formats, access, quality assurance, and citation requirements.

## Purpose and background

- LCM1990 is a parcel-based land cover map for the UK, classifying Landsat-5 imagery (30 m) into 21 Broad Habitat-based classes.
- Built to be compatible with LCM2015 and LCM2007 frameworks to enable long-term change assessments (e.g., 1990–2015).
- Spatial framework and class structure are designed for easy interpretation and interoperability with other geospatial data.
- Distinguishes land cover from land use in many cases; some land uses cannot be inferred purely from land cover.

## Data products and structure

- Core concepts
  - Vector data set: polygons with rich metadata per parcel, including dominant class, per-polygon classifications, and uncertainty metrics.
  - Raster data: derived 25 m and 1 km products from the vector, supporting various modelling scales.
- Vector data set
  - Contains 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Key attributes include gid (unique parcel ID), hist (list of classes per polygon with pixel counts), mode (recommended display class), purity, conf (mean confidence from Random Forest), stdev, n (pixel count), and cmp (composite image source).
- Raster data sets
  - 25 m raster: 3-band GeoTIFF
    - Band 1: dominant LCM1990 class per polygon
    - Band 2: mean per-polygon confidence from RF classifier
    - Band 3: percentage of polygon area covered by the modal class
  - 1 km raster: summary products derived from 25 m data
    - Dominant cover per 1 km pixel (target and aggregate classes)
    - Percentage cover per 1 km pixel (21 target bands; 10 aggregate bands)
  - Coordinate systems: GB datasets use British National Grid; NI datasets use Irish Grid
  - Minimum mappable area: >0.5 ha; features smaller than this are dissolved into surrounding areas
- Class structure
  - 21 LCM1990 target classes aligned with UK Broad Habitats; some classes subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment)
  - Tables describe how 21 LCM1990 classes map to Broad Habitats and aggregate 1 km products
- Data formats and delivery
  - 25 m raster: uncompressed GeoTIFF, 8-bit unsigned
  - 1 km raster: uncompressed GeoTIFF, 8-bit unsigned
  - Vector: polygon features with associated attributes
  - Example spatial extents and metadata details provided for interoperability

## Data quality, validation, and uncertainty

- QA checks cover projections, spatial completeness, modal class presence, header consistency, value ranges (0–100 for raster products), and pixel size accuracy.
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; a full validation publication is planned.
- Uncertainty information included: per-pixel Random Forest probability translated to polygon-level mean confidence and standard deviation.

## Access, licensing, and citation

- Data access
  - Raster products (25 m and 1 km) are available via the CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
  - Full vector product is available on request under licence from CEH (details at https://www.ceh.ac.uk/services/land-cover-map-1990 or contact spatialdata@ceh.ac.uk); licence fees may apply.
- Citation and DOIs
  - Each LCM1990 product has an individual DOI (published for Great Britain and Northern Ireland) to enable precise citation.
  - Example citation format recommended: include author and date in-text (e.g., Rowland et al., 2020) and full DOI in references, e.g., Land Cover Map 1990 (vector, GB). NERC EIDC. https://doi.org/...
  - DOIs cover GB vector, GB 25 m raster, 1 km percentage and dominant target classes (and aggregates), and NI equivalents.
- Use in publications
  - Citations should acknowledge authors, year, and DOI to ensure reproducibility and traceability of methods and usage.

## Practical notes for analysts

- The dataset supports long-term environmental monitoring and change-tracking when used in conjunction with LCM2007/LCM2015 and other datasets.
- Users should be mindful of the distinction between land cover and land use; some land uses (e.g., recreation on grassland) may not be distinguishable from land cover alone.
- The per-polygon histograms and RF-based confidence allow assessment of classification reliability at the parcel level.
- For modelling at national scales, 1 km percentage/dominant products provide efficient integration with meteorological and species distribution datasets.
- Because some coastal and small features are near the minimum mapping unit, users should consider potential underestimation or misclassification in marginal areas.

## Support and contact

- Further information and access requests: CEH Environmental Information Platform (EIP) and spatialdata@ceh.ac.uk
- Journal paper and additional documentation are in preparation, with Appendix and methodological detail available in the dataset documentation and related CEH portals.

## Related materials

- Appendix information and methodological references (e.g., classification framework, Broad Habitat definitions, and DOIs) are provided within the full dataset documentation and linked resources.