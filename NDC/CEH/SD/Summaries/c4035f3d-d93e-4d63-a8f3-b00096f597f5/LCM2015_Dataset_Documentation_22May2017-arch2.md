# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) provides a UK-wide, parcel-based land cover map classified into 21 classes based on UK Broad Habitat definitions.
- Uses two-date Landsat-8 (30 m) composites with optional AWIFS data; produced as per-pixel classifications to support environmental monitoring and policy assessment over time.
- Outputs include a rich vector dataset, a 25 m raster, and 1 km aggregated products, with uncertainty and probability information from the classifier.

## Data sources and classification approach
- Input data: satellite imagery (Landsat-8; 30 m; complemented by AWIFS at 60 m) plus ancillary datasets used directly in classification.
- Classification algorithm: Random Forest, enabling multi-modal training data and avoiding spectral sub-class simplifications.
- Training data: initial stable areas defined from 2000 and 2007 classifications, supplemented with coastal areas and classes historically challenging to map.
- Output framework: per-pixel polygonal land cover with real-world boundaries, designed to be compatible with other geospatial data sets.

## Data products and access
- Vector data set
  - Polygons with nine attributes (land cover class, source image, uncertainty, pixel counts per class, dominant class, etc.).
  - Great Britain: ~6.7 million polygons; Northern Ireland: ~0.9 million polygons.
- Raster data sets
  - 25 m raster: two-band image (band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability).
  - 1 km raster products: dominant class (and aggregates) and percentage cover for all classes (or aggregates), derived from the 25 m data.
  - Separate GB and NI datasets with appropriate projections (GB National Grid; NI TM75 Irish Grid).
- Data access
  - 1 km raster products available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products available on request under licence from CEH.
  - DOIs provided for all GB and NI products to enable citation and reproducibility.

## Classes, labeling, and metadata
- LCM2015 uses 21 target classes based on Broad Habitat definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved/Neutral/Calcareous/Acid Grasslands, various aquatic and coastal habitats, Urban/Suburban, Inland Rock, etc.).
- Some classes are subdivided or mapped differently (e.g., Built-up Areas and Gardens into Urban and Suburban; Littoral and Supra-littoral distinctions in coastal zones).
- Each parcel (gid) has a unique label; metadata-rich vector attributes include dominant class, pixel distributions, and probability-related uncertainty.
- Color mapping and class definitions are provided in appendices; per-pixel probabilities are available for uncertainty assessment.

## Differences from LCM2007 and methodological changes
- Output data changes
  - Montane class removed; Montane areas reclassified as Inland Rock or other upland habitats based on spectral data.
  - Rough grassland class removed; polygonal grassland types now align with JNCC Broad Habitat types; no soil data used in LCM2015.
  - 25 m raster expanded to two bands (classification band and mean probability).
  - Probability data simplified: vector stores mean polygon probability; 25 m raster band 2 holds mean per-polygon probability; 1 km products do not include per-pixel probabilities.
  - No spectral sub-classes used; Random Forest handles multi-modal data, making spectral Sub-classes redundant.
  - Spatial framework: segmentation-based segmentation removed; per-pixel per- polygon approach replaces prior segmentation, with fixed spatial framework to improve change mapping consistency.
- Methodology changes
  - New classifier: Random Forest vs. Maximum Likelihood in LCM2007.
  - Training data preparation uses stable areas plus coastlines and historically hard-to-map classes.
  - Ancillary data integrated into the input as part of the classification process rather than post-classification rule-based adjustments.
- Impact
  - These changes improve suitability for change mapping and reduce segmentation-related inconsistencies, though they require careful interpretation when comparing to earlier LCM products.

## Data quality, usage notes, and citations
- LCM2015 is a stable, archived dataset with DOIs for each product; users should cite the DOIs to ensure reproducibility.
- Differences with earlier maps mean caution is required when comparing LCM2015 outputs with LCM2007 or prior maps; some change signals reflect methodological updates rather than real land cover change.
- The documentation notes that LCM2015 is not recommended for change mapping in its current state without careful handling of methodological differences.

## Projections, licensing, and further information
- Projections: GB vector/raster in British National Grid; NI vector/raster in TM75 Irish Grid.
- Access details and contact: data requests via CEH websites or spatialdata@ceh.ac.uk; licensing may apply for some users.
- Additional information and references: CEH LCM2015 pages and data citations guidelines; DOIs for all GB and NI products provided for reliable citation.

## Appendices and supplemental information
- Appendix 1: Comments on class definitions mapped in LCM2015, aligned with JNCC Broad Habitat definitions.
- Appendix 2: Summary of JNCC Broad Habitat definitions for reference.
- Appendix 3: Standard colour mapping recipes for LCM2015 classes.
- Appendix 4: Composite image usage details for LCM2015 production.