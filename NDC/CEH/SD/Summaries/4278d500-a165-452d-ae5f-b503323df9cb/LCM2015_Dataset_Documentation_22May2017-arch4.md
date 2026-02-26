# Dataset documentation

- Purpose and scope
  - Land Cover Map 2015 (LCM2015) provides parcel-based UK land cover data classified into 21 Broad Habitat classes, using satellite imagery to support diverse user needs.
  - Built to support change mapping with a repeatable, object-based approach; notes that LCM2015 is not a ready-made change map in its current state and differences from prior maps reflect methodological and data evolution.

- Data products (structure and access)
  - Vector core dataset: 6.7 million GB polygons and 0.9 million NI polygons, each with rich attributes to describe dominant class, uncertainty, and class breakdown.
  - 25m raster: two-band product per polygon; band 1 = dominant class, band 2 = mean per-polygon probability from Random Forest.
  - 1km raster: aggregates including dominant class at 1km, dominant aggregate class, and 21-band (GB) or 10-band (NI) percentage cover products.
  - Metadata and uncertainty: per-polygon probability (unc) and standard deviation; per-polygon class breakdown (Pix_dist); composite image source.
  - Access and citation: DOIs for GB and NI products; 1km rasters available via CEH Environmental Information Platform; full vector and 25m data by license on request; contact spatialdata@ceh.ac.uk. Projections: GB = British National Grid; NI = TM75 Irish Grid.

- Data characteristics and classifications
  - 21 target classes based on the UK Broad Habitat framework; some classes have sub-types or are split for detail (e.g., Urban/Suburban, Heather/Heather grassland, Littoral categories).
  - LCM2015 maps land cover rather than land use; minimum mapping unit is >0.5 ha; small parcels and very narrow features are dissolved into surrounding landscape.
  - Spatial resolution and data formats: vector polygons with extensive attribute data; 25m raster with per-polygon classification and probability; 1km products built from 25m data.
  - Colour mapping and labeling: Appendix 3 provides standard LCM2015 colour coding; gid (Geometry Id) provides a unique parcel identifier to enable unambiguous cross-reference.

- Methodology (how LCM2015 was produced)
  - Classification framework: Random Forest classifier used to assign per-pixel classes, enabling multi-modal training data without spectral sub-classes.
  - Training data and ancillary inputs: initial training areas derived from stable 2000/2007 classifications, augmented with coastal and difficult classes; ancillary data (e.g., slope, proximity to rivers) integrated as input to the classifier.
  - Spatial framework and segmentation: no segmentation-based spatial framework (unlike LCM2007); per-pixel classification fed into a polygon summary.
  - Output structure: core vector as the primary product; 25m raster derived from the vector; 1km rasters created by aggregating 25m results.
  - Uncertainty and probability: probability estimates accompany outputs; mean polygon probability is recorded for vector and in band 2 of the 25m raster.

- Methodological differences from earlier versions (LCM2007)
  - Montane class removed; reclassified using spectral data (as Inland Rock or upland habitats) to support change mapping.
  - Rough grassland class removed; grassland types aligned to JNCC Broad Habitats without soil data reliance.
  - 25m raster changed to two-band format; probability data streamlined (mean probability per polygon in vector; band 2 in 25m raster); no probability data for 1km products.
  - Spectral sub-classes removed; Random Forest obviates the need for sub-class grouping.
  - Spatial framework segmentation removed; training data updated with coastal and poorly mapped classes.
  - Mixed woodland handling updated: training uses pure stands with per-pixel classification and polygon-mode aggregation.

- Data quality and caveats
  - Differences between LCM revisions reflect genuine change plus classification error; some habitat classes (e.g., Montane, Bracken handling) require caution when comparing across years.
  - Change mapping remains challenging due to mixed signals from spectral data and temporal variation; users should verify applicability to their use case.
  - Some broad habitat distinctions (e.g., Fen/Marsh/Swamp vs. Bog) can be difficult to separate spectrally; appendix provides detailed definitions to aid interpretation.

- Documentation and appendices
  - Appendix 1–2: detailed Broad Habitat definitions aligned with JNCC classifications.
  - Appendix 3: standard LCM2015 colour mapping scheme.
  - Appendix 4: lists composite images used in LCM2015.
  - Data citation: each product has its own DOI to support reproducibility and scholarly citation.

- Practical considerations for data leaders
  - Use the vector core for rich attribute-based analysis; the 25m raster offers a lighter-weight alternative with the same classification basis.
  - Leverage the 1km products for regional-scale modelling and integration with other datasets (e.g., climate, biodiversity, species distribution).
  - Treat LCM2015 as a stable, archived dataset with detailed metadata and uncertainty measures, suitable for integration into data governance, procurement, and data-sharing strategies.
  - When communicating results, reference the DOIs for precise data versioning and use the gid attribute to maintain clear data provenance across systems.