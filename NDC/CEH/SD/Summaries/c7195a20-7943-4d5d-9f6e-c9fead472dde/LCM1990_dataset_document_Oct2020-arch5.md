# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map produced from Landsat-5 imagery (30 m), classified into 21 Broad Habitat-based classes. It replaces LCMGB and aligns with the LCM2007/LCM2015 framework to enable long-term change analyses (e.g., 1990–2015).
- The dataset is distributed in multiple data products (vector, 25 m raster, 1 km aggregates) to support diverse applications and user needs.
- DOIs exist for all LCM1990 products (GB and Northern Ireland), enabling formal citation and reproducibility in publications.

- Purpose and governance context:
  - Designed to be stable, archived data with comprehensive metadata and uncertainty information, suitable for discovery, reuse, and data governance within organisations managing large datasets.
  - Classified using Broad Habitat definitions (JNCC Jackson, 2000) and linked to the 25-year land cover change objective.

- Data provenance and framework:
  - Spatial framework derived from generalised cartography (OSMM for GB; LPS vector for NI) and refined with rural boundary data; methods consistent with LCM2015 to maximise interoperability.
  - Vector products use polygon-based parcels with real-world boundaries; raster products derived from the vector data (25 m) and aggregated to 1 km.

- Access, licensing, and citation:
  - 25 m and 1 km rasters available via CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request (licence fees may apply).
  - Projections: Great Britain uses British National Grid; Northern Ireland uses Irish Grid (TM75) for respective rasters.
  - Each product has its own DOI; citations should include author and year in-text with full DOI in references.

- Data products and attributes:
  - Vector product: ~6.7 million GB polygons and ~0.9 million NI polygons; key attributes include gid (unique parcel ID), hist (class composition per polygon), mode (dominant LCM1990 class), purity (percent coverage of modal class), conf (mean RF vote confidence 0–100), stdev (uncertainty), n (pixel count), and cmp (composite image source).
  - 25 m raster: 3-band GeoTIFF per region (GB/NI) with band 1 = dominant class, band 2 = mean confidence, band 3 = percentage of polygon area covered by modal class.
  - 1 km rasters: dominant cover (target and aggregate classes) and percentage cover (21 target bands and 10 aggregate bands); values are integers and may sum to slightly over/under 100 due to rounding.
  - Minimum mappable unit: polygons > 0.5 ha; linears < 20 m dissolved to surrounding area.

- Class structure and interpretation:
  - 21 target LCM1990 classes, mapped from UK Broad Habitats; some broad habitats subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral/Coastal classes subdivided for coastal application).
  - 1 km products include both target and aggregated classes to support different levels of detail.

- Data quality, QA, and validation:
  - QA checks verify projections, spatial completeness, modal class presence in polygons (vector), value ranges (0–100 for rasters), and pixel size accuracy.
  - Full validation against other datasets (Countryside Survey, National Forest Inventory, validation points) conducted; results to be published separately.
  - The parcel framework is based on 2007 OS MasterMap data; changes in field boundaries are infrequent and have limited effect on accuracy.

- Documentation, metadata, and usage notes:
  - Rich metadata per polygon in the vector product, including dominant class details and pixel-level breakdowns; includes per-polygon uncertainty metrics from the Random Forest classifier.
  - DOIs should be cited when referencing any LCM1990 product; examples provided in the dataset documentation.
  - Important caveats for users: remote-sensing-based mapping may misclassify some land uses; some grassland classes are spectrally similar and may require ancillary data for improved accuracy; coastal and coastal-intertidal classes are challenging in some areas.

- Access details and contact:
  - CEH Environmental Information Platform provides access to the 25 m and 1 km raster datasets; full vector product is available on request.
  - Contact: spatialdata@ceh.ac.uk; further licensing details available at CEH LCM1990 data pages.
  - Acknowledgement: CEH and NERC support under the UK-SCAPE programme.

- References and further information:
  - Core references include Jackson (2000) for Broad Habitat definitions, Morton et al. (2011) for LCM2007 framework, and Rowland et al. (2020) for LCM1990 data products and DOIs.
  - Appendix material provides detailed class definitions, colour mappings, and composite image information relevant for consistent data use and interpretation.