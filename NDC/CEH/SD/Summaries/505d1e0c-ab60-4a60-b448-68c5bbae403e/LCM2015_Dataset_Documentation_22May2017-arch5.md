# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a UK parcel-based land cover map classified into 21 Broad Habitats, using two-date Landsat-8 (30m) and AWIFS data, updating the LCM2007 framework.
- Treat with caution: differences across LCM products and changes over time; not suitable for current change-mapping without careful consideration.
- Built to support a diverse user community; reflects evolving user needs, data availability, and computational capabilities.
- Distinctions from prior versions include methodological and data-structure changes aimed at enabling change mapping and reducing manual input.

## Data products and structure
- Products and resolutions:
  - Vector data: polygons with rich attributes (6.7 million in GB, 0.9 million in NI).
  - 25m raster: two-band image per area (band 1 = dominant class, band 2 = mean per-polygon probability).
  - 1km raster: and associated products (dominant class, dominant aggregate class, and percentage cover for both 21 target classes and 10 aggregates).
- Classes and aggregation:
  - 21 LCM2015 target classes mapped from UK Broad Habitats (JNCC definitions).
  - Aggregates used for 1km raster products to support broader analyses.
- Spatial framework and labeling:
  - GB and NI data are provided in separate projections (British National Grid for GB, Irish National Grid for NI).
  - Each parcel has a unique gid (Geometry Id) for unambiguous communication; recommended to retain.
- Minimum mapping unit:
  - Minimum mappable area > 0.5 ha; parcels < 0.5 ha or linear features < 20 m dissolved into surrounding landscape.
- Data richness:
  - Vector attributes include dominant class, pix_dist (per-class pixel counts), uncertainty (mean per-polygon probability), npix, modal_class, modal_prop, and composite image origin.
  - Probability information provided for vector and 25m raster; not provided for 1km products.
- Documentation and provenance:
  - Full metadata accompanying polygons; DOIs assigned to all products (see citing information).
  - Appendix literature provides class definitions and mapping details.

## Access and licensing
- Data access:
  - 1km raster products available via the CEH Environmental Information Platform (EIP).
  - Full vector and 25m raster products available under licence on request from CEH.
- Licensing and fees:
  - Licence fees may apply; some uses may require formal licensing.
  - Online application process available for licensing or access; contact spatialdata@ceh.ac.uk for details.
- Citing and DOIs:
  - Each product has a DOI for precise citation (GB vector, GB 25m, GB 1km percentage and dominant classes, aggregate products; NI equivalents).
  - Guidance provided on including DOIs in publications and references.

## Metadata and provenance
- Metadata richness:
  - Each vector polygon includes dominant class, per-class pixel counts, uncertainty, and related statistics.
  - Pixel-level probabilities are summarized per polygon for at least the dominant class.
- Provenance traceability:
  - Information about processing, data sources, and composite image specifics retained where possible.
  - Composite image metadata and historical context documented to support reproducibility.

## Methodology and data quality
- Classification approach:
  - New Random Forest classifier (versus previous Maximum Likelihood), handling multi-model training data without spectrally defined sub-classes.
- Training data and ancillary information:
  - Stable training areas constructed from 2000 and 2007 classifications; coastal and difficult areas supplemented manually in initial sets.
  - Ancillary data (e.g., slope, distance to rivers) used as part of the input data rather than post-classification rules.
- Spatial framework:
  - No segmentation-based spatial framework in LCM2015; per-pixel classification improves consistency and aids change mapping.
- Output and uncertainty:
  - Per-polygon mean probability provided; uncertainty quantified and linked to the classification.
  - No spectral sub-classes used; caution for users who historically relied on sub-class distinctions.
- Notes on class mappings:
  - Montane and Rough grassland classes removed to align with spectral data and change-mapping suitability.
  - Mixed woodland handled by pixel-level labeling with polygon-level modal_class, potentially affecting some woodland classifications.
- Data consistency and limitations:
  - LCM2015 is designed for stability and repeatability but differences from prior LCM products mean script compatibility should be verified.

## Data management and updates
- Version history:
  - Version 1.0: Original release.
  - Version 1.1: Publication year correction in Tables 4 and 5.
  - Version 1.2: Updated vector attribute 'composite' in Table 2; vector and raster outputs refined.
- DOIs and citation:
  - Data sets published with DOIs to facilitate reproducible citation and usage tracking.
- Practical usage notes:
  - Users should verify data version and corresponding methodological notes before applying scripts or integrating with other datasets.

## Citing and references
- DOIs provided for all products (GB NI distinctions) to support repeatable methodology and usage tracking.
- Key references for background and methodology include:
  - Jackson (2000) on Broad Habitat definitions.
  - Morton et al. (2011) on LCM2007 methodology and framework.

## Contact and further information
- CEH contact: spatialdata@ceh.ac.uk
- CEH pages:
  - Land Cover Map 2015 information
  - CEH Environmental Information Platform (EIP) access
- Additional information and data papers forthcoming to supplement this documentation.