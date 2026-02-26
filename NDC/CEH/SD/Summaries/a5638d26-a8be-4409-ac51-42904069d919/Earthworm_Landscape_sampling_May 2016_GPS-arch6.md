# GPS accuracy = 4m

- Overview of content
  - A field-style geospatial data extract listing multiple labeled locations (e.g., LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB).
  - For each label, coordinates (latitude and longitude) are provided at successive distance steps, labeled variably as H, M, 2, 4, 8, 16, 32, 64, etc.
  - The document begins with a note that GPS accuracy is 4 meters and that some samples required digging “where easiest.”

- Data structure and patterns
  - Distance labels include: H, M, then a sequence of powers of two (2, 4, 8, 16, 32, 64).
  - Coordinates are given in latitude and longitude, with formats mixing degrees, minutes, and decimal values (e.g., N 54 21.312, W001 30.840) and sometimes using decimal minutes or variants.
  - Each location block follows a nested pattern: a starting coordinate at a given distance, followed by coordinates at increasing distances.
  - Some entries show missing values for longitude (indicated by a dot), suggesting incomplete data capture in places (e.g., “OV 7” and certain entries).

- Notable content and examples
  - Labels include: LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB.
  - Example structure: “LL A1, distance = H. LL A1, latitude = ..., LL A1, longitude = ..., distance = M. , latitude = ..., longitude = ...” progressing through distance steps.
  - End of the extract shows continued propagation of latitude/longitude values for WHB, with an entry ending in “latitude = N 54 07.175., longitude = W001 01.231.”

- Data quality and challenges
  - GPS accuracy is stated as 4 meters, appropriate for some field mapping but not high-precision.
  - Inconsistent formatting across entries (e.g., variations in degree-minute formats, use of decimal points, and occasional missing longitude values).
  - Some lines indicate incomplete data (longitude or other fields missing), which would require cleaning before analysis or integration into a product.

- Implications for data support work
  - The dataset could feed a geospatial product (maps, dashboards) that allows exploration by location label and distance from a reference point.
  - Useful as a baseline for validating GPS collection methods and for demonstrating distance-based coordinate sampling.

- Recommendations for cleaning and productization
  - Normalize coordinate formats to a single standard (e.g., decimal degrees) and consistently parse degree-minute representations.
  - Address missing values (impute or mark as missing) and verify with source references.
  - Create a structured schema: label, distance_label, latitude, longitude, source_distance, and timestamp if available.
  - Validate GPS accuracy against the stated 4m specification and document any outliers or inconsistencies.
  - Build a data product (e.g., a map plus a self-serve table) to enable end users to query by label or distance and to compare coordinates across distance steps.