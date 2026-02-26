# Social-economic-environmental trade-offs in managing the Land-River-Interface

- Purpose and scope
  - Aims to understand how hydrological and geomorphological changes driven by human alterations to river flows and riparian land management relate to vegetation community changes along the Sutlej and Beas Rivers, India.
  - Uses long-term (1989–2020) winter NDVI trends and seasonal landcover classifications from Landsat data to quantify vegetation and landcover dynamics in plains (Punjab) and upper Beas.

- Data components
  - River Section, Zone and Test Site delineation (shapefiles) for plains and upper Beas.
  - Winter season average NDVI by section and zone (1989–2020) for plains.
  - Landcover maps (raster) by season (winter, pre-monsoon, monsoon, post-monsoon) 1989–2020 for plains and upper Beas.
  - Landcover fractions by section and zone (seasonally) 1989–2020 (plains) plus test-site fractions.

- Spatial extent and coordinate system
  - Beas River: Pong Dam downstream to Sutlej confluence; Sutlej River: Bhakra Dam downstream to confluence with Beas; Upper Beas (landcover only) from Palchan downstream to just upstream of Pong Dam.
  - Coordinate System: WGS84.
  - Study extent bounded by longitudes 74.957–77.357 and latitudes 32.393–30.780.

- Section, zone and test-site delineation
  - Plains: longitudinal sections S0 (below dams; braided) and S1–S4/5 (flatter plains; mostly single-thread); each section ~30 km.
  - Upper Beas: 11 sections (S1–S11); S5 coincides with a dam lake; S3A is part of the Pandoh Dam lake.
  - Geomorphic zones: Active Channel defined by maximum wetted area (1989–2018); Valley Bottom and Valley Slopes delineated using geomorphon classification with DSM data.

- Test sites
  - Goindwal-Sahib (Beas, S4): channel simplification and reduced anabranching.
  - Zindanpur (Sutlej, S1): significant channel narrowing.
  - Mau (Sutlej, S3): gravel/sand bars vegetating.

- Data processing and quality control
  - Winter NDVI (1989–2020): Landsat TOA data (Landsat 5/7/8); cloudy pixels masked; NDVI averaged per year for each section/zone using GEE zonal statistics; water masked using mNDWI threshold (>0.15 water surface excluded from NDVI).
  - Landcover maps: seasonal classification using Gradient Tree Boosting (10 trees) with multispectral bands; training datasets created by manual inspection of invariant landcover features; separate training sets for plains vs Upper Beas due to spectral differences.
  - Landcover fractions: pixel counts per landcover class within each section/zone divided by total pixel counts to derive seasonal fractions; applied similarly to test sites.
  - Quality assurance: cloud-free imagery prioritized via Landsat QA bands; validation against aerial imagery; data verified by project team at Cranfield University.

- Formats and data organization
  - Formats used: ESRI Shapefiles, CSV spreadsheets, GeoTIFF landcover rasters.
  - Two dataset sets: Plains (below Bhakra and Pong Dams) and Upper Beas (above Pong Dam); training points are geographically separated to maintain spectral consistency.
  - File naming conventions: season_LC_(PLAINS/UPPERBEAS)-(X_START)-(Y_START).tif; accompanying CSVs detailing band names and classifications.
  - Key contents by group:
    - River Section, Zone and Test Site delineation (shapefiles)
    - Winter NDVI by section/zone (CSV)
    - Landcover maps (seasonal GeoTIFFs) and training data (CSV)
    - Landcover fractions by section/zone (CSV) and for test sites

- Derived outputs and usage
  - Enables assessment of how river geomorphology and land-water interface management relate to vegetation trends over 30+ years.
  - Supports standardized, exportable datasets for environmental health monitoring and policy performance review over time.
  - Datasets are designed for storage and sharing via appropriate data portals and institutional repositories.

- References
  - Friedman, J.H. (2002); Gorelick et al. (2017); Jasiewicz & Stepinski (2013); Vercruysse & Grabowski (2021a, 2021b).

- Contact
  - Dr Robert Grabowski, Cranfield University; tel: +44 (0) 1234 758360; email: r.c.grabowski@cranfield.ac.uk.