# Dataset documentation

- LCM2015 is a parcel-based UK land cover map classifying satellite imagery into 21 Broad Habitat-based classes, created mainly from Landsat-8 (30 m) with AWIFS (60 m) as needed.
- The dataset provides multiple data products to support GIS-based analysis and map-making, with per-polygon (vector) and raster representations, plus 1 km aggregated products.

## Important context for use

- LCM2015 is complex and should be reviewed before use; it is not advised to use the LCM series for change mapping in its current state.
- Differences between LCM products reflect real changes and classification error, plus varying methodological and data inputs over time.

## Aims and design

- Deliver map-based data suitable for diverse users (policy teams, clients, public) with clear spatial boundaries and rich metadata.
- Per-pixel spectral classification framework with polygons reflecting real-world boundaries to improve interpretation and compatibility with other data.
- Encodes uncertainty and detailed metadata to support robust analysis and interpretation.

## Key differences from LCM2007 (highlights)

- Montane class removed; upland areas reclassified as Inland Rock or other upland habitats to support change mapping. For Montane distribution, use LCM2007.
- Rough grassland class removed due to data and classification issues; grid now aligns with JNCC Broad Habitat types.
- 25 m raster now two bands: band 1 = classification; band 2 = mean per-polygon probability.
- Probability data streamlined: vector includes mean polygon probability; 25 m raster band 2 provides this value; 1 km products do not include probability.
- Spectral sub-classes removed; Random Forest replaces maximum likelihood, reducing the need for sub-class training.
- Spatial framework moved away from segmentation: no segmentation polygons in LCM2015; segmentation changes from LCM2007 aimed to improve per-area match but introduced variability.
- Mixed woodland training updated: training uses pure stands and polygon-level modal_class; some mixed-wood patches may be assigned to other classes; users can check pix_dist for details.

## Classification methodology and data inputs

- New classifier: Random Forest, handling multi-model training data and often outperforming previous methods.
- Training areas established from stable areas classified similarly in 2000 and 2007, with additional coastal and poorly mapped classes added manually.
- Ancillary data (e.g., slope, distance to rivers) are integrated into the input data for classification, making knowledge-based enhancements an integral part of the process.

## Data scope and products

- LCM2015 maps land cover (not land use).
- Stable, archived dataset with DOIs for citation.
- Minimum mappable area: >0.5 ha (parcels smaller than 0.5 ha and lines <20 m dissolved).
- 21 target classes, with some Broad Habitats subdivided (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral Sediment includes Saltmarsh).

## Data products and formats

- Core vector data set: polygons with rich attributes.
- 25 m raster: two-band raster (band 1 = dominant class, band 2 = mean probability).
- 1 km rasters: several products including dominant cover and percentage cover for both 21 target classes and 10 aggregate classes.
- GB and NI data are provided separately with respective projections (GB: British National Grid; NI: Irish Grid).

## Vector data (GB and NI)

- ~6.7 million polygons (GB) and ~0.9 million polygons (NI).
- Key attributes (Table 2): gid (unique parcel identifier), BHAB (dominant Broad Habitat class), Pix_dist (distribution of pixels per class within the polygon; includes npix and modal_class), unc and unc_stdev (uncertainty metrics from Random Forest), npix, Modal_class (recommended display class), Modal_prop (dominant class proportion), Composite (classification source image set).

## Raster data

- 25 m raster: 2-band; band 1 = dominant class; band 2 = mean per-polygon probability.
- 1 km raster products: dominant class per 1 km cell; 1 km percentage cover per class (21-band for target classes; 10-band for aggregates).
- Metadata: Table 3 details grid dimensions, pixel sizes, data types, and coordinate systems for GB (BNG 27700) and NI (TM75 Irish Grid 29903).

## Uncertainty and metadata

- Uncertainty is quantified via per-pixel probability from the Random Forest classifier.
- Probability values are provided in vector (uncertainty fields) and in 25 m raster band 2, but not for 1 km products.
- Rich polygon metadata includes dominant class, pixel counts per class, and mean probabilities, enabling detailed assessments of classification quality.

## Class definitions and labeling

- 21 LCM2015 target classes are linked to UK Broad Habitats concepts, with hierarchical refinements for certain groups (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral Sediment splits).
- Each parcel receives a unique gid in the vector product to support unambiguous communication and cross-referencing.

## Access and citation

- 1 km rasters available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25 m products available on request under licence from CEH; fees may apply.
- Each LCM2015 product has a DOI for citation (GB and NI vector, 25 m, 1 km percentage and dominance products; both GB and NI variants).

## Spatial reference and mapping details

- GB: British National Grid (EPSG: 27700) for vector and 25 m raster.
- NI: Irish Grid (TM75 Irish Grid; EPSG: 29903) for vector and 25 m raster.
- The dataset contains comprehensive documentation, including Appendix 1–4 with class definitions, color mapping, and composite image details.

## How to cite and where to find more information

- DOIs are provided for all LCM2015 products (GB and NI; vector, 25 m, and 1 km products).
- Citations should include author names and year, with the DOI in the references.
- Further information and data access are available at the CEH pages and the EIDR data portal.

## Contact and references

- CEH contact: spatialdata@ceh.ac.uk; dataset information via CEH and EIDC portals.
- References include Jackson (2000) and Morton et al. (2011) for Broad Habitat definitions and LCM2007 methodology.