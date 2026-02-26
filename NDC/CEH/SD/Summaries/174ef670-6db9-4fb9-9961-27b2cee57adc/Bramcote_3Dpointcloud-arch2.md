# Data collection

- A dataset of 3D point clouds from two overlapping terrestrial LiDAR scans over an 18,000 m2 wooded area in Bramcote Hills Park, Nottinghamshire, UK.
- Purpose: study ecological connections facilitated by lianas (Hendra helix) by linking forest structure data with eDNA metabarcoding of soil and leaf litter.
- Scope: mixture of trees infested with lianas and non-infested trees; lianas are associated with increased forest structure and leaf litter production, potentially affecting soil and litter-dwelling organisms.
- Date and instrument: collected on 13 January 2023 using a Leica RTC360.
- Spatial coverage: coordinates [52.936°, 52.938°, -1.251°, -1.249°] in WGS84 UTM Zone 30N.
- Data format and contents: 3D point clouds in LAS (.las) format, with per-point X, Y, Z (easting, northing, height), intensity (0–65534), return_number, number_of_returns, and RGB color (R, G, B) (0–65280).
- Units: all spatial measurements in metres; intensity and color values are unitless.
- Quality control and processing:
  - Original scans captured with Leica RTC360; raw data converted from .scan to .las via Leica Cyclone.
  - Missing header information added using LAStools.
  - Combined dataset contains ~200 million points with an average density of ~11,000 points per m2.
  - Leica RTC360 specifications: 3D point accuracy of 5.3 mm at 40 m.
- Dataset specifics:
  - Two LAS files: wooded_scan_location1.las and wooded_scan_location2.las.
  - Spatial extents and count details provided for each scan (easting, northing, height ranges; points: ~94.9M and ~100.7M respectively).
- Data structure: per point fields include X, Y, Z, intensity, return_number, number_of_returns, R, G, B.
- Context and future use: part of a broader study to link forest structure with ecological indicators; data could be stored, standardised, and made accessible to support environmental monitoring and policy performance assessments, aligning with standard QA and data-sharing practices.