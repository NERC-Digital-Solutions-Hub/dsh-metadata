# Errata for dataset http://doi.org/10.5285/047d914f-2a65-4e9c-b19109abf57423db

## Summary of issue
- An error was found in the Met Office gridded monthly rainfall data for 1960–2000.

## Constraints and reason for workaround
- The Met Office cannot provide a corrected version of the monthly grids because the dataset will be superseded by UKCP18 data in March 2018.

## Fix implemented by CEH
- CEH derived monthly rainfall grids for the problematic period from Met Office daily rainfall grids.
- Recalculated the Standardized Precipitation Index (SPI) for the entire period using the corrected dataset.

## Additions and updates based on feedback
- Added an extra accumulation period of 9 months, identified from feedback on the superseded dataset.

## Implications for users
- SPI and related analyses for 1960–2000 are now based on the corrected daily-derived monthly rainfall data.
- Dataset is superseded by UKCP18; users should align with the newer data framework when possible.