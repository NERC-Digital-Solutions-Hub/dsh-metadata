# Land Cover Map 2015 (LCM2015)

- LCM2015 is a parcel-based UK land cover map created by spectral classification of satellite data (Landsat-8 and AWIFS) into 21 Broad Habitat classes aligned with JNCC Broad Habitat definitions.
- Products are designed to support a wide user community with varying needs, from detailed vector polygons to coarser 1km summaries.
- Data formats and resolutions:
  - Core vector product (polygons with rich attributes)
  - 25m raster (dominant class per polygon + per-polygon probability)
  - 1km raster products (dominant class and percentage cover for both 21 target classes and 10 aggregates)
- Each data set has DOIs for citation and is intended as a stable, archived resource with metadata and uncertainty information.
- Projections: Great Britain in British National Grid; Northern Ireland in Irish National Grid.

## Overview and purpose for monitoring

- Designed to support environmental monitoring, policy scrutiny, and informing future decisions by providing a standardized, openly documented UK land cover reference.
- Clarifies that LCM2015 maps land cover (not strictly land use) and provides a framework for comparing change over time, while acknowledging inherent limitations in change mapping across versions.
- Emphasizes transparent data provenance, metadata richness, and uncertainty indicators to aid governance and evidence-based decision making.

## Data products and structure

- Vector data set
  - 6.7 million polygons (GB) and 0.9 million polygons (NI)
  - 9 attributes including:
    - gid (unique parcel identifier)
    - BHAB (dominant Broad Habitat class)
    - Pix_dist (counts of pixels per class within polygon)
    - unc (mean per-polygon probability)
    - unc_stdev (uncertainty standard deviation)
    - npix (number of pixels in polygon)
    - Modal_class (recommended display class, 1–21)
    - Modal_prop (proportion of polygon classified as dominant class)
    - Composite (source composite image)
- 25m raster data set
  - 2-band raster:
    - Band 1: dominant LCM2015 class per polygon
    - Band 2: mean per-polygon probability from Random Forest
  - Great Britain and Northern Ireland provided separately with appropriate projections
- 1km raster data set
  - Summary products derived from 25m raster:
    - Dominant cover (21 target classes and 10 aggregate classes)
    - Percentage cover for each class (21 bands for GB; 10 aggregate bands)
  - Rounding may cause small deviations from 100% within a 1km pixel
- Class mapping
  - 21 LCM2015 target classes aligned to Broad Habitat definitions; some classes are split into sub-categories (e.g., Urban vs Suburban; Heather vs Heather grassland)

## Methodology and classification approach

- New classification algorithm
  - Random Forest classifier (per-pixel)
  - Handles multi-modal data and avoids the need for spectral sub-classes
  - Trains on an initial stable set of training areas (areas classified consistently in 2000 and 2007) and expands to coastal and other challenging areas
- Use of ancillary data
  - Ancillary layers (e.g., slope, proximity to rivers, soil context) are integral inputs to the classifier rather than post-classification rules
  - This makes knowledge-based enhancements objective and embedded in the classification
- Spatial framework and segmentation
  - No segmentation-based final polygons in LCM2015; per-pixel classification summarized to polygons
  - Removal of prior segmentation in the spatial framework to improve change-mapping consistency
- Data and processing notes
  - LCM2015 maps land cover (not land use) and uses a fixed minimum mapping unit
  - Stable training areas built from legacy datasets; cross-validated training regions for challenging classes
- Output and uncertainty
  - Vector includes per-polygon probability and detailed class breakdown (via Pix_dist)
  - 25m raster includes per-polygon mean probability in band 2
  - Uncertainty is explicit, aiding interpretation and decision making

## Differences from previous versions (LCM2007 and earlier)

- Montane class removed; upland areas reclassified using spectral data into Inland Rock or other upland habitats
- Rough grassland class removed; grassland types re-aligned with Broad Habitat types without relying on soil data
- 25m raster becomes a two-band product (classification band + probability band)
- Probability data streamlined: vector includes mean polygon probability; 25m raster band 2 carries mean probability
- No spectral sub-classes; Random Forest replaces Maximum Likelihood Classification
- Spatial framework segmentation removed; no segmentation polygons in LCM2015
- Mixed woodland handling updated: training uses pure stands; final polygon labels reflect modal class with pix_dist details
- Methodology shifts to incorporate ancillary data within the classifier, reducing reliance on post-classification rules

## Metadata, uncertainty, and data governance

- Rich metadata for each polygon, including dominant class, pixel-level breakdown, and probability
- Uncertainty information provided as mean per-polygon probability (and standard deviation for the uncertainty)
- Per-polygon attributes enable detailed reporting and transparent data provenance
- DOIs assigned to all products to support reproducibility and proper citation
- Data governance considerations addressed via explicit data sharing guidance, licensing on request for some products, and clear provenance

## Access, citation, and usage guidance

- Access
  - 1km raster data available via CEH Environmental Information Platform
  - Full vector and 25m products available under license on request from CEH
  - Contact: spatialdata@ceh.ac.uk; website links provided for access and licensing details
- Citation
  - Each product has its own DOI; users should cite according to the provided DOIs in the data paper and references
  - Example citation guidance provided for including author names, year, and DOI in publications
- Practical usage notes for monitoring
  - LCM2015 is a stable, archived dataset suitable for long-term monitoring and policy assessment
  - Minimum mappable unit is 0.5 ha; smaller features are dissolved into surrounding landscape
  - Users should be mindful of change-mapping limitations when comparing across LCM generations due to methodological and data differences

## Class definitions and mapping notes (Appendices)

- Appendix 1–3 offer detailed explanations of Broad Habitat definitions and LCM2015 class distinctions
- Examples include distinctions among Broadleaved and Coniferous Woodlands, Arable and Horticulture, various Grassland types, Wetlands (Fen, Marsh, Swamp; Bog), Water bodies, Urban and Suburban areas, Littoral and Supralittoral habitats, and Inland Rock
- Appendix 3 includes a standard LCM2015 colour mapping scheme for visualization
- Appendix 4 lists composite images used during data production

## Practical guidance for readers and users

- Use the vector data when detailed polygon-level attributes and metadata are required; prefer 25m or 1km rasters for applications where polygons are unwieldy or when a coarser output is appropriate
- Be cautious with change detection across LCM versions due to evolving methodologies, class definitions, and data inputs
- Leverage the uncertainty information to assess confidence in classifications, particularly for policy-relevant assessments
- Reference the DOIs and underlying metadata when citing and integrating LCM2015 products into monitoring frameworks

## Contacts and further information

- Data access and enquiries: spatialdata@ceh.ac.uk
- Further information: CEH pages on Land Cover Map 2015, and the CEH Environmental Information Platform links
- Data paper and references provide additional methodological and definitional context