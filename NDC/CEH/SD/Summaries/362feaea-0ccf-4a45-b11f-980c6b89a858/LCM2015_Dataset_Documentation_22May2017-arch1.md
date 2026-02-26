# Dataset documentation

- LCM2015 is a parcel-based UK land cover map produced by classifying satellite data into 21 Broad Habitat-based classes.
- Data are provided as multiple products to support different user needs: a core vector dataset, a 25m raster, and 1km aggregated rasters.
- The dataset uses two-date Landsat-8 composites (30m) with AWIFS (60m) as needed, and is aligned to real-world boundaries for interoperability with other geospatial data.
- LCM2015 is designed to support change mapping in the future, but users are cautioned not to rely on current outputs for change mapping without understanding methodological differences and potential classification errors.

Overview of data products
- Vector data set
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Attributes include: gid (unique parcel ID), BHAB (dominant Broad Habitat class), Pix_dist (counts per class within polygon), unc (mean per-polygon probability), unc_stdev, npix (pixels in polygon), Modal_class (recommended display class), Modal_prop, Composite (composite image source).
  - Rich metadata at polygon level and per-polygon class distribution for uncertainty assessment.
- 25m raster
  - Two-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon classification probability.
- 1km rasters
  - Dominant cover at 1km for both 21 target classes and 10 aggregate classes.
  - Percentage cover at 1km for both target and aggregate classes (21 and 10 bands respectively).
  - Rounding can cause sums to differ from 100%; coastal areas may sum to less than 100%.
- Data access and citations
  - 1km rasters available via CEH Environmental Information Platform.
  - Full vector and 25m products available on request under licence; license fees may apply.
  - Each product has its own Digital Object Identifier (DOI) for citation purposes.
- Projections and extents
  - Great Britain: British National Grid (BNG, EPSG 27700) for vector and 25m/1km rasters.
  - Northern Ireland: Irish Grid (TM75 Irish Grid, EPSG 29903) for vector and 25m/1km rasters.
  - Minimum mapping unit: >0.5 ha; polygons smaller than 0.5 ha or linear features <20 m dissolved into surrounding landscape.

LCM2015 classes and labelling
- 21 target classes map to Broad Habitats; some classes are subdivided for greater detail (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Habitat divisions).
- Unique object labelling: each polygon has a gid; recommended to retain gid for traceability and communication.
- Cited mapping framework: based on JNCC Broad Habitat definitions; Appendix materials provide definitions and color mappings.

Key methodological and output differences from LCM2007
- Classification algorithm: LCM2015 uses Random Forest instead of Maximum Likelihood, enabling better handling of multi-modal training data and reducing need for spectral sub-classes.
- Training data strategy: start with a stable core set of training areas (areas classified the same in 2000 and 2007), supplemented with coastal areas and hard-to-map classes.
- Ancillary data integration: ancillary layers (e.g., slope, proximity to water) are integrated into the input data rather than applied post-classification, making knowledge-based enhancements objective.
- Spatial framework: no segmentation-based polygons in LCM2015; eliminates segmentation-related inconsistencies and simplifies cross-time mapping.
- Output and class handling changes:
  - Montane class removed; areas map to Inland Rock or other upland habitats based on spectral data.
  - Rough grassland class removed; grassland types re-aligned with JNCC Broad Habitats and spectral data only.
  - 25m raster now two-band; probability data recorded as mean polygon probability in vector and band 2 of 25m raster.
  - Spectral sub-classes removed; Random Forest obviates the need for sub-class grouping.
  - Mixed woodland handling updated: training uses pure stands and per-pixel classification with polygon-level modal_class.
- Land cover mapping scope: LCM2015 maps land cover (not necessarily land use); examples show grass could be land use or cover depending on context.

Metadata, documentation, and citations
- LCM2015 provides extensive metadata for each polygon, including per-class pixel counts and mean probabilities.
- DOIs are provided for GB vector, GB 25m raster, GB 1km target and aggregate products, NI vector, NI 25m raster, NI 1km target and aggregate products.
- Publication and data-citation guidance are included to promote reproducibility and traceability of analyses.

Data access and contact
- CEH Environmental Information Platform hosts the 1km raster data.
- The full vector and 25m products require an application on the CEH site; licensing and fees may apply.
- Queries should be directed to spatialdata@ceh.ac.uk.

Appendices and technical notes
- Appendix 1 and 2: detailed definitions of Broad Habitats (JNCC) and mapping notes for each class.
- Appendix 3: standard LCM2015 colour mapping recipes for display.
- Appendix 4: composite image configurations used in LCM2015 production.
- Map projections and coordinate details, grid extents, and metadata conventions are outlined to support integration and analysis.

Notes for analysts
- When using LCM2015 data, be mindful of potential differences due to methodological changes and the absence of a segmentation framework.
- Use the gid and comprehensive metadata to interpret uncertainty and per-polygon class composition.
- Consider cross-walking LCM2015 classes with other habitat classifications when comparing across time or datasets.