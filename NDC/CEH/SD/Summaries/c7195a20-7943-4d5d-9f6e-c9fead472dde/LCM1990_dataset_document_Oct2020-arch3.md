# Dataset documentation

- Overview: LCM1990 is a parcel-based UK land cover map derived from Landsat-5 satellite imagery (30 m) and aligned with the LCM2007/LCM2015 spatial framework to enable long-term change analyses. It provides vector (parcels) and raster products to support diverse user needs and is archived with DOIs for citation.

- Purpose and scope
  - Supports diverse monitoring and policy scrutiny needs by delivering standardized land cover data and change products.
  - Aims to be interoperable with other LCM products to enable 25-year change analyses (Rowland et al., 2020a, 2020b).

- Background and methodology
  - Replaces LCMGB; uses UK-wide framework tied to UK Biodiversity Action Plan Broad Habitats.
  - Built from two-date composite images; framework derived from Ordnance Survey cartography and rural boundary data for GB and NI.
  - Object-based classification with polygons reflecting real-world boundaries; trained with pure stands of woodland types and other habitats.
  - Minimum mappable area: >0.5 ha; smaller parcels and very short features are dissolved into surrounding landscape.

- Classes and labeling
  - Maps 21 land cover classes based on Broad Habitats (JNCC Jackson 2000). Some classes are subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - Each polygon carries a unique identifier (gid) and rich attribute sets, including dominant class, per-polygon pixel breakdown, and classification confidence.

- Data products and formats
  - Vector data set: 6.7 million polygons for GB and 0.9 million for NI; eight core attributes including class, source image, uncertainty, pixel counts, and modal class proportion (mode).
  - Raster data sets:
    - 25 m raster: three bands per polygon (dominant class, per-polygon confidence, percent coverage of modal class).
    - 1 km rasters: aggregate products (dominant cover and percentage cover) for both target classes (21) and aggregate classes (10).
  - Relationships: 1 km products summarize 25 m data; some rounding may cause minor sums to diverge from 100%.

- Metadata and uncertainty
  - Rich metadata per polygon, including dominant class, histogram of class counts, confidence, and standard deviation.
  - Uncertainty represented as per-pixel probability from the Random Forest classifier, included in both vector and 25 m raster outputs.

- Spatial scope and projections
  - Separate datasets for Great Britain (British National Grid) and Northern Ireland (Irish National Grid).
  - Vector and raster products are provided in multiple formats to accommodate different workflows.

- Access, licensing, and citation
  - Data access via CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request (licence may apply).
  - All products have DOIs for citation; guidance provided for how to cite (author/date + DOI) in publications.
  - Example citations and reference format are provided to ensure reproducible methods.

- Quality assurance and validation
  - QA checks cover projections, spatial completeness, polygon modal class presence (vector), value ranges (raster), and pixel-size accuracy.
  - A full validation exercise comparing LCM1990 to other datasets (e.g., Countryside Survey, National Forest Inventory, validation points) has been conducted; results published separately.

- Projections, data usage notes
  - GB data in British National Grid; NI data in Irish Grid; users should respect the MMU and classification nuances (e.g., some grassland sub-classes may require aggregation for specific analyses).

- Appendices and related information
  - Appendix 1 and 2 provide mapping notes between LCM1990 classes and Broad Habitats definitions; guidance on class interpretation and potential misclassifications.
  - Appendix 3 contains standard LCM color mapping recipes for visualization.
  - Appendix 4 lists composite images used during classification.

- Further information and contact
  - Additional details and data access: https://eip.ceh.ac.uk/lcm/lcmdata
  - Contact: spatialdata@ceh.ac.uk
  - Acknowledgements: CEH/UK-SCAPE support; references to Jackson (2000) and Morton et al. (2011); Rowland et al. (2020a, 2020b) for land cover change datasets.

- Endnotes
  - The document signals ongoing and forthcoming publications, including a journal paper detailing LCM1990 validation and methods.