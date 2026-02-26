# Dataset documentation

## Overview

- Land Cover Map 2015 (LCM2015) is a UK-wide parcel-based land cover map classifying satellite data into 21 Broad Habitat classes, aligned with UK Biodiversity Action Plan definitions.
- Built from two-date Landsat-8 imagery (30 m) with AWIFS data as needed; used to update LCM2007 and support change mapping and diverse data users.
- Outputs a suite of products: detailed vector, 25 m raster, and 1 km aggregated products, with emphasis on per-polygon interpretation and self-serve data access for users.

## Data products and structure

- Core data model
  - Vector: polygons with rich attributes per parcel (gid, dominant class, uncertainty, pixel counts per class, modal class, etc.). Approximately 6.7 million parcels in GB and 0.9 million in Northern Ireland.
  - 25 m raster: two bands per cell; Band 1 = dominant LCM2015 class, Band 2 = mean per-polygon probability from Random Forest.
  - 1 km rasters: derived products including dominant class and percentage cover for both 21 classes and 10 aggregate classes; created by summarising 25 m results.
- Class and label details
  - 21 target classes based on Broad Habitats; some categories are further split (e.g., Built-up Areas and Gardens into Suburban and Urban).
  - Aggregated 1 km products provide 10 classes for simplified analyses.
- Metadata and uncertainty
  - Each polygon includes dominant class, pixel breakdown per class, mean probability, and uncertainty metrics.
  - Uncertainty is derived from the Random Forest classifier (per-polygon probability; band 2 of 25 m raster; not provided for 1 km products).
- Spatial and data specifics
  - Vector and 25 m rasters are GB-wide and NI-wide; separate coordinate systems: Great Britain uses British National Grid; Northern Ireland uses TM75 Irish Grid.
  - Minimum mappable unit (MMU) of >0.5 ha; parcels <0.5 ha and certain linear features are dissolved into surrounding landscape.
- Access and identifiers
  - Each vector parcel has a unique gid for unambiguous communication; comprehensive metadata accompanies polygon attributes.
  - DOIs provided for all products to support citation and reproducibility (vector, 25 m, 1 km target and aggregate classes for GB and NI).

## How to use the outputs

- Vector data are suitable for detailed per-polygon analysis with full attribute context; 25 m raster provides a compact, less verbose raster alternative with per-polygon probabilities accessible in band 2.
- 1 km products are useful for regional or national-scale modelling, including percentage and dominant cover for each class or aggregate class.
- LCM2015 is designed for land cover interpretation (not direct land use) and is intended to support change mapping and cross-dataset analyses.

## Methodology and key differences from earlier maps

- New classifier: Random Forest replaces Maximum Likelihood, improving handling of multi-model training data and reducing need for spectral sub-classes.
- Training and ancillary data
  - Training areas are built from stable areas across prior datasets (2000 and 2007) and expanded for coastal and challenging classes.
  - Ancillary data (e.g., altitude, soil) are integrated into the classification input rather than post-classification adjustments, making enhancements more objective.
- Output and data structure changes
  - Montane and Rough Grassland classes removed; mapped by spectral data into Inland Rock or other upland habitats to better support change mapping.
  - 25 m raster becomes two-band (classification band and mean probability) vs. previous single-band plus probability lists.
  - Probability data is streamlined: vector stores mean polygon probability; 25 m raster band 2 provides per-polygon probability; 1 km products do not include probability data.
  - Segmentation-based spatial framework removed; per-pixel, per-polygon labeling remains the basis for outputs.
- Woodland customization
  - Mixed woodland is defined and labeled based on analysis of pixels, with modal_class assigned at the polygon level; users can inspect pixel distributions (pix_dist) for details.

## Data quality, caveats, and cautions

- LC2015 maps land cover, not land use; interpretation may vary where cover resembles land use (e.g., grass in recreation vs. grazing).
- Change mapping caveats: differences between LCM products reflect real change and classification error; users should treat differences with caution, especially for time-series analyses.
- Some habitat types (e.g., Fen, Marsh and Swamp) may be underestimated due to spectral confusion and MMU constraints; caution advised when using for detailed ecological assessments.
- The montane category is removed for change-mapping suitability; historical montane distributions should use LCM2007 if required.
- The dataset is a stable, archived product with DOIs; however, users should cite DOIs and authors properly in publications.

## Data access and licensing

- Access via CEH Environmental Information Platform for 1 km raster products; full vector and 25 m products available on request under licence.
- Contact: CEH spatialdata@ceh.ac.uk; licence fees may apply for some users and applications.
- Data citations are required for reproducibility, using the provided DOIs for each product (GB and NI variants).

## Projections and extents

- GB: British National Grid (OSGB 27700) for vector and 25 m/1 km products.
- NI: Irish National Grid (TM75 Irish Grid) for corresponding products.
- Separate GB and NI datasets reflect their respective projections and extents.

## Citation and provenance

- All LCM2015 products have DOIs; users should cite the DOIs in publications and include author/date in-line and full references in bibliography.
- Data paper in preparation; additional methodological details available via CEH portals.

## Appendices and class mappings (high-level)

- Appendix 1-2: Definitions and interpretations of JNCC Broad Habitat classes as mapped in LCM2015, including notes on how field classifications relate to remote-sensing outcomes.
- Appendix 3: Standard LCM2015 colour mapping guidelines for visualisation.
- Appendix 4: Composite images used in LCM2015 (for documentation of data sources and image combinations).

## Quick reference for data support

- Core products: LCM2015 vector (gb/ni), 25 m raster, 1 km percentage and dominant cover products (gb/ni).
- Output attributes: gid, dominant class, pixel breakdown (pix_dist), uncertainty metrics (unc, unc_stdev), npix, modal_class, modal_prop, composite images.
- 21 target classes with possible aggregation to 10 for 1 km rasters; links to detailed class descriptions in the appendices.
- Data access channels: CEH EIP for 1 km; licensing and full vector/25 m products on request; contact spatialdata@ceh.ac.uk for details.