# Collection, generation methods and quality control

## Overview
- Orthophoto mosaic for Iron Tongue Hill, Swineshaw Moor.
- Area of interest: ~0.45 km² including seven erosion plots (~5 × 5 m).
- Purpose: capture surface conditions in late July 2019 to monitor erosion and vegetation recovery.
- Figure 1 displays the location; Figure prepared by Jeff Warburton using EDINA Digimap Ordnance Survey Collection, 2021.
- Plot setup date: 26/07/2018.

## Data collection
- Imagery: 786 individual photos captured with a DJI Mavic 2 Pro drone.
- Capture date: 29 July 2019.
- Drone operator ID: OP-FNVFWNM (CAA registration).

## Processing and data products
- Structure-from-Motion (SfM) workflow conducted in Agisoft Metashape to produce a dense point cloud.
- Ground Control Points (GCPs) used to scale and georeference the model based on field dGPS coordinates.
- Outputs: cleaned dense DEM point cloud and orthomosaic exported as TIFF (.tif).
- GIS processing: TIFFs imported into ArcGIS ArcMap 10.5; orthomosaic projected to OSGB coordinates.
- Resolution: resampled to 5 × 5 cm ground sampling distance; final TIFF saved.

## Georeferencing, metadata, and provenance
- Coordinate system: OSGB.
- Ground sampling distance: 5 cm.
- Data provenance: drone imagery, SfM processing, GCP-based georeferencing, and GIS resampling steps documented.
- Attribution for figures: Jeff Warburton (Figure 1); source content prepared using EDINA Digimap Ordnance Survey Collection, 2021.

## Quality control
- QC steps include:
  - Use of Ground Control Points with field dGPS for accurate georeferencing.
  - Cleaning of the dense point cloud and DEM.
  - Verification of projection to OSGB and standardized resampling to a consistent resolution.

## Accessibility, sharing, and governance considerations
- Data format: final orthomosaic TIFF and associated DEM/point cloud outputs.
- Coordinate system and metadata alignment (OSGB, 5 cm resolution) support discoverability and reuse in related coastal/moorland erosion studies.
- Attribution and dependencies noted (image source, processing software, and figure preparation).
- Potential considerations for data stewards: ensure metadata completeness (sensor, flight, processing steps, GCP details), document licensing/permissions, and indicate any access restrictions or embargoes if applicable.