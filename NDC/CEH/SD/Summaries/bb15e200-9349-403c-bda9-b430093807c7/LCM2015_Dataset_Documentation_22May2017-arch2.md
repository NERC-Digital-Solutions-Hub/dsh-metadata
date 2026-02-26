# Dataset documentation

- Purpose and scope
  - LCM2015 provides UK-wide land cover maps to support environmental monitoring and policy performance assessment.
  - A complex, archive-grade data set designed for standardised, repeatable outputs; not recommended for current-state change mapping without caution.

- Data products and formats
  - Core vector data set: polygons with rich attributes (6.7 million polygons in Great Britain; 0.9 million in Northern Ireland).
  - 25m raster: two-band image per area; band 1 = dominant land cover class per polygon; band 2 = mean per-polygon classification probability.
  - 1km raster: derived products including dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
  - Classes: 21 LCM2015 target classes aligned to UK Broad Habitat definitions; some splits (e.g., Urban vs Suburban) exist within Broad Habitats.
  - Spatial framework: GB and NI provided separately using appropriate national grid projections; pixel sizes 25 m (vector-derived), 1 km (raster products).

- Data origins and methodology
  - Based on two-date composites of Landsat-8 (30 m) with supplementary AWIFS data (60 m).
  - Classifications produced with a Random Forest algorithm (replacing previous Maximum Likelihood); ancillary data (e.g., slope, hydrology) integrated as inputs.
  - No segmentation in the spatial framework to avoid segmentation-related errors; stable training areas built from legacy LCM datasets with targeted additions for challenging classes.
  - Outputs reflect land cover, not strictly land use; per-polygon dominant class is provided alongside detailed per-class breakdowns.

- Key methodological differences from LCM2007
  - Montane and Rough Grassland classes removed; their previous mappings reinterpreted spectrally.
  - 25m raster now 2-band; probability data restructured (mean polygon probability in vector; band 2 of 25m raster).
  - No spectral sub-classes; simpler training data requirements with Random Forest.
  - Spatial segmentation removed; simplification aimed at robust change mapping and consistency across time.

- Data products in detail
  - Vector product: 21 target classes; gid (unique parcel ID); BHAB (dominant Broad Habitat); Pix_dist (pixel counts per class); unc and unc_stdev (uncertainty); npix; Modal_class; Modal_prop; Composite.
  - 25m raster: 2 bands (dominant class; mean probability); metadata structured to map band 1 values to LCM2015 classes.
  - 1km rasters: dominant target class and 1km percentage cover for both 21 classes and 10 aggregates; rounding means sums may differ slightly from 100; coastlines have reduced totals.

- Metadata, uncertainty, and data quality
  - Rich metadata and per-polygon breakdowns; uncertainty reported as mean per-polygon probability (0–255 scale) with standard deviation.
  - Probability outputs enable assessment of classification confidence; cautions noted for change-mapping applications due to methodological differences over time.

- Access, licensing, and citation
  - 1km raster data available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25m products available on request under licence; licensing fees may apply.
  - Each product has its own DOI for citation (GB and NI tables provided); guidance on citing DOIs in publications.
  - File formats support both per-polygon detail (vector) and streamlined raster usage; Appendix 3 provides standard colour mapping.

- Practical guidance for analysts
  - Use LCM2015 for baseline, cross-temporal analyses with awareness of methodological changes relative to earlier maps.
  - Leverage uncertainty metrics to evaluate reliability at polygon and per-pixel levels.
  - Prefer the 25m raster for high-detail analyses when metadata is not required; use vector for rich attribute information and polygon-level summaries.
  - When aggregating to 1km, expect minor rounding so totals may not sum exactly to 100; treat coastal areas with appropriate adjustments.
  - Cite the appropriate DOI when referring to specific LCM2015 products in analyses or publications.

- Access points and contact
  - CEH Environmental Information Platform for 1km products; spatialdata@ceh.ac.uk for data requests, licensing, and further details.
  - Additional information and data papers available through CEH pages and the LCM2015 project site.

- References and background
  - Grounded in UK Broad Habitat definitions (JNCC Jackson, 2000) and CEH/Land Cover Map lineage (Morton et al., 2011; Jackson, 2000).
  - DOI-based citations recommended for reproducibility and data usage tracking.