# Geolocated aerial orthomosaics of the South Saskatchewan River near Outlook, Canada (2015–2017)

## Overview
- A set of geolocated aerial orthomosaic TIFF files covering the South Saskatchewan River near Outlook, Canada, across four dates (2015, 2016, 2017) and two river sections.
- Purpose: provide high-resolution imagery of the river bed and surrounding valley floor to support environmental monitoring and analysis.
- Files include: downstream_2015_transparent_mosaic.tif, downstream_2016_transparent_mosaic.tif, downstream_2017a_transparent_mosaic.tif, downstream_2017b_transparent_mosaic.tif, upstream_2015_transparent_mosaic.tif, upstream_2016_transparent_mosaic.tif, upstream_2017a_transparent_mosaic.tif, upstream_2017b_transparent_mosaic.tif.

## Data and context
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith.
- Data specifics:
  - Geolocated orthomosaics of two river sections near Outlook, Canada.
  - Ground resolution: 0.06 m.
  - Acquisition dates: 13 May 2015; 2 Sept 2016; 8 June 2017; 12 June 2017.
  - Sensor/platform: conventional aerial photography from a fixed-wing aircraft at ~1500 m altitude using an UltraCamXp sensor; up to 160 images per mosaic.
- Processing and provenance:
  - Orthomosaics generated from aerial imagery using Pix4D (SfM) with the “large frame” option; bundle adjustment performed with Pix4D’s key point matching system optimized for nadir imagery.
  - Camera properties specified via calibration certificates and held constant during processing.
  - UTM coordinates included in the image metadata and viewable in GIS; the file set provides geolocation context (Easting 356500, Northing 5712400; Latitude 51.5 N, Longitude 107.07 W).

## Metadata and data governance
- Metadata quality:
  - Spatial coordinates are embedded and GIS-viewable, enabling integration with other environmental datasets.
  - Processing chain and calibration data are documented (Pix4D workflow, fixed camera parameters), aiding reproducibility.
- Data sharing and accessibility:
  - Data is provided as geolocated TIFF mosaics suitable for analyses and dashboarding; explicit licensing and metadata completeness beyond geolocation are not stated, presenting potential governance considerations.
- Relevance for monitoring frameworks:
  - High-resolution, multi-temporal imagery supports monitoring of river morphology, sediment dynamics, and habitat features.
  - Consistent acquisition and processing approach (same sensor, fixed camera calibration, Pix4D workflow) enhances comparability across years and sections.

## Considerations for implementation in monitoring programs
- Use the orthomosaics as baselines for change detection in river morphology and valley-floor processes.
- Leverage precise geolocation and GIS-integrated metadata for linking imagery with other environmental indicators (water quality proxies, vegetation, erosion hot spots).
- Ensure clear data governance:
  - Clarify licensing and data sharing permissions to facilitate broader reuse.
  - Maintain detailed metadata (sensor settings, weather conditions at capture, tie points, tie accuracy) to improve data quality assessment and future reuse.
- Document processing steps for transparency and reproducibility (inputs, software versions, calibration certificates, parameter settings).