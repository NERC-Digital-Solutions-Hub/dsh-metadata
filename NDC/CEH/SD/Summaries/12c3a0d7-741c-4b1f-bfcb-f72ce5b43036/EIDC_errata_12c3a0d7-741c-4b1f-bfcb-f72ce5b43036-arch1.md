# Errata for dataset https://catalogue.ceh.ac.uk/documents/12c3a0d7- 741c-4b1f-bfcb-f72ce5b43036

## Overview
- This document announces an erratum: NoData values were incorrect in the SPI18 and SPI24 data files within the referenced dataset.

## Implications for analysis
- Incorrect NoData values can affect missing-data handling, data quality assessment, and analyses that rely on SPI18 and SPI24.
- Potential impacts include biased results, incorrect null-value treatments, and reproducibility concerns if the erroneous values were used in analyses or reported figures.

## Recommended actions for analysts
- Retrieve the corrected SPI18 and SPI24 data files from the CEH dataset repository.
- Update your data processing pipelines to use the corrected NoData values and re-run analyses that used SPI18 or SPI24.
- Reproduce key results, figures, and metadata conclusions; update documentation to reflect the correction.
- Verify consistency with the dataset’s metadata to ensure correct interpretation of the NoData code.

## Data management and provenance
- Document the erratum in project records, citing the corrected dataset version.
- Maintain versioned datasets and clearly indicate which analyses were reworked due to the correction.

## Verification steps
- Check the NoData value definitions in the metadata after replacement.
- Compare missing-value counts before and after applying the corrected files to ensure alignment with expectations.