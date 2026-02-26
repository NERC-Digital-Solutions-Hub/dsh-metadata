# Errata for dataset http://doi.org/10.5285/bf48a9a3-7370-4114-9c4060af57a0c8bc

## Overview
- Erratum documents erroneous data in the POND_SITE_INFO.csv file.
- Affected columns: PSYM_GT75 and PSYM_ASSESSMENT.
- Corrected data has been replaced in POND_SITE_INFO_V_0_1.csv.
- Date of the erratum: 28/10/16.

## Key corrections
- PSYM_GT75 and PSYM_ASSESSMENT data were found to be erroneous in POND_SITE_INFO.csv.
- Corrected values are now available in POND_SITE_INFO_V_0_1.csv.

## Implications for GIS workflows
- Any maps or analyses that used PSYM_GT75 or PSYM_ASSESSMENT from POND_SITE_INFO.csv may have reflected incorrect values.
- Updated dataset should be used to ensure accurate map symbology, filtering, and attribute-based queries.

## Recommended actions for GIS Specialists
- Replace references to POND_SITE_INFO.csv with POND_SITE_INFO_V_0_1.csv in data pipelines and map projects.
- Re-validate any maps or analyses that relied on PSYM_GT75 or PSYM_ASSESSMENT.
- Update documentation and data provenance to reflect the corrected file version.
- Implement version control and communicate the correction to stakeholders who accessed the previous dataset.

## Metadata and provenance
- Updated dataset file: POND_SITE_INFO_V_0_1.csv.
- Original issue date of the erratum: 28/10/16.