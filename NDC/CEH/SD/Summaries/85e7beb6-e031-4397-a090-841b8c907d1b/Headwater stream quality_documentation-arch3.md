# Headwater stream quality (Countryside Survey)

- Purpose and scope
  - Assess headwater stream quality in Great Britain using macroinvertebrate indicators (BMWP) and model-based expectations (RIVPACS).
  - Two survey years (1998 and 2007) across 478 headwater sites downstream of source locations.
  - Outputs include a 1 km raster map of water-quality measures and a modeled relationship between stream quality and landscape/stream characteristics.

- Experimental design and sampling regime
  - Standardised macroinvertebrate sampling: 3 minutes of active sampling plus 1 minute hand search per site, over 5–15 m of stream length where possible.
  - Use of a Freshwater Biological Association pond net; samples returned to CEH for sorting/identification.
  - Supplemental field measurements (width, depth, substrate) required for RIVPACS.
  - BMWP scores calculated; RIVPACS used to derive expected macroinvertebrate communities.
  - Sites chosen in headwater streams (Strahler order 1–3) and aligned with 1:50,000 mapping.

- Data products and indicators
  - Observed vs. expected BMWP (Observed BWMP / Expected BWMP) as the primary water-quality measure.
  - Data pooled across 1998 and 2007 to model relationships with catchment/stream characteristics.
  - National-scale application: predictions extended to 1 km grid squares; outputs presented as 1 km raster layers.
  - Excludes grid squares without Strahler order 1–3 headwater streams.

- Analytical methods
  - Boosted Regression Tree modeling to relate observed BWMP to predictor variables.
  - Predictors include: 
    - % arable land, % improved grassland, % urban within 1 km (LCM)
    - % woody cover along the stream within 1 km
    - Slope (within 1 km around the site)
    - Altitude
    - Strahler stream order (1, 2, or 3)
    - Easting and Northing
    - Survey year
  - Model training/validation: split sample; extrapolate to unmonitored grid squares.
  - Output: spatially explicit water-quality measure per headwater stream.

- Data collection, processing, and quality assurance
  - Field and lab processing to record species counts, BMWP taxa, and RIVPACS status; harmonisation to a common modern taxonomy.
  - Standardisation to derive a mutually exclusive taxon list for species richness calculations.
  - QA following Defra/NERC Joint Codes of Practice; detailed QA reports and methodological references available.

- Spatial reference and data attributes
  - Coordinate system: OSGB 1936 / British National Grid (EPSG: 27700).
  - Data attribute: Value = Observed BWMP score divided by the Expected BWMP score.

- Methods and references
  - Sampling and protocol details described in Murphy & Weatherby (2008); field manual for 2007 survey in Murphy et al. (2008/2007).
  - BMWP foundational method (Armitage et al., 1983); RIVPACS framework (Dunbar et al., 2010; Bunce et al., 2007).
  - Modelling and scale considerations discussed in Norton et al. (2016); related landscape classification and land-cover data (Morton et al., 2011).

- Data governance, openness, and dissemination (monitoring framework considerations)
  - Data collection, processing, and sharing follow established QA practices; datasets are prepared for public-facing outputs (e.g., raster maps and model results) with clear provenance.
  - Emphasis on reproducibility through documented protocols, standard taxonomic harmonisation, and transparent modelling steps.