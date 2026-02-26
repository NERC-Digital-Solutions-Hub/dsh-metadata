# Collection, generation methods and quality control

- Scope and purpose
  - Focused on Iron Tongue Hill on Swineshaw Moor; area of interest ~0.45 km2 with seven erosion plots (~5 x 5 m) established 26/07/2018 to monitor erosion and vegetation recovery.
  - The orthophoto mosaic provides spatial context for the seven erosion plots (Figure 1).

- Data collection
  - 786 individual images captured using a DJI Mavic 2 Pro drone (CAA Operator ID OP-FNVFWNM) on 29 July 2019.

- Data processing and georeferencing
  - Dense structure-from-motion (SfM) point cloud generated in Agisoft Metashape.
  - Ground Control Point coordinates used to scale and georeference the point clouds based on field-recorded dGPS coordinates.

- Data products and formats
  - Cleaned DEM dense point cloud and orthomosaic exported as .tif files.
  - TIFFs imported into ArcGIS (ArcMap 10.5); orthomosaic projected to OSGB coordinates and resampled to 5 x 5 cm ground resolution; final TIFF saved.

- Metadata, provenance, and attribution
  - Figure 1 (location map) prepared by Jeff Warburton using EDINA Digimap Ordnance Survey Collection, 2021.
  - Document describes the snapshot nature of the image (late July 2019) and its role in supporting erosion plot analyses.

- Quality control and governance considerations
  - Use of Ground Control Points and dGPS for accurate georeferencing ensures spatial accuracy.
  - Clear documentation of processing steps (SfM, georeferencing, projection, resampling) supports reproducibility and data quality assessment.
  - Outputs are high-resolution georeferenced TIFFs suitable for GIS-based analysis and integration with related datasets.