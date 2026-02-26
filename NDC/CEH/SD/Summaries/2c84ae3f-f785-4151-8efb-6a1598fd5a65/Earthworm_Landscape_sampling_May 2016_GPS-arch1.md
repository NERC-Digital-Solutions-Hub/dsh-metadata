# GPS accuracy = 4m

## Overview
- The document presents GPS measurement data for multiple sites, listing a baseline coordinate followed by position points at increasing distances.
- The stated GPS accuracy is 4 meters.
- Sites include LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB (and related variants), each with a similar pattern of coordinates.

## Data structure and content
- For each site:
  - A baseline entry: "distance = H" or "distance = M" accompanied by a latitude and longitude.
  - A series of subsequent entries labeled with numeric distances: 2, 4, 8, 16, 32, 64 (meters), each with corresponding latitude and longitude.
- Coordinates are presented in a mixed format (degrees, minutes, decimal parts) with directional indicators (N/S, W/E). Some lines show punctuation inconsistencies or missing values.
- The initial baseline often uses placeholders (H or M) rather than numeric distances, followed by the incremental distance steps.

## Patterns and implications
- The data appears designed to examine how reported GPS coordinates shift with increasing distance from a baseline, potentially to assess drift or accuracy across multiple locations.
- Distances increase geometrically (2, 4, 8, 16, 32, 64), suggesting a test of positional stability or error growth with separation.
- Lat/long values vary slightly across distance steps, consistent with a drift or grounding exercise around each site.

## Data quality and gaps
- Formatting inconsistencies: trailing periods, uneven punctuation, and occasional non-numeric distance labels (H, M).
- Some lines show missing or incomplete values, notably:
  - Entries with "longitude = ." or truncated numeric values (e.g., OV 7, several lines).
  - The final line ends abruptly, indicating incomplete data capture.
- Inconsistent coordinate formatting across sites complicates immediate automated parsing.

## Analytical opportunities
- Clean and structure the data into a consistent schema:
  - Site, distance_m, latitude, longitude (with proper decimal degrees).
- Convert coordinates from the given format to decimal degrees for analysis.
- Compute haversine distances from baseline to each subsequent point and compare against the stated distances to evaluate internal consistency and reported accuracy.
- Compare drift patterns across sites to identify environmental or methodological influences on GPS performance.
- Visualize trajectory drift by site and distance to assess whether accuracy degrades with distance as expected.
- Address data quality issues:
  - Standardize punctuation and formatting.
  - Fill or flag missing values, and handle or impute incomplete lines.
  - Clarify meaning of baseline distance labels (H, M) relative to numeric distances.