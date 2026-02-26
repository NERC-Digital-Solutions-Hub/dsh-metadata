# Dataset documentation

- LCM1990 is a parcel-based UK land cover map created from Landsat-5 imagery (30 m) classified into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions.
- It replaces the earlier LCMGB and aligns its spatial framework with LCM2015 to enable a future 25-year land cover change product (1990–2015).
- The dataset supports a range of user needs and applications with rich metadata and uncertainty information to aid proper use and interpretation.

## Data products and structure

- Core products:
  - Vector data: polygons with detailed attributes per parcel.
  - 25 m raster: derived from the vector data, used for broader analyses.
  - 1 km raster products: dominant cover and percentage cover for both 21 target classes and 10 aggregate classes.
- Class structure and subdivision:
  - 21 LCM1990 classes mapped; some broad habitats are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Parcel-based design:
  - Each polygon has a unique geometry identifier (gid) and rich per-polygon metadata, including dominant class, per-class pixel counts, and mean classification probability.
- Uncertainty:
  - Random Forest per-pixel probability is provided as a polygon-averaged value (and in the raster products), enabling assessment of classification confidence.

## Data formats, access, and provenance

- Data formats and resolutions:
  - Vector: polygons with attribute tables (6.7 million polygons GB, 0.9 million NI).
  - 25 m raster: three-band GeoTIFF (dominant class, mean confidence, percent cover per polygon).
  - 1 km rasters: dominant cover (1 band) and percentage cover (21 bands for target classes; 10 bands for aggregates).
- Projections:
  - Great Britain: British National Grid (OSGB36).
  - Northern Ireland: Irish Grid (TM75).
  - GB and NI data are provided separately to match their projections.
- Access:
  - 25 m and 1 km rasters are available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product is available on request under licence from CEH (licence fees may apply).
- DOIs and citation:
  - All LCM1990 products have individual DOIs for citation (Table 5 for GB and Table 6 for NI). See the document for exact DOIs and recommended citation format.
  - Example citation pattern: Rowland et al. (2020). Land Cover Map 1990 (vector, GB). DOI provided in Table 5.
- Documentation and access guidance:
  - More information at https://eip.ceh.ac.uk/lcm/lcmdata and https://www.ceh.ac.uk/services/land-cover-map-1990.
  - Queries: spatialdata@ceh.ac.uk.
- Acknowledgement:
  - Funded by NERC under award NE/R016429/1 (UK-SCAPE National Capability).

## Data quality, validation, and reliability

- Quality assurance:
  - Regular QA checks for projection correctness, spatial completeness, modal class presence in polygons, metadata alignment, value ranges (0–100 for raster percent covers), and pixel size accuracy.
  - A full validation exercise has been performed against reference datasets (e.g., Countryside Survey, National Forest Inventory) with results to be reported separately.
- Data lineage and compatibility:
  - Built using the 2007 Ordnance Survey MasterMap-based parcel framework; designed to be compatible with other CEH Land Cover Maps and to enable long-term change studies (e.g., 1990–2015 analyses).
- Granularity and mapping decisions:
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha and linear features < 20 m are dissolved into surrounding landscape.
  - Some land use may not be directly inferred from land cover (e.g., recreation grass vs. grazing pastures with similar spectral signatures).

## Class definitions and interpretation notes

- 21 Broad Habitat classes are defined (Appendix 2 summarizes JNCC Broad Habitat definitions); 21 target LCM1990 classes map to these Broad Habitats with some cross-walk to aggregate classes for 1 km products.
- Important interpretation notes:
  - LCM1990 maps land cover (not always land use); certain land uses may be indistinguishable spectrally from others.
  - Grassland classes (Neutral, Calcareous, Improved, Acid, etc.) may be spectrally similar and require ancillary data or field verification for precise classification.
  - Water bodies and coastal classes near shore can be challenging; some categories are mapped only where extents are reliable from the underlying cartography.
  - The vector product provides rich metadata (dominant class, per-class pixel counts, uncertainty) to aid nuanced interpretation and potential re-aggregation.

## Usage guidance for data leadership

- Governance and stewardship:
  - Data are delivered with robust metadata and per-polygon uncertainty, supporting governance, reproducibility, and audit trails.
  - DOIs and clear citation practices enable traceability and reuse in policy, research, and networks.
- Interoperability and integration:
  - Consistent with LCM2015 framework to support cross-product compatibility and multi-temporal analyses.
  - Multiple resolution options (25 m, 1 km, vector) support diverse modeling approaches, from fine-scale mapping to national-scale modeling with aggregation.
- Accessibility and licensing:
  - Access through CEH platforms; vector data on request; licensing considerations may affect some users and applications.
  - Clear pathway for incorporating the dataset into organizational data inventories, governance dashboards, and data sharing within data networks.
- Strategic value:
  - Facilitates co-ownership and collaborative development of data products by providing detailed attributes and confidence metrics.
  - Supports integration with other geospatial datasets (meteorology, biodiversity, habitat networks) for policy, planning, and environmental monitoring.

## Appendix highlights and references (high-level)

- Appendix 1–3 cover class-specific interpretations, standard color mappings, and details about composite images used in LCM1990.
- Appendix 4 lists composite image metadata used during classification.
- Biodiversity Action Plan Broad Habitats (Appendix 2) provide concise definitions for the 21 Broad Habitat classes.
- References include Jackson (2000), Morton et al. (2011), and Rowland et al. (2020) for related LCM products and methodology.