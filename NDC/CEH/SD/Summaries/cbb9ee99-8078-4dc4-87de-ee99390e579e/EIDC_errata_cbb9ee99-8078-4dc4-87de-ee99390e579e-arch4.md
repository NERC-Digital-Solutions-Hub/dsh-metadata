# Errata for dataset http://doi.org/doi.org/bf48a9a3-7370-4114-9c4060af57a0c8bc

- Issue identified: The data in two columns of POND_SITE_INFO.csv were erroneous (PSYM_GT75 and PSYM_ASSESSMENT).
- Correction: The erroneous data have been replaced in the file POND_SITE_INFO_V_0_1.csv.
- Effective date: 28/10/16.

Implications for Data Leaders

- Data quality improvement: An updated version of the pond site info dataset is now available to replace the faulty data.
- Impact on analyses: Any analyses or dashboards using PSYM_GT75 or PSYM_ASSESSMENT should be reviewed and potentially re-run with POND_SITE_INFO_V_0_1.csv.
- Metadata and provenance: Update data catalogs, documentation, and provenance records to reflect the corrected columns and the new file version.
- Data governance: Reinforce versioning and change-notice processes to capture similar corrections in the future.

Recommended actions

- Replace references to POND_SITE_INFO.csv with POND_SITE_INFO_V_0_1.csv in data pipelines and analyses.
- Re-validate results that used PSYM_GT75 and PSYM_ASSESSMENT; flag any discrepancies due to the correction.
- Communicate the correction to stakeholders and ensure discoverability of the updated dataset version.