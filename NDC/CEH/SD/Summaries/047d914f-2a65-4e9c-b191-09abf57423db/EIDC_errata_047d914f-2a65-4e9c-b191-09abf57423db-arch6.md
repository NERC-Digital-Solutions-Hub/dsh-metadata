# Errata for dataset http://doi.org/047d914f-2a65-4e9c-b19109abf57423db

## Overview
- An error was found in the Met Office gridded monthly rainfall data for 1960–2000.
- The Met Office cannot provide a corrected version; the dataset will be superseded by UKCP18 data in March 2018.
- As a fix, CEH derived monthly rainfall grids from the Met Office daily rainfall grids for the problematic period.
- CEH recalculated the SPI (Standardised Precipitation Index) for the entire period using this newly corrected dataset.
- An extra 9-month accumulation period was added based on feedback from users.

## What was wrong
- Erroneous monthly rainfall grids for 1960–2000 in the Met Office dataset; specifics of the error are not detailed here.

## What was done to fix
- Derived monthly rainfall grids from Met Office daily rainfall grids for the affected period.
- Recalculated SPI for 1960–2000 using the corrected monthly data.
- Added a 9-month accumulation period to the dataset in response to user feedback.

## Data products impacted
- Monthly rainfall grids for 1960–2000 (re-derived from daily data).
- SPI values for the entire period (recalculated).
- Introduction of a 9-month accumulation period.

## Implications for users
- Analyses using the 1960–2000 monthly rainfall and SPI should refer to the corrected dataset.
- Results may differ from those produced with the original, flawed monthly grids.
- The dataset context remains that UKCP18 will supersede older datasets in 2018.

## Recommendations for Data Support
- Ensure metadata clearly documents the derivation method (daily-to-monthly conversion) and the addition of the 9-month accumulation period.
- Communicate that a retrospective correction was made and advise re-running analyses if applicable.
- Maintain versioning information to help users distinguish between pre- and post-correction data.

## Provenance and versioning
- Correction carried out by CEH because the original Met Office data could not be corrected directly; dataset is anchored to UKCP18 supersedence in March 2018.
- Updated monthly grids and SPI recalculation, with a new 9-month accumulation feature added.