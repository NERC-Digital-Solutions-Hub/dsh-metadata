# 01_GEE_Code

## Overview
- Folder contains JavaScript code to export binary images for the Abulug active river channel at 2-year intervals.
- Contains two files: a deprecated version and a migrated version.

## Files Included
- GEE_Code_Abulug_Deprecated.txt: original code using Landsat Collection 1 (now deprecated).
- GEE_Code_Abulug_Migrated.txt: modified code migrated to Landsat Collection 2.

## Migration Details
- Landsat Collection 1 has been deprecated.
- Migrated code updates to Landsat Collection 2 to ensure continued compatibility and data availability.

## Usage Notes
- Intended for use in Google Earth Engine (GEE) JavaScript environment.
- Produces binary image outputs representing the Abulug river channel at 2-year intervals.

## Considerations for GIS Specialists
- When upgrading, verify that Landsat Collection 2 data aligns with project needs (resolution, availability, and metadata).
- Check for any changes in asset IDs, image collection naming, or processing steps introduced in the migrated code.
- Confirm the definition of “binary images” (thresholding or masking criteria) remains consistent after migration.

## Potential Implications and Risks
- Data gaps may persist due to cloud cover or Landsat revisit timing, even with the migration to Collection 2.
- Ensure downstream workflows accommodate any changes in data properties from Collection 1 to Collection 2.