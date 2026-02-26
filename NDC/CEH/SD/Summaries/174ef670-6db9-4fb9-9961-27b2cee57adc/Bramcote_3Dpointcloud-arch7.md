# Data collection

## Overview
- Dataset comprises 3D terrestrial LiDAR point clouds from two overlapping scans in Bramcote Hills Park (Nottinghamshire, UK), covering a 18000 m² wooded area.
- About 200 million forest-structure measurements, including trees infested with lianas (Hendra helix) and non-infested trees.
- Collected to study ecological connections facilitated by lianas, linking forest structure with eDNA metabarcoding of soil and leaf litter.

## Data collection details
- Date of acquisition: 13 January 2023
- Instrument: Leica RTC360
- Spatial coverage: latitude/longitude bounds [52.936°, 52.938°, -1.251°, -1.249°]

## Nature and units of recorded values
- Data format: LAS (.las) point clouds in the WGS84 UTM Zone 30N coordinate system
- Units: x and y (easting, northing) and z (height) in metres
- Point attributes:
  - intensity: unitless scale 0-65534
  - RGB: R, G, B color values on unitless scale 0-65280

## Quality control and processing
- Scans converted from proprietary .scan to LAS (.las) using Leica Cyclone; missing header information added with LAStools
- Combined dataset size: ~200 million points
- Point density: ~11000 points per square metre
- 3D point accuracy: 5.3 mm at 40 m
- Individual scans:
  - Wooded_scan_location1.las
  - Wooded_scan_location2.las
  - Each file provides bounding extents for easting (X), northing (Y), and height (Z) along with point counts

## Data structure and key attributes
- LAS format with per-point fields:
  - X (easting), Y (northing), Z (height)
  - intensity
  - return_number
  - number_of_returns
  - R, G, B (color values)

## Notes for GIS use
- Suitable for mapping and analyzing forest structure, canopy geometry, and spatial distribution of lianas within a woodland context.
- Can be integrated with ecological data such as soil and leaf litter samples to explore relationships between structure and arthropod or other soil-dwelling communities.
- Large data volume; practical use may involve subset extraction, tiling, or processing with compatible GIS/LiDAR software.