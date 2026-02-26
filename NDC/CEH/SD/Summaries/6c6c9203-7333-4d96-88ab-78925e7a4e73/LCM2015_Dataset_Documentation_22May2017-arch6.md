# Dataset documentation

- LCM2015 (Land Cover Map 2015) is a parcel-based UK land cover map classifying satellite data into 21 Broad Habitat-based classes, built from two-date Landsat-8 (30 m) and AWIFS (60 m) imagery, updating LCM2007 and aligning with a per-polygon spatial framework.
- The dataset is provided as multiple data products to support diverse needs (vector, 25 m raster, and 1 km percentage/dominant products) and is available separately for Great Britain and Northern Ireland.

## Data products and formats

- Core vector data: polygons with rich attributes per parcel (gid, dominant class, pixel counts by class, uncertainty, modal class, etc.).
- 25 m raster: two-band product per polygon; band 1 = dominant class, band 2 = mean per-polygon probability from the classifier.
- 1 km raster products: summary of 25 m data to produce dominant class (1 km) and percentage cover (21-class and 10-aggregate classifications).
- Data availability:
  - 1 km rasters accessible via CEH Environmental Information Platform (EIP).
  - Full vector and 25 m rasters available on request under licence from CEH (licence fees may apply).
- Coordinate systems: Great Britain in British National Grid; Northern Ireland in TM75 Irish Grid.

## Data structure and key attributes

- Vector data:
  - gid: unique parcel identifier.
  - BHAB: dominant Broad Habitat class (text).
  - Pix_dist: breakdown of pixels per class within the polygon (plus npix and modal_class).
  - unc: mean per-polygon uncertainty (0–255 scale); Unc_stdev: std deviation.
  - npix: number of pixels in the polygon.
  - Modal_class: recommended display class (1–21).
  - Modal_prop: proportion of polygon classified as the dominant class.
  - Composite: composite image used for the classification.
- Metadata and provenance:
  - Each polygon includes detailed metadata about processing and class composition.
  - Data are provided with Digital Object Identifiers (DOIs) for reproducibility and citation.
- 25 m raster:
  - Band 1: dominant LCM2015 class per polygon.
  - Band 2: mean per-polygon probability from the Random Forest classifier.
- 1 km rasters:
  - Dominant cover per 1 km pixel (21-class and 10-aggregate options).
  - Percentage cover per class per 1 km pixel (21 bands for GB, 10 aggregate bands).

## Methodology and data quality

- Classification approach:
  - Random Forest classifier (replacing previous Maximum Likelihood), enabling multi-modal training data without spectral-subclass grouping.
  - Ancillary data (e.g., slope, proximity to rivers) are integrated as inputs rather than post-classification rules.
  - Training areas built from a stable base (areas consistently classified in 2000 and 2007) plus coastal and difficult classes.
- Spatial framework and segmentation:
  - No segmentation-based polygons in LCM2015; per-pixel classification with a per-polygon summarization.
  - Aims to improve consistency for change detection and reduce segmentation-related errors.
- Output details and caveats:
  - LCM2015 maps land cover, not land use; some land uses may be indistinguishable spectrally.
  - 0.5 ha is the minimum mappable unit; parcels smaller than 0.5 ha are dissolved.
  - Montane class removed; areas previously mapped as Montane are reclassified as Inland Rock or upland habitats. For Montane distributions, use LCM2007.
  - Rough grassland class removed to maintain consistency with JNCC Broad Habitats; grassland types now align spectrally with Broad Habitat definitions.
  - 25 m raster is two-band; 1 km products are derived by aggregating the 25 m raster.
  - Mixed woodland training uses pure stands for training with per-pixel classification, then polygon-level labeling by modal class; pix_dist can be used to investigate mixed results.
- Outputs and uncertainty:
  - Per-pixel probability from Random Forest is provided for vector (mean polygon probability) and 25 m raster (band 2); not provided for 1 km products.
  - Uncertainty is explicitly documented to aid data use and interpretation.

## Coverage and classes

- 21 target LCM2015 classes derived from UK Broad Habitats (JNCC framework), with some subdivisions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- The dataset provides a robust framework for comparing with other spatial data but notes that differences between LCM products and past maps can reflect real change and classification error.

## Data access, citation, and licensing

- DOIs are provided for all GB and NI products (vector, 25 m raster, 1 km percent and dominant classes, both GB and NI).
- Data citation recommended in publications using the formats specified (include authors, date, and DOI).
- Access details:
  - 1 km rasters via CEH EIP.
  - Full vector and 25 m rasters on request; licensing may apply.
- Map projections:
  - GB products in British National Grid; NI products in TM75 Irish Grid.
- For more information and access, contact spatialdata@ceh.ac.uk or visit CEH pages listed in the document.

## Practical notes for data use

- The dataset is intended as a stable, archived resource with detailed metadata and uncertainty information to support data integration, analysis, and product development.
- Users should refer to the DOIs and Appendix material for class definitions and color mappings when visualizing results.
- Users planning change mapping should be aware that LCM2015 is not recommended in its current state for change-metection use without careful methodological alignment.

## Additional information and contacts

- Further information and data product details are available at CEH’s LCM2015 pages and the CEH Environmental Information Platform (EIP).
- Queries: spatialdata@ceh.ac.uk