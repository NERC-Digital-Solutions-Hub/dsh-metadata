# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover dataset produced to support diverse user needs with a publishing-friendly, repeatable method.
- Contains 21 land cover classes based on UK Broad Habitats, derived from two-date Landsat-8 imagery (30 m) with AWIFS as needed.
- Products include a core vector dataset, a 25 m raster, and 1 km aggregated products for Great Britain and Northern Ireland, with rich metadata and uncertainty information.
- LCM2015 is a stable, archived dataset with DOIs for each product; data citation is encouraged.

## Data products and structure
- Vector data set
  - ~6.7 million polygons (GB) and ~0.9 million polygons (NI)
  - Key attributes per polygon: gid (unique identifier), BHAB (dominant Broad Habitat class), Pix_dist (distribution of pixels across all classes), unc (mean per-polygon probability), unc_stdev, npix (number of pixels in polygon), Modal_class (recommended display class), Modal_prop (dominant class proportion), Composite (composite image source).
- 25 m raster
  - 2-band raster: Band 1 = dominant LCM2015 class; Band 2 = mean per-polygon probability from Random Forest.
- 1 km raster
  - Dominant class per 1 km cell (GB and NI)
  - Percentage cover per class (21 classes) and per aggregate (10 aggregates)
  - The 1 km products support broader-scale analyses and modeling
- Class mapping and metadata
  - Appendix-based color mapping guidance; extensive metadata for each polygon; DOIs provided for citation.
- Projections and area
  - GB in British National Grid; NI in TM75 Irish Grid
  - Minimum mappable unit: polygons > 0.5 ha; dissolves smaller parcels and very small linear features

## Classification and methodology
- Classification method: Random Forest classifier (new for 2015), handling multi-modal training data and avoiding the need for spectral sub-classes.
- Training data: initial training areas defined from stability across 2000 and 2007, supplemented with coastal and poorly mapped classes.
- Ancillary data: integrated into the input alongside satellite data (no post-classification KBEs); enhances objectivity and reduces manual adjustment.
- Spatial framework: per-pixel approach; no segmentation applied in LCM2015 (unlike LCM2007), improving change-mapping flexibility.
- Output specifics: stable, per-pixel classifications; per-polygon and per-band probability values included for uncertainty assessment.

## Differences and methodological changes from earlier maps
- Output data changes
  - Montane class removed (reclassified as Inland Rock or upland habitats based on spectral data)
  - Rough grassland class removed (to align with JNCC Broad Habitats and reduce misclassifications)
  - 25 m raster now 2-band (classification and mean probability)
  - Probability information simplified: vector carries mean polygon probability; 25 m band 2 contains the same probability; 1 km products do not include per-pixel probability
  - No spectral sub-classes; Random Forest removes need for sub-class grouping
  - Spatial framework: segmentation removed; full per-pixel approach; clarifications on upland and segmentation impacts
  - Mixed woodland handling: training uses pure stands; modal_class assigned to polygons; may affect some woodland classifications
- Methodology differences
  - Switch to Random Forest classifier
  - Stable training areas used as a seed for training, with manual augmentation for coastal and difficult classes
  - Ancillary datasets are integral to input data rather than post-classification refinements

## Data quality, uncertainty, and usage notes
- Uncertainty is provided via per-polygon mean probability (RF-based) and standard deviation.
- The dataset includes guidance on potential classification ambiguities, especially for grasslands, montane areas, and mixed woodland.
- LCM2015 is designed for land cover mapping (not necessarily land use); some land uses may be spectrally similar to others.
- Minimum mapping unit and dissolution rules can affect small features and coastal boundaries.

## Data access, licensing, and citation
- Access
  - 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - Full vector and 25 m raster products available under licence on request from CEH
- Licensing and fees
  - Licence terms may apply; please apply online or contact spatialdata@ceh.ac.uk
- Citation and DOIs
  - Each LCM2015 product has its own DOI for citation (GB vector, GB 25 m raster, GB 1 km products, NI products)
  - Example citation format provided in the document; include authors, year, and DOI in references
- Map projection details
  - GB products: British National Grid; NI products: TM75 Irish Grid
- Data provenance and documentation
  - Rich metadata for vector polygons, including dominant class, pixel distributions, and probabilities
  - Appendix-based details on color mapping and the composite imagery used in production

## Practical guidance for data stewards
- Use the vector dataset when rich polygon-level metadata and pixel distributions are needed; use 25 m raster for processing efficiency and simpler data structures.
- For change mapping or longitudinal studies, be aware of changes in class definitions (e.g., Montane and Rough grassland removal) and the absence of segmentation in 2015.
- When reporting analyses, cite the appropriate DOI for the data product used and reference the LCM2015 documentation for methodological context.
- Maintain gid attributes in vector data to preserve unambiguous communication across datasets and users.

## Additional information
- The document includes appendices detailing standard LCM2015 colour mapping, composite image recipes, and a comprehensive description of each Broad Habitat class (with notes on how they map spectrally and to field definitions).