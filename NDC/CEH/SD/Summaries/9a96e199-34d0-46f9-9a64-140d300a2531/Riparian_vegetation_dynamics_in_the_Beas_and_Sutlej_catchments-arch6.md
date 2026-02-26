# Social-economic-environmental trade-offs in managing the Land-River-Interface

- Purpose: A dataset produced to study how human alterations to river flows and riparian land management affect vegetation communities along the Sutlej and Beas Rivers in India. It links geomorphic/ hydrological changes to vegetation dynamics using long-term NDVI and landcover data to support analysis and decision-making.

- Key data products:
  - River Section, Zone and Test Site delineations (shapefiles) for plains (and upper Beas delineations)
  - Winter season average NDVI by section and zone (plains only) for 1989–2020 (CSV)
  - Seasonal landcover maps (rasters) 1989–2020 (plains and upper Beas)
  - Landcover fractions by section and zone (seasonally) 1989–2020 (plains)
  - Test-site specific outputs for focused case studies

- Spatial and temporal coverage:
  - Rivers included: Beas (Pong Dam downstream to confluence with Sutlej), Sutlej (Bhakra Dam downstream to confluence with Beas), and Upper Beas (above Pong Dam; landcover only)
  - Extent: WGS84 coordinates; West 74.957°, East 77.357°, North 32.393°, South 30.780°
  - Time span: 1989–2020
  - Seasons:
    - NDVI: winter season (January–March)
    - Landcover: winter, pre-monsoon, monsoon, post-monsoon

- Section, zone, and test-site framework:
  - Plains sections: S0 (below dams) and S1–S4/5 (Punjab plains); lower plains feature braided vs. single-thread sections
  - Upper Beas: 11 sections (S1–S11), with S5 and S3A linked to dam lakes
  - Geomorphic zones: Active Channel (based on maximum wetted area 1989–2018), Valley Bottom, and Valley Slopes (defined with geomorphon classification and DSM data)
  - Test sites across plains: Goindwal-Sahib (Beas, S4; channel simplification), Zindanpur (S1; channel narrowing on Sutlej), Mau (S3; vegetation on gravel/sand bars)

- Methods and processing highlights:
  - NDVI (1989–2020): Landsat 5/7/8, winter imagery in Google Earth Engine; cloud masking; water masking with mNDWI; yearly mean NDVI per section/zone
  - Landcover mapping (1989–2020): seasonal classification using Gradient Tree Boost (10 trees) with Landsat bands; training data created from manual inspection; separate training sets for plains below dams and above Pong Dam (Beas) to account for spectral differences
  - Landcover classes: Water (including dam lakes), Sand, Vegetated, Densely vegetated, Other non-vegetated
  - Outputs: Seasonal landcover rasters and derived landcover fractions by section/zone (and per test site)

- Data quality and validation:
  - Cloud-free image selection via Landsat QA bands
  - Validation through statistical accuracy measures (e.g., consumer’s accuracy) and spot checks against aerial photography
  - Processing conducted and quality-checked by Cranfield University

- Formats and file structure:
  - Formats: ESRI Shapefiles, CSVs, GeoTIFF rasters
  - Two geographic sets: Plains (below Bhakra/Pong Dams) and Upper Beas (Beas above Pong Dam)
  - Image tiling: SEASON_LC_(PLAINS/UPPERBEAS)-(X_START)-(Y_START).tif
  - Training data and lookup CSVs accompany the rasters to describe band names and classes
  - Example file types included:
    - River Sections, TestSites, Zones shapefiles
    - NDVI_1989_2020.csv and TEST_SITES_NDVI_1989_2020.csv
    - Plains and Upper Beas landcover training sets and multiple seasonal landcover TIFFs
    - Landcover Section and Zone CSVs for plains and upper Beas

- Intended uses and potential outputs for data support:
  - Support analyses of how hydromorphology and riparian management influence vegetation dynamics
  - Enable cross-temporal and cross-scales assessment of land-river interface trade-offs for policy and planning
  - Create data products (dashboards, reports, maps) to aid stakeholders in understanding spatial/seasonal vegetation responses
  - Facilitate integration with other datasets to generalize insights across river systems or to similar environments

- Project context and contacts:
  - Project: SEELARI (NE/S01232X/1) — Social-economic-environmental trade-offs in managing the Land-River-Interface
  - Lead contact: Dr Robert Grabowski (cranfield University)

- References for methods:
  - Friedman, J.H. (2002) stochastic gradient boosting
  - Gorelick et al. (2017) Google Earth Engine
  - Jasiewicz & Stepinski (2013) Geomorphons
  - Vercruysse & Grabowski (2021a, 2021b) related geomorphology and river dynamics work