# Dataset documentation

- Land Cover Map 2015 (LCM2015) dataset documentation describing the data products, methodology, usage cautions, and access details.

## Purpose and scope
- Provides a range of land cover data products for UK users to support environmental monitoring, policy scrutiny, and decision-making.
- Aims to deliver useful, verifiable, and openly governed land cover information to inform policy and future monitoring.

## Key data products (LCM2015)
- Vector data set (core product)
  - Polygons with attached attributes describing dominant land cover class, provenance, uncertainty, pixel counts per class, and dominant-class proportion.
  - ~6.7 million polygons for Great Britain; ~0.9 million for Northern Ireland.
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest classifier.
- 1 km raster
  - Summary products derived from 25 m data: dominant class per 1 km cell; dominant aggregate class; and 21 (or 10) percentage-cover bands representing class proportions.
  - British and Northern Ireland data are provided separately due to projection differences.
- Spatial and thematic resolution
  - Minimum mappable unit: >0.5 ha; parcels smaller than 0.5 ha dissolved into surrounding landscape.
  - 25 m and 1 km products enable both detailed mapping and national-scale modelling.

## Methodology highlights
- Classification approach
  - Uses Random Forest classifier (instead of previous Maximum Likelihood) to better handle multi-modal training data and to simplify training data preparation.
- Training data and stability
  - Initial training areas derived from areas consistently classified in 2000 and 2007; augmented for coastal zones and challenging classes.
  - Ancillary data (e.g., slope, distance to rivers) integrated into input data rather than applied post-classification, allowing objective knowledge-based enhancements.
- Spatial framework
  - Per-pixel, unsegmented (no segmentation-based polygons) spatial framework to improve change-mapping suitability and reduce segmentation misalignments.
- Data provenance and uncertainty
  - Each polygon includes per-polygon probability (uncertainty measure) derived from the Random Forest classifier; 25 m raster band 2 provides per-polygon mean probability.
  - Probability data are not provided for 1 km products.
- Training and validation notes
  - Shift from sub-classes of spectral signatures to primary classes, reflecting changes in classifier design and data handling.
  - Mixed woodland and other nuanced classes trained with pure stands or polygon-level aggregation; modal_class used for polygon labeling.

## Classes and labeling
- LCM2015 maps 21 target classes based on UK Broad Habitats (JNCC framework) with specific refinements (e.g., subdivision of Built-up Areas and Gardens; Heather vs Heather grassland; Littoral/sub-littoral distinctions).
- Class relationships and mappings to broader habitats are documented; Appendix materials detail class definitions and how spectral data map to habitat concepts.

## Data quality, caveats, and guidance
- Important cautions
  - LCM2015 is not recommended for change mapping in its current state due to real-change signals mixed with classification changes and methodological differences.
  - Differences from LCM2007 include removals of certain classes (e.g., Montane, Rough grassland), changes in output formats, and methodological updates (Random Forest, no segmentation).
- Uncertainty and interpretation
  - Per-polygon mean probability provides a quantitative uncertainty proxy; users should consider this in analyses and reporting.
  - Coasts and some transitional areas may show uncertainty or misclassification; 1 km products provide a higher-level view with aggregation, which can mitigate some issues.
- Metadata and provenance
  - Rich metadata accompany the vector data, including per-polygon breakdown of pixel counts by class, dominant-class proportion, and composite image origin.
  - Each polygon carries a unique geometry identifier (gid) to aid unambiguous communication of results.

## Data access and licensing
- Data access
  - 1 km raster data sets available via the CEH Environmental Information Platform (EIP).
  - Full vector product and 25 m product available on request under licence from CEH; online application process and potential licence fees.
- Projections
  - Great Britain data: British National Grid.
  - Northern Ireland data: Irish National Grid (TM75 Irish Grid).
- DOIs and citation
  - Each LCM2015 product has a DOI for citation, promoting repeatability and tracking usage.
  - Guidance provided on how to cite each product in publications.

## Projections, formats, and documentation
- Formats and data structure
  - Vector data: polygon features with attributes including gid, dominant class, pixel counts per class, uncertainty, and MODAL_CLASS.
  - 25 m raster: two-band raster with classification and per-polygon probability.
  - 1 km rasters: aggregate and percentage-cover products at both 21-class and 10-aggregate-class levels.
- Documentation and appendices
  - Appendices include standard LCM2015 color mapping, composite image references, and detailed definitions of Broad Habitats (for user interpretation).
  - Colour mapping and class definitions are provided to aid consistent visualization.

## Citing and references
- DOIs provided for Great Britain and Northern Ireland vector, 25 m, and 1 km products.
- Data citation recommended in the form of author names, year, and DOI, e.g., Land Cover Map 2015 (vector, GB). NERC Environmental Information Data Centre, with the respective DOI.

## Additional information
- Data paper and further information are in preparation or available via CEH channels.
- Related background references include Jackson (2000) on Broad Habitat definitions and Morton et al. (2011) on LCM2007 methodology.