# Land Cover Map 1990 (LCM1990)

- Overview
  - UK parcel-based land cover map created from Landsat-5 (30 m) satellite imagery, classified into 21 land cover classes.
  - Built using two-date composite imagery; aligned with the LCM2007 framework for compatibility with LCM2015 and to enable long-term change products.
  - Classes are based on UK Biodiversity Action Plan Broad Habitat definitions; includes some subdivisions to reflect spectral distinctions.

- Data products and structure
  - Vector data set
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - Each polygon has rich attributes, including dominant class, per-class pixel counts, confidence, and a unique geometry identifier (gid).
  - Raster data sets
    - 25 m raster (three-band): band 1 = dominant LCM1990 class per polygon; band 2 = mean per-polygon confidence; band 3 = percentage of polygon area covered by the modal class.
    - 1 km raster products: dominant cover (target and aggregate classes) and percentage cover (21 target bands; 10 aggregate bands).
    - Aggregated products are designed to support shoal-scale modelling and cross-data comparisons; coastal areas use adjusted accounting, so percentages may not sum exactly to 100.
  - Spatial resolution and domain
    - Great Britain and Northern Ireland provided separately with different projections.
    - Minimum mappable unit: >0.5 ha; polygons <0.5 ha or linear features <20 m dissolved into surrounding landscape.
  - Object labelling and metadata
    - Each vector parcel has a gid; attributes include a per-polygon histogram of class votes (_hist), mode class (_mode), purity, confidence (_conf), and standard deviation (_stdev).
    - Uncertainty estimates come from a Random Forest per-pixel classifier, reported as mean per-polygon confidence.
  - Data formats and access
    - Core product is the vector dataset; 25 m raster derived from it; 1 km rasters derived by aggregating the 25 m data.
    - Available as uncompressed GeoTiffs; DOIs exist for all products to support citation and reproducibility.

- Map projections and coordinate systems
  - Great Britain: British National Grid (EPSG 27700).
  - Northern Ireland: TM75 Irish Grid (EPSG 29903).

- Citing and DOIs
  - Each LCM1990 product has an individual DOI for citation (GB vector, GB 25 m raster, GB 1 km products, NI vector, NI rasters, etc.).
  - Citations should include authors, year, and the DOI; example formats are provided in the documentation.

- Data access, licensing, and use
  - 25 m and 1 km rasters available via the CEH Environmental Information Platform.
  - Full vector product available on request from CEH; license fees may apply for some users/applications.
  - Contact spatialdata@ceh.ac.uk or follow CEH’s LCM1990 access pages for details.

- Quality assurance and validation
  - Rigorous QA checks: projection correctness, spatial completeness, modal class presence in vector polygons, data range checks for rasters, and pixel-size verification.
  - Validation carried out against external datasets (e.g., Countryside Survey, National Forest Inventory) with results to be published separately.
  - Processed using well-defined methods and trained staff to ensure consistency with the 2007 Mastermap-based parcel framework.

- Class definitions and mapping rationale
  - LCM1990 maps 21 classes aligned to Broad Habitat definitions; several classes are subdivided to reflect spectral signatures (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - Appendix 1 provides detailed mapping notes, including spectral behavior, training data selection, and caveats (e.g., mixed woodlands, coniferous vs. broadleaf distinctions, grassland classifications).
  - Appendix 2 summarizes the UK Biodiversity Action Plan Broad Habitats (e.g., Broadleaved Woodland, Coniferous Woodland, Arable, Improved Grassland, Neutral/Calcareous/Acid Grasslands, Wetlands, Coastal/Habitat types, Urban).

- Data products in practice (illustrative guidance)
  - Vector vs. raster trade-offs: vector offers rich per-polygon metadata at the cost of larger file sizes; 25 m raster provides a simpler, width-friendly representation; 1 km rasters enable regional-scale modelling and integration with other datasets.
  - Example usage includes deriving 1 km dominance/percentage products for broad-scale environmental monitoring, trend detection, and integration with climate, hydrology, or biodiversity datasets.

- Metadata, provenance, and documentation
  - Rich polygon metadata (dominant class, class composition, confidence, and provenance) supports auditability and data governance.
  - Documentation includes class mappings, color recipes, and details on composite image usage (Appendices 3–4).

- Appendices (highlights)
  - Appendix 1: In-depth notes on how LCM1990 classes relate to Broad Habitats and field interpretations.
  - Appendix 2: Summaries of Biodiversity Action Plan Broad Habitats definitions.
  - Appendix 3: Standard colour mapping recipe for class visualization.
  - Appendix 4: List of composite images used for classification and training.

- Reproducibility and acknowledgments
  - Data cited via DOIs enhances reproducibility and traceability of usage in publications.
  - Acknowledged support from the Natural Environment Research Council as part of the UK-SCAPE programme.

- Practical implications for monitoring frameworks
  - Clear, auditable data lineage with DOIs and metadata supports policy scrutiny and longitudinal monitoring.
  - Uncertainty information at the polygon level aids risk assessment and decision-making.
  - Defined QA processes and validation against independent datasets improve reliability and trust in environmental health assessments.
  - Data access paths and licensing considerations highlight governance and openness constraints, relevant for data-sharing policies within monitoring programs.