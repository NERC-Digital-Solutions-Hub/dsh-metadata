# Dataset documentation

- LCM2015 provides a parcel-based UK land cover map with 21 classes derived from Landsat-8 (30 m) and AWIFS (60 m) data, using two-date composites. It supports diverse data users but cautions that the LCM series should not be used for current change mapping without careful consideration of methodological changes and potential classification errors.
- Data products are designed to support a range of applications from detailed mapping to national-scale modeling, with explicit metadata and uncertainty information to aid governance and reuse.

## Data products and structure

- Vector data set
  - 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland
  - Attributes include: dominant land cover (text and numeric), per-polygon pixel counts for all classes, mean polygon probability, uncertainty metrics, polygon size, and a unique geometry identifier (gid)
- 25 m raster
  - 2-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest
- 1 km raster
  - Derived products: dominant class (1-band), dominant aggregate class (1-band), and percentage cover for 21 classes (21 bands) or 10 aggregates (10 bands)
  - Rounding may cause totals to exceed or fall short of 100 within a 1 km pixel
- Data coverage and resolution
  - Great Britain and Northern Ireland provided separately to accommodate different projections
  - Minimum mapping unit: >0.5 ha; parcels smaller than 0.5 ha or very small lines dissolved into surrounding landscape
- Class structure
  - 21 target classes aligned with UK Broad Habitat definitions (JNCC Jackson 2000), with some finer splits (e.g., Urban vs Suburban; certain grassland and woodland distinctions)
  - Appendix 1–3 provide mapping details and colour-coding guidance

## Methodology and data lineage

- Classification algorithm
  - Random Forest classifier (multivariate, handles multiple training sets)
  - Replaced previous Maximum Likelihood approach to better handle multi-modal data and reduce need for spectral sub-classes
- Training data and ancillary information
  - Stable training areas derived from cross-year consistency (2000 and 2007) and supplemented for coastal areas and challenging classes
  - Ancillary data (e.g., slope, distance to rivers) integrated into the input data rather than applied post-classification
- Spatial framework and segmentation
  - No segmentation in LCM2015 spatial framework (removal of prior segmentation steps to improve change-mapping consistency)
  - This primarily affects upland areas; Northern Ireland data were not segmented
- Labeling and metadata
  - Each parcel polygon is labeled with a unique gid
  - Rich metadata and uncertainty information accompany vector products
- Outputs and products
  - Core vector dataset from which 25 m raster and 1 km products are derived
  - 1 km products include both 21-class and 10-aggregate classifications

## Differences from LCM2007 (methodology and outputs)

- Montane class removed; replaced by inland rock or upland habitat classifications
- Rough grassland class removed to align with Broad Habitat types and avoid inconsistent soil data
- 25 m raster changed to a two-band format; probability data moved to band 2
- Probability information streamlined: vector stores mean polygon probability; 25 m raster band 2 holds this; 1 km products do not include per-pixel probabilities
- No spectral sub-classes used; Random Forest obviates the need for sub-class grouping
- Spatial segmentation removed from the LCM2015 framework; segmentation-related errors reduced, with upland corrections and other fixes

## Data quality, uncertainty, and guidance

- Uncertainty
  - Random Forest provides per-pixel probability estimates; reported as mean per polygon in the vector data and in band 2 of the 25 m raster
  - 1 km products do not report uncertainty
- Change mapping cautions
  - Differences across LCM versions reflect both real change and classification changes; the document cautions that direct change mapping using LCM2015 outputs may require careful interpretation and validation
- Labelling and interpretation
  - Unique gid labeling supports unambiguous communication; some class distinctions may require consultation of Appendix material for accurate interpretation

## Data access, licensing, and citation

- DOIs and citation
  - Each LCM2015 product has an individual DOI; recommended to cite authors and year (e.g., Rowland et al., 2017) with full DOI in references
  - DOIs cover GB vector, GB 25 m raster, GB 1 km percentage and dominant target classes, and NI equivalents
- Access and licensing
  - 1 km raster data accessible via CEH Environmental Information Platform (EIP)
  - Full vector and 25 m raster available on request under licence from CEH; pricing may apply
  - Contact spatialdata@ceh.ac.uk or submit licensing requests via the CEH information products portal
- Projections
  - GB data in British National Grid; Northern Ireland data in TM75 Irish Grid

## Practical use and governance considerations

- Data products suitability
  - Vector vs. 25 m raster: vector provides rich attribute data but larger file size; 25 m raster offers a lighter-weight alternative with consistent classification without polygon metadata
  - 1 km products are suitable for national-scale modeling and integration with other datasets (e.g., meteorology, species distributions)
- Documentation and reuse
  - Comprehensive metadata and DOIs facilitate reproducibility and data provenance
  - Users should refer to Appendix definitions for Broad Habitats and colour mappings to ensure consistent interpretation

## Appendix and references (high-level)

- Appendix 1–3 provide detailed Broad Habitat definitions and LCM2015 class descriptions, including colour-coding guidance and how certain habitats are spectrally mapped
- Foundational references: Jackson 2000 (JNCC Broad Habitat definitions) and Morton et al. 2011 (LCM2007 methodology)