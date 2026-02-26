# Land Cover Map 2015 (LCM2015)

- Overview
  - UK parcel-based land cover map created from satellite data (Landsat-8 30 m, AWIFS 60 m) using two-date composites.
  - Maps 21 Broad Habitat-based land cover classes (based on JNCC/Biodiversity Action Plan definitions).
  - Outputs include a core vector data set, a 25 m raster, and 1 km aggregated products; vector contains per-polygon attributes and a unique geometry identifier (gid).
  - LCM2015 updates LCM2007 with methodological and data-source changes; it is a stable, archived data set with DOIs for citation.

- Data products
  - Vector data set: approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland; attributes include land cover class (text and integer), source image, uncertainty, pixel counts per class, dominant class proportion, and gid.
  - 25 m raster: two-band image; band 1 = dominant class per polygon, band 2 = mean per-polygon probability from the classifier.
  - 1 km raster products: dominant class and percentage cover per class (21 target classes or 10 aggregate classes); GB and NI provided separately.
  - Metadata and uncertainty: rich polygon-level metadata; per-pixel probability from Random Forest; uncertainty values provided in vector and raster formats.
  - Data access: 1 km rasters via CEH Environmental Information Platform; full vector and 25 m rasters on request under licence (fees may apply).

- Classification method and data framework
  - New Random Forest classifier used (replacing Maximum Likelihood).
  - Ancillary data (e.g., slope, soil, coastal context) integrated as inputs to the classifier; no separate post-classification knowledge-based rules.
  - Stable training areas from prior LCMs used as a starting point, supplemented with coastal and problematic classes.
  - No segmentation in the spatial framework to avoid segmentation-related misalignment with classifications; aims to support change mapping in future.

- Differences from previous maps (LCM2007)
  - Montane class removed; reclassified using spectral data as Inland Rock or other upland habitats.
  - Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitats; no soil data used in LCM2015.
  - 25 m raster becomes 2-band (classification + probability).
  - Probability information streamlined (mean per-polygon probability); no probability data for 1 km products.
  - Spectral sub-classes removed due to use of Random Forest; segmentation-based spatial framework removed to simplify per-pixel classification and future change mapping.
  - Mixed woodland training uses pure stands for training; final polygon labels are based on modal_class of pixels.

- Classes and labeling
  - 21 LCM2015 target classes mapped from Broad Habitats (with some classes further subdivided for 25 m and 1 km products).
  - Some classifications align with JNCC Broad Habitats definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grassland types, wetlands, urban/rural built-up classes).
  - Each parcel (polygon) receives a unique gid; detailed per-polygon and per-class distribution statistics are available in the vector attributes.

- Data structure and attributes
  - Vector attributes (Table 2 in the document) include:
    - gid: unique geometry identifier
    - BHAB: dominant land cover class (Broad Habitat level, textual)
    - pix_dist: counts of pixels per class within the polygon
    - unc: mean per-polygon probability (uncertainty)
    - unc_stdev: standard deviation of the uncertainty
    - npix: number of pixels in the polygon
    - Modal_class: numeric code for the dominant LCM2015 class
    - Modal_prop: proportion of polygon classified as the dominant class
    - Composite: composite image number used for the classification
  - 25 m raster bands: band 1 = dominant class code; band 2 = mean probability for the polygon.
  - 1 km products: aggregates and percentage covers; GB and NI provided separately with the appropriate projections.

- Spatial specifics and data accessibility
  - Projections: Great Britain uses British National Grid; Northern Ireland uses TM75 Irish Grid.
  - Resolution and minimum mapping unit: minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha or line features < 20 m dissolved into surrounding landscape.
  - Spatial geography: vector and raster products cover GB and NI separately due to differing coordinate systems.
  - Documentation and citation: each product has its own DOI; recommended citation format provided for publications.

- Usage cautions and interpretation
  - Do not use the LCM2015 dataset in its current state for change mapping without careful consideration of differences from previous maps and methodological changes.
  - Differences between LCM2015 and LCM2007 can affect longitudinal analyses; scripts and workflows should be adapted accordingly.
  - The dataset includes complexities in class definitions and spatial boundaries; Appendix material provides detailed class definitions and color mappings to aid interpretation.

- Appendices and references
  - Appendix 1 and Appendix 2 summarize Broad Habitat definitions (with notes on grassland and woodland distinctions).
  - Appendix 3 provides standard LCM2015 colour mapping guidelines.
  - Appendix 4 lists composite images used in LCM2015 production.
  - Key references: Jackson (2000) on Broad Habitat definitions; Morton et al. (2011) on LCM2007 methodology.