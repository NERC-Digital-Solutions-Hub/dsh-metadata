# Errata for dataset https://doi.org/10.5285/672f5522-7917-42fc-a80665cb5c1d2709

## Overview
- A few data points within the ECN dataset have been altered or removed following updated information from ECN site managers.
- Updates pertain to instrument error and/or coding changes.
- Data are removed only if clearly in error; apparent errors may represent valid outliers and are retained when appropriate.

## Implications for Data Leaders
- Data governance and provenance: document corrections, maintain versioning, and capture the rationale for changes.
- Data quality and integrity: distinguish between confirmed errors and potential valid outliers; avoid unnecessary removal without clear error.
- Metadata and discoverability: update metadata to reflect changes and ensure users can identify corrected vs original values.
- User impact and reproducibility: communicate changes to stakeholders; assess how corrections affect ongoing analyses and dashboards.

## Recommended Actions
- Update data catalogs and metadata to include the errata, with notes on which points were altered or removed.
- Establish or apply a protocol for data corrections (when to flag versus remove data points).
- Preserve historical versions to support auditability and reproducibility.
- Notify data users and teams about changes; review and adjust analytical workflows if needed.

## Risks and Considerations
- Risk of misinterpretation if changes are not clearly documented.
- Time-series continuity may be affected if data points are removed; ensure proper time indexing and downstream alignment.
- Ongoing instrument or coding issues may necessitate broader data quality reviews.