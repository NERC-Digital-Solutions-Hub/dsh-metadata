# Dataset documentation

- LCM2015 provides a parcel-based UK land cover map classified into 21 Broad Habitat classes, derived from Landsat-8 (30 m) and AWIFS (60 m) two-date composites.
- Outputs include a core vector product (polygons with rich attributes), a 25 m raster, and 1 km raster products (dominant and percent cover), for Great Britain and Northern Ireland.
- The dataset is stable and archived with DOIs; each product has specific DOIs for citation.

## Data and products

- Vector data set
  - 6.7 million polygons (GB) and 0.9 million polygons (NI).
  - Attributes include gid (unique parcel ID), BHAB (dominant Broad Habitat), Pix_dist (pixel counts per class plus totals), uncertainty (mean per-polygon probability), npix, Modal_class (1–21), Modal_prop, and Composite (composite image source).
- 25 m raster
  - 2-band raster: Band 1 = dominant LCM2015 class per polygon; Band 2 = mean per-polygon probability from Random Forest.
- 1 km raster
  - Four products: dominant class (21 target classes and 10 aggregated classes) and percentage cover (21 bands and 10 aggregated bands).
  - Spatially separated for GB and NI; rounding can cause small sums to differ from 100%.
- Spatial resolutions and projections
  - GB: British National Grid (EPSG 27700); NI: Irish Grid (TM75, EPSG 29903).
  - 25 m and 1 km raster products; vector separately for GB and NI.
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon probability from Random Forest included in vector (and in 25 m raster Band 2).
  - Gid ensures unambiguous communication; per-polygon polygon-level statistics available (e.g., npix, Pix_dist, unc).
- Data access and licensing
  - 1 km raster via CEH Environmental Information Platform (EIP).
  - Full vector and 25 m products available on request under licence; fees may apply.
- Citing and DOIs
  - Each product has its own DOI (GB vector, GB 25 m, GB 1 km target and aggregate classes, NI vector, NI 25 m, NI 1 km products).
  - Citing DOIs in publications supports reproducibility.

## Methodology and differences from earlier maps (LCM2007)

- Classification algorithm
  - Uses Random Forest instead of Maximum Likelihood; handles multi-modal training data and often out-performs ML.
- Training data and ancillary information
  - Ancillary data (e.g., slope, proximity to rivers) are integrated into the input and used by the classifier, rather than applied post-classification.
  - Stable training areas begin with land classified the same in 2000 and 2007, then augmented (coastal areas, difficult classes).
- Spatial framework and segmentation
  - No segmentation-based polygons in LCM2015; per-pixel classification forms the basis, improving consistency for change mapping.
- Output changes and class definitions
  - Montane class removed; areas previously Montane are now mapped as Inland Rock or other upland habitats based on spectral data.
  - Rough Grassland class removed; grassland types re-aligned with JNCC Broad Habitats without soil data in LCM2015.
  - 25 m raster became a two-band image; spectral sub-classes removed due to the Random Forest approach.
  - Mixed woodland handling changed: training uses pure stands for Coniferous/Broadleaf; polygon labels reflect modal class after pixel-level classification.
- Broad Habitat class structure
  - 21 target classes, with some internal divisions (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral/Littoral Sediment divisions).
- Output interpretation
  - LCM2015 maps land cover (not strictly land use); in some cases land cover does not imply land use (e.g., recreation grass vs grazing land).

## Classes and mapping notes

- 21 LCM2015 target classes derived from UK Broad Habitat definitions; detailed descriptions and mappings to JNCC Broad Habitats are provided in appendices, including color-coding schemes and target class numbers.
- Some categories have sub-divisions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).

## Usage guidance and cautions

- LCM2015 is complex; differences between maps over time reflect real change and classification error, and not all change is reliably mapped.
- Advisories on change mapping: not recommended to use the LCM series for change mapping in their current state without careful validation.
- Minimum mapping unit
  - Minimum mappable area > 0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape.
- Data usage considerations
  - Vector provides rich metadata but may be unwieldy for some applications; 25 m raster offers the same detail without polygon boundaries and metadata.
  - 1 km products are suitable for national-scale modelling and integration with meteorological or species distribution data.

## Practical guidance for GIS workflows

- Choose data product based on application
  - Use vector for detailed attribute information and per-polygon analysis.
  - Use 25 m raster for analysis that benefits from per-pixel classification without extensive metadata.
  - Use 1 km rasters for large-scale modelling and integration with other national datasets.
- Data integration and cross-compatibility
  - Be aware of changes in spatial framework and class definitions when comparing with LCM2007 or LCM2000.
  - When aggregating to 1 km, expect some minor rounding differences across bands and datasets.
- Citing data
  - Always use the DOI corresponding to the product and include author/date as per the provided citation guidance.

## Appendices and additional information

- Appendix 1 and Appendix 2 provide detailed Broad Habitat definitions and nuances for the 21 LCM2015 classes.
- Appendix 3 provides the standard LCM2015 color mapping recipe.
- Appendix 4 lists the composite images used in LCM2015.
- For further information and access, see CEH and EIDP pages and contact spatialdata@ceh.ac.uk.