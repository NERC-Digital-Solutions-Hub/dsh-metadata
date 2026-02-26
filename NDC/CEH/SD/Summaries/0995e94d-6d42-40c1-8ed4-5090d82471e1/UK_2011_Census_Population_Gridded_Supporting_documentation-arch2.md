# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

- Purpose and scope
  - Creates a consistent, spatially homogeneous 1 km × 1 km gridded population dataset for the UK by combining 2011 Census Output Areas with Land Cover Map 2015 land-use classes (Urban and Suburban).
  - Produces both residential and workday population distributions to support environmental health and policy monitoring over time.
  - Data product is mapped on the British National Grid framework (OSGB36 base for mapping; final clipping to OSGB63 grid).

- Data sources
  - Census 2011: population data at Output Area (OA) level (UK-wide), provided as CSV; includes separate residential and workday definitions.
  - Land Cover Map (LCM) 2015: vector land-use data, specifically Urban and Suburban classes (BH/BHSUB).
  - OA geography extents for England & Wales, Northern Ireland, and Scotland.
  - Geographic basis: starting with OSGB36; final gridding performed on a 1 km OSGB grid (OSGB63).

- Data collection methods
  - Census data downloaded from the Office for National Statistics (CSV).
  - LCM 2015 vector data obtained from CEH.
  - OA geographic extents sourced for England & Wales, Northern Ireland, and Scotland.

- Data processing and workflow
  - All steps implemented in FME Desktop 2016; visualizations produced with ArcGIS Desktop 10.1.
  - Step 1: Aggregate 2011 OA population data to UK OA geography; generate QC CSV.
  - Step 2: Extract Urban/Suburban land-use polygons from LCM 2015.
  - Step 3: Clip land-use polygons to OA geographies and compute clipped polygon areas; store in CSV.
  - Step 4: Merge clipped land-use parcels with population data; distribute population by relative area weight within each spatial unit (OA and later 1 km grid).
  - Step 5: Apply equal weight to all land-use types; consider potential density differences when aggregating to 1 km grid.
  - Step 6: Clip to 1 km × 1 km grid (OSGB63); compute grid cell populations; scale totals to preserve the total Census 2011 UK population; round results; output as shapefile and ASCII raster (plus CSV).
  - Calibration at each step to maintain consistency with official 2011 totals; address inevitable mismatches due to boundary clipping and land-use data currency (LCM 2015 vs. 2011 census).

- Calibration, quality control and uncertainties
  - Overall discrepancy between total Census 2011 population and gridded total is 0.47%.
  - A final scaling factor is applied to align the gridded totals with the official 2011 UK population (63,185,612).
  - Residential vs. workday totals differ by 0.107%, but the same population figure is used for scaling.
  - Resulting totals are consistent to 0.0012% (residential) and 0.0005% (workday) with the Census totals.
  - Quality control includes visual inspection at each processing step and summary statistics; the FME workflow is documented for reproducibility.

- Outputs and data structure
  - Data outputs provided as:
    - ESRI Shapefile (vector) and ESRI ASCII Raster (raster grid)
    - Additional CSV files for quality control and provenance
  - Data records include:
    - Unique grid reference ID (TEXT), grid row (INTEGER), grid column (INTEGER), and population (INTEGER)
  - Outputs cover both residential and workday populations at 1 km grid resolution.

- Access, reproducibility and citation
  - Dataset citation: Reis, S.; Liska, T.; Steinle, S.; Carnell, E.; Leaver, D.; Roberts, E.; Vieno, M.; Beck, R.; Dragosits, U. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1
  - Workflow is documented; processing steps, inputs, and outputs are described to ensure transparency and reproducibility.
  - Data intended for storage and sharing via appropriate environmental information portals (as per standard practice for monitoring datasets).

- Relevance for environmental monitoring and policy analysis
  - Provides a spatially explicit representation of population exposure potential, enabling analysis of environmental determinants of public health, resource allocation, and policy performance over time.
  - Standardised, transparent methodology supports integration with other environmental datasets and multi-source analyses.
  - Acknowledges limitations due to temporal mismatch between 2011 census data and 2015 land-cover data, plus inevitable boundary- and scale-related uncertainties.