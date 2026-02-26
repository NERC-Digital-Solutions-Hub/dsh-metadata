# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Purpose and scope
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Map products cover 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with associated aggregate classes.
  - Automatic production aims to enable annual updates; no manual corrections were performed this release, but visual checks and formal validation were conducted.
  - Emphasis on helping users understand data production, content, validation, and appropriate use.

- Data products and formats
  - 20m Classified Pixels (GB and NI): RF classification outputs with per-pixel class and a confidence score (0–100).
  - Land Parcels: attributes derived from intersecting 20m pixels with the UKCEH Land Parcel Spatial Framework; includes parcel-level statistics.
    - Key parcel attributes: gid, _hist (histogram of class counts per parcel as tuples), _mode (dominant class), _purity, _conf (mean class membership probability), _stdev, _n (npix).
  - 25m Rasterised Land Parcels: three-band rasters (band 1: _mode, band 2: _conf, band 3: _purity).
  - 1km Raster datasets (summaries at 1km grid):
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Dataset extents: Great Britain and Northern Ireland, with GB and NI coordinate systems defined (British National Grid and Irish Grid as appropriate).
  - Dataset structure is designed to enable cross-year comparison and integration with the UKCEH Land Parcel Spatial Framework.

- Production methodology
  - Bootstrap Training
    - Automated training data derived from historic LCM2015 (and prior) to bootstrap training observations for 2017–2019.
    - Selection of high-purity parcels (≥99% purity) to create spectral training observations.
    - Goal: leverage large historic signals to train the classifier without field campaigns; bootstrap improves with time as maps evolve.
  - Random Forest classification
    - RF classifier trained with balanced sampling: 10,000 samples per class per Classification Scene.
    - Training data drawn from Bootstrap Training sets; classification scenes yield the 20m Classified Pixels product.
    - Production software integrates Weka, PostGIS, and GDAL (open source).
  - Classification Scenes and Context
    - Seasonal Composite Images (TOA reflectance) per season generated from Sentinel-2 via Google Earth Engine (four seasons: winter, spring, summer, autumn).
    - 9 Sentinel-2 bands used to form 46-band GB Classification Scenes when combined with 20m Context Rasters.
    - Context Rasters (20m) provide structural information to reduce spectral confusion (e.g., terrain, proximity to buildings/roads/sea, land/water masks).
    - GB uses 100x100 km tile arrangement for classification; NI uses a single tile covering its landmass.
  - Seasonal and spectral choices
    - Decision to use TOA reflectance rather than surface reflectance (SR) based on assessments during production; SR did not improve classification for these land cover classes.
    - Context rasters include terrain (height, aspect, slope) and proximity masks (urban, coastal, freshwater, road, etc.).
  - Land Parcel Spatial Framework
    - Framework maintained from LCM2015 with minor changes; parcel geometries unchanged, but identifiers (gid) differ from LCM2015.
    - MMU around 0.5 ha; parcels are designed to represent discrete real-world units (fields, parks, urban areas, etc.).
    - The 20m Classified Pixels are summarized into parcels to produce cleaner classification and a stable basis for change detection.
  - Data processing and overlap
    - 74 overlapping GB Classification Scenes classified independently; overlaps resolved by visual inspection to select the best results into the final product.
    - For NI, classification is performed on a single tile per year.

- Validation and accuracy
  - Validation approach
    - UK-scale validation using 22,325 points from GB countryside survey (2019), National Forest Inventory data, IACS data, and bespoke LCM validation points.
    - Points intersected with LCM Land Parcel datasets to assess correspondence.
  - Reported accuracy
    - LCM2017: ~78.6% overall accuracy
    - LCM2018: ~79.6% overall accuracy
    - LCM2019: ~79.4% overall accuracy
  - Notes on validation
    - Validation uses the same point set across products; currency relative to each product varies.
    - Validation points were mapped to UKCEH classes; conversions from other schemes introduce some subjectivity.
    - Approximately 80% correspondence is considered strong for an automatically produced, year-on-year updated national-scale map suite.
  - Validation details
    - Full correspondence tables and Appendix 4 provide confusion matrices, producer’s and user’s accuracies by class.

- Content interpretation and usage guidance
  - 21 UKCEH Land Cover Classes aligned with BAP Broad Habitats and cross-walks to UKCEH Aggregate Classes.
  - Appendix 1 and 2 provide notes on class definitions and their relation to BAP Broad Habitats; some classifications are constrained by spectral detectability and training data limitations.
  - Some classes (e.g., Linear Features) are not individually classified due to narrow width and current spectral limitations; these are represented conceptually within the habitat framework.
  - Color scheme recommendations and class-specific mapping guidance are provided in Appendix 3.

- Data access, metadata, and references
  - Datasets are accompanied by metadata and documentation, with references to foundational work on RF, bootstrap sampling, and UK land cover classifications.
  - Appendix 5 lists the full dataset suite per year and per geography (GB/NI) and indicates dataset names and storage conventions used in production.

- Practical considerations and future plans
  - The production pipeline emphasizes rapid annual updates; manual corrections are deprioritized to maintain automation, with validation guiding quality assessment.
  - The UKCEH aims to refine bootstrap strategies and expand satellite input, including potential future use of alternative optical sources or SAR data to fill seasonal gaps.
  - Plans to maintain consistency with historical LCMs for change detection while continuing to improve detection and accuracy through updated training data and expanded context information.

- Appendices (highlights)
  - Appendix 1: Notes on UKCEH Land Cover Classes and their interpretation relative to BAP Broad Habitats.
  - Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions.
  - Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes.
  - Appendix 4: Validation confusion matrices and accuracy metrics by class.
  - Appendix 5: Full dataset listing for LCM2017, LCM2018, and LCM2019, including GB/NI distinctions and dataset naming.