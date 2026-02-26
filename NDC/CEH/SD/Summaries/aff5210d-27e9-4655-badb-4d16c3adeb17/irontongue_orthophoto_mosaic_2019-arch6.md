# Collection, generation methods and quality control

- What this dataset covers
  - Orthophoto mosaic for Iron Tongue Hill on Swineshaw Moor
  - Area of interest: ~0.45 km²
  - Contains seven erosion plots (~5 × 5 m) established on 26/07/2018 to monitor erosion and vegetation recovery
  - Snapshot of surface conditions captured in late July 2019; provides spatial context for the seven erosion plots shown in Figure 1

- Data collection details
  - 786 individual images captured with a DJI Mavic 2 Pro drone (CAA Operator ID OP-FNVFWNM)
  - Image acquisition date: 29 July 2019

- Data processing workflow
  - Structure-from-Motion (SfM) dense point cloud generated in Agisoft Metashape
  - Ground Control Points used to scale and georeference point clouds based on field dGPS coordinates
  - Cleaned DEM dense point cloud and orthomosaic exported as .tif files

- Data products and formats
  - Orthomosaic and DEM provided as .tif files
  - Orthomosaic projected in OSGB coordinates
  - Final orthomosaic resampled to 5 × 5 cm ground resolution

- Spatial reference and resolution
  - Coordinate reference system: OSGB (Ordnance Survey Great Britain)
  - Ground sampling distance: 5 cm

- Software and tools used
  - Agisoft Metashape for SfM processing
  - ArcGIS (ArcMap 10.5) for projection and handling of the orthomosaic
  - Field data: ground control points from dGPS measurements
  - Figure 1 prepared by Jeff Warburton using EDINA Digimap Ordnance Survey Collection (2021)

- Quality assurance and provenance
  - Use of Ground Control Points to ensure accurate georeferencing
  - Careful cleaning of the dense point cloud and DEM prior to export
  - Clear documentation of capture date, area, and plotting locations to support traceability

- Usage notes and limitations
  - This is a single-date snapshot (late July 2019) and not a time-series dataset
  - Coverage limited to the specified area and seven erosion plots
  - Outputs are suitable for spatial analysis and as a contextual reference for erosion monitoring, with OSGB coordinates ensuring compatibility with UK geospatial data

- Attribution and references
  - Figure 1 location map prepared by Jeff Warburton; based on EDINA Digimap Ordnance Survey Collection, 2021
  - Data products rely on standard geospatial workflows enabling replication with similar imagery and control data