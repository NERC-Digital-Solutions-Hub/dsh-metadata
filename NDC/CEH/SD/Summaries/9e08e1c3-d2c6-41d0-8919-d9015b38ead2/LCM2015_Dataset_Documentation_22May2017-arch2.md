# Dataset documentation

- LCM2015 is a UK parcel-based land cover map produced from satellite data, mapped into 21 Broad Habitat classes, with multiple data products (vector, 25 m raster, and 1 km aggregates).
- It uses two-date Landsat-8 composites (supplemented with AWIFS as needed) and integrates ancillary data as part of the input to a Random Forest classifier.
- It is a stable, archived dataset with DOIs for all products; terminology and structure are designed to support a broad range of monitoring analyses and policy evaluation over time.

## Purpose and key points for environmental analysts

- Purpose: provide a consistent, large-scale representation of land cover to support monitoring of environmental health, habitat distribution, and policy performance over time.
- Output formats designed for diverse applications:
  - Vector data: per-parcel polygons with rich metadata (dominant class, pixel counts, uncertainty, and probabilities).
  - 25 m raster: per-polygon dominant class (band 1) and mean per-polygon probability (band 2).
  - 1 km raster: aggregate percentage cover and dominant class, enabling UK-scale modeling with other datasets.
- Classes reflect UK Broad Habitats definitions; some classes are subdivided to capture key spectral distinctions (e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral components).
- Uncertainty is quantified via Random Forest output (per-polygon mean probability) and included in vector attributes and raster band 2.

## Data products and formats

- Vector dataset (core product)
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Attributes include gid, dominant land cover (BHAB and LCM2015 target class), pixel counts per class, uncertainty, number of pixels, and modal_class with a robust metadata set.
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability.
- 1 km raster
  - Dominant class and percent cover per 1 km pixel for both 21 classes and 10 aggregate classes.
- Spatial coverage and projections
  - Great Britain: British National Grid (BNG, EPSG 27700)
  - Northern Ireland: TM75 Irish Grid (EPSG 29903)
  - Separate GB and NI datasets for GB vector, GB 25 m, NI 25 m, and corresponding 1 km products.

## Key methodological differences from earlier LCM versions

- Classification algorithm
  - New: Random Forest classifier (handles multi-modal training data; avoids spectral sub-class grouping).
  - Previous: Maximum Likelihood Classifier.
- Training data and stability
  - Built from an initial stable set (areas classified the same in 2000 and 2007) plus additional training for coastal areas and historically challenging classes.
  - Ancillary data (e.g., altitude, distance to rivers) are integrated as input features rather than post-classification rules.
- Spatial framework
  - No segmentation-based polygons in LCM2015; per-pixel classifications with a simplified spatial framework to improve change mapping consistency.
- Class changes
  - Montane class removed; upland areas now mapped as Inland Rock or other upland habitats based on spectral data.
  - Rough grassland removed; grassland is aligned with JNCC Broad Habitat definitions without requiring soil data.
  - Mixed woodland training shifted to per-pixel classification with polygon-level modal labeling.
- Output and data structure
  - 25 m raster now includes two bands; spectral sub-classes deprecated; probability data stored as mean polygon probability (vector) and in raster band 2.
  - Stable per-polygon training areas and updated composite handling influence how outputs are produced and interpreted.

## Land Cover Map 2015 classes and labeling

- 21 target classes, based on UK Broad Habitats; some classes decoupled into sub-classes for reporting (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral components).
- Each parcel has a unique gid in the vector product to support unambiguous communication and data integration.
- Detailed mapping rules and class definitions are provided in Appendices (e.g., Broad Habitat definitions and class mapping to LCM2015 codes).

## Data access and citation

- Access
  - 1 km raster data sets available via the CEH Environmental Information Platform (EIP).
  - Full vector product and 25 m raster available on request under licence from CEH.
  - Licensing fees may apply for some users/applications.
- DOIs
  - Each LCM2015 product has its own DOI for proper citation and reproducibility (GB vector, GB 25 m, GB 1 km percentage and dominant classes, GB 1 km aggregate classes; NI equivalents).
  - Example citation formats and DOI details are provided in the data documentation.
- Usage notes
  - LCM2015 is a stable, archived product; DOIs should be cited in publications.
  - The dataset is complex; users should review Appendix details for class definitions and color mappings.
  - Not recommended to use LCM2015 for current-state change mapping without caution due to differences between time steps and methodological updates.

## Citing and references

- References include JNCC Broad Habitat definitions and the LCM2007 technical reports; users should consult these for background and classification criteria.

## Additional notes for monitoring and analysis

- The data structure provides rich metadata and uncertainty information to support quality assessment and traceability in analyses.
- Researchers planning long-term trend analyses should account for methodological changes between LCM2007 and LCM2015, and among the various LCM products, when interpreting changes over time.
- The documentation emphasizes the complexity of direct change mapping using LCM2015 in its current state and encourages careful methodological alignment with the data's design and metadata.