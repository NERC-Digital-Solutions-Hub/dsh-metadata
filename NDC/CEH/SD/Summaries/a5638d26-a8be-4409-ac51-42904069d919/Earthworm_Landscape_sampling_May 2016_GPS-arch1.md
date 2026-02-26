# GPS accuracy = 4m

## Overview
- A GPS-based accuracy assessment with an explicit stated accuracy of 4 meters.
- Includes multiple waypoint groups: LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB.
- Each group provides a baseline latitude/longitude and a sequence of positions at increasing distances, labeled with distance values (H, M, 2, 4, 8, 16, 32, 64).

## Data structure
- For each group:
  - A label (e.g., LL A1) and a baseline coordinate (latitude and longitude).
  - A distance category (H or M) followed by progressive distance steps (2, 4, 8, 16, 32, 64).
  - Each step records a latitude and longitude, showing small shifts from the baseline.
- The data formatting shows export characteristics (commas, periods) and includes a field indicating GPS accuracy.

## Key patterns by group
- LL A1 and LL A2: base coordinates around lat N 54 21.x, lon W001 30.x; subsequent points drift slightly with distance.
- LL B1 and LL B2: base around lat N 54 21.x, lon W001 31.x; progressive points show small positional shifts.
- HWA1 and HWB: bases around lat N 53 56.x to 53 56.x, lon W001 13.x to W001 12.x; distance progression shows drift patterns.
- OV 7, WHA, WHB: bases around lat N 53–54.x, with longitudes around W001 01.x to W001 01.x and W001 12–13.x; position updates continue for each distance tier.
- Across groups, coordinates move slightly away from the baseline as distance increases, illustrating positional variability within the 4m accuracy scope.

## Data quality and notes
- The header emphasizes GPS accuracy of 4 meters.
- A note mentions some samples required digging "where easiest," indicating field collection constraints.
- Data presents mixed distance labels (H, M) alongside numeric steps (2, 4, 8, 16, 32, 64) and contains formatting inconsistencies.

## Potential uses and next steps
- Quantify positional drift at each distance to assess accuracy and precision.
- Compare drift patterns across groups to identify regional performance differences.
- Use as a validation dataset for GPS devices and GIS workflows, or to calibrate local-scale analyses.
- Data cleaning: standardize formatting, unify distance labels, and enrich with metadata for portal dissemination.