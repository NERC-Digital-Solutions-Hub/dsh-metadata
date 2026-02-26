# RGB aerial imagery collection method using a DJI Mavic Pro 2 UAV

## Overview
- Describes the collection, processing, and basic QA of RGB aerial imagery captured over a dune using a consumer UAV, with high-precision ground control and standard photogrammetry workflows.

## Collection details
- Date and duration: 5 February 2020, 6-minute flight
- Equipment: DJI Mavic Pro 2 UAV
- Flight planning: Pix4DCapture
- Ground sample distance: 0.01 m (0.01 m pixel size)
- Image overlap: 80% both lateral and longitudinal
- Ground control: eight GCPs (5.8 per 100 photos) distributed across the dune
- GCP surveying: Trimble R8 differential GPS
- Data processing: Structure-from-Motion photogrammetry via Pix4Dmapper for orthorectification and mosaicking

## Processing and quality assurance
- GCPs identified in imagery and matched to surveyed coordinates
- Absolute coordinate comparison used to assess accuracy
- Reported RMS error: 0.003 m (X, Y, Z), indicating high relative positional accuracy

## Data attributes and structure
- Data format: GeoTIFF
- Recorded values: Red, Green, Blue channels at 0.01 m resolution
- Coordinate system: WGS84 30N (EPSG:32630)

## Data management and governance considerations
- Method emphasizes transparent processing steps and standard QA/QA workflows
- Metadata and data sharing specifics are not detailed; potential barriers (e.g., public data sharing requirements) are not described in the document
- Data is presented in standard, open-compatible formats (GeoTIFF) with precise georeferencing.