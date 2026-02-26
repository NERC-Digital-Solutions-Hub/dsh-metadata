# Data collection

- Dataset purpose and ecological context
  - Terrestrial LiDAR 3D point clouds of a 18000 m2 wooded area in Bramcote Hills Park, Nottinghshire, UK
  - Aim: study ecological connections facilitated by lianas (Hendra helix) by linking forest structure data with eDNA metabarcoding of soil and leaf litter
  - Includes both liana-infested and non-infested trees; lianas influence forest structure and leaf litter production and quality

- Collection details
  - Date: 13 January 2023
  - Instrument: Leica RTC360 terrestrial LiDAR
  - Coverage: two overlapping scans covering approximately 200 million measurements
  - Spatial reference: lat/long bounds provided; final data in projected coordinates

- Data content and provenance
  - Data type: 3D LiDAR point cloud
  - Area and context: Bramcote Hills Park, Nottinghamshire, UK
  - Scans used: two overlapping scans to capture forest structure
  - Link to broader study: intended to be combined with environmental DNA data for ecological analyses

- Data format, units, and attributes
  - File format: LAS (.las)
  - Coordinate system: WGS84 UTM Zone 30N
  - Units: all x, y, z in metres; intensity as unitless (0-65534); RGB values (0-65280)
  - Point attributes per point:
    - X, Y, Z (easting, northing, height)
    - intensity
    - return information: return_number, number_of_returns
    - color: R, G, B

- Quality control and processing
  - Raw data conversion: from proprietary .scan to LAS (.las) using Leica Cyclone
  - Metadata/header completion: missing header information added with LAStools
  - Data characteristics: ~200 million points; ~11,000 points per square metre
  - Spatial accuracy: Leica RTC360 accuracy ~5.3 mm at 40 m
  - Scan-specific statistics (sample highlights):
    - Minimum/maximum easting (x) and northing (y) values; height (z) ranges noted per scan
    - Points per scan: ~94.9 million and ~100.7 million for the two scans

- Data structure and schema
  - LAS format fields included for each point:
    - X, Y, Z coordinates
    - intensity
    - return_number
    - number_of_returns
    - R, G, B color values

- Data stewardship considerations
  - Data volume: large dataset with high transfer and storage requirements
  - Metadata and provenance: includes instrument, date, processing steps; ensure comprehensive metadata for discoverability and reuse
  - Accessibility and sharing: considerations for repository storage, licensing, and potential embargoes or usage restrictions
  - Linkage potential: dataset designed to be integrated with eDNA/metabarcoding data for multidisciplinary analyses

- Limitations and caveats for users
  - Spatial bounds provided via approximate coordinate ranges; precise bounds should be consulted in metadata
  - Two-scans approach may introduce stitching considerations; ensure awareness of potential alignment issues
  - Large file size may necessitate chunked processing and specialized tools for handling LAS data