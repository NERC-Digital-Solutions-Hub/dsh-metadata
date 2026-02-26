# Social-economic-environmental trade-offs in managing the Land-River-Interface

- Purpose: Dataset from a study on how human alterations to river flows and riparian land management affect vegetation communities along the Sutlej and Beas Rivers, India. Produces winter-season NDVI trends and seasonal landcover classifications over ~30 years to analyze geomorphic and ecological dynamics.

- Data components (produced dataset):
  - River Section, Zone and Test Site delineation (shapefiles) for plains; Sections Upper Beas shapefiles (Upper Beas only); Zones shapefiles (plains and Upper Beas); TestSites shapefile (plains)
  - Winter Season average NDVI by section and zone (CSV; 1989–2020; plains only)
  - Landcover maps (raster, seasonal; 1989–2020; plains and Upper Beas)
  - Landcover fractions by section and zone (seasonally; 1989–2020; plains; plus test sites)
  - Training data and class keys for landcover (plains and Upper Beas)
  - Numerous tiled landcover rasters with naming convention indicating season, region (Plains/UpperBeas), and tile coordinates

- Spatial and temporal scope:
  - Beas River: Pong Dam downstream to confluence with Sutlej
  - Sutlej River: Bhakra Dam downstream to confluence with Beas
  - Upper Beas: Palchan downstream to just upstream of Pong Dam (landcover only)
  - Coordinate system: WGS84
  - Extent: roughly 74.957°–77.357° E, 32.393°–30.780° N
  - Time span: 1989–2020 (NDVI, landcover per season; multiple seasonal mosaics)

- Data formats and naming conventions:
  - Shapefiles for delineations (Sections, Zones, TestSites)
  - CSV for NDVI by section/zone; training data references
  - GeoTIFFs for landcover rasters, tiled by season (Winter, Pre-monsoon, Monsoon, Post-monsoon) and region (Plains vs Upper Beas)
  - Training sets provided separately for plains and Upper Beas
  - Naming convention: SEASON_LC_(PLAINS/UPPERBEAS)-(X_START)-(Y_START).tif
  - Band names and class keys provided in CSVs (e.g., WINTER_LC_PLAINS.csv, PREMONSOON_LC_PLAINS.csv, etc.)

- Data provenance and methods:
  - NDVI derived from Landsat 5/7/8 TOA reflectance; cloud masking via Google Earth Engine (GEE) algorithms; NDVI averaged per year within each section/zone
  - Landcover maps produced with Gradient Tree Boosting (10 trees) using bands blue, green, red, NIR, SWIR1, SWIR2; four seasonal classifications across 1989–2020
  - Training data selected through manual inspection of imagery; separate training sets to accommodate differing spectral characteristics below dams vs above Pong Dam
  - Landcover fractions computed by counting landcover-class pixels within each section/zone and normalizing by total pixels

- Quality control and validation:
  - Cloud-free image selection using Landsat QA bands via GEE
  - Validation through spot checks against aerial photography; dataset processing and quality assessment conducted by Cranfield University team
  - Spectral processing and class definitions documented; separation of plains and Upper Beas training data to mitigate spectral differences

- Documentation and metadata:
  - Detailed file listing and structure provided; references to related methodological works (Friedman 2002; Gorelick et al. 2017; Jasiewicz & Stepinski 2013; Vercruysse & Grabowski 2021a, 2021b)
  - Explicit separation of plains vs Upper Beas datasets, with corresponding training data and rasters
  - Training point counts and class values summarized in descriptions for reproducibility

- Access and reuse considerations for Data Stewards:
  - Datasets are organized for update and reuse across river sections and geomorphic zones; clear versioning through seasonal tiling and region-specific datasets
  - Potential for updating with new Landsat data; maintain separation of plains and Upper Beas for spectral consistency
  - Metadata should document scope (Beas and Sutlej rivers, plains/upper Beas), processing steps (GEE NDVI, Gradient Tree Boosting for landcover), and QA procedures
  - Licensing and portal deposition should reflect the study’s provenance and provide guidance on cross-region comparisons due to differing training data

- Practical governance notes:
  - Inherent challenges relevant to data stewardship include aligning user needs with dataset sections/zones, handling large multi-season rasters, and ensuring interoperability across systems due to separate plains and Upper Beas datasets
  - Ensure ongoing data availability by maintaining training sets, class keys, and consistent naming conventions to support reproducibility and discoverability
  - Document any limitations, such as potential spectral differences between regions and temporal gaps, to inform data users and governance policies

- Suggested best practices for future stewardship:
  - Maintain comprehensive metadata capturing data lineage, processing algorithms, season definitions, and spatial extents
  - Use consistent versioning and release notes when updating NDVI or landcover products
  - Ensure clear licensing, citations, and attribution in downstream analyses
  - Provide user guidance for integrating plains and Upper Beas datasets, given their separate training and classification databases