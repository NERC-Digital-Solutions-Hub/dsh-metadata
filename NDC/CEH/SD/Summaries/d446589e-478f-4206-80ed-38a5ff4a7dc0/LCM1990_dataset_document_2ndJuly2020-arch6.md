# Dataset documentation

- The Land Cover Map 1990 (LCM1990) dataset documentation explains a complex, parcel-based land cover map for the UK, derived from Landsat-5 imagery at 30 m resolution and categorized into 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitats. The dataset is designed to be compatible with later LCM products (e.g., 2007, 2015) to support long-term change analyses and broad applicability across user communities.

## Overview and scope

- Purpose: Provide a range of data products to support diverse LCM user needs, including data discovery, combination, analysis, and application development.
- Core features:
  - Maps land cover (not land use) with 21 classes based on Broad Habitats.
  - Uses a polygon-based (vector) framework with a 25 m raster derivative for analysis at multiple scales (25 m, 1 km; separate GB and NI projections).
  - Includes rich metadata, per-polygon uncertainty, and per-polygon class probabilities from a Random Forest classifier.
- Versions and access: Version 1.0 (2020); data distributed via CEH platforms; vector product available on request; licensing may apply for some users.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each polygon includes attributes such as dominant class, source image, per-polygon confidence, number of pixels, and a detailed histogram of class composition.
  - Key attributes:
    - gid: Unique parcel identifier
    - hist: List of classes present with pixel counts (e.g., "20:1, 21:9")
    - mode: Recommended display class (1–21)
    - purity: Percentage of polygon covered by the modal class
    - conf: Mean per-polygon vote confidence (0–100)
    - stdev: Uncertainty standard deviation
    - n: Number of pixels in polygon
    - cmp: Composite image source index
- Raster data sets (derived from vector)
  - 25 m raster: 3-band GeoTIFF
    - Band 1: Dominant class per polygon
    - Band 2: Mean per-polygon confidence (RF)
    - Band 3: Percentage of polygon area covered by the modal class
  - 1 km raster: Aggregate and percentage cover products
    - Dominant cover (1 band) for both target and aggregate classes
    - Percentage cover (21 bands for target, 10 bands for aggregate)
  - Grid and projection details vary GB vs NI (British National Grid for GB; TM75 Irish Grid for NI)
  - Spatial extents provided for GB and NI with explicit metadata on pixel counts and corner coordinates
- Class relationships
  - 21 LCM1990 target classes correspond to Broad Habitats; certain classes are subdivided (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh distinctions)
- Data formats and resolution
  - Vector: polygon-based with rich metadata
  - Raster: 25 m and 1 km products; uncompressed GeoTIFFs; 8-bit unsigned for pixel values
  - 1 km products derived from 25 m data by calculating class percentages and dominant class per 1 km cell

## Class system and mapping details

- 21 LCM1990 classes derived from UK Broad Habitats definitions (JNCC Jackson, 2000)
- Some sections of Broad Habitats are split to improve classification clarity in spectral data (e.g., urban vs suburban, heather vs heather grassland)
- Appendix 1 and Appendix 2 provide detailed interpretations, caveats, and guidance on how spectral signatures map to Broad Habitats, including potential misclassifications (e.g., Neutral vs Improved Grassland) and considerations for field verification

## Data access, usage, and citation

- Access points
  - 25 m and 1 km raster products available via the CEH Environmental Information Platform (EIP)
  - Full vector product available on request from CEH (licensing may apply)
- Data citation and DOIs
  - Each LCM1990 product has an associated DOI; examples include GB vector, GB 25 m raster, GB 1 km percentage/dominant classes, NI counterparts
  - Citations should include author and date (e.g., Rowland et al., 2020) and full DOI in references
  - Example citation format provided for journal publications and data products
- Map projections and coordinate systems
  - GB vector/raster: British National Grid (EPSG 27700)
  - NI vector/raster: TM75 Irish Grid (EPSG 29903)
- Data licensing
  - CEH CEH Environmental Information Platform provides access; vector product may require licence or formal access; fees may apply for some users and applications
- Usage guidance
  - The vector product’s gid enables unambiguous communication across outputs
  - The raster products (25 m and 1 km) are suitable for broad-range modelling and aggregation with other data (e.g., meteorological, species distribution)

## Quality assurance and validation

- QA checks ensure projections, spatial completeness, correct polygon modal class, proper headers, value ranges (0–100 for 1 km percentage data), and correct pixel sizes
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) performed; results to be published separately
- The LCM1990 dataset leverages the UK CEH land cover map framework and 2007 OS MasterMap-derived parcel framework; occasional field boundary changes are noted as having limited impact on overall mapping accuracy

## Metadata richness and uncertainty

- Rich per-polygon metadata includes dominant class, per-class pixel counts, and mean classification probability
- Uncertainty is captured via per-polygon confidence (RF-based) and standard deviation
- This enables users to assess reliability when combining polygons or performing change analyses

## Appendices and supplementary information

- Appendix 1: Comments on LCM1990 class mappings to Broad Habitats, with guidance on interpretation and potential ambiguities (e.g., grassland classifications, shrub/heath distinctions)
- Appendix 2: Overview of Biodiversity Action Plan Broad Habitats (21 categories) with concise definitions to aid interpretation
- Appendix 3: Standard LCM colour mapping recipe for display (class-number to RGB values)
- Appendix 4: Composite images used for classification (metadata details)

## Summary for data users and data support

- LCM1990 provides a robust, multi-resolution data framework (vector and raster) mapping 21 land cover classes aligned with Broad Habitats, enabling self-serve analysis and cross-product compatibility with later LCM datasets
- Rich metadata and uncertainty measures support quality assessment and informed data integration
- Access is via CEH platforms with DOI-backed citations; licensing considerations may apply for vector data
- The documentation emphasizes careful interpretation of classes, potential misclassifications, and the need for field validation in some contexts
- For further information and access, see the CEH LCM1990 data pages and contact spatialdata@ceh.ac.uk