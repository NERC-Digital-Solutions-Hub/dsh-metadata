# Forest structure, composition, and bird counts in windblown and control sites in Kielder Forest, Northumberland, UK, May-July 2022

## Objective and monitoring context
- Provides standardized, quality-assured environmental data from windblown versus control paired sites to assess forest structure, species composition, and bird assemblages.
- Aims to support environmental health monitoring and policy performance evaluation over time, leveraging clearly defined outputs (datasets, coordinates, and derived environmental context).

## Study design and data collection
- Paired site design: windblown and control sites in Kielder Forest, Northumberland, UK, surveyed May–July 2022.
- Bird data collection: 
  - Bird point counts conducted on each paired site (2–4 points per site; 2 visits per point) from 6:00–10:30 am.
  - 5-minute stationary counts per point with birds recorded by species and distance band (0–50 m in five bands: 0–10, 10–20, 20–30, 30–40, 40–50 m).
- Timber and vegetation surveys:
  - 100-m transects per site with three 10×10 m plots and three 2×2 m quadrats along each transect (0–10 m, 50–60 m, 90–100 m).
  - Measurements include fallen trees, diameter at breast height (DBH), tree species, and plant cover/identification in quadrats.
- Environmental characterization:
  - 100-, 200-, and 400-m buffers around survey sites created in QGIS.
  - Intersection with National Forest Estate Subcompartments England 2019 to obtain tree species, cover estimates, and related planning data.

## Data structure and contents
- BirdCounts-Kielder.csv
  - Contains results of bird point counts by site, point, and visit across both windblown and control plots.
  - Columns include SiteID, PointNumber, Type (windblown/control), coordinates (X.or, Y.or, ODS, X, Y, Lat, Long), Date, HourStart, Visit, Species (scientific and common names), and Bird counts by five distance bands.
- Coordinates-Sites-Birds.csv
  - Coordinates for each bird point count with SiteID, Type, coordinates (X.or, Y.or, ODS, X, Y, Lat, Long).
  - Includes ODS reference and visit information.
- Kielder-FallenTimberTransect.csv
  - Results of fallen timber along 100-m transects; one row per fallen tree with site, date, transect details, species, timber measurements (Diameter1/2/3), and status (Standing/Snapped).
- Kielder-Trees10x10Plots.csv
  - Trees measured in three 10×10 m plots per site (PlotID 1–3 across transect); includes species, DBH, position along transect, and standing/leaning status.
- Kielder-Plants2x2Quadrats.csv
  - Plant species present in three 2×2 m quadrats per site; Braun-Blanquet cover scores for grasses, shrubs, ferns, mosses, fungi, and lichens; includes plot position along transect.
- Coordinates-Sites-PlotsTimber.csv
  - Coordinates for the 10×10 m plots and 2×2 m quadrats (start, middle, end along transect) with site and plot metadata.
- Coordinates-Sites-Total.csv
  - Consolidated coordinates for lower corners of plots/quadrats and bird counts; used for defining buffers; notes that some survey points share locations.
- KielderBuffer-100mTotal-Subcompartments.csv
- KielderBuffer-200mTotal-Subcompartments.csv
- KielderBuffer-400mTotal-Subcompartments.csv
  - Environmental characteristics derived from National Forest Estate Subcompartments England 2019 within 100/200/400 m buffers around survey sites; columns include SiteID, Type, coordinate references, ODS, X/Y/Lon/Lat, and subcompartment attributes.
- GIS shapefiles and related files
  - Kielder-100mBufferPoints-Birds.* (points within 100 m buffers around bird counts)
  - Kielder-200mBufferPoints-Birds.* 
  - Kielder-400mBufferPoints-Birds.* 
  - Kielder-100mBufferPoints-Timber.* 
  - Kielder-200mBufferPoints-Timber.* 
  - Kielder-400mBufferPoints-Timber.* 
  - ESRI shapefiles and projection files for buffer definitions around bird counts and timber plots.

## Data provenance, accessibility, and metadata
- Authors and contacts: García-Díaz, P. (University of Aberdeen), Powell, P.A. (CONICET-UNTA, Argentina), and Lambin, X. (University of Aberdeen).
- Data sources include:
  - Primary field observations (bird counts, timber plots, and plant quadrats).
  - National Forest Estate Subcompartments England 2019 for environmental context.
  - GIS-derived buffers and coordinate transformations to standardize spatial references.
- Data are organized in CSV and ESRI shapefiles to support standardized analysis, mapping, and integration with other environmental datasets.

## Analytical relevance and use
- Enables monitoring of environmental condition and policy performance by providing standardized, QA-checked datasets across multiple ecological dimensions (birds, timber, plant communities, and environmental context).
- Facilitates data integration and cross-site comparisons through consistent site pairing, coordinate systems, and buffer analyses.
- Supports downstream analyses such as habitat association, impact assessment of windthrow events, and spatially explicit environmental modeling by supplying precise georeferenced observations and derived environmental variables.