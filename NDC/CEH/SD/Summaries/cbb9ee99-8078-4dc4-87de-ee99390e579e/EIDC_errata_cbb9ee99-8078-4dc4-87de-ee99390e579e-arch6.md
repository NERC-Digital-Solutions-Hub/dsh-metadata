# Errata for dataset http://doi.org/10.5285/bf48a9a3-7370-4114-9c4060af57a0c8bc

## Summary
- Two columns in POND_SITE_INFO.csv were found to contain erroneous data: PSYM_GT75 and PSYM_ASSESSMENT.
- Corrected data have been incorporated into a new file: POND_SITE_INFO_V_0_1.csv.
- Erratum date: 28/10/16.

## What changed
- Columns corrected: PSYM_GT75, PSYM_ASSESSMENT.
- Revised dataset version: POND_SITE_INFO_V_0_1.csv.

## Impact for data users
- Analyses using the affected columns should reference the updated file/version.
- Results may change; consider re-running analyses or updating dashboards/reports that rely on these fields.
- Update data provenance, metadata, and any code or workflows to point to POND_SITE_INFO_V_0_1.csv.

## Data quality and governance notes
- Indicates a data quality issue was identified and addressed via versioned file replacement.
- Highlights importance of version control and clear provenance for datasets.

## Recommendations for data support
- Provide access to the corrected file and confirm the availability of POND_SITE_INFO_V_0_1.csv.
- Offer assistance with reprocessing analyses, validating outputs, and updating documentation that references the previous dataset version.