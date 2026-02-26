# Dataset documentation

- LCM1990 is a parcel-based land cover map for the UK, produced from Landsat-5 imagery (30 m) and classified into 21 land cover classes aligned with UK Biodiversity Action Plan Broad Habitats.
- The dataset is distributed as multiple data products (vector and raster) with rich metadata and uncertainty information, designed to support diverse GIS applications and people who need to map, analyse, and communicate spatial land cover.

## Data products and formats

- Vector data set
  - Polygons with attached attributes for dominant class, per-polygon pixel breakdown, source image, uncertainty metrics, and a unique geometry identifier (gid).
  - 6.7 million polygons in Great Britain; 0.9 million in Northern Ireland.
  - Key attributes include _hist (class composition), _mode (recommended display class), _purity, _conf, _stdev, _n, and cmp (composite image).
- 25 m raster
  - Three-band GeoTIFF: band 1 dominant class per polygon, band 2 mean per-polygon confidence, band 3 percent coverage by modal class.
  - Separate rasters for Great Britain and Northern Ireland; coordinate systems: GB (British National Grid, EPSG 27700), NI (TM75 Irish Grid, EPSG 29903).
- 1 km raster
  - Aggregated products derived from the 25 m raster:
    - Dominant cover at 1 km for Target and for Aggregate classes (1 band each)
    - Percentage cover at 1 km for Target classes (21 bands) and for Aggregate classes (10 bands)
  - Percentage values are integer; sums may not exactly equal 100 due to rounding; coastal pixels may sum to less than 100.
- Core product and relations
  - Core product: LCM1990 vector from which the 25 m raster is derived.
  - The 25 m raster feeds the 1 km percentage/dominant products and the dominant cover products.
- Minimum mapping unit
  - Parcels smaller than 0.5 ha and linear features under 20 m were dissolved into the surrounding landscape.

## Class structure and mapping

- 21 LCM1990 classes (based on UK Broad Habitats). In some cases, broader classes can be subdivided by spectral signatures:
  - Built-up Areas and Gardens split into Suburban and Urban
  - Dwarf Shrub Heath split into Heather and Heather grassland
  - Littoral Sediment split into Littoral sediment and Saltmarsh (Priority Habitat)
- LCM1990 maps land cover (not strictly land use); some land uses cannot be inferred from the spectral data alone.
- Object-based vector labelling
  - Each parcel has a unique gid; users are advised to retain gid for unambiguous communication.
- Metadata and uncertainty
  - Rich per-polygon metadata and per-polygon mean classification probability (uncertainty) from the Random Forest classifier.
  - Uncertainty is also available as per-pixel probability in the 25 m raster.

## Data quality, QA, and provenance

- QA checks include: correct projections, spatial completeness, modal class presence for vector polygons, matching documentation headings, value ranges (0–100 for raster percentage products), and pixel size validation.
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) described in separate publications.
- Production framework is aligned with LCM2015 methods to maximise compatibility across LCM products.

## Data access, formats, and citation

- Data access
  - 25 m and 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available on request under licence from CEH (spatialdata@ceh.ac.uk); licensing fees may apply.
- DOIs and citation
  - Each LCM1990 product has a DOI; see Tables 5 (Great Britain) and 6 (Northern Ireland) for the exact identifiers.
  - Example citation: Rowland et al. (2020). Land Cover Map 1990 (vector, GB). NERC Environmental Information Data Centre. https://doi.org/...
  - For publications, include author(s) and date in text and full DOI in the references.
- Projections and geographic coverage
  - Great Britain vector/raster: British National Grid (OSGB 27700)
  - Northern Ireland vector/raster: Irish Grid (TM75)
- Access URLs and documentation
  - Main information and data access: CEH eIP pages for LCM1990
  - Contact: spatialdata@ceh.ac.uk
  - Dataset documentation and related references available via CEH LCM data pages

## Documentation depth and content

- Appendix-like documentation
  - Appendix 1 and 2 provide insights into class definitions and how Broad Habitat concepts map to LCM1990 classes.
  - Appendix 3 contains the standard LCM colour mapping scheme.
  - Appendix 4 lists the composite images used during classification.
- Map projections and coordinate details included in Table metadata for rasters.
- The dataset is designed to enable both detailed, parcel-level analyses (vector) and efficient, large-area modelling or visualization (raster products).

## Practical notes for GIS specialists

- Choose between vector vs. raster based on use case:
  - Vector: rich per-polygon metadata; best for detailed feature-based analysis and display where polygon boundaries matter.
  - 25 m raster: compact per-pixel data with confidence and modal-class information; suitable for overlay in map viewers and raster-based analyses.
  - 1 km raster: ideal for UK-scale modelling with percentage/dominant coverage summaries when high-resolution detail is not required.
- Be mindful of the minimum mapping unit and dissolution of small features during data preparation.
- When citing or reusing data in analyses or publications, use the provided DOIs and include citations as described in the documentation.
- Review Appendix resources for interpretation guidance on Broad Habitat mappings and color conventions to ensure consistent visualization and reporting.