# Social-economic-environmental trade-offs in managing the Land-River-Interface

## Overview
- A data package from a study linking geomorphic changes caused by human alterations to river flows and riparian management with vegetation community changes along the Sutlej and Beas Rivers, India.
- Uses winter-season NDVI trends (Punjab plains) and seasonal Landsat-based landcover classifications over 1989–2020 to quantify vegetated and other land cover, including water.
- Aims to support GIS-based data exploration and map-based visualization for stakeholders.

## Data products (main components)
- River Section, Zone and Test Site delineation (shapefiles) for plains; sections and zones for Upper Beas
- Winter Season average NDVI by section and zone, 1989–2020 (plains only)
- Landcover maps (raster, seasonally 1989–2020) for plains and Upper Beas
- Landcover fractions by section and zone (seasonally) 1989–2020

## Spatial extent and projection
- Beas River: Pong Dam downstream to confluence with Sutlej
- Sutlej River: Bhakra Dam downstream to confluence with Beas
- Upper Beas: above Pong Dam (landcover only)
- Coordinate System: WGS84
- Bounding box: West 74.957, East 77.357, North 32.393, South 30.780

## Delineation and zones
- Sections (plains): S0 near dams (braided planform) and S1–S4/5 in Punjab plains; lower reaches have ~30 km sections
- Upper Beas: 11 sections (S1–S11); S5 and S3A correspond to dam lakes (Pandoh Dam areas)
- Geomorphic Zones: Active Channel (max wetted area 1989–2018), Valley Bottom, Valley Slopes (defined with geomorphon classification using 30 m DSM data reduced to 90 m)
- Boundaries adjusted to include historical river channels where uncertainty exists

## Test sites
- Goindwal-Sahib: Beas, section S4; evidence of channel simplification and straightening
- Zindanpur: Sutlej, section S1; area of significant channel narrowing
- Mau: Sutlej, section S3; gravel/sand bars becoming vegetated

## Winter NDVI by section and zone (1989–2020)
- Landsat 5/7/8 images (winter: Jan–Mar) processed in Google Earth Engine
- Cloud/cloud-free masking applied; water bodies masked using mNDWI
- NDVI averaged per pixel, then zonal statistics computed to annual mean NDVI for each section/zone

## Landcover maps (seasonal, 1989–2020)
- Generated with Gradient Tree Boost (10 trees) in Google Earth Engine
- Spectral inputs: Landsat blue, green, red, NIR, SWIR1, SWIR2
- Seasons: Winter, Pre-monsoon, Monsoon, Post-monsoon
- Training data: manually labeled, invariant locations; separate training sets for plains (below dams) and Upper Beas (above Pong Dam) to account for spectral differences
- Landcover classes include Water, Sand, Vegetated, Densely vegetated, Other Non-vegetated (with pixel-value semantics)

## Landcover fractions by section/zone (seasonal, 1989–2020)
- Computed by counting pixels per landcover class in each section/zone and dividing by total pixels in the area
- Also computed for test sites without sectional/zone differentiation

## Formats and data structure
- ESRI Shapefiles (with mandatory/optional accompanying files)
- CSV spreadsheets (training, NDVI, and landcover summaries)
- GeoTIFF rasters for landcover imagery
- Two geographic sets: Plains (below Bhakra and Pong Dams) and Upper Beas (above Pong Dam)
- Tile-based GeoTIFF naming convention: SEASON_LC_(PLAINS/UPPERBEAS)-(X_START)-(Y_START).tif
- Bands are numbered; a CSV file provides band-name mappings
- Training points and key to band names provided in CSVs

## Quality control
- Landsat quality assessment bands used to select cloud-free imagery
- Processing and analyses conducted by Cranfield University project team
- Spot validation against aerial photography; consumer’s accuracy and error checks performed

## Accessing the data and files
- Example contents include:
  - River Section, Zone and Test Site delineation shapefiles for plains and Upper Beas
  - NDVI CSVs for plains (1989–2020)
  - Training sets and landcover TIFFs for multiple seasons
  - Landcover fraction CSVs and related test-site CSVs
- Contact: Dr Robert Grabowski (r.c.grabowski@cranfield.ac.uk; +44 (0) 1234 758360)

## References
- Friedman, J.H. (2002); Gradient Tree Boosting
- Gorelick et al. (2017); Google Earth Engine
- Jasiewicz & Stepinski (2013); Geomorphons
- Vercruysse & Grabowski (2021a, 2021b); related geomorphology and hydrology studies