# Dataset documentation

- Purpose and scope
  - Provides Land Cover Map 2015 (LCM2015) data for the UK, built to support diverse user needs with 21 land cover classes aligned to UK Broad Habitats.
  - Delivered as multiple data products (vector, 25m raster, 1km percentage/dominant) for Great Britain and Northern Ireland.
  - LCM2015 is a stable, archived dataset with DOIs for all products; cautions issued about using the LCM series for change mapping in its current state.

- What the data are and how they are built
  - Parcel-based land cover map created by classifying two-date satellite composites (mainly Landsat-8; supplemented by AWIFS) into 21 classes.
  - Built from polygons reflecting real-world boundaries; spatial framework derived from OS MasterMap/NI equivalents and refined boundary data.
  - Aimed at enabling rapid, repeatable change mapping while maintaining interpretability and interoperability with other geospatial data.

- Data products and structure
  - Vector data set
    - ~6.7 million polygons (GB) and ~0.9 million (NI) with rich attributes per polygon.
    - Key attributes: gid (unique parcel ID), BHAB (dominant Broad Habitat level), Pix_dist (per-class pixel counts), unc (mean per-polygon probability), Unc_stdev, npix, Modal_class (dominant class code), Modal_prop, Composite (which composite image was used).
  - 25m raster
    - 2-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest.
  - 1km rasters
    - Dominant class per 1km pixel (for both 21-class and 10-aggregate schemes) and percentage cover per class (and per aggregate class).
  - Data scope and formats
    - Great Britain and Northern Ireland provided in separate datasets due to differing projections.
    - 0.5 ha minimum mapping unit; smaller parcels dissolved into surrounding landscape.

- Classification approach and data quality
  - 21 target classes are based on JNCC Broad Habitats; some classes are subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral classifications).
  - Random Forest classifier replaces the previous Maximum Likelihood approach; supports multi-model training data and reduces need for spectral sub-classes.
  - Training areas established from stable areas (2000 and 2007) and supplemented for coastal and poorly mapped classes.
  - Ancillary data (e.g., slope, distance to rivers) are incorporated into the input, making knowledge-based enhancements part of the core algorithm.
  - Uncertainty information provided: per-polygon mean probability (unc) and standard deviation (Unc_stdev); probability data also embedded in the 25m raster band 2.

- Methodological and output differences from earlier LCM versions
  - Montane class removed; upland areas reclassified using spectral data (Inland Rock or other upland habitats).
  - Rough grassland class removed; grassland types now aligned with Broad Habitat definitions without relying on soil data.
  - 25m raster now two-band (class + mean probability); vector uses mean polygon probability rather than per-subclass probabilities.
  - No spectral sub-classes; Random Forest handles multi-modal data without subclassing.
  - Spatial framework moved away from segmentation-based polygons to per-pixel classification, simplifying change mapping in uplands and other areas.
  - Mixed woodland training updated to rely on pure stands for training; final polygon labels are the modal class of classified pixels.

- Data products and how to use them
  - Vector product: rich metadata per polygon; suitable for detailed analysis and tracing class composition within parcels.
  - 25m raster: useful when reduced metadata is preferred or for seamless integration into raster-based workflows.
  - 1km products: suitable for national-scale modelling and integration with other gridded data (e.g., climate, species distribution).

- Citing and data access
  - Each product has its own DOI (GB and NI) to ensure reproducibility; cite DOIs in publications as with other data sources.
  - Access:
    - 1km raster data available via CEH Environmental Information Platform (EIP).
    - Full vector and 25m raster data available on request under license; licensing may apply.
  - Projections:
    - GB data in British National Grid; NI data in TM75 Irish Grid.

- Practical guidance and caveats
  - LCM2015 is a stable, archived dataset; not all products are directly interchangeable with past LCM maps for change detection without careful handling.
  - Differences between LCM2007 and LCM2015 can affect compatibility; users should review methodological changes before applying legacy scripts.
  - For some classes, especially coastal and upland areas, interpretation should consider classification uncertainties and potential misclassifications.
  - The document emphasizes using the DOIs and accompanying metadata for transparency and repeatability in analyses.

- Additional information and contact
  - Further information and data access details available at CEH websites and the Environmental Information Platform.
  - For inquiries, contact spatialdata@ceh.ac.uk.