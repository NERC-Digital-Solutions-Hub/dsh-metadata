# 01_GEE_Code

## Overview
- Folder contains JavaScript code to export binary images for the Abulug active river channel at 2-year intervals using Google Earth Engine (GEE).

## Files
- GEE_Code_Abulug_Deprecated.txt: Original code that uses Landsat Collection 1 (deprecated).
- GEE_Code_Abulug_Migrated.txt: Modified code migrated to Landsat Collection 2.

## Migration and data implications
- Migration to Landsat Collection 2 updates the workflow to current data standards and accessibility.
- Deprecated version relies on Landsat Collection 1, which is no longer supported.

## How this supports data use
- Enables systematic generation of binary imagery for the Abulug river channel at regular 2-year steps, suitable for temporal analysis and downstream data products.
- Provides a repeatable, end-user-accessible script in GEE for data extraction and export.

## Considerations for data support
- Recommend adopting the migrated code for ongoing use to ensure compatibility with current Landsat data.
- Potential next steps: document usage instructions, data outputs, and any required GEE credentials or permissions.