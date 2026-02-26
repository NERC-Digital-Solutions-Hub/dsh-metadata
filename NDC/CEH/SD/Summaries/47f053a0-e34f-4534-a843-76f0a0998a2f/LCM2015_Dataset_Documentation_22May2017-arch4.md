# Dataset documentation

- LCM2015 is a UK parcel-based land cover map, produced to support diverse data user needs. It provides 21 Broad Habitat classes mapped from satellite imagery, plus corresponding 25m raster and 1km products. The vector (core) dataset contains 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland; the 25m raster is two-band (classification band + mean per-polygon probability); the 1km products include dominant and percentage cover for both 21 target classes and a reduced set of 10 aggregate classes.
- The dataset is described as a stable, archived product with individual DOIs for all components. Access options include the CEH Environmental Information Platform for 1km rasters and licensing on request for the full vector and 25m products.

Key facts and scope
- Name and purpose: Land Cover Map 2015 (LCM2015) datasets supporting land cover classification, not land use.
- Classification: 21 target Broad Habitat classes based on JNCC Broad Habitat definitions; some classes are further divided or aggregated in specific products.
- Data lineage: Built from two-date composite satellite images, primarily Landsat-8 (30 m) with AWIFS (60 m) as needed; uses a Random Forest classifier with ancillary data incorporated into the input.
- Training and methodology: Uses stable training areas (areas classified the same in 2000 and 2007) plus additional coastal and difficult classes; no segmentation in LCM2015 spatial framework; per-pixel classification summarized to polygons at the polygon level.
- Uncertainty and outputs: Provides per-polygon mean probability (uncertainty) from the classifier; includes pixel-level breakdown (Pix_dist) across classes; two-band 25m raster provides both class and probability; 1km rasters provide dominant class and percentage cover (for both 21 classes and 10 aggregates).
- Data products: 
  - Core vector product (GB and NI)
  - 25m raster (GB and NI)
  - 1km raster products (GB and NI): dominant cover and percentage cover (21 and 10-class groupings)
- Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha are dissolved into surrounding areas.
- Coordinate systems: GB data in British National Grid; NI data in TM75 Irish Grid.
- Accessibility and citation: DOIs provided for all products; licensing for vector and 25m raster on request; 1km rasters available via CEH platform; data citation guidelines included.

Data products and formats (high level)
- Vector data set
  - Attributes per polygon (nine core attributes, including gid, dominant class, uncertainty, pixel counts, and mosaic of per-class counts)
  - Pix_dist: 23 numbers listing counts for each of the 21 classes, plus npix and modal_class
  - Uncertainty information: unc and unc_stdev (mean per-polygon probability and its standard deviation)
  - Composite: indicates the composite image used for the classification
  - Volume: GB ~6.7M polygons; NI ~0.9M polygons
- 25m raster
  - Two bands: Band 1 = dominant LCM2015 class; Band 2 = mean per-polygon probability
  - Spatial resolution: 25 m
- 1km raster
  - Summary products derived from 25m data
  - Dominant cover (21-class and 10-aggregate class)
  - Percentage cover (21-class and 10-aggregate class) per 1 km pixel
  - Rounding may cause totals to deviate slightly from 100%; coastal pixels sum to less than 100%
- Spatial specifics
  - Great Britain grids: 25m and 1km rasters in GB National Grid; Northern Ireland grids use TM75 Irish Grid
  - DOIs exist for each product (vector GB, 25m raster GB, 1km GB target and aggregate classes, NI vector, NI rasters)

Citing and data access
- Access: 
  - 1km raster data: CEH Environmental Information Platform
  - Full vector and 25m raster: license on request from CEH
- Citing LCM2015: each product has its own DOI; example format provided in the document
- Projections and data specifics are documented in tables; data provenance and processing metadata are retained for transparency

Methodology and background highlights
- Data sources and classification approach
  - Landsat-8 and AWIFS imagery used to produce two-date composites
  - Random Forest classifier chosen to handle multi-modal training data; eliminates need for spectral sub-classes
  - Ancillary data (e.g., slope, distance to rivers) integrated as inputs rather than post-classification rules
- Training data and framework
  - Stable data areas from 2000 and 2007 used as a baseline, supplemented with coastal and difficult classes
  - Per-polygon labels derived from modal class across constituent pixels
- Spatial framework decisions
  - No segmentation in LCM2015 to improve change mapping suitability and avoid segmentation mismatch across time
  - Minor spatial framework fixes implemented; segmentation used in prior maps is not employed in LCM2015
- Class definitions and mapping
  - 21 target Broad Habitat classes aligned with JNCC definitions; several classes are further divided (e.g., Urban vs Suburban; Heather vs Heather grassland)
  - Appendix materials provide detailed class definitions and color mappings
  - Some nuances exist in mapping mixed woodland, bracken, and grassland categories due to spectral signatures and training data limitations
- Versioning and updates
  - Version 1.2 (updates include data publication year correction and vector composite attribute adjustments)

Important cautions and usage notes for data leaders
- Change mapping caveat: The report advises that LCM2015 is not suitable for change mapping in its current state; differences across time come from real changes and classification/methodological differences between products
- Data quality and interpretation cautions
  - Differences from LCM2007 and changes in output data reflect methodological evolution (random forest, lack of segmentation, changes to grassland and montane classes)
  - Users should consult appendices for class definitions and notes on potential misclassifications (e.g., grassland subtypes, mixed woodland)
- Metadata richness and uncertainty
  - Rich polygon metadata and per-polygon probability provide transparency for assessing confidence and enabling quality control
  - The gid attribute enables unambiguous cross-dataset communication and downstream data integration
- Data governance considerations
  - Strong emphasis on data provenance, DOIs for reproducibility, and licensing controls
  - Encourages use of the DOIs in publications to support traceability and repeatability
  - Clear guidance on when to rely on vector vs. raster products depending on application needs

Appendices and supplementary details (highlights)
- Appendix 1 and 2: Detailed Broad Habitat class definitions aligned with JNCC (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, wetlands, urban, littoral, and marine-related habitats)
- Appendix 3: LCM2015 color mapping recipe for visualization
- Appendix 4: Composite image metadata used in the LCM2015 production

Notes for data governance and policy teams
- The dataset is designed to support a wide range of users, but governance and change mapping considerations require careful interpretation of changes across versions
- The DOIs and licensing pathways should be integrated into data access policies and citation workflows to ensure reproducibility and proper attribution
- Ensure downstream procurement and licensing agreements consider the potential for substantial data volumes (vector + 25m) and associated storage/processing requirements

Further information and contact
- Data access and information: CEH websites and the CEH Environmental Information Platform
- Queries: spatialdata@ceh.ac.uk
- The LCM2015 data paper is in preparation and will include additional information