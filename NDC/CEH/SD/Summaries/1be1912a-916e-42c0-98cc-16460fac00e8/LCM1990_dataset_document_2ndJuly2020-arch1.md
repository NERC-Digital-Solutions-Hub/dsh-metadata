# Dataset documentation

- Overview
  - Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map created by classifying Landsat-5 satellite imagery into 21 Broad Habitat-based classes.
  - Built to be compatible with the LCM2015/LCM2007 frameworks to enable long-term change analyses (e.g., 1990–2015).
  - Spatial framework derived from generalised cartography (OSMM GB; Lands & Property Services NI) and refined with rural boundary data.
  - Minimum mapping unit is >0.5 ha; polygons <0.5 ha or linear features <20 m are dissolved into surrounding areas.
  - Distinguishes land cover (not always strictly land use) and provides rich metadata and uncertainty information.

- Data products and formats
  - Vector data set: polygons with key attributes (gid, hist, mode, purity, conf, stdev, n, cmp) and 21 target classes; GB has ~6.7 million polygons, NI ~0.9 million.
  - 25 m raster: 3-band GeoTIFF
    - Band 1: dominant class per polygon
    - Band 2: mean per-polygon confidence from Random Forest
    - Band 3: percentage area of the polygon covered by the modal class
  - 1 km raster: derived from 25 m data
    - Dominant cover at 1 km (21 target classes; 1-band)
    - Dominant cover at 1 km (10 aggregate classes; 1-band)
    - Percentage cover at 1 km for target classes (21 bands)
    - Percentage cover at 1 km for aggregate classes (10 bands)
  - Aggregate classes simplify usage; 1 km products support UK-scale modelling with other datasets (e.g., climate, species distribution).

- Class structure
  - 21 Broad Habitat-based classes (based on UK Biodiversity Action Plan definitions)
  - Some classes subdivided for spectral clarity:
    - Built-up Areas and Gardens → Urban and Suburban
    - Dwarf Shrub Heath → Heather and Heather grassland
    - Littoral Sediment → Saltmarsh and Littoral sediment
  - LCM1990 maps land cover (not strictly land use); spectral distinctions may not perfectly separate some land-use types.

- Metadata and uncertainty
  - Rich polygon metadata including dominant class, pixel-level breakdown, and mean classification probability.
  - Uncertainty captured via Random Forest per-pixel probabilities; reported per polygon and in raster bands.

- Data access and citation
  - Access via CEH Environmental Information Platform (eip.ceh.ac.uk) for 25 m raster and related products.
  - Full vector product available on request; licensing fees may apply.
  - Every product has its own Digital Object Identifier (DOI); guidance provided for citations and references.
  - Example citation format provided (Rowland et al., 2020; DOI references included in Table 5 for GB and Table 6 for NI).

- Spatial reference and coverage
  - GB data: British National Grid (EPSG 27700)
  - NI data: Irish Grid (TM75 Irish Grid; EPSG 29903)
  - GB and NI datasets provided separately to reflect distinct projections and extents.

- Quality assurance and validation
  - QA checks ensure correct projections, spatial completeness, modal class assignment for vector data, value ranges (0–100 for raster data), and pixel size accuracy.
  - Full validation against other datasets (Countryside Survey, National Forest Inventory, etc.) conducted; results reported in a separate publication.
  - Production framework aligned with LCM2007 and LCM2015 methods to maximize cross-product compatibility.

- Related information and context
  - Data underpin long-term land cover change analyses (e.g., 1990–2015) and support integration with meteorological and species distribution datasets.
  - Documentation notes the complexity of LCM1990 and provides extensive appendices on class definitions and colour mappings (Appendix content described in the document).

- Practical notes for analysts
  - Use 1 km products for UK-scale modelling; use 25 m or vector data when finer detail and metadata are required.
  - Be mindful of potential minor discrepancies in 1 km percentage sums due to rounding.
  - Retain gid and hist attributes in vector data for detailed, source-specific analysis and traceability.
  - Cite DOIs and author dates when publishing analyses that rely on LCM1990 data.