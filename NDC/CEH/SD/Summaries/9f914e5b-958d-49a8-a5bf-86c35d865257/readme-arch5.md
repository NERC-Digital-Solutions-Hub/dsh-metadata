# Forest structure, composition, and bird counts in windblown and control sites in Kielder Forest, Northumberland, UK, May-July 2022

- Study focus: Forest structure, plant communities, and bird counts across paired windblown and control sites in Kielder Forest during May–July 2022.
- Outputs and data types: Multiple data files (CSV and ESRI shapefiles) detailing bird surveys, timber and plant measurements, coordinates, and environmental context derived from national forest data and GIS buffers.
- Authors and contacts: García-Díaz et al. from the University of Aberdeen and collaborators; contact emails provided for data queries.

## Data collected and study design

- Bird surveys
  - Point counts conducted at paired windblown and control sites (2 or 4 points per site; each point counted twice).
  - Observers recorded all birds seen/heard for 5 minutes per point, with birds assigned to five distance bands (0–10 m, 10–20 m, 20–30 m, 30–40 m, 40–50 m).
  - Surveys performed between 6:00 and 10:30 am; two visits per point.
- Timber and vegetation surveys
  - 100-m transects per site with three 10×10 m plots and three 2×2 m quadrats along each transect.
  - Measurements include fallen trees, diameter at breast height (DBH) for trees, and plant cover/species within quadrats.
  - Plots/quadrats positioned at 0–10 m, 50–60 m, and 90–100 m along transects.
- Environmental characterization
  - Surrounding environment characterized using 100 m, 200 m, and 400 m buffers around survey sites.
  - Data extracted from National Forest Estate Subcompartments England 2019 to provide tree species, cover, and related attributes.

## Key datasets and what they contain

- BirdCounts-Kielder.csv
  - Contains species-by-site-by-point-by-visit data.
  - Columns include SiteID, PointNumber, Type (windblown/control), coordinates (X, Y, Lat, Long), Date, Visit, and counts by distance band (Band 1–Band 5).
- Coordinates-Sites-Birds.csv
  - Bird point count coordinates; includes SiteID, Type, coordinates in original GPS format, ODS, converted X/Y/Lat/Long, Date, HourStart, Visit, and comments.
- Kielder-FallenTimberTransect.csv
  - Results of fallen timber along 100 m transects; includes SiteID, Date, Type, transect start coordinates, end coordinates, and three diameter measures for volume estimation; NAs indicate no fallen trees.
- Kielder-Trees10x10Plots.csv
  - Tree data from three 10×10 m plots per site; includes PlotID, date, type, location (X/Y, ODS, Lat/Long), and tree-specific measurements (Species, DBH, standing/leaning status, etc.).
- Kielder-Plants2x2Quadrats.csv
  - Plant species within three 2×2 m quadrats per site; includes Braun-Blanquet cover scores for grasses, shrubs, ferns, mosses, fungi, and lichens; species-level identifications.
- Coordinates-Sites-PlotsTimber.csv
  - Coordinates for 10×10 m plots and 2×2 m quadrats; includes location data and species of trees/plants present.
- Coordinates-Sites-Total.csv
  - Combined coordinates for lower corners of plots/quadrats and bird points; notes that some data share coordinates where bird counts and plots overlapped.
- KielderBuffer-100mTotal-Subcompartments.csv, KielderBuffer-200mTotal-Subcompartments.csv, KielderBuffer-400mTotal-Subcompartments.csv
  - Environmental characteristics by survey site usingNational Forest Estate Subcompartments England 2019, at 100 m, 200 m, and 400 m buffers respectively; first nine columns include SiteID, Type, original coordinates, ODS, converted coordinates/lat/long; remaining columns come from the Subcompartments dataset.
- Shapefiles for buffers
  - Kielder-100mBufferPoints-Birds.* (and similarly for 200 m and 400 m, and for Timber)
  - ESRI shapefiles defining 100 m, 200 m, and 400 m buffers around bird points and around plots/quadrats for timber analyses.
- Additional notes
  - Some datasets reference results contained in associated datasets; spatial buffers and intersections were produced via QGIS.

## Data standards, provenance, and governance

- Coordinate reference and data transformation
  - Field coordinates recorded in British National Grid (OSGB36/British National Grid).
  - Coordinates converted to latitude/longitude (WGS84) for distribution and sharing.
  - Use of Ordnance Survey grid references (ODS) to link original locations with converted coordinates.
- Metadata and provenance
  - Date last modified: 06/04/2023; Date submission: 06/04/2023.
  - Contact authors provided for data access and clarifications.
  - Descriptions specify which datasets contain results vs. coordinates; some results are in associated datasets not included in BirdCounts-Kielder.csv.
- Data sources for environmental context
  - National Forest Estate Subcompartments England 2019 used to characterize environmental features in buffers around survey sites; data accessed via data.gov.uk.
  - Buffers created with QGIS (100 m, 200 m, 400 m) and intersections performed to derive site-by-feature attributes.

## Data governance and sharing considerations

- Data organization and naming conventions
  - Consistent SiteID scheme (e.g., 3.1 vs 3.2 for windblown and control pair) across datasets.
  - Clear distinction between windblown and control sites, and between plots, quadrats, and bird points.
- Data reuse and caveats
  - Bird survey results are in associated datasets; BirdCounts-Kielder.csv provides counts by distance band but references other files for survey results.
  - Some fields contain missing values (NA) where measurements were not taken or transects had no targets (e.g., fallen timber).
- Temporal scope
  - Data collected in May–July 2022; site and plot coordinates reflect sampling periods within this window.

## Practical guidance for data stewards and users

- Data accessibility and format
  - CSV files for tabular data and ESRI shapefiles for spatial data; provides multiple coordinate representations (OSGB36, ODS, WGS84).
- Data quality and interoperability
  - Standardized field names and coding (SiteID, Type, Visit, Band x) support cross-dataset joins and reproducibility.
  - Buffers and environmental attributes enable ecological context analyses and reproducible spatial analyses.
- Documentation and provenance
  - Metadata includes data sources (Subcompartments England 2019), processing steps (buffer creation, intersections), and linkages between coordinate systems and observed data.
- Potential improvements for governance
  - Consider publishing a consolidated metadata record or data package-level README to explicitly document dataset relationships (which CSV corresponds to which plots/points and how results relate).
  - Establish explicit update and versioning policy if data are to be revised or expanded in the future.

## Contact and usage notes

- Primary contact: Pablo García-Díaz (pablo.garciadiaz@abdn.ac.uk) with additional contacts for co-authors.
- Researchers should reference the multiple files collectively to reconstruct site-level analyses (bird counts, timber/plant measurements, and environmental context).
- When redistributing, maintain the provided data provenance, file formats, and the site-specific identifiers to preserve traceability.