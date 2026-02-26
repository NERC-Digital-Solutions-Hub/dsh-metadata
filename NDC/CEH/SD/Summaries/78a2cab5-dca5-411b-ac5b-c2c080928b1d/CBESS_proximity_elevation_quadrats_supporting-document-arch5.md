# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Purpose and scope
- Dataset records elevations and proximity metrics for CBESS survey quadrats across six UK sites, covering saltmarsh and adjacent mudflat habitats.
- Each site includes 22 quadrats on mudflat and 22 quadrats on saltmarsh (totaling 264 quadrats per habitat across all sites).
- Data prepared to support analyses of coastal biodiversity and ecosystem services; staff responsible and locations documented for governance and stewardship.

## Data content and key variables
- Core coordinates and elevations:
  - x, y (Easting, Northing in OSGB)
  - elevationGPS (GPS-derived elevation), elevation5 (5 m DTM), elevation50 (50 m DTM)
- Tidal metrics:
  - Tidal gauge, Diff.CD-OD, Port.MLWS, Port.MHWS, Diff.MLWS, Diff.MHWS, MLWS, MHWS, MLWS.OD, MHWS.OD, tidal.range
  - tidal.height.GPS, tidal.height.elevation5, tidal.height.elevation50 (relative to datum)
- Proximity metrics (5 m raster scale):
  - creekdist5 (distance to creek edge for saltmarsh), HWdist5 (distance to mean high water line for saltmarsh)
  - landdist5 (distance to land edge for mudflat)
- Metadata fields describe sample context:
  - Quadrat, Season, Location, Site, Habitat, Scale categories (A–D), and related descriptive fields
- All measured or derived values are in metres
- Observations describe elevations at 1 m square quadrats oriented NS-EW, with GPS-derived positions and raster-derived elevation surfaces

## Data sources and processing workflow
- Input data sources:
  - CBESS_gps_quadrats.csv for GPS positions and elevations
  - Ordnance Survey 5 m and 50 m Digital Terrain Models (via Edina Digimap)
  - Tidal data from Admiralty standard ports and local tidal gauges
  - Saltmarsh boundaries from Environment Agency GIS shapefiles; high-water line from OS Boundary Line; land edge from OS Vector Map
  - Mudflat boundaries from Natural England Priority Habitat Inventory; similarly rasterized to 5 m
- Processing steps:
  - Elevations extracted at quadrat locations from 5 m and 50 m DTM rasters
  - Tidal heights converted to Ordnance Datum; relative tidal height computed
  - Distances computed from boundary rasters/tables (5 m resolution)
  - Shapefiles converted to 5 m rasters for distance calculations
  - Data manipulated with PROJ4 and R; tidal heights calculated in Excel
- Data formats:
  - Original data in .csv, .shp, and .asc
  - Outputs include GIS-ready fields and derived metrics

## Locations and site descriptions
- Sites and habitats:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) — predominantly saltmarsh and cohesive clays/mudflat
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) — saltmarsh and mudflat with sandy soils and heterogeneous inundation
- Site-level context:
  - Essex and Morecambe Bay sites chosen to represent contrasting sediment types, inundation frequencies, creek structures, and vegetation
  - Quadrats located at the south-east corner of 1 m square plots

## Data quality, governance and stewardship
- Data collection and preparation date:
  - Calculations completed in February 2016, after field campaigns
- Quality assurance and documentation:
  - The dataset includes sections for data procedures and quality control, but some fields are marked NA (not described) in the provided documentation
- Documentation and provenance:
  - Staff: Thomas P. Adams, Michael T. Burrows
  - Clear provenance from GPS, OSGB coordinates, and multiple authoritative geospatial data sources
- Sharing and cataloguing:
  - Data described as intended for upload to relevant portals and catalogue holdings; structured for easy discovery and reuse

## Practical considerations for data stewards and reuse
- Governance and standards:
  - Metadata includes detailed variable definitions, units (metres), and provenance of each derived metric
  - GIS-ready formats (.csv, .shp, .asc) with clear links to source rasters and boundary data
- Reuse considerations:
  - Coordinate system: OSGB; derived elevations in relation to Ordnance Datum
  - Temporal context: dataset reflects conditions and measurements around 2016 field campaigns
  - Reproducibility: processing workflow documented (R, PROJ4, Excel) enabling reproduction of derived metrics
- Limitations and notes:
  - Some QA and procedure details are not fully described in the provided documentation (NA fields)
  - No explicit licensing or access restrictions are stated in the extract; practitioners should verify sharing permissions and any embargoes before distribution