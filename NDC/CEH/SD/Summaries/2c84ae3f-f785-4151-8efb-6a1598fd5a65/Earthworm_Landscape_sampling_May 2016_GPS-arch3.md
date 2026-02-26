# GPS accuracy = 4m

## Overview
- Field GPS sampling log with multiple labeled points (e.g., LL A1/A2, LL B1/B2, HWA1/HWB, OV 7, WHA/WHB).
- Each label has an initial entry (distance = H or M) followed by successive coordinates at increasing distances (2, 4, 8, 16, 32, 64) from the starting point.
- Initial GPS accuracy stated as 4 meters; some samples note occasional digging to reach a suitable location.

## Data structure and sampling protocol
- For each site:
  - Initial coordinates are provided (lat/long).
  - A distance category (H or M) is recorded, then a sequence of coordinates corresponding to distances of 2, 4, 8, 16, 32, and 64 (units likely meters).
  - Coordinates are presented in varying formats (degrees-minutes with decimal seconds and decimal minutes); some entries have missing longitude values later in the sequence.

## Data quality observations
- Inconsistencies in formatting and some missing metadata (e.g., some longitudes shown as ".").
- Repeated capturing at multiple radii suggests a protocol to verify location accuracy or create spatial buffers around central points.
- Some entries include notes about field conditions (e.g., “dig where easiest” for certain samples), indicating practical measurement constraints.

## Relevance to monitoring framework authors
- Illustrates the importance of explicit metadata for spatial data (GPS accuracy, sampling method, distance steps).
- Demonstrates common data quality issues in field data collection (format inconsistencies, missing values, incomplete attributes).
- Highlights the need for standardized data schemas and clear documentation to support data sharing and reproducibility.

## Challenges and governance implications
- Data completeness and metadata adequacy can hinder verification and reuse.
- Inconsistent coordinate formats and missing values complicate integration with other datasets.
- Public sharing of datasets may be hindered by formatting gaps and insufficient metadata; underscores the need for data governance, validation, and standardization.

## Takeaways for monitoring framework authors
- Implement standardized coordinate formats and complete, machine-readable metadata (accuracy, method, units, spatial references).
- Define clear protocols for recording sampling distances and for handling missing data.
- Build in data quality checks and governance processes to ensure datasets are open, interoperable, and reusable across projects.