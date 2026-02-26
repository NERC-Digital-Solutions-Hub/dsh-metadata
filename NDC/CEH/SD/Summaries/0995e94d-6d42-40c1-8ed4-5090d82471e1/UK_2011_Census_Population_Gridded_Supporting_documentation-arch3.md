# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

- Overview
  - Produces a 1 km x 1 km gridded population dataset for the UK by combining 2011 Census Output Area (OA) population with the 2015 Land Cover Map (LCM) to allocate population across a uniform grid.
  - Generates both residential and workday population estimates to support environmental health monitoring and policy evaluation.

- Data sources and access
  - Census 2011 OA population data (England & Wales, Northern Ireland, Scotland) sourced from the Office for National Statistics (ONS).
  - Land Cover Map 2015 (vector) data obtained from CEH.
  - OA geography extents for England & Wales, Northern Ireland, and Scotland.
  - Citation: Reis et al. (2017), UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. DOI provided.

- Experimental design
  - Population data include residential and workday populations for the UK.
  - Aims to produce a spatially homogeneous gridded representation at 1 km resolution, using OA populations distributed onto grid cells based on urban/suburban land use classes from LCM 2015.
  - Coordinate reference: British National Grid (OSGB36); final grid clipping to 1 km × 1 km (OSGB63).

- Collection methods
  - Census 2011 OA population data downloaded as CSV files.
  - LCM 2015 vector data obtained from CEH.
  - OA extent/geography data collected for England & Wales, Northern Ireland, and Scotland.

- Data processing workflow
  - Step 1: Aggregate Census 2011 OA population data to OA geography (matching OA zone codes) to produce OA-level population CSV and shapefiles.
  - Step 2: Extract Urban and Suburban land use classes from LCM 2015 (PARCEL_ID, BH, BHSUB) (vector shapefile output).
  - Step 3: Clip land use polygons to OA geographies, compute clipped polygon areas, and store area shares (CSV and shapefile output).
  - Step 4: Merge land use polygons with OA population, distribute population according to relative area shares within each OA, across land-use categories and subsequent 1 km grid cells.
  - Step 5: Apply equal weight to all land-use types, project population to 1 km grid, and scale to maintain the total Census 2011 UK population. Output final shapefile and ASCII raster with grid_ID, row, column, and population values.

- Calibration and validation
  - Recognizes inevitable inconsistencies from clipping and mismatches between administrative boundaries and land use polygons, plus land use data being from 2015 while census data are from 2011.
  - Overall discrepancy between total Census 2011 population and the gridded total is 0.47%.
  - A scaling factor is computed to align the gridded totals with the official Census total (63,185,612) and applied before rounding.
  - Final residential and workday totals align with Census 2011 within 0.0012% and 0.0005%, respectively.

- Data structure and outputs
  - Outputs are ASCII Grid (*.asc) files for residential and workday populations.
  - Each record includes a unique grid reference ID, grid row and column, and population (INTEGER).

- Quality control and reproducibility
  - Visual inspection at each processing step, plus summary statistics and aggregations to verify consistency with Census totals.
  - The FME workflow is documented and annotated to ensure transparency and reproducibility of the data processing steps.
  - Outputs include both shapefiles and ASCII rasters for traceability.

- Data governance and sharing considerations
  - Uses open data sources (ONS, CEH LCM) with a transparent, step-by-step processing pipeline.
  - Processing leverages reproducible software tools (FME and ArcGIS) and provides documentation to support auditability.

- Relevance to monitoring frameworks
  - Provides a reproducible, high-resolution, spatially explicit population metric suitable for environmental health monitoring and policy evaluation.
  - Demonstrates handling of data gaps and metadata considerations through explicit calibration, validation, and documentation.
  - Highlights practical governance aspects: data provenance, quality assurance, and reproducibility in distributing population data across land-use categories.