# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - First continuous parcel-based (polygon) UK land cover map (LCM2007) with associated raster products.
  - Provides stock estimates and distributions of Broad Habitat (BH) classes across the UK, GB, and its constituent countries.
  - Aims to support biodiversity monitoring, landscape planning, ecosystem services, and policy development; designed for integration with other national datasets.

- Data sources and spatial framework
  - Spatial framework derived from detailed national cartography: OS MasterMap (GB) and NI LPS data.
  - Parcel-based vector framework built by merging generalized cartography with image segments and additional boundaries to delineate land parcels.
  - Minimum mapping unit of 0.5 ha (MMU); features below MMU dissolved into surrounding parcels.

- Imagery and pre-processing
  - Primary sensors: Landsat TM/ETM+, SPOT-4/5 (20–30 m), AWIFS (60 m) as backup; LISS-3 (23.5 m) included.
  - 73 images processed; 34 multi-date summer–winter composites produced; 91% UK mapped from composites; 9% from single-date imagery; 0.5% manually hole-filled.
  - Pre-processing includes cloud masking, atmospheric/topographic correction, and multi-date compositing with rigorous processing logs for traceability.

- Image processing, segmentation and classification
  - All 60 composite images segmented; results integrated with generalized cartography to form UK-wide parcel-based framework.
  - Supervised parcel-based maximum likelihood classification into 23 LCM2007 land cover classes, linked to 17 Broad Habitats; 10 aggregates used for 1 km rasters and certain analyses.
  - Training data from ground references and Countryside Survey data; iterative refinement and manual edits for rare/topographic classes.
  - Knowledge-Based Enhancements (KBEs): seven KBEs applied post-classification to resolve spectral confusion and improve thematic resolution (affecting about 20% of parcels). Examples include altitude-based adjustments and soil-context typing; KBEs are recorded in vector attributes.

- Outputs and data products
  - Vector product: 23 LCM2007 classes, plus 17 Broad Habitats; 10 attribute fields documenting processing steps, KBE history, and probabilities.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summary formats per class — (A) percentage cover per 1 km pixel and (B) dominant class per 1 km pixel.
  - Data richness: extensive metadata and a ProbList of the five closest spectral matches for each parcel to support user-driven validation.

- Key figures
  - LCM2007 maps 23 land cover classes, aggregating to 17 Broad Habitats.
  - Overall accuracy: 83% (based on ground-reference validation); class-level accuracy varies, with some grassland, bog and montane classes showing lower accuracies due to spectral ambiguity and resolution limits.
  - Ground truth: 9,127 reference points collected 2006–2008 for training/validation.

- Comparison with Countryside Survey (CS)
  - CS provides 2007 field-based estimates; LCM2007 offers wall-to-wall UK coverage.
  - Grassland and arable categories show notable differences due to spectral variability, MMU differences, and how boundaries/linear features are represented.
  - Broad Habitat Associations (BHA) rules added to interpret one-to-many grassland correspondences between CS and LCM2007, improving interpretability of correspondences at BH and aggregate levels.
  - Fen, Marsh and Swamp exhibits large discrepancies; CS often records mosaic habitats that are difficult to classify spectrally; LCM2007 tends to reallocate to Rough Grassland or other habitats.
  - Overall: LCM2007 shows high correspondence with CS arable/horticulture in 1 km squares but higher CS-derived agricultural extents than LCM2007 in aggregated broad habitats; differences are attributed to mapping philosophies, temporal image ranges, and MMU.

- UK-wide and country-level distribution (examples)
  - Over 50% of the UK comprises intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up areas.
  - Woodland ~12% UK total (broadleaved and coniferous), with Scotland hosting a larger share of coniferous woodland and montane habitats.
  - Scotland exhibits more semi-natural areas (montane habitats, mountain heath, etc.); England tends toward higher intensive land use; Northern Ireland and Wales show similar trends with regional variations.

- Access, licensing and data availability
  - 1 km raster data accessible via the CEH Information Gateway.
  - Full vector and 25 m raster products available on request under license; licensing fees may apply for some users/applications.
  - Data formats include: vector (land parcels with attributes) and 25 m raster (23 classes); 1 km rasters provide aggregated summaries.

- Applications and use cases
  - Habitat monitoring, biodiversity policy support, landscape planning, ecosystem services assessment, carbon accounting, water and catchment studies, and integration with other environmental datasets.
  - Establishes a consistent UK-wide frame of reference for policy analysis and cross-country comparisons.
  - Provides a foundation for change detection and monitoring over time, with a robust spatial structure to facilitate future mapping and monitoring.

- Validation, quality assurance and bespoke validation
  - Bespoke validation framework emphasizes “fit for purpose” assessment tailored to end use.
  - Parcel-level metadata enables users to audit KBE history and Top-5 spectral probabilities; encourages user validation using high-resolution imagery (e.g., Google Earth) as an informal Bayesian check.
  - Producers and users should apply their own validation strategy, recognizing the uncertainties inherent in spectral classification and complex habitat mosaics.

- Change detection and methodological considerations
  - LCM2007 introduces a new spatial structure based on real-world units, improving comparability with other national products and enabling more reliable change detection.
  - Direct cross-comparison with earlier CEH maps (LCM1990, LCM2000) is complex due to differences in spatial structure, scope, and classification schemes; recommended approaches include focusing on aggregated classes or a common BH framework for comparison.

- Key takeaways for data support and use
  - LCM2007 provides a robust, census-scale land cover map with detailed parcel-level metadata and knowledge-based enhancements to support standardized analysis and policy needs.
  - The combination of national cartographic-derived spatial structure and multi-date remote sensing improves both spatial and thematic consistency, while acknowledging residual uncertainties in uplands, grasslands, and mosaic habitats.
  - The dataset is designed to be reused and integrated with other data sources for comprehensive landscape and policy analyses across the UK.

- Implications for data use and governance
  - Encourages integration with European datasets (e.g., Corine) and national biodiversity monitoring programs.
  - Supports a multi-tiered approach to habitat monitoring, combining EO data with field surveys, LiDAR, and sub-surface/climate information for comprehensive decision-making.
  - Ongoing opportunities exist to refine grassland classifications and coastal/bathymetric distinctions as part of future monitoring initiatives.