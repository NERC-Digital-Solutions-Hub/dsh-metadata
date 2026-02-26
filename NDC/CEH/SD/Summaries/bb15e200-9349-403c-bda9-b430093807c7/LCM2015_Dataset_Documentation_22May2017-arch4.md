# Dataset documentation

- Overview
  - Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classified from satellite data (Landsat-8 30 m, AWIFS 60 m as needed) into 21 Broad Habitat classes aligned with UK Biodiversity Action Plan definitions.
  - Built on a two-date composite and updated from LCM2007, using a per-polygon framework that reflects real-world boundaries for easy interpretation and compatibility with other geospatial data.
  - Spatial framework derived from generalised cartography (OS MasterMap for GB, LPS vector for NI), refined with rural boundaries; aims to support change mapping with a repeatable workflow.
  - LCM2015 focuses on land cover (not necessarily land use) and provides multiple data products (vector, 25 m raster, 1 km percent/dominant products) with rich metadata and uncertainty information.
  - Acknowledges that differences between years reflect real change and classification error; caution advised when using LCM series for change mapping in their current state.

- Data products and structure
  - Vector data set
    - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
    - 9 attributes per polygon, including gid (unique geometry ID), BHAB (dominant Broad Habitat class), Pix_dist (23-class pixel counts plus npix and modal_class), unc (mean per-polygon probability), unc_stdev, npix, Modal_class, Modal_prop, Composite.
  - 25 m raster
    - 2-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean probability for the polygon from the Random Forest classifier.
  - 1 km raster and aggregates
    - 1 km products: dominant class (21 target or 10 aggregate), and percentage cover per class (21 bands for target, 10 for aggregates).
    - Values are integer percentages; sums may deviate from 100 due to rounding and coastal areas being treated differently.
  - Accessibility and DOIs
    - Each LCM2015 product has a Digital Object Identifier (DOI) for citation.
    - GB vector and rasters available via CEH; 1 km rasters via CEH Environmental Information Platform; full vector and 25 m products on request under licence.

- Class structure and labelling
  - 21 LCM2015 classes, based on UK Broad Habitat definitions; several Broad Habitats are further divided for certain products (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Appendix-hosted mappings show relationships between LCM2015 classes and broader Habitats; a gid attribute ensures unambiguous communication of parcel-level data.
  - Spatial outputs: vector and 25 m rasters provide detailed per-polygon/class information; 1 km rasters provide dominant class and percentage cover, enabling landscape-scale analyses.

- Methodology and data quality
  - New classification algorithm: Random Forest (RF) replaces Maximum Likelihood, enabling handling of multi-modal training data and often improving accuracy.
  - Training data approach: uses an initial stable training set (areas consistently classified the same in 2000 and 2007) and supplements with coastal and difficult classes; ancillary data (e.g., slope, proximity to rivers) are incorporated as input features rather than post-classification rules.
  - No spectral sub-classes or segmentation: RF handles multi-modal outputs; LCM2015 removes segmentation-based polygons to avoid cross-map segmentation inconsistencies; segmentation removal primarily affects GB upland areas.
  - Training and uncertainty: per-pixel RF probabilities are retained; polygon-level mean probability provided in vector and 25 m raster; uncertainty metrics (unc, unc_stdev) accompany attributes.
  - Differences from earlier maps (LCM2007)
    - Montane class removed; Rough grassland removed; 25 m raster now two-band; probability data re-encoded; no spectral sub-classes; segmentation framework removed.
  - Data scope and caveats
    - LCM2015 maps land cover; some sites may reflect both land cover and land-use signals.
    - Change mapping between years is not straightforward due to real changes, methodological differences, data availability, and border definitions; users should validate outputs for time-series analyses.
  - Minimum mapping unit
    - Minimum mappable area set at >0.5 ha; parcels smaller than 0.5 ha or very narrow features (<20 m) dissolved into surrounding landscape.

- Technical details
  - Spatial resolution: vector (parcels), 25 m raster, 1 km raster.
  - Projections: Great Britain uses British National Grid; Northern Ireland uses TM75 Irish Grid.
  - Data formats and guidance
    - Core vector product followed by 25 m raster and then 1 km products.
    - Rich metadata at polygon level, including dominant class, per-class pixel counts, and probabilities.
    - DOIs provided for all products to support reproducible citing in publications.
  - Access and licensing
    - 1 km rasters accessible via CEH EIP; full vector and 25 m products available on request under licence; licensing fees may apply for some users or applications.
    - Contact spatialdata@ceh.ac.uk and refer to CEH information portal for access.

- Practical use and governance
  - Data leaders can use LCM2015 to:
    - Model land cover at multiple scales (1 km to parcel level) with robust uncertainty metrics.
    - Compare across GB and NI with harmonised 21-class structure and corresponding aggregates.
    - Assess data lineage and reproducibility via DOIs and metadata-rich outputs.
  - Governance and community
    - Emphasises a repeatable workflow suitable for monitoring change over time (but with caveats about change mapping accuracy).
    - Encourages citation and traceability through DOIs; metadata and gid enable clear communication and interoperability across teams and partners.