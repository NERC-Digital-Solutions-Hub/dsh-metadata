# Land Cover Map 2015 (LCM2015) dataset documentation

- LCM2015 is a parcel-based UK land cover map with 21 classes based on UK Biodiversity Action Plan Broad Habitats. It classifies two-date Landsat-8 (30 m) composites, supplemented by AWIFS (60 m) data, to update LCM2007 and align with generalised boundary-fed mapping. It emphasizes per-pixel classification and a repeatable production method suitable for change mapping in the future.

## Data products and formats

- Vector data set
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland
  - Attributes per polygon include: gid (unique geometry id), dominant land cover (BHAB), Pix_dist (23-class pixel counts plus npix and modal_class), unc (mean per-polygon probability), unc_stdev, npix, Modal_class (LCM2015 target class), Modal_prop, Composite (source of classification)
- 25 m raster
  - 2-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest
- 1 km raster
  - Dominant class at 1 km; percentage cover per class (21 bands for target classes; 10 bands for aggregate classes)
- Class structure
  - 21 target classes mapped from 21 Broad Habitats; some categories are split (e.g., Built-up Areas and Gardens into Urban and Suburban)
  - Aggregates for 1 km products (10 aggregate classes)
- Spatial detail and extents
  - GB and NI provided separately with respective coordinate systems and projections
- Metadata and uncertainty
  - Rich polygon metadata; per-polygon likelihood via Random Forest; per-pixel probability in the 25 m raster; uncertainty not provided for all products

## Methodology and production approach

- Classification algorithm
  - Random Forest classifier (replacing the previous Maximum Likelihood approach)
  - Handles multi-modal training data; eliminates need for spectral sub-classes
- Training data and inputs
  - Begins with an initial stable set of training areas (areas consistently classified in 2000 and 2007)
  - Supplemented with coastal areas and difficult classes (Fen, Marsh and Swamp; semi-natural grasslands)
  - Ancillary data (e.g., slope, proximity to rivers) are integral inputs to the classifier (not post-classification refinements)
- Spatial framework and segmentation
  - No segmentation-based spatial framework in LCM2015 (removal of segmentation polygons used in LCM2007)
  - Output is per-pixel classification; aims to ease change mapping and improve robustness across time
- Training specifics
  - Mixed woodland handled by training on pure stands for Coniferous and Broadleaf; final polygon label is the modal class of classified pixels
- Output interpretation
  - 1 km products derived from 25 m data by aggregating to percentage and dominant cover per 1 km square

## Key differences from LCM2007

- Output class handling
  - Montane class removed; converted to Inland Rock or other upland habitats based on spectral data
  - Rough grassland class removed; grassland types map to JNCC Broad Habitat types without dedicated Rough Grassland
- Data formats and reporting
  - 25 m raster becomes a two-band image (classification band + probability band)
  - Probability information simplified to mean per-polygon probability in vector and band 2 of 25 m raster
  - No spectral sub-classes; sub-classes deemed redundant with Random Forest
- Spatial framework
  - No segmentation-based polygons in LCM2015; segmentation present in LCM2007 is removed to reduce misalignment with classification
- Mixed woodland handling
  - Transition from object-based training to pixel-based training with modal_class summary, affecting some woodland classifications

## Data access and citation

- Access
  - 1 km raster data available via CEH Environmental Information Platform
  - Full vector and 25 m raster data available under licence on request from CEH (licensing fees may apply)
- Data citations and DOIs
  - Each LCM2015 product has its own DOI for GB and NI (vector, 25 m, 1 km aggregate/dominant/percentage products)
  - Examples include DOIs for GB vector, GB 25 m, GB 1 km percentage/dominant classes, and corresponding NI DOIs
  - Citations should include author names, date, and full DOI in references
- Projections
  - Great Britain: British National Grid (EPSG 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)

## Data structure and class details

- Core vector product
  - Polygon-level metadata plus per-polygon class distribution (Pix_dist), uncertainty, number of pixels (npix), and dominant class (Modal_class)
- 25 m raster product
  - Band 1: dominant LCM2015 class per polygon
  - Band 2: mean per-polygon probability from Random Forest
- 1 km products
  - Percentage cover per class (21 bands for target classes; 10 bands for aggregates)
  - Dominant cover at 1 km (single-band)
- Class mapping and interpretation
  - 21 target classes aligned with JNCC Broad Habitats definitions
  - Appendix materials provide color mappings and detailed class definitions
  - LCM2015 per-polygon labels are designed to be used with the gid attribute to ensure unambiguous communication

## Practical usage notes and cautions

- LCM2015 maps land cover, not always land use; some land-use distinctions cannot be inferred reliably from spectral data
- The dataset is stable and archived with DOIs; proper citation is encouraged for reproducibility
- Minimum mapping unit
  - Parcels smaller than 0.5 ha and line features under 20 m are dissolved into surrounding areas
- Change mapping considerations
  - The document notes caution: differences between LCM editions and change mapping limitations; users should be aware of methodological changes when comparing to earlier maps
- Data limitations and accessibility
  - Some datasets may require extensive data access steps; ancillary data integration is powerful but depends on data availability and quality
- Administrative and boundary details
  - Spatial alignment with national cartography boundaries; field-level interpretation requires consideration of scale and spectral similarity across habitats