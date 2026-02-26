# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presents the UK Land Cover Map 2007 (LCM2007) as a first continuous parcel-based (polygon) national land cover dataset aligned to Broad Habitats, intended to support environmental monitoring, biodiversity policy, landscape planning, and catchment management.
  - Builds on earlier CEH maps (LCMGB/Land Cover Map of Great Britain 1990 and LCM2000) with improved spatial precision and a framework designed for future change detection and policy evaluation.
  - Delivers UK-wide continuous vector coverage with enhanced data integration potential and a standard spatial framework for monitoring across England, Scotland, Wales, and Northern Ireland.

- What LCM2007 is and how it supports monitoring
  - Parcel-based land cover map with 23 LCM2007 classes, aligned to Broad Habitat groupings (17 terrestrial Broad Habitats mapped).
  - Produces multiple data products:
    - Vector parcels with attributes including area, source images, Broad Habitat, and detailed processing history (KBE history, ProbList, core pixels, etc.).
    - 25 m raster with 23 classes.
    - 1 km raster products providing either percentage cover or dominant class per grid cell.
  - Spatial framework built from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector), enabling consistent boundaries and easier integration with other datasets.
  - Supports monitoring at multiple scales and enables habitat extent, distribution, connectivity, and trend analyses for biodiversity and ecosystem service policy.

- Data architecture and governance
  - Spatial units: nearly 9–10 million land parcels across Great Britain and Northern Ireland; minimum mapping unit of 0.5 ha; minimum feature width of 20 m.
  - Rich metadata and a documented processing lineage for each parcel (including KBE history and probability rankings of spectral classes).
  - Knowledge-Based Enhancements (KBEs): seven automated rules applied post-classification to improve thematic accuracy (contextual data such as urban proximity, soils, elevation, coastal proximity, boundary features), with a knowledge-base for management of rules.
  - Data provenance and validation support: training data from ground references; core pixels used for classification robustness; parcel-level metadata enables user-specific quality checks.

- Data sources and processing workflow
  - Imagery: multi-temporal composites from Landsat-TM5, IRS-LISS3, SPOT-4/5; backup imagery from AWIFS; typical 20–30 m resolution; seasonal timing chosen to capture phenology.
  - External datasets: OS MasterMap topography, agricultural boundaries; DEM (NextMap Britain) and soils (NSRI Soilscapes); Countryside Survey (CS) Broad Habitat data for cross-comparison; additional ground reference data for training/validation.
  - Classification approach: parcel-based supervised maximum likelihood classification across 37 composites and 21 single-date images; training areas derived from ground truth with iterative refinement.
  - Post-classification refinements: seven KBEs applied in sequence to adjust classifications using contextual and ancillary data (e.g., urban context, proximity to coast, terrain, soils); aimed at reflecting Broad Habitat associations more realistically.
  - Quality assurance: pre-processing chain (cloud masking, atmospheric/topographic correction, geo-registration), image segmentation to create a segment-based vector framework, and extensive validation.

- Accuracy, validation, and interpretation
  - Validation: 9,127 ground reference points used for accuracy assessment.
  - Overall accuracy: about 83% across classes; however, class-specific accuracies vary widely due to spectral variability, MMU differences, and space-for-time effects.
  - Key comparatives with Countryside Survey (CS) 2007:
    - LCM2007 shows strong correspondence for some broad habitats and at aggregated levels, but notable discrepancies for arable, improved grassland, neutral grassland, and montane/coastal habitats.
    - Fen, Marsh and Swamp shows substantial differences due to complexities in spectral signatures and small patch sizes; CS often records fen areas as rough grassland or acid grassland in LCM2007 comparisons.
    - Differences arise from spatial structure (vector vs. CS parcels), MMU, and interpretive differences; spectral confusion and temporal mismatch between imagery years contribute to variability.
  - Change detection caveats: substantial methodological differences among LCM1990, LCM2000, and LCM2007 make direct change detection challenging; recommended approaches include using aggregated classes, focusing on consistently mapped classes, or reorganising prior CEH maps into a common spatial framework to enable reliable change assessment.

- Data products, access, and licensing
  - 1 km raster data sets available via the CEH Information Gateway.
  - Full vector product and 25 m raster products available under licence on request from CEH (licence fees may apply).
  - The vector product provides detailed parcel-level metadata, whereas the 25 m raster offers similar land cover resolution without additional polygon metadata.

- Practical implications for monitoring frameworks
  - Provides a scientifically robust, policy-relevant base for multi-tier habitat monitoring and evidence-based decision making.
  - Enables landscape-scale monitoring of habitat extent, distribution, and connectivity across the UK, informing biodiversity policy, Natura targets, and ecosystem service assessments.
  - The continuous UK vector framework reduces boundary inconsistencies and enhances temporal/spatial comparability for future monitoring and trend analysis.
  - Supports integration with other datasets (climate, hydrology, soils, ecology) to inform policy in a consistent UK-wide frame, while allowing country-level distinctions.

- Beginning, middle, and end takeaways (as context for monitoring framework authors)
  - Beginning: LCM2007 introduces the first UK-wide continuous parcel-based land cover map aligned with Broad Habitats, using a generalised but interoperable spatial framework to improve policy-relevant monitoring.
  - Middle: details the data sources, processing workflow (pre-processing, segmentation, classification, KBEs), validation results, and the resulting data products; highlights the innovations in spatial framework and knowledge-based enhancements for improved thematic accuracy and reusability for change detection.
  - End: discusses how LCM2007 compares with Countryside Survey, outlines data access and licensing, and presents LCM2007 as a robust environmental health monitoring tool to inform policy and guide future national monitoring efforts, while acknowledging limitations and areas for methodological improvement.