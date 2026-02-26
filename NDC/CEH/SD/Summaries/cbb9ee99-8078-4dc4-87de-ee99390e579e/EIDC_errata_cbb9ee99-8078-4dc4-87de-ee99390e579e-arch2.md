# Errata for dataset http://doi.org/bf48a9a3-7370-4114-9c4060af57a0c8bc

## Summary
- PSYM_GT75 and PSYM_ASSESSMENT columns in POND_SITE_INFO.csv were found to contain erroneous data.
- The corrected data have been applied in POND_SITE_INFO_V_0_1.csv.
- Erratum date: 28/10/16.

## Implications for environmental monitoring analysis
- Analyses relying on the affected columns may be impacted; users should switch to the updated file to ensure outputs reflect corrected values.
- Highlights the importance of data quality assurance and version control in monitoring datasets.

## Actions for analysts
- Adopt POND_SITE_INFO_V_0_1.csv for ongoing work; update references from the original POND_SITE_INFO.csv.
- Check and revise any dashboards, reports, or analyses that used the erroneous columns.
- Document the correction and maintain clear data provenance by referencing the erratum and the updated dataset version.