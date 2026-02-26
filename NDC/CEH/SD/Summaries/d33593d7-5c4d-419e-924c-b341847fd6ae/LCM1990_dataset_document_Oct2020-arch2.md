# Land Cover Map 1990 (LCM1990) Dataset Documentation

- Purpose and scope
  - Provides a range of data products to support diverse LCM user needs.
  - Focuses on LCM1990 data products; references other Land Cover Maps in separate documents.
  - Aims to enable consistent monitoring of land cover over time and compatibility with newer LCM products for long-term change analysis.

- Key data products and formats
  - Vector data set
    - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland.
    - Core attributes include dominant class, source image, per-polygon pixel breakdown, uncertainty, and a unique geometry identifier (gid).
    - Rich metadata per polygon, including mean classification probability and pixel counts for all classes.
  - 25 m raster
    - 3-band raster: band 1 = dominant class per polygon; band 2 = mean per-polygon confidence; band 3 = percentage of polygon area covered by the dominant class.
    - Used to generate 1 km products and aggregate statistics.
  - 1 km raster
    - Dominant cover (1 band) for target and aggregate classes.
    - Percentage cover (21 bands for target classes; 10 bands for aggregate classes). Values are integers; rounding can affect sums to meet 100%.
    - Coasts may have sums totaling less than 100% due to mapping extents and MMU considerations.
  - Aggregate classes
    - Defined to support applications that do not require full 21-class detail; used in 1 km products.

- Spatial framework and comparability
  - Built on the LCM2007 framework for consistency with LCM2015; enables creation of a 25-year land cover change product (1990–2015).
  - Vector and raster products provided in separate GB and NI coordinate systems:
    - GB: British National Grid
    - NI: Irish National Grid (TM75)
  - Minimum mappable unit (MMU) and dissolution rules
    - Minimum area > 0.5 ha; polygons < 0.5 ha and linear features < 20 m dissolved into surrounding landscape.

- Land cover classes and interpretation
  - 21 classes based on UK Biodiversity Action Plan Broad Habitat definitions.
  - Some classes subdivided due to spectral distinctions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - LCM1990 maps land cover (not strictly land use); some examples where land use cannot be inferred from land cover.

- Uncertainty, quality, and validation
  - Random Forest classifier provides per-pixel probability; reported as mean per polygon in vector and in the 25 m raster.
  - QA checks cover projection correctness, spatial completeness, modal class presence in polygons, value ranges (0–100 for rasters), and pixel size accuracy.
  - Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.

- Data access and licensing
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence (fees may apply).
  - DOIs assigned to all LCM1990 products; recommended citation format provided (GB and NI tables with DOIs).

- Citing and reproducibility
  - Example citation format includes author(s), year, product description, and DOI.
  - DOIs enable clear, repeatable methods and tracking of usage across publications.

- Data provenance and maintenance
  - Dataset created and archived by CEH; static, stable data with long-term accessibility.
  - Emphasis on retaining unique gid for unambiguous communication and traceability.

- Version and updates
  - Version 1.1 (dated 8/10/2020) includes updates to DOIs in Tables 5 and 6; initial release was Version 1.0 (02/07/2020).

- Appendix highlights (supporting context)
  - Appendix 1: Detailed cell notes and mapping decisions for each LCM1990 class, including grassland and shrub classifications.
  - Appendix 2: Biodiversity Action Plan Broad Habitat definitions (JNCC), linked to LCM1990 classes.
  - Appendix 3: Standard LCM color mapping (class-to-color guidance).
  - Appendix 4: Composite images used in LCM1990 production (image metadata and dates).

- Further information and contact
  - Access details and additional information available at the CEH LCM1990 page and CEH spatialdata contact.
  - Acknowledgement of support from the Natural Environment Research Council under the UK-SCAPE programme.