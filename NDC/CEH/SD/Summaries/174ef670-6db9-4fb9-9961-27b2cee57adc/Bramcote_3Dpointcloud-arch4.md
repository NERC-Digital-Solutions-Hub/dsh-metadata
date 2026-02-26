# Data collection

## Dataset overview
- Terrestrial LiDAR point clouds collected from a 18000 m² wooded area in Bramcote Hills Park, Nottinghamshire, UK.
- Two overlapping scans yielding ~200 million forest-structure measurements.
- Includes trees infested with the liana Hendra helix (ivy) and non-infested trees.
- Data collected to study ecological connections facilitated by lianas by linking forest structure with eDNA metabarcoding of soil and leaf litter.

## Study context
- Part of a study aiming to understand ecological links mediated by lianas, by integrating forest-structure data with eDNA analyses of soil and leaf litter.

## Data collection details
- Date of collection: 13 January 2023.
- Instrument: Leica RTC360 terrestrial LiDAR scanner.
- Spatial coverage: approximately 52.936°–52.938° latitude and -1.251° to -1.249° longitude.
- Data formats: two LAS (.las) files (Wooded_scan_location1.las and Wooded_scan_location2.las).
- Point counts: ~94.9 million points in scan 1; ~100.1 million points in scan 2.
- Estimated point density: ~11000 points per square metre.

## Quality control and processing
- Raw data converted from proprietary .scan to LAS format using Leica Cyclone.
- Missing header information (e.g., projection) filled with LAStools.
- Reported 3D point accuracy: 5.3 mm at a distance of 40 m.

## Data structure and contents
- LAS format per point includes:
  - X, Y, Z coordinates (easting, northing, height)
  - intensity (unitless, 0–65534)
  - return_number (order of return for the laser pulse)
  - number_of_returns (total returns for the pulse)
  - R, G, B color values (unitless, 0–65280)

## Spatial reference and units
- Coordinate system: WGS84 UTM Zone 30N.
- Distances (X, Y, Z) and heights in metres.
- Intensity and RGB values are unitless.

## Data extent and coverage
- Combined dataset comprises nearly 200 million points across two scans.
- Each scan file (Wooded_scan_location1.las, Wooded_scan_location2.las) contains its own extent information (easting, northing, and height ranges) in the LAS headers.