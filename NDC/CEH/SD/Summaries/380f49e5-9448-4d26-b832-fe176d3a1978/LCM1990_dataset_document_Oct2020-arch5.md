# Dataset documentation

- LCM1990 (Land Cover Map 1990) is a parcel-based UK land cover map created from Landsat-5 imagery (30 m) and aligned with the LCM2015 framework to enable 25-year change analyses.
- The dataset comprises multiple data products: a core vector (parcels) and raster products at 25 m and 1 km resolutions, plus aggregate/dominant-class outputs for 21 target classes.
- Each parcel is assigned a unique geometry ID (gid) and rich metadata, including per-polygon class breakdowns, mean classification probability, and uncertainty measures.
- DOIs are provided for all products to support stable citation and reproducibility (GB and NI separately; vector, 25 m raster, and 1 km products in various target/aggregate formats).

## Data products and structure

- Vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland.
  - Key attributes: gid, hist (class composition per polygon), _mode (dominant class), _purity (percent mapped to dominant class), _conf (mean confidence 0–100), _stdev (uncertainty), _n (pixel count), cmp (composite image source).
- Raster data sets
  - 25 m raster: 3-band GeoTIFF (band 1 dominant class per polygon; band 2 mean confidence; band 3 percent coverage of dominant class). Spatial extents differ GB vs NI; 25 m resolution.
  - 1 km raster: aggregation of 25 m results to provide dominant class (1 band) and percentage cover (21 bands for target classes; 10 bands for aggregate classes).
  - Minimum mappable unit: >0.5 ha; polygons smaller than 0.5 ha and linear features <20 m were dissolved into surrounding landscape.
- Class framework
  - 21 classes based on UK Biodiversity Action Plan Broad Habitats (with some subclasses available, e.g., Built-up Areas subdivided into Urban and Suburban; Dwarf Shrub Heath subdivided into Heather and Heather grassland; Littoral Sediment subdivided into Saltmarsh and Littoral sediment).
  - Vector provides detailed metadata for each polygon plus pixel-level class proportions and per-polygon probability; raster products provide summaries and confidence measures.

## Data access, licensing, and citation

- Access
  - 25 m and 1 km rasters: CEH Environmental Information Platform (EIP) at https://eip.ceh.ac.uk/
  - Full vector product: available on request from CEH; licence fees may apply for some users/applications.
- Citation and DOIs
  - Each LCM1990 product has its own DOI (GB and NI combinations for vector, 25 m, 1 km target, 1 km dominant, and 1 km aggregates). Use author(s) and date in text and include full DOI in references.
  - Example citation: Rowland et al. (2020) Land Cover Map 1990 (vector, GB). CEH Environmental Information Data Centre. https://doi.org/10.5285/304a7a40-1388-49f5-b3ac-709129406399
- Data licensing notes
  - Licence fees may apply; some data are available under licence on request; check CEH pages for access specifics.

## Metadata, provenance, and data quality

- Rich metadata
  - Each vector polygon includes dominant class, per-class pixel breakdown, mean probability, and processing details.
  - Processing lineage mirrors LCM2007/LCM2015 methods to maximize compatibility across LCM products.
- Uncertainty and confidence
  - Random Forest classification provides per-pixel probability; polygon-level mean confidence is included in 25 m raster band 2 and in vector _conf.
  - Uncertainty and accuracy validated against external datasets (Countryside Survey, NFIs, validation points); results to be published separately.
- Quality assurance
  - QA checks cover projections, spatial completeness, modal class presence, data set headings, value ranges (0–100 for rasters), and pixel size accuracy.
  - Data preparation builds on 2007 OS MasterMap-derived parcel framework; field boundary changes are infrequent, limiting impact on overall accuracy.
- Data completeness and consistency
  - DOIs enable consistent citation and reuse tracking; documentation provides detailed guidance on class definitions and mapping decisions (Appendices describe Broad Habitat mappings and related caveats).

## Data governance, stewardship, and practical considerations

- Multi-format delivery
  - Vector data provides rich, attribute-dense parcels; raster products offer simpler processing routes with reduced metadata load.
- Interoperability and comparability
  - The 1990 product uses an updated spatial framework to align with LCM2007/LCM2015, supporting long-term change analysis (e.g., 1990–2015).
- Documentation and user guidance
  - Detailed appendices explain class definitions, colour mappings, composite imagery, and limitations of remote-sensing classification for certain Broad Habitats (e.g., fen, bog, littoral habitats).
- Data discovery and contact
  - Access details and contact information provided (spatialdata@ceh.ac.uk) for further queries and access arrangements.

## Endnotes and references

- Data citations and DOIs, access portals, and contact details are provided to support data discovery, reuse, and proper attribution.
- Acknowledgement: CEH work supported by NERC under UK-SCAPE programme.
- Further information: CEH CEH Environmental Information Platform and LCM1990 data pages; journal papers and appendices detailing methodologies and habitat classifications.