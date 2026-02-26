# Errata for dataset http://doi.org/10.5285/047d914f-2a65-4e9c-b19109abf57423db

## Overview
- An error was found in the Met Office gridded monthly rainfall data for 1960–2000.
- The dataset is being superseded by UKCP18 data (expected March 2018), limiting available corrected versions from the original source.

## What was done (the fix)
- CEH derived monthly rainfall grids for the problematic period from Met Office daily rainfall grids.
- Recalculated the Standardised Precipitation Index (SPI) for the entire period using the corrected dataset.
- Added an extra 9-month accumulation period, identified as beneficial from user feedback on the previous dataset.

## Rationale
- Maintain data integrity and continuity in the face of data source updates and corrected measurements.
- Address user feedback to improve applicability and accuracy of the rainfall and SPI calculations.

## Implications for data governance and usage
- Users should reference the corrected monthly rainfall grids and the recomputed SPI values.
- Updated dataset version and metadata should reflect the derivation method (from daily data) and the new 9-month accumulation period.
- Be aware that the original source is superseded by UKCP18; the erratum provides an interim correction using the daily-derived grids.
- Documentation should note the data lineage, rationale for the fix, and the scope (1960–2000) to support transparency and reproducibility.