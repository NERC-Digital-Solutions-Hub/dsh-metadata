# Social-economic-environmental trade-offs in managing the Land-River-Interface

- Purpose: Part of a study to understand how human-induced changes to river flows and riparian land management affect geomorphic form, dynamics, and vegetation communities along the Sutlej and Beas Rivers in India. Uses winter-season NDVI trends and seasonal Landsat-based landcover classifications over a 30-year period (1989–2020) to quantify vegetated and other land cover changes.

- Project context: Project SEELARI (NE/S01232X/1) focused on social-economic-environmental trade-offs in managing the Land-River-Interface. Details and outputs are designed to support monitoring of environmental health and policy-relevant decision making.

- Data components (comprising the dataset):
  - River Section, Zone and Test Site delineation (shapefiles) for plains (and upper Beas)
  - Winter Season average NDVI by section and zone (CSV) 1989–2020 (plains)
  - Landcover maps (raster, seasonal) 1989–2020 (plains and upper Beas)
  - Landcover fractions by section and zone (seasonally) 1989–2020 (plains)

- Spatial extent:
  - Beas River: Pong Dam downstream to confluence with Sutlej
  - Sutlej River: Bhakra Dam downstream to confluence with Beas
  - Upper Beas: Palchan downstream to just upstream of Pong Dam (landcover only)
  - Coordinate System: WGS 1984
  - Study extent defined within specified latitude/longitude bounds

- Section and zone delineation:
  - Lower plains sections: S0 (below dams) distinct braided planform, S1–S4/5 (flatter plains), ~30 km segments
  - Upper Beas: 11 sections (S1–S11); some subsections correspond to dam lakes
  - Geomorphic zones: Active Channel (max wetted area 1989–2018), Valley Bottom, Valley Slopes (geomorphon-based classification using 30 m DSM reduced to 90 m)
  - Boundaries adjusted where uncertain to ensure inclusion of historic river channels

- Test sites (for understanding vegetation response to geomorphic change):
  - Goindwal-Sahib (Beas, S4): channel simplification and straightening
  - Zindanpur (Sutlej, S1): channel narrowing
  - Mau (Sutlej, S3): gravel/sand bars becoming vegetated

- Winter NDVI analysis (1989–2020):
  - Data: Landsat 5/7/8 winter images (Jan–Mar)
  - Processing: Google Earth Engine; cloud masking; exclude water surfaces using mNDWI; compute mean NDVI per year per section/zone via zonal statistics

- Landcover classification and maps:
  - Method: Gradient Tree Boosting (10 trees) on Landsat spectral bands (various channels per sensor)
  - Seasonal analyses: winter, pre-monsoon, monsoon, post-monsoon
  - Training data: manually labeled, invariant-location training points; separate plains and upper Beas training sets to account for spectral differences due to topography
  - Landcover classes: Water (including dam lakes), Active channel/sand bars/banks, Sand, Vegetated (agricultural areas, mid-NDVI), Densely vegetated (forest/high NDVI), Other Non-vegetated (urban/rocks/other soils)
  - Dataset details: pixel-level counts per class used to derive landcover fractions

- Landcover fractions by section/zone:
  - Computation: for each image, count pixels per landcover class, divide by total for area to obtain seasonal fractions
  - Includes fractions for plains (Sutlej and Beas) and Upper Beas; also calculated for test sites without zone/section differentiation

- Quality control and processing:
  - Data sources: Landsat spectral reflectance with QA bands for cloud-free selections
  - Processing and validation: project team at Cranfield University; statistical accuracy checks and spot validation against aerial imagery; error checks at all stages

- Format and organization:
  - Main formats: ESRI Shapefiles, CSV, GeoTIFFs
  - Two primary dataset sets: Plains (below Bhakra and Pong Dams) and Upper Beas
  - File naming and structure: season-specific landcover TIFFs, training sets, and index CSVs; explicit naming conventions to distinguish plains vs. Upper Beas
  - Representative file groups:
    - River Section, Zone and Test Site delineation (Sections.shp, TestSites.shp, Zones.shp; plus Upper Beas variants)
    - NDVI 1989–2020 (SUTLEJ_BEAS_NDVI_1989_2020.csv; TEST_SITES_NDVI_1989_2020.csv)
    - Landcover rasters by season (WINTER_LC_*, PREMONSOON_LC_*, MONSOON_LC_*, POSTMONSOON_LC_*) for PLAINS and UPPERBEAS
    - Training sets and LC band key CSVs (e.g., PLAINS_TrainingSet.csv, WINTER_LC_PLAINS.csv)
    - Landcover fractions (Landcover Section and Zone.csv; Landcover Test Sites.csv; Upper Beas variant)

- Key references:
  - Friedman, J.H. (2002) on stochastic gradient boosting
  - Gorelick et al. (2017) Google Earth Engine platform
  - Jasiewicz & Stepinski (2013) geomorphons
  - Vercruysse & Grabowski (2021a, 2021b) on river planform dynamics and related hydromorphology

- Access and contact:
  - Project lead: Dr Robert Grabowski
  - Email: r.c.grabowski@cranfield.ac.uk; Tel: +44 (0) 1234 758360

- How this supports monitoring frameworks:
  - Provides structured, repeatable measures of geomorphic change and vegetation response across multiple river segments and seasons
  - Enables assessment of trade-offs between land-river interface management and ecological outcomes
  - Emphasizes data provenance, standardized formats, and reproducible processing (GEE workflow, training data separation, QA/validation) to facilitate governance, data sharing, and transparent decision-making