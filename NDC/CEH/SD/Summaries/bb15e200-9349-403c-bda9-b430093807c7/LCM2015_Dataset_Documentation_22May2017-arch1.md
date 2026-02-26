# Land Cover Map 2015 (LCM2015) Dataset documentation

- UK parcel-based land cover map with 21 classes based on JNCC Broad Habitat definitions; created from two-date Landsat-8 (30 m) composites, supplemented by AWIFS data; updates LCM2007; polygons reflect real-world boundaries for easy interpretation and compatibility with other geospatial data.
- Provides a range of data products to support diverse user needs, including a core vector dataset, a 25 m raster, and 1 km aggregated products.

## Data products and structure

- Core data sets
  - Vector data: polygons with 9 attributes (including gid, dominant BHAB class, pix_dist, uncertainty, npix, modal_class, and composite source).
  - 25 m raster: two-band image (band 1 = dominant class per polygon, band 2 = mean per-polygon probability).
  - 1 km rasters: dominant cover and percentage cover for both 21 classes and 10 aggregates.
- Coverage and scale
  - GB and Northern Ireland provided separately; vector: ~6.7 million polygons (GB) and ~0.9 million (NI).
  - Spatial resolutions: 25 m, 1 km, with per-polygon metadata and uncertainty estimates from Random Forest.
- Metadata and citations
  - Rich metadata for polygons; per-polygon probability (uncertainty) from the classifier.
  - Each product has its own DOI for citation (GB and NI datasets provided in Tables 4 and 5).
- Access
  - 1 km raster data via CEH Environmental Information Platform.
  - Full vector and 25 m products available on request under licence (fees may apply).

## Classification and methodology

- Classifier: Random Forest (robust handling of multi-modal training data; no spectral sub-classes necessary).
- Training data: initial stable areas defined from 2000 and 2007 classifications; supplemented with coastal areas and difficult classes.
- Ancillary data: incorporated as input alongside satellite data to guide classification; knowledge-based enhancements are integral rather than post-classification.
- Spatial framework: no segmentation was used in LCM2015; per-pixel polygons provide a stable framework suitable for change mapping.

## Differences from previous LCMs (notably LCM2007)

- Montane class removed; upland areas reclassified as Inland Rock or other upland habitats based on spectral data.
- Rough grassland removed; aligns with JNCC Broad Habitats; no soil data used in 2015 method.
- 25 m raster updates: two-band output; band 2 contains mean probability for the majority class.
- Probability data changes: LCM2015 vector stores mean polygon probability; 25 m raster band 2 stores the same; top-5 spectral sub-classes do not appear in LCM2015; 1 km products do not include probability data.
- Classification approach shift: from Maximum Likelihood (LCM2007) to Random Forest; training areas derived from stable areas with coastal and difficult class enhancements.
- Spatial framework: segmentation-based polygons removed; this mainly affects GB vector and GB 25 m raster (NI unaffected).

## Data scope, classes, and labeling

- 21 target classes based on UK Broad Habitats; some classes subdivided for reliability (e.g., Urban vs Suburban; Heather vs Heather grassland).
- Unique object labeling: gid (Geometry Id) retained for unambiguous communication.
- Output products include uncertainty/percentages to support quantitative analysis and reproducibility.

## Data formats and class mapping

- Vector: polygons with attributes such as BHAB, pix_dist (counts per class), unc, npix, Modal_class, etc.
- 25 m raster: 2-band raster (class code in band 1; probability in band 2).
- 1 km raster: dominant class and percentage cover products for both 21 classes and 10 aggregates.
- Classes are mapped to a wide range of applications; Appendix 3 provides standard colour mappings; Table 1 and Appendix 2 document the relationships between Broad Habitats and LCM2015 classes.

## Spatial coverage and projections

- GB: British National Grid (EPSG 27700); NI: TM75 Irish Grid (EPSG 29903).
- Data are provided separately for GB and NI to reflect different projections.

## Data access, licensing, and citation

- CEH Environmental Information Platform provides 1 km raster data.
- Full vector and 25 m products available on request under licence; fees may apply.
- Each product has a DOI for precise citation; guidance provided for citing data in publications (including example format).

## Practical considerations and caveats

- LCM2015 is a stable, archived dataset; differences from prior maps reflect methodological changes and updates.
- Minimum mapping unit: 0.5 ha (parcels smaller than 0.5 ha dissolved into surrounding landscape).
- Change mapping cautions: differences between LCM2015 and previous maps may reflect both real change and classification differences; the document advises caution when using LCM2015 for change mapping in its current state.
- LCM2015 maps land cover, not strictly land use; some land-use inferences (e.g., arable land) may not be determinable from the data alone.
- Rounding in 1 km percentage cover means totals may not sum exactly to 100; coastal areas may sum to less than 100.

## Appendices and supplementary information (highlights)

- Appendix 1 and 2 provide detailed Broad Habitat definitions and mapping considerations.
- Appendix 3 contains the standard LCM2015 colour mapping for each class.
- Appendix 4 lists composite images used in LCM2015 production.