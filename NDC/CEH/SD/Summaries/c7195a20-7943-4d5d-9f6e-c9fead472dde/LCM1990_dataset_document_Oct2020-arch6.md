# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying Landsat-5 imagery into 21 Broad Habitat classes (based on JNCC/Jackson definitions) and structured to be compatible with the LCM2015 framework.
- Data products include vector (parcels with rich metadata), a 25m raster, and 1km aggregated products (dominant and percentage covers for target and aggregate classes).
- The dataset supports long-term land cover change analysis (planning for 25-year change products) and is archived with DOIs for reproducible citation.

## Data products and structure

- Vector data set
  - ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland.
  - Eight key attributes per polygon, including dominant class, uncertainty, and per-polygon pixel breakdown.
  - Unique geometry identifier (gid) stored for unambiguous communication.
- 25m raster
  - Three-band GeoTIFF: band 1 = dominant LCM1990 class, band 2 = mean per-polygon confidence, band 3 = percentage of polygon area covered by the modal class.
- 1km raster
  - Dominant cover (target and aggregate classes) and percentage cover (21 target, 10 aggregate) per 1km pixel.
  - Percentage layers are integer values; sums may not precisely equal 100 due to rounding.
- Data access formats and projections
  - Great Britain and Northern Ireland provided in separate datasets.
  - GB vector and rasters in British National Grid (EPSG: 27700); NI in Irish TM75 grid (EPSG: 29903).
- Minimum mapping unit
  - Parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape.

## Class definitions and mapping

- Total of 21 classes mapped from Broad Habitats (with some intra-class splits):
  - Examples of splits: Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh.
- Class relationships
  - Tables map LCM1990 target classes to Broad Habitats and aggregate/percentage products (kinship between 21 LCM1990 classes and the aggregate class schema used in 1km rasters).
- Metadata richness
  - Each polygon includes dominant class, per-polygon pixel breakdown by class, confidence, and other statistics to aid interpretation and quality checks.

## Data access and citation

- Unique DOIs exist for each product to enable precise citation (GB vector, GB 25m raster, GB 1km target/aggregate classes, NI vector, NI 25m raster, NI 1km target/aggregate classes).
- Access points
  - 25m and 1km raster data via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request; licensing may apply.
- Citation examples
  - Publications should include the DOI and authorship with year; example DOIs and recommended references are provided for GB and NI products.

## Projections and data details

- Projections
  - GB vector and raster data use British National Grid.
  - NI vector and raster data use TM75 Irish Grid.
- Spatial framework and compatibility
  - LCM1990 uses a polygonal framework aligned with LCM2015 to enable cross-era comparisons (e.g., 25-year change products).
- Citing DOIs for reproducibility
  - Each product has a DOI to support traceability and reuse in research and policy contexts.

## Quality assurance and validation

- QA checks include:
  - Correct projections and spatial completeness.
  - Modal class consistency in vector polygons.
  - Header and data range consistency (0–100 for raster percent values).
  - Pixel size verification and overall product integrity.
- Validation
  - A full validation exercise comparing LCM1990 against other datasets (Countryside Survey, National Forest Inventory, validation points) has been conducted; results to be reported in a separate publication.

## Usage notes and caveats

- LCM1990 maps land cover rather than strictly land use; some land uses may be indistinguishable from spectral data alone (e.g., recreation grass versus grazed grass).
- Some habitat classes (e.g., Fen/Marsh/Swamp, Saltmarsh) can be spectrally challenging and may be underestimated in certain patches.
- Coarse aggregation and rounding in 1km products can lead to slight deviations from 100% sums; coastal areas may show under- or overestimation due to coastal mapping extent and MMU considerations.
- The vector metadata enables detailed exploration, including per-polygon class breakdowns and confidence, which can inform data filtering and aggregation decisions.

## Appendix and metadata details

- Appendix coverage includes:
  - Broad Habitat definitions (for context on class mappings and interpretations).
  - Color-mapping schemes for standard LCM color legend representations.
  - Details on composite images used during classification.
- The dataset emphasizes metadata richness and per-polygon uncertainty, aiding assessment of reliability in downstream analyses.

## Contact and further information

- Access and information:
  - CEH Environmental Information Platform: https://eip.ceh.ac.uk/lcm/lcmdata
  - General inquiries: spatialdata@ceh.ac.uk
  - Licensing and access details: https://www.ceh.ac.uk/services/land-cover-map-1990
- Acknowledgement and references:
  - Supported by Natural Environment Research Council (UK-SCAPE program).
  - Key references include Jackson (2000), Morton et al. (2011), and Rowland et al. (2020) for change products.