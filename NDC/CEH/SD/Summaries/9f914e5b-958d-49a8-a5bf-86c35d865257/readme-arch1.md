# Forest structure, composition, and bird counts in windblown and control sites in Kielder Forest, Northumberland, UK, May-July 2022

## Overview
- Paired windblown versus control sites in Kielder Forest, studied May–July 2022 to assess effects on birds, timber, and understory plants.
- Data collected across multiple linked datasets including bird surveys, timber and plant surveys, and environmental context.
- Spatially explicit design with transects and plots along the windthrow-control pairs; environmental attributes derived at multiple buffer scales (100, 200, 400 m).

## Study design and sampling
- Site pairing: windblown (1) vs control (2) sites arranged in pairs; coordinates and site identifiers encode pairing.
- Bird surveys:
  - Conducted May–June 2022; 2–4 bird point counts per site, each counted twice.
  - At each point, observers recorded all birds seen/heard for 5 minutes, grouped into five distance bands (0–10 m to 40–50 m).
  - Surveys occurred between 6:00 and 10:30 am.
- Timber and plant surveys:
  - 100 m transects within each site; three 10×10 m plots and three 2×2 m quadrats along each transect (at 0–10, 50–60, 90–100 m for plots; 0–2, 50–52, 90–92 m for quadrats).
  - Timber: counted/fallen trees, measured circumference at breast height (DBH-related volumes) and classed trees by species, condition (standing/snapped), and dead/alive status.
  - Plants: identified species in plots/quadrats; measured cover of grasses, shrubs, ferns, mosses, fungi, and lichens using Braun-Blanquet scales.
- Environmental context:
  - Surrounding environment characterized by defining 100-, 200-, and 400-m buffers around survey sites.
  - Data extracted from the National Forest Estate Subcompartments England 2019 dataset (via QGIS) to obtain tree species/cover and related attributes.

## Data files and key variables
- BirdCounts-Kielder.csv
  - Rows: species × site × point × visit; counts by five distance bands.
  - Key columns: SiteID, Type (windblown/control), PointNumber, Visit, Band1–Band5 counts, coordinates (X/Y, Lat/Long), Date, HourStart, Species (scientific/common names).
- Coordinates-Sites-Birds.csv
  - Bird point coordinates per SiteID/PointNumber/Visit; includes original and converted coordinates (X/Y, Lat/Long).
- Kielder-FallenTimberTransect.csv
  - Timber along 100 m transects; per-tree records with SiteID, Date, coordinates, Species, Flat/Leaning, Dead/Alive, Diameter1/2/3 (volume estimates).
- Kielder-Trees10x10Plots.csv
  - Trees within 10×10 m plots; PlotID, SiteID, Date, coordinates, Species, Standing/Snapped, DBH (Diameter at Breast Height).
- Kielder-Plants2x2Quadrats.csv
  - Plants within 2×2 m quadrats; Quadrat-level data including species, Braun-Blanquet cover for grasses, shrubs, ferns, mosses, fungi, lichens.
- Coordinates-Sites-PlotsTimber.csv
  - Coordinates for 10×10 m plots and 2×2 m quadrats along transects; includes SiteID, Type, coordinates, ODS grid refs and converted Lat/Long.
- Coordinates-Sites-Total.csv
  - Lower corners of plots/quadrats and bird point counts; used for buffering analyses; notes potential co-location of some bird counts and plots.
- KielderBuffer-100mTotal-Subcompartments.csv
  - Environmental attributes for each site from 100 m buffers, derived from Subcompartments England 2019; columns include SiteID, Type, coordinates, ODS, Lat/Long, and subcompartment-derived variables.
- KielderBuffer-200mTotal-Subcompartments.csv
  - Same as above for 200 m buffers.
- KielderBuffer-400mTotal-Subcompartments.csv
  - Same as above for 400 m buffers.
- Shapefiles for buffers
  - Kielder-100mBufferPoints-Birds.* and Kielder-200m/400mBufferPoints-Birds.*: ESRI shapefiles defining buffers around bird points.
  - Kielder-100mBufferPoints-Timber.*, Kielder-200mBufferPoints-Timber.*, Kielder-400mBufferPoints-Timber.*: buffers around plots/quadrats for timber analyses.
- Notes on data structure
  - Coordinates provided in British National Grid (OSGB36) with conversions to WGS84 (Lat/Long).
  - Some files contain only coordinates; results and analyses are in associated datasets.
  - NA values indicate missing observations (e.g., no trees found in a transect).

## GIS, buffers, and environmental context
- Buffers (100/200/400 m) were created around survey locations to extract environmental characteristics.
- Data integrated from National Forest Estate Subcompartments England 2019 dataset to relate site surroundings to tree species composition and estimated cover.
- Buffers applied to both avian and vegetation/timber datasets to enable multi-scale habitat analyses.

## Potential analyses and uses
- Compare bird abundance/diversity between windblown and control sites across distances and years.
- Examine links between windthrow effects and timber metrics (fallen timber, DBH distributions, species composition) and plant community structure (Braun-Blanquet cover, species richness).
- Investigate how environmental context (subcompartment attributes) at different spatial scales moderates windthrow impacts on birds and vegetation.
- Conduct multi-source data integration across spatial scales (plot-level, transect-level, point counts) to identify correlations and potential causal relationships.
- Utilize coordinates and buffers to reproduce or extend analyses with spatial modeling or predictive mapping.

## Contacts
- García-Díaz, P. (University of Aberdeen) — pablo.garciadiaz@abdn.ac.uk
- Powell, P.A. (CONICET-Universidad Nacional de Tucumán) — priscilaapowell@gmail.com
- Lambin, X. (University of Aberdeen) — x.lambin@abdn.ac.uk