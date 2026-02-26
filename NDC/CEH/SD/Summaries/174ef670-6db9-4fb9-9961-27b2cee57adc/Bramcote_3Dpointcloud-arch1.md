# Data collection

## What the dataset comprises
- Terrestrial LiDAR 3D point clouds collected over a 18000 m2 wooded area in Bramcote Hills Park, Nottinghamshire (UK).
- Two overlapping scans yielding ~200 million forest structure measurements.
- Includes trees infested with lianas (Hendra helix/common ivy) and non-infested trees.
- Study goal: understand ecological connections facilitated by lianas by linking forest structure data with eDNA metabarcoding of soil and leaf litter.

## Measurements and scope
- Instrument and date: Leica RTC360; scans conducted on 13 January 2023.
- Spatial coverage: dataset extent [52.936°, 52.938°, -1.251°, -1.249°].
- Liana-related implications: lianas increase forest structure and leaf litter production/quality, potentially affecting soil/detritivore communities.

## Data formats and units
- Data format: LAS (.las) point clouds (two overlapping scans).
- Coordinate system and units: WGS84 UTM Zone 30N; x (easting) and y (northing) and z (height) in metres.
- Per-point measurements: intensity (0–65534), RGB colours (R, G, B) in 0–65280.

## Quality control
- Raw data converted from proprietary .scan to LAS using Leica Cyclone.
- Missing header information (e.g., projection) filled with LAStools.
- Overall point density: ~11000 points/m2.
- 3D point accuracy: 5.3 mm at a distance of 40 m.
- Individual scan statistics:
  - Wooded_scan_location1.las: ~94,896,646 points
  - Wooded_scan_location2.las: ~100,692,741 points
  - Scan metadata includes minimum/maximum easting, northing, and height values.

## Data structure
- LAS format per point includes:
  - X, Y, Z = coordinates (easting, northing, height)
  - intensity = laser return strength
  - return_number = order of return for multi-return pulses
  - number_of_returns = total returns for the pulse
  - R, G, B = colour values

## Relevance for analysis
- Enables linking high-resolution forest structure with ecological variables from soil/leaf litter (via eDNA), useful for identifying correlations between liana presence, canopy/understory formation, and biodiversity responses.
- Supports developing predictive insights on how structural changes (e.g., due to lianas) may impact soil fauna and litter dynamics.