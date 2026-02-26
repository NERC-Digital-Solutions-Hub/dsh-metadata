# GPS accuracy = 4m

## Overview
- A field GPS sampling log documenting coordinates along multiple lines with an stated accuracy of 4 meters.
- Notes indicate some samples (H, M) were taken where easiest, implying practical field constraints.

## Data contents
- Sample lines/transsects include: LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB.
- Each line lists a sequence of positions at increasing distances:
  - Distance categories used: H, M, then numeric steps (2, 4, 8, 16, 32, 64).
  - Coordinates provided as latitude and longitude in various formats (e.g., N 54 21.312, W001 30.840), with corresponding distance values.
- Examples of coordinate entries show progressive moves along the line (e.g., LL A1 from lat/lon around N 54 21.x and W001 30.x to later positions like N 54 21.314, W001 30.827, etc.).

## Data quality and formatting notes
- GPS accuracy explicitly stated as 4m.
- Formatting is inconsistent: some coordinates use degrees and minutes with spaces; others appear to mix notations (e.g., N 54 21.312 vs N 54.21.317).
- Some entries show incomplete data (e.g., "OV 7, longitude = .", "WHB end is truncated").
- Data appears to be a raw field log rather than a standardized GIS dataset, with potential gaps and irregular punctuation.

## GIS implications
- Potential uses:
  - Convert to GIS point features with attributes: transect_id (e.g., LL A1), distance_category (H, M, 2, 4, 8, 16, 32, 64), latitude, longitude, and accuracy (4m).
  - Visualize transects as line features or as a series of points along survey routes.
- Data preparation steps:
  - Normalize coordinate formats to a single standard (preferably decimal degrees).
  - Address missing values and incomplete entries; flag or exclude incomplete points.
  - Validate spatial references and ensure consistent datum (likely WGS84).
- Quality assurance considerations:
  - Cross-check against known benchmarks or base maps.
  - Assess consistency across transects and resolve formatting inconsistencies before integration with other datasets.

## End notes
- The document exemplifies field data collection for GIS use, highlighting common challenges such as varying coordinate formats, incomplete records, and the need for careful QA and standardization to produce reliable map-based data products.