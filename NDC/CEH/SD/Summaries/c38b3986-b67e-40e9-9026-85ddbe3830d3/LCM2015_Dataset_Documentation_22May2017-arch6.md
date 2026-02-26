# Dataset documentation

- UK Land Cover Map 2015 (LCM2015) is a parcel-based land cover map for the UK, classifying satellite data into 21 Broad Habitat-based classes. It uses two-date composites primarily from Landsat-8 (30 m) with AWIFS (60 m) as needed, and is built on real-world boundaries for easier interpretation and compatibility with other geospatial data.
- LCM2015 updates LCM2007, continuing the move toward a repeatable method suitable for mapping change, while using an updated spatial framework derived from OS MasterMap and other boundary data.

## Data products and formats

- Core vector data: polygons with 9 attributes (dominant class, source image, uncertainty, pixel counts per class, mean polygon probability, etc.). ~6.7 million polygons for Great Britain and ~0.9 million for Northern Ireland.
- 25 m raster: two-band product per polygon; Band 1 = dominant class, Band 2 = mean per-polygon probability.
- 1 km raster products: aggregate outputs including dominant class (21-class and 10-aggregate options) and percentage cover for each class (21 bands and 10-aggregate bands). Rasters are provided separately for Great Britain and Northern Ireland.
- Data resolutions and projections: GB uses British National Grid; NI uses TM75 Irish Grid. Detailed metadata provided for each product.
- Minimum mapping unit: parcels smaller than 0.5 ha and linear features less than 20 m are dissolved into surrounding areas.

## Key methodological changes and differences from prior versions (LCM2007)

- Classification approach:
  - LCM2015 uses Random Forest instead of Maximum Likelihood, handling multi-modal training data and eliminating the need for spectral sub-classes.
  - Stable training areas concept built on 2000 and 2007 classifications; coastal areas supplemented for coverage.
  - Ancillary data (e.g., slope) are integrated into the input rather than applied post-classification, making enhancements objective within the model.
- Output changes:
  - Montane class removed; replaced by Inland Rock or upland habitat based on spectral data for change-mapping readiness. Use LCM2007 for Montane distribution if required.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats; no soil data used in LCM2015 classification.
  - 25 m raster becomes a two-band image (classification band + mean probability in band 2).
  - Probability data:
    - Vector: mean per-polygon probability stored as uncertainty attribute.
    - 25 m raster: probability stored in band 2.
    - 1 km products do not include per-polygon/probability data.
- Spatial framework and segmentation:
  - No segmentation-based polygons in LCM2015; per-pixel classification with subsequent polygon summarization.
  - Removal of segmentation in GB framework; this affects GB vector and GB 25 m raster, with some spatial framework corrections.
- Grassland and woodland:
  - Mixed woodland training shifted to pixel-level classification; modal_class assigned to polygons; some mixed-woodland polygons may be classified to Coniferous or Broadleaved classes instead of mixed categories; users should consult pix_dist for details.

## Class structure and labeling

- LCM2015 maps 21 target classes, with some internal splits to reflect broader habitat groups (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Unique object labeling: each parcel has a geometry ID (gid) to enable unambiguous communication of results.
- Rich metadata: polygon-level attributes include dominant class, detailed pixel breakdown (Pix_dist), uncertainty (unc), standard deviation (unc_stdev), number of pixels (npix), and Modal_class with its proportion (Modal_prop). Composite image source is tracked for traceability.

## Metadata, uncertainty, and data quality

- Uncertainty is provided as per-polygon mean probability from the Random Forest classifier (also available in band 2 of the 25 m raster).
- Pix_dist provides the pixel-level distribution across all 21 classes plus the majority class, aiding assessment of classification confidence.
- The dataset is designed as a stable, archived resource with DOIs for citation; metadata is comprehensive to support audits, reproducibility, and data integration.

## Data access and citations

- Data access:
  - 1 km raster products are accessible via the CEH Environmental Information Platform (eIP).
  - Full vector and 25 m raster products are available on request under licence; some applications may incur licence fees.
- Citations and DOIs:
  - All LCM2015 products have individual DOIs for proper citation in publications. GB and NI products have separate DOIs listed in the documentation.
  - Proper citation includes author names, date, and full DOI; example formats are provided in the dataset documentation.

## Usage notes, cautions, and applicability

- LCM2015 provides land cover (not necessarily land use) and is intended for broad-scale analysis, modelling, and data integration with other spatial datasets.
- Change mapping: the document cautions that LCM2015 is a complex product and should not be used for change mapping in its current state; differences between LCM products reflect real change and classification errors, influenced by evolving methods and data sources.
- Cross-version comparability: users should be cautious when comparing LCM2015 with previous versions (LCM2007/LCM2000) due to methodological and class-definition changes.
- 1 km products: rounding in percentage calculations means totals may not sum exactly to 100%; coastal areas may sum to less due to mapping extents.
- Class definitions: Appendix sections provide detailed class definitions and color mappings for consistent interpretation; some classes are subdivided to reflect spectral distinctions, though the core output remains per-polygon classification.

## Summary of practical implications for data support

- Provides a richly documented, multi-product dataset suitable for self-service analysis, with both detailed vector data and scalable raster aggregations.
- Benefits include a robust uncertainty framework (per-polygon probability), a modern classifier (Random Forest), and integrated ancillary data within the classification workflow.
- Requires attention to usage cautions around change mapping and cross-version comparisons; ensure appropriate citation using DOIs and adhere to licensing terms for full dataset access.