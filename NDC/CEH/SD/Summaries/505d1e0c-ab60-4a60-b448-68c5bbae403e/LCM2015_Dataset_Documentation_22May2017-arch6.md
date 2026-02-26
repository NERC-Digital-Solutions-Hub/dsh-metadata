# Dataset documentation

- Purpose and scope
  - Land Cover Map 2015 (LCM2015) provides a parcel-based UK land cover map classified into 21 classes based on UK Broad Habitat definitions.
  - Built from two-date Landsat-8 (30 m) composites, supplemented with AWIFS (60 m) data; designed to support a broad user community with emphasis on repeatable methods and change mapping readiness.
  - Noted caution: LCM2015 in its current state should not be used for change mapping; differences between maps reflect real change and classification error, compounded by varying timeframes and data sources.

- Data products and formats
  - Core vector dataset: polygons with rich attribute data.
  - 25 m raster: two-band image (band 1 = dominant class; band 2 = mean per-polygon classification probability).
  - 1 km raster: dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
  - Spatial coverage: Great Britain (GB) and Northern Ireland (NI) in separate datasets; GB vector ~6.7 million polygons; NI vector ~0.9 million polygons.
  - Projections: GB (British National Grid); NI (TM75 Irish Grid).

- Data structure and attributes
  - Vector attributes include gid (unique parcel ID), BHAB (dominant Broad Habitat class), Pix_dist (distribution of pixels across all classes within the polygon), unc (mean per-polygon probability from Random Forest), npix, Modal_class (recommended display class), Modal_prop, and Composite (source composite image).
  - 25 m raster band 2 contains the mean probability of the majority class for each polygon.
  - A per-polygon uncertainty measure is provided, derived from the Random Forest classifier.

- Classification methodology and processing
  - Uses a Random Forest classifier (replacing the previous Maximum Likelihood approach).
  - Training areas built from a stable set: areas consistently classified in 2000 and 2007, enhanced with coastal and poorly mapped classes.
  - Ancillary data (e.g., slope and proximity data) are integrated into the input data stream rather than applied post-classification.
  - No spectral sub-classes needed due to multi-model training capability of Random Forest.
  - Spatial framework does not use segmentation-based polygons (no image segmentation in the final spatial framework); per-pixel classification with polygon-level summarisation.
  - Output includes per-polygon probability (uncertainty) and a robust metadata-rich dataset.

- Classes and labeling
  - 21 LCM2015 target classes aligned to Broad Habitat types; some classes further subdivided for user convenience (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral subtypes).
  - The dataset provides detailed mappings to Broad Habitat definitions (see Appendix sections in the dataset documentation).

- Data access, citation, and DOIs
  - 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products available on request under licence from CEH; licence fees may apply.
  - Each LCM2015 product has a DOI for citation; separate DOIs exist for GB vector, GB 25 m, GB 1 km percentage and dominant classes, GB 1 km aggregate classes, and NI equivalents.
  - Guidance provided for proper citation (author list, date, and DOI in references).

- Usage notes and limitations
  - LCM2015 is a stable, archived dataset with a Digital Object Identifier (DOI) for reproducibility.
  - Caution that outputs are subject to real change plus classification errors; outputs should be interpreted with awareness of MMU and potential misclassification, especially near coastal and transitional habitats.
  - The 0.5 ha minimum mapping unit and dissolution of small parcels into surrounding landscape help standardise outputs but may affect fine-scale analyses.
  - The 1 km products reflect aggregation from 25 m data; totals may slightly exceed or fall short of 100% due to rounding.

- Documentation and supplemental information
  - Rich metadata accompanies the vector dataset, including dominant class, per-polygon pixel counts, and probability metrics.
  - Appendices provide definitions for Broad Habitats, class mappings, colour mapping recipes, and composite image details.
  - Contact: spatialdata@ceh.ac.uk; more information at CEH LCM2015 pages and eIDC citing guidance.