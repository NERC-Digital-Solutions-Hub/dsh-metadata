# GPS accuracy = 4m

## Overview
- Field data collection log documenting sampling points with precise GPS coordinates and distance steps.
- Note of GPS accuracy (4 meters) and occasional need to dig at easier locations for sampling.
- Data structured around labeled locations (e.g., LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB) and a series of distance increments (H, M, 2, 4, 8, 16, 32, 64), with corresponding latitude and longitude values.

## Data Structure and Content
- Each site entry includes:
  - Site label (e.g., LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB).
  - An initial distance category (H or M) followed by a set of exact coordinates.
  - Successive distance steps with exact latitude and longitude for each increment (2, 4, 8, 16, 32, 64).
- Examples of patterns:
  - LL A1: starting at distance H, then M, then 2, 4, 8, 16, 32, 64 with progressively adjusted coordinates.
  - HWA1 and HWB: similar progression of coordinates from initial to 64 units outward.
  - OV 7, WHA, WHB: include defined coordinate sequences across increasing distances.
- Indicates a grid/transect approach to position sampling points relative to each labeled location.

## Geographic Coverage (implicit)
- Coordinates cluster around latitudes near N 54.x and longitudes around W001.x, suggesting sampling within a UK-related region.
- Additional clusters include latitudes around N 53.x to N 54.x and longitudes around W001.x to W001.x.x, covering multiple nearby sub-areas (e.g., LL, HWA/HWB, OV, WHA/WHB).

## Data Management and Outputs
- The document aligns with standardized environmental monitoring practices:
  - Verify and quality-assure data from established sources.
  - Clean, transform, and analyse data using standardized methods.
  - Present outputs as clear formats (reports, maps, charts).
  - Store datasets and upload to appropriate portals.

## Challenges and Opportunities
- Challenge: Increasing the value of monitoring datasets by integrating them with complementary data (avoiding single-use datasets).
- Challenge: Enabling broad access to the underlying data used to generate final outputs.

## Practical Implications for Analysts
- The log illustrates a rigorous, repeatable sampling protocol with precise geolocation to support temporal environmental health assessments.
- Emphasizes data quality, traceability, and accessibility to support policy performance review and environmental health scrutiny over time.