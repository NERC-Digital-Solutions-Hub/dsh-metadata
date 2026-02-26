# Errata for dataset http://doi.org/047d914f-2a65-4e9c-b19109abf57423db

## Overview
- An error was found in the Met Office gridded monthly rainfall data for 1960–2000.

## Remediation and actions taken
- The Met Office cannot provide a corrected version of the monthly grids because the dataset will be superseded by UKCP18 in March 2018.
- CEH created a fix by deriving monthly rainfall grids for the problematic period from the Met Office daily rainfall grids.
- CEH recalculated the Standardized Precipitation Index (SPI) for the entire period using this derived dataset.
- An extra 9-month accumulation period was added based on user feedback on the superseded dataset.

## Data provenance and transformations
- Source: Met Office daily rainfall grids; issue identified in the 1960–2000 monthly grids.
- Derivation: monthly grids derived from daily grids for the problematic period.
- Outputs: corrected monthly rainfall grids; recalculated SPI; added 9-month accumulation.

## Data quality and limitations
- We rely on a derived dataset due to unavailability of corrected original data; this may affect comparability with other official monthly grids.
- Dataset is superseded by UKCP18; users should note the replacement status and provenance.

## Metadata, documentation, and governance
- Documentation should capture: reason for erratum, data sources, transformation steps, updated accumulation period, and versioning/lineage.
- Record the supersession status and the relationship to UKCP18 for future governance and user guidance.

## Implications for data stewardship
- Update catalogs and metadata to reflect the correction and use of derived data for 1960–2000.
- Clearly communicate the change to data users, maintain provenance, and monitor for any further updates or supersession.