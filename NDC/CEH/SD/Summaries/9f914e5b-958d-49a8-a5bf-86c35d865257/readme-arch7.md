# Forest structure, composition, and bird counts in windblown and control sites in Kielder Forest, Northumberland, UK, May-July 2022

## Overview
- Geospatially rich, multi-taxa field study in Kielder Forest, UK, conducted May–July 2022.
- Paired windblown and control sites to compare forest structure, plant communities, and bird occurrences.
- Data products include bird counts, timber and plant surveys, transect and plot coordinates, and environmental context through buffer analyses.

## Data and data files (formats and contents)
- BirdCounts-Kielder.csv
  - Compositional table of bird counts by site pair, bird species, point count, visit, and five distance bands (0–10m, 10–20m, 20–30m, 30–40m, 40–50m).
  - Key fields: SiteID (pair and site type), PointNumber, Type (windblown/control), X.or/Y.or, ODS, X/Y/Lat/Long, Date, HourStart, Visit, Species (scientific/common), Band1–Band5.
  - Note: Results of surveys are stored in associated datasets; this file contains counts and coordinates.

- Coordinates-Sites-Birds.csv
  - Coordinates for bird point counts; includes SiteID, Type, X.or/Y.or, ODS, X/Y/Lat/Long, Date, HourStart, Visit, Comments, Species (names), Band1–Band5.
  - Purpose: precise geolocations for bird counts, with multiple coordinate representations and reference systems.

- Coordinates-Sites-PlotsTimber.csv
  - Coordinates for 10x10 m plots and 2x2 m quadrats used for timber and plant surveys; includes SiteID, PlotID, Date, Type, Side, GPS coordinates (X.or/Y.or, ODS, X/Y/Lat/Long).
  - Provides spatial placement (start/middle/end positions along transects where applicable).

- Kielder-Trees10x10Plots.csv
  - Tree inventory within three 10x10 m plots per site (0–10 m, 50–60 m, 90–100 m along transect).
  - Contains DBH-related measurements and species for trees in each plot.

- Kielder-Plants2x2Quadrats.csv
  - Plant quadrats (2x2 m) per site and transect; includes species, Braun-Blanquet cover scores for grasses, shrubs, ferns, mosses, fungi, lichens.
  - Location and plot/ quadrat identifiers match along transects.

- Coordinates-Sites-Total.csv
  - Combined coordinates for 10x10 m plots, 2x2 m quadrats, and bird point counts; used for buffer definitions.
  - Notes potential coordinate overlaps (some bird counts and plots share locations).

- KielderBuffer-100mTotal-Subcompartments.csv
  - Environmental characteristics within 100 m buffers around survey plots, derived from National Forest Estate Subcompartments England 2019.
  - Columns include SiteID, Type, X.or, Y.or, ODS, X/Y/Lat/Long, plus remaining NF-subcompartment attributes (first 9 columns shown).

- KielderBuffer-200mTotal-Subcompartments.csv
  - Same structure as 100 m but for 200 m buffers.

- KielderBuffer-400mTotal-Subcompartments.csv
  - Same structure as 100 m but for 400 m buffers.

- Shapefiles and related files
  - Kielder-100mBufferPoints-Birds.shp/.dbf/.shx/.prj (and equivalents for Birds at 200 m and 400 m)
  - Kielder-100BufferPoints-Timber.shp/.dbf/.shx/.prj (and equivalents for Timber at 200 m and 400 m)
  - Purpose: ESRI shapefiles defining buffers around bird counts and timber plots (100 m, 200 m, 400 m).
  - Prj files provide coordinate reference systems; data derived from QGIS processing (buffer/intersection).

- Additional notes
  - All original coordinates are in British National Grid (OSGB36). Lat/Long coordinates are provided in WGS84 (EPSG:4326) for broader GIS compatibility.
  - NF Subcompartments dataset referenced: National Forest Estate Subcompartments England 2019 (link provided within the document).

## Methods and spatial processing (GIS-focused)
- Bird surveys
  - Paired windblown and control sites; 2–4 bird point counts per site; each point count lasted 5 minutes.
  - Counts recorded for birds seen/heard, assigned to five distance bands (0–50 m total range covered).
  - Counts conducted between 6:00 and 10:30 am; results are stored separately from coordinates.

- Timber and plant surveys
  - 100 m transects per site with three 10x10 m plots (0–10 m, 50–60 m, 90–100 m) and two 2x2 m quadrats along each transect.
  - Measurements include fallen trees (for volume), DBH measurements of live trees, and plant cover/identity data within quadrats.
  - Plot/Quadrat coordinates denote start (0 m), middle (50 m), and end (100 m) along transects; side (left/right) recorded.

- Environmental characterization (buffers and subcompartments)
  - 100 m, 200 m, and 400 m buffers created around each survey site/plot.
  - Spatial intersection performed with the National Forest Estate Subcompartments England 2019 dataset to extract tree species, estimated cover, and related planning data.
  - Data used to contextualize biological measurements with habitat structure and forest composition.

## How to use these GIS-ready data products
- Map creation
  - Visualize windblown vs. control sites across bird counts, timber plots, and plant quadrats.
  - Display buffers (100/200/400 m) around survey locations and overlay NF subcompartment attributes for habitat context.

- Spatial joins and analyses
  - Join Coordinates-Sites-* files by SiteID to unite bird counts, plot locations, and environmental context.
  - Use KielderBuffer-*-Subcompartments.csv or shapefiles to correlate species abundance, vegetation structure, and timber metrics with forest compartments.

- Multi-scale habitat assessment
  - Compare avifaunal counts and vegetation metrics across buffer scales (100–400 m) to explore proximity effects and habitat context on forest birds and plant communities.

- Data integration
  - Shapefiles provide ready-to-map buffers for GIS software; CSVs provide tabular data for joins and statistical analyses.
  - Ensure coordinate systems are harmonized (OSGB36 origins and WGS84 lat/long for mapping and reporting).

## Key considerations for GIS work
- Coordinate reference systems
  - Original field coordinates are OSGB36; convert to WGS84 for global compatibility where needed; lat/long fields are provided.

- Data scope and completeness
  - Bird survey results are available in associated datasets; this suite provides the spatial scaffolding and descriptive coordinates to support mapping and spatial analyses.

- Data organization
  - Paired design is encoded in SiteID (e.g., 3.1 windblown vs 3.2 control); use this to group comparisons across wind exposure.

- Data sources and provenance
  - NF Subcompartments England 2019 dataset used for environmental context; buffers generated in QGIS; multiple 100/200/400 m scales.

- Usability for policy, clients, and public audiences
  - Map-ready buffers and plots enable clear visualizations of forest structure, species distribution, and bird counts under windblown vs control conditions.