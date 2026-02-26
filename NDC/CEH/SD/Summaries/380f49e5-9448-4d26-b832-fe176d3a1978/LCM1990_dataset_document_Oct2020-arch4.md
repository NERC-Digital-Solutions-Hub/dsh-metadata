# Dataset documentation

- LCM1990 (Land Cover Map 1990) is a UK parcel-based land cover map created by classifying Landsat-5 imagery (30 m) into 21 classes based on JNCC Broad Habitat definitions. It provides a suite of data products to support diverse user needs and is designed for long-term archiving and cross-product compatibility with later LCM versions (LCM2007, LCM2015).

- Data products and structure
  - Vector data set: polygons with rich attributes per parcel, including dominant class, pixel counts per class, source image, uncertainty metrics, and a unique geometry identifier (gid). GB vector contains 6.7 million polygons; NI vector ~0.9 million.
  - Raster data sets: derived from the vector product
    - 25 m raster: 3-band GeoTIFF (dominant class, per-polygon confidence, and percent coverage)
    - 1 km raster: dominant cover (1-band) and percentage cover (21-band for target classes; 10-band for aggregate classes)
  - Spatial references: GB uses British National Grid; NI uses Irish Grid (TM75); separate GB and NI data sets reflect their projections.
  - The core product is the 1990 vector; the 25 m raster is derived from it; 1 km products summarize the 25 m data for broad-scale modelling (e.g., climate, species distribution).

- Classes and mapping
  - 21 LCM1990 target classes mapped from 21 Broad Habitat categories; several broad habitats are subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral/Supra-littoral distinctions).
  - Appendix 1 and Appendix 2 provide detailed definitions and mapping considerations for each Broad Habitat class.
  - LCM1990 maps land cover (not strictly land use); some land-use inferences may be limited (e.g., grass used for recreation may resemble grazing land).

- Metadata and uncertainty
  - Vector attributes include dominant class (mode), hist (class composition within polygon), purity (dominant fraction), conf (mean classifier confidence), stdev, n (number of pixels), and cmp (composite image source).
  - Uncertainty is explicitly captured via per-pixel probability from the Random Forest classifier, reported per polygon and in the 25 m raster’s band 2.
  - Rich metadata accompanies polygons to aid interpretation and data reuse.

- Data access and licensing
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk/lcmdata). 
  - The full vector product is available on request under licence from CEH; some uses may incur licence fees.
  - DOIs exist for all LCM1990 products to support citation and reproducibility (separate DOIs for GB vector, GB 25 m raster, GB 1 km targets, GB 1 km aggregates, NI vector, NI 25 m raster, NI 1 km targets, NI 1 km aggregates).

- Citation and reuse
  - When using LCM1990 data in publications or analyses, cite the specific product DOIs (e.g., GB vector, GB rasters, NI rasters) and include author(s) and date (e.g., Rowland et al., 2020).
  - Data citation guidance and DOI URLs are provided to facilitate transparent, repeatable methods (examples and references included in the documentation).

- Quality assurance and validation
  - UK CEH Land Cover Maps are produced with defined methods and QA checks (projections, spatial completeness, modal class in polygons for vectors, value ranges for rasters, correct pixel sizes).
  - A formal validation exercise was conducted comparing LCM1990 with other datasets (Countryside Survey, National Forest Inventory) with results to be described in a separate publication.
  - The dataset is designed for transparency and traceability, with a documented lineage from 1990 imagery through to current, interoperable products.

- Projections and geographic scope
  - British National Grid for Great Britain; Irish National Grid (TM75) for Northern Ireland.
  - Spatial units include a minimum mapped area threshold (>0.5 ha for polygons; smaller features dissolved into surrounding landscape).

- Access points and contact
  - Data and documentation available at CEH’s LCM data portal: https://eip.ceh.ac.uk/lcm/lcmdata
  - For access or licensing inquiries: spatialdata@ceh.ac.uk

- Documentation scope and support
  - This dataset documentation emphasizes responsible use and provides context on methods, class definitions, data structure, and how to cite the data.
  - Appendix materials cover detailed class mappings, colour mapping, and information on composite images used during production.

- Acknowledgement and provenance
  - Funded by the Natural Environment Research Council as part of UK-SCAPE National Capability.