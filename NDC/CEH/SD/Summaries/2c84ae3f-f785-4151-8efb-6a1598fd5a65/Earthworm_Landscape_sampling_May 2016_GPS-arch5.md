# GPS accuracy = 4m

## Overview
- Field collection log of GPS coordinates across multiple lines/areas (e.g., LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB, etc.).
- Reports GPS accuracy as 4 meters and notes that some samples were taken by digging where easiest.
- Entries present sequential latitude and longitude values with associated distance markers for various sampling points.

## Dataset structure and content
- Each entry includes:
  - A label (e.g., LL A1, LL A2, LL B1, LL B2, HWA1, HWB, OV 7, WHA, WHB).
  - A distance field with values such as H, M, or numeric steps (2, 4, 8, 16, 32, 64).
  - Latitude and longitude values in N and W hemispheres, sometimes with varying formats (e.g., degrees, minutes with decimals; some entries show incomplete values).
- Spatial coverage appears to spread across multiple survey lines/areas, indicating a grid-like sampling pattern with increasing distances from a reference point.
- Some entries show complete coordinates, while others have missing longitude or incomplete fields, suggesting partial data capture or formatting inconsistencies.

## Data quality, provenance, and challenges
- GPS accuracy is stated as 4 meters, providing a baseline for positional precision.
- Practical field notes imply non-uniform data collection (e.g., “dig where easiest”), which may introduce sampling bias or gaps.
- Variability in coordinate formatting and occasional missing values indicate potential interoperability and standardization issues.
- Large and diverse set of lines/areas (LL, HW, OV, WH) implies a complex data environment with multiple source systems or collection methods.

## Data governance, metadata, and sharing
- The document highlights the need for consistent data governance when handling large, multi-source geospatial datasets.
- To enable discoverability and reuse, datasets should be accompanied by clear metadata describing:
  - Coordinate reference system and conversion methods (current formats shown; standardization recommended).
  - Meaning of distance codes (H, M) and the sequence logic for numeric steps.
  - Data collection methods, timing, and responsible data producers.
  - Handling of incomplete fields and any data cleaning performed.

## Implications and best practices for Data Stewards
- Ensure data provenance and lineage are captured, including who collected data, when, and using which instruments.
- Establish a data dictionary clarifying codes (e.g., H, M, LL, HW, OV, WH) and units of measure.
- Standardize coordinate formats (prefer decimal degrees) and confirm the referenced datum/CRS.
- Implement quality checks to identify and address missing values (e.g., missing longitudes) and formatting inconsistencies.
- Create procedures for timely data ingestion from field teams and for updating datasets as new samples are collected.
- Prepare data for publication and portal deposition with accompanying metadata and versioning.

## Recommendations and actions for data stewardship
- Develop and publish a data dictionary for all labels, distance codes, and coordinate formats used in the log.
- Validate and harmonize coordinate data into a consistent CRS and formatting standard.
- Annotate entries with timestamps, instrument details, and collection methodology to improve reproducibility.
- Implement data quality rules to flag incomplete records and guide remediation (e.g., missing longitude, inconsistent decimal formats).
- Document data lineage and sharing rules, including embargoes, accessibility, and update cadence.
- Upload the cleaned dataset to appropriate portals and maintain an accessible metadata catalog for discoverability.