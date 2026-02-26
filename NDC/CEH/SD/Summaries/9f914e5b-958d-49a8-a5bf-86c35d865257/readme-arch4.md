# Forest structure, composition, and bird counts in windblown and control sites in Kielder Forest, Northumberland, UK, May-July 2022

- Purpose and scope
  - Comparative study of forest structure, plant communities, and bird counts between windblown and control sites in Kielder Forest, conducted May–July 2022.
  - Data shared across multiple datasets to support analyses of ecological responses to windblown disturbance and habitat change.

- Study design and context
  - Paired windblown–control sites with data collected on the same transects and points to enable direct comparisons.
  - Data sources include bird surveys, timber and plant inventories, and environmental context derived from geographic buffers and forest estate subcompartments.

- Data collection methods
  - Bird point counts
    - Conducted at paired sites (windblown vs control) in May–June 2022; 2 or 4 points per site, each visited twice.
    - At each point: 5-minute observation period; all birds seen/heard recorded and assigned to five distance bands (0–10, 10–20, 20–30, 30–40, 40–50 m).
    - Counts performed between 6:00 and 10:30 am; coordinates captured (GPS) and later reported in multiple coordinate formats.
  - Timber and plant surveys
    - 100-m transects per site with three 10×10-m plots and two 2×2-m quadrats along each transect (positions at 0–10, 50–60, 90–100 m).
    - Measurements include fallen trees, DBH (diameter at breast height), tree species, and live/dead status; plants identified to species level within quadrats; Braun-Blanquet cover scales estimated for grasses, shrubs, ferns, mosses, fungi, and lichens.
  - Environmental characterization
    - 100-, 200-, and 400-m buffers around survey sites created in QGIS to extract forest estate subcompartment data (England 2019) for main tree species, estimated cover, and relational links to subcompartment data.
    - Reference dataset: National Forest Estate Subcompartments England 2019 (with a provided data link).

- Data files and contents
  - BirdCounts-Kielder.csv
    - Per-species counts by site, point, visit, and five distance bands; includes SiteID (windblown vs control segmentation), PointNumber, Type, coordinates, Date, Visit, and band-specific counts.
  - Coordinates-Sites-Birds.csv
    - Coordinates for bird point counts; fields include SiteID, Type, original coordinates, ODS reference, converted X/Y and Lat/Long, Date, Visit.
  - Kielder-FallenTimberTransect.csv
    - Fallen timber data along 100-m transects; per-tree records with SiteID, Date, coordinates, species, standing/snapped status, and diameter measurements (three measurements for volume estimation).
  - Kielder-Trees10x10Plots.csv
    - Tree data within three 10×10-m plots per site; PlotID, date, side, coordinates, species, and DBH-related measurements.
  - Kielder-Plants2x2Quadrats.csv
    - Vascular plant data within three 2×2-m quadrats per site; species, Braun-Blanquet cover scores for grasses, shrubs, ferns, mosses, fungi, and lichens.
  - Coordinates-Sites-PlotsTimber.csv
    - Coordinates for 10×10-m plots and 2×2-m quadrats; includes location references, ODS, and converted coordinates (X/Y, Lat/Long).
  - Coordinates-Sites-Total.csv
    - Combined coordinates for 10×10-m plots, 2×2-m quadrats, and bird points; used for buffer analyses; notes that some data points share locations.
  - KielderBuffer-100mTotal-Subcompartments.csv, KielderBuffer-200mTotal-Subcompartments.csv, KielderBuffer-400mTotal-Subcompartments.csv
    - Environmental characteristics by site derived from NF Subcompartments England 2019 within 100-, 200-, and 400-m buffers; first nine columns include SiteID, Type, original coordinates, ODS, converted coordinates, Lat/Long; remaining columns come from the subcompartments dataset.
  - Shapefiles and related files
    - Buffers around data points:
      - Kielder-100mBufferPoints-Birds.* (points around bird counts)
      - Kielder-200mBufferPoints-Birds.* and Kielder-400mBufferPoints-Birds.* (larger buffers)
      - Kielder-100mBufferPoints-Timber.* (buffers around plots/quadrats)
      - Kielder-200mBufferPoints-Timber.* and Kielder-400mBufferPoints-Timber.* 
    - Each set includes shapefile components (dbf, shp, shx, prj) for GIS analyses.

- Geospatial references and data quality
  - Coordinates provided in British National Grid (OSGB36) with conversions to WGS84 (Lat/Long) for broad compatibility.
  - Original coordinates and grid references (ODS) retained alongside converted coordinates to support traceability and reproducibility.
  - Buffers and subcompartment data enable context-driven analyses of habitat features around survey points and plots.

- Data provenance and usage notes
  - Results of bird and plot surveys are reported in associated datasets beyond those listed here; this collection focuses on raw counts, coordinates, and environmental context.
  - Data sources include field observations, GPS measurements, NF Subcompartments England 2019, and publicly available data portal references (e.g., data.gov.uk NF subcompartments dataset).
  - The data structure is designed to support cross-site, cross-dataset analyses of disturbance (windblown) versus undisturbed (control) forest responses across multiple spatial scales.

- Relevance for data strategy and governance (Data Leaders perspective)
  - Demonstrates an integrated data system: field data, geospatial processing, and environmental context are distributed across clearly labeled files with explicit coordinate systems and metadata.
  - Supports co-ownership and iterative use: multiple datasets can be linked via SiteID, PlotID, and consistent coordinate references to address user needs across policy, conservation, and research workflows.
  - Highlights data accessibility and standards: standardized file formats (CSV, shapefiles), explicit metadata on coordinates, dates, and species, and linkages to external authoritative datasets.
  - Enables scalable analysis across buffers and subcompartments, facilitating spatially explicit data governance and replication for future monitoring programs.

- Useful references and resources
  - National Forest Estate Subcompartments England 2019 dataset (linked in the environment section for buffer-derived attributes).
  - Tools used for geospatial conversions and buffer analyses include QGIS (buffers and intersections) and Grid Reference Finder Batch Convert utility for coordinate conversions.
  - Public data source for NF subcompartments: data.gov.uk dataset link provided in the dataset descriptions.