# Countryside Survey: Ash tree distribution in areas <5ha,  2007

- Overview
  - Provides estimates of ash trees for Great Britain in broadleaved woodland areas less than 5 hectares, based on Countryside Survey (CS) 2007 data.
  - File: CS07_ashtree_areas; part of Countryside Survey data curated by NERC - CEH.

- Data contents and structure
  - Columns:
    - Gridcode: Code for the 1km square band interval (1-7).
    - Ha_per_km: Estimate of hectares of ash per km square, expressed in 7 bands: 0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1, 1-5, >5 (text).
  - Resolution: 1 km.
  - Extent and projection: Great Britain; British National Grid (OSGB1936), Transverse Mercator.
  - Purpose: Estimates reflect ash presence specifically in 2007 within areas <5 ha, aligned with standard Countryside Survey outputs.
  - Geographic scope: Excludes larger woodlands to avoid duplicating analyses with the Forestry Commission; focuses on areas where ash is present in 2007.

- Associated datasets
  - ITE Land Classification (1990) with 32 land classes.
  - Land Cover Map 2007 (1 km raster).
  - Countryside Survey outputs (general CS data and results).

- Methodology and how estimates are derived
  - CS uses stratified random sampling of 1 km squares across GB, based on major ecological gradients (soils, geology, climate).
  - In each 1 km square:
    - Habitats are mapped and dominant species recorded by percent cover categories (e.g., <10%, 10-25%, 25-50%, 50-75%, 75-95%, 95-100%).
  - For ash in 2007:
    - Uses mean area of ash woodland within a 1 km square by land class.
    - Multiplies by the area of each land class and sums across land classes to produce national ash area estimates.
  - Land classification and weighting:
    - Land classification used: 1990 ITE Land Classification (32 classes).
    - Means per land class scaled to percent of 1 km by weighting with the proportion of Broadleaved Woodland in each 1 km square according to Land Cover Map 2007.

- Outputs and usage
  - Enables national-scale assessment of ash distribution by integrating CS observations with land classification and land cover data.
  - Data quality and storage: part of the CS data suite; intended to be stored and accessible via appropriate data portals (aligned with CS data practices).

- Further reading and references
  - Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013). Maskell et al., CEH.
  - CS Sampling Strategy documentation and updates (Barr 1998; Wood 2011).
  - ITE Merlewood Land Classification of GB (Bunce et al., 1996).
  - Countryside Survey UK Results from 2007 (Carey et al., 2008).
  - LCM2007 Final Report and related CS outputs.