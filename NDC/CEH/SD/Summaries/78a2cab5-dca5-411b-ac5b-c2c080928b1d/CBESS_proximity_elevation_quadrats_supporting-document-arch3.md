# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Purpose and scope
- Provides elevation, tidal height, and proximity metrics for survey quadrats in saltmarsh and adjacent mudflat habitats across six UK sites.
- Variables include spatial position (x, y), multiple elevation measures, tidal height relative to Admiralty standards, and distances to key habitat boundaries (creek edge, high water mark, saltmarsh edge, land edge).
- Each site comprises both saltmarsh and mudflat quadrats, with 22 quadrats per habitat (1 m square, oriented NS/EW).

## Study design and locations
- Sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Site selection represents contrasting habitats: sediment types (clay vs sandy soils) and inundation characteristics; differences in creek structure and vegetation between Essex and Morecambe Bay.
- Sampling timeframe: field campaigns completed before February 2016; records calculated in February 2016.
- Responsible staff: Thomas P. Adams and Michael T. Burrows.

## Data sources and processing
- Spatial locations sourced from CBESS_gps_quadrats.csv (GPS-derived x, y, elevation).
- Elevations derived from Ordnance Survey Digital Terrain Models (5 m and 50 m resolution) via Edina Digimap.
- Tidal height information referenced to Admiralty Standard Ports; conversions to Ordnance Datum for Mean Low Water Springs (MLWS) and Mean High Water Springs (MHWS).
- Edge proximity metrics derived by rasterizing boundary shapefiles:
  - Saltmarsh: distance to creek edge (creekdist5) and distance to high water (HWdist5) using Environment Agency saltmarsh extent shapefiles and OS boundary data.
  - Mudflat: distance to saltmarsh edge and to mean high water (landdist5) using Natural England Priority Habitat Inventory mudflat extent and OS boundary data.
- Boundary and boundary-line data sources: Environment Agency GIS shapefiles, Natural England Priority Habitats Inventory, and Ordnance Survey boundary lines.
- Data processing: shapefiles converted to 5 m rasters; elevations mapped to quadrat locations; tidal heights computed from GPS elevations and OS DTMs; 5 m rasterization used for distance calculations.
- Software and formats: data manipulated with PROJ4 and R; tidal heights calculated in Microsoft Excel; original data in .csv, .shp, and .asc formats.

## Observed and derived variables
- Spatial and elevation variables: x (Easting), y (Northing), elevationGPS, elevation5, elevation50.
- Tidal and reference measurements: Tidal gauge, Diff.CD-OD, Port.MLWS, Port.MHWS, Diff.MLWS, Diff.MHWS, MLWS, MHWS, MLWS.OD, MHWS.OD, tidal.range, tidal.height.GPS, tidal.height.elev5, tidal.height.elev50.
- Proximity metrics (distance measurements): creekdist5 (to creek edge, saltmarsh only), HWdist5 (to mean high water, saltmarsh only), landdist5 (to land edge, mudflat only).
- Metadata fields: row number, season (Winter/Summer), location (Morecambe Essex), site (e.g., Cartmel Sands, Abbotts Hall), habitat (Mudflat or Saltmarsh), Quadrat (1–22), Scale categories (A–D) describing spatial extent, and data format notes.
- All distance and elevation metrics are in metres.

## Data quality, provenance, and governance
- Documentation covers data provenance, processing steps, and variable definitions in detail.
- Calibration procedures, statistical treatments, and data checking procedures are listed but marked NA, indicating those QA steps may not be documented in this record.
- Data provenance includes explicit sources for elevations, tidal data, and boundary shapefiles; conversion and processing workflows are described.
- Clear notes on data transformations (e.g., rasterization to 5 m, ND conversions to Ordnance Datum) and software tools used.

## Data formats and accessibility
- Original data formats: .csv, .shp, .asc.
- Processed using PROJ4 and R; tidal heights computed in Excel.
- Documentation is thorough regarding variable definitions and data processing, aiding re-use in monitoring frameworks.

## Potential uses for monitoring and policy
- Supports evaluation of coastal biodiversity and ecosystem service sustainability by linking elevation, tides, and spatial proximity to habitat features.
- Useful for assessing vulnerability of saltmarsh and mudflat habitats to sea-level rise, inundation frequency, and boundary dynamics.
- Can inform policy decisions and monitoring strategies related to habitat conservation, flood risk management, and coastal resilience planning.
- Provides a structured dataset that can be integrated into larger environmental health dashboards, reports, and decision-support tools.

## Limitations and gaps
- Quality assurance details (calibration, QC checks) are not documented (NA in those sections).
- Scope limited to six sites with 44 quadrats per site (22 per habitat); temporal coverage limited to field campaigns completed by 2016, potentially restricting long-term trend analyses.
- Some metadata fields (e.g., full metadata on data collection procedures) are not fully elaborated in this record.