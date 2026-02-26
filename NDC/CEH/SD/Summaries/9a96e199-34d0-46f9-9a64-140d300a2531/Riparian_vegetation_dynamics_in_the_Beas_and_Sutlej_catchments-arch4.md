# Social-economic-environmental trade-offs in managing the Land-River-Interface

## Overview
- Data from a study on how human-driven river flow and riparian land management affect geomorphic form and vegetation in the Sutlej and Beas Rivers, India.
- Key outputs quantify vegetation and land cover using winter-season NDVI trends and seasonal Landsat-based landcover classifications over 1989–2020.
- Study areas include plains Beas/Sutlej, upper Beas, and test sites; coordinate system is WGS84.

## Data Assets and Products
- Section, Zone and Test Site delineation
  - Shapefiles defining river sections (plains and upper Beas), geomorphic zones, and designated test sites.
- Winter season NDVI (1989–2020)
  - Spreadsheet by section/zone with mean winter NDVI for each year (plains only).
- Landcover maps (seasonal, 1989–2020)
  - GeoTIFF rasters for winter, pre-monsoon, monsoon, and post-monsoon seasons (plains and upper Beas).
- Landcover fractions by section/zone (seasonal, 1989–2020)
  - Fractional area per landcover class by section/zone (plains; also for test sites).
- Test-site landcover data
  - Separate landcover data for test sites without zone/section differentiation.
- Training data and class definitions
  - Plains and Upper Beas training points with five landcover classes (water, sand, vegetated, densely vegetated, other non-vegetated) and associated metadata (pixel counts, typical locations).
- File formats and structure
  - ESRI Shapefiles, CSV, and GeoTIFF (tiled with season-specific naming conventions).
  - Separate training points for plains vs Upper Beas to address spectral differences.
  - Detailed file listing and naming conventions provided.

## Scope and Spatial Extent
- Beas River: Pong Dam downstream to Sutlej confluence.
- Sutlej River: Bhakra Dam downstream to Beas confluence.
- Upper Beas: Palchan downstream to just upstream of Pong Dam (landcover only).
- Extent coordinates: West 74.957, East 77.357, North 32.393, South 30.780.
- All data are in the WGS84 coordinate system.

## Methods and Processing
- NDVI analysis
  - Landsat 5/7/8 top-of-atmosphere data (1989–2020) processed in Google Earth Engine.
  - Winter season (Jan–Mar); cloud masking; NDVI and mNDWI computed; water pixels excluded (mNDWI > 0.15).
  - Yearly mean NDVI computed per section/zone using zonal statistics.
- Landcover classification
  - Gradient Tree Boosting (10 trees) applied to multi-band Landsat data (blue, green, red, NIR, SWIR1, SWIR2).
  - Seasonal models built for winter, pre-monsoon, monsoon, and post-monsoon.
  - Training data created by manual inspection of invariant-year pixels; separate plains vs Upper Beas datasets.
- Landcover fractions
  - Pixel counts within each section/zone divided by total to yield class fractions (also computed for test sites).

## Quality Control and Validation
- Cloud-free image selection using Landsat QA bands; cloud masking applied in GEE.
- Validation through spot checks against aerial imagery; statistical checks (e.g., consumer’s accuracy) performed by Cranfield University team.

## Formats, Access, and Metadata
- Formats
  - ESRI Shapefiles (with mandatory/optional accompanying files)
  - CSV (tabular data and training metadata)
  - GeoTIFF (landcover rasters)
- Naming conventions
  - Season_LC_PLains/UPPERBEAS_(X_START)-(Y_START).tif (tiled geotiffs)
- Metadata and provenance
  - Documented methods, training data, and references; project SEELARI: NE/S01232X/1.
  - References to key methods: gradient boosting (Friedman, 2002); GEE platform (Gorelick et al., 2017); geomorphon-based analysis (Jasiewicz & Stepinski, 2013).

## Quality and Documentation
- Data rely on satellite-derived spectral information with explicit cloud-filtering and QA processes.
- Ground-truth-like validation through aerial photography comparison and internal quality checks.

## Project Context and Contacts
- Project: SEELARI – Social-economic-environmental trade-offs in managing the Land-River-Interface.
- Principal contact: Dr Robert Grabowski, Cranfield University (r.c.grabowski@cranfield.ac.uk; Tel: +44 (0) 1234 758360).

## Reuse, Applications, and Implications for Data Leaders
- Provides end-to-end data products linking hydrological/geomorphological changes to vegetation dynamics, useful for policy, planning, and river-land management.
- Demonstrates an integrated data system: delineation of study units, multi-temporal NDVI, seasonal landcover mapping, and sector-specific training data.
- Supports data ownership and cross-disciplinary collaboration by offering co-ownership of NDVI and landcover products and clear data governance (formats, provenance, and seasonality).
- Offers a model for managing scattered data assets, ensuring discoverability, metadata clarity, and consistent updates across seasons and years.