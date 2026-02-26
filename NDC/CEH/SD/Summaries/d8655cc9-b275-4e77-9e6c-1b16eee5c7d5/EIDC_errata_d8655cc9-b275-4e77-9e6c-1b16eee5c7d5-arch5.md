# Errata for dataset http://doi.org/10.5285/d8655cc9-b275-4e779e6c-1b16eee5c7d5

## Overview
- An error was found in the Met Office gridded monthly rainfall data for 1960–2000.
- The Met Office cannot provide a corrected version now because the dataset will be superseded by UKCP18 in March next year.
- As a fix, CEH derived monthly rainfall grids from the Met Office daily rainfall grids for the problematic period.
- CEH recalculated the Standardized Precipitation Index (SPI) for the entire period using the newly derived corrected dataset.
- An extra 9-month accumulation period was added based on feedback related to the superseded dataset.

## Data lineage and processing
- Original source: Met Office gridded monthly rainfall data (1960–2000).
- Derived data: Monthly rainfall grids computed from Met Office daily rainfall grids for the affected period.
- Calculations: SPI recalculated for the full period using the corrected dataset.

## Corrections and additions
- Correction approach: Re-derive monthly grids from daily data rather than correcting the monthly series directly.
- Additional update: Include a 9-month accumulation period identified as useful from user feedback.

## Versioning, governance, and access
- The affected dataset will be superseded by UKCP18 in March next year; this has implications for versioning and future updates.
- Practitioners should note the corrected data as the authoritative version for analyses covering 1960–2000 and be aware of the impending UKCP18 changes.

## Implications for data users
- Previous analyses using the original monthly grids and SPI for 1960–2000 may be affected; use the corrected dataset for updated results.
- Documentation and metadata should reflect the data derivation, updated SPI calculations, and the added 9-month accumulation period.
- Users should reference the corrected dataset and be aware of the new data lineage and justification for changes.

## Implications for data stewards
- Update metadata to capture data lineage, derivation method (from daily data), and rationale for the 9-month accumulation period.
- Maintain clear versioning and communication about the transition to UKCP18.
- Ensure accessibility of the corrected dataset and any related revisions to SPI, including notices about changes from the superseded dataset.