# 01_GEE_Code

- Overview
  - Folder contains JavaScript code to export binary images for the Abulug active river channel at 2-year intervals.

- File Versions and Migration
  - GEE_Code_Abulug_Deprecated.txt: original code using Landsat Collection 1 (deprecated).
  - GEE_Code_Abulug_Migrated.txt: updated code migrated to Landsat Collection 2.

- Governance and Metadata Implications
  - Deprecation of Landsat Collection 1 necessitates updating sources to maintain reproducibility.
  - Migration to Collection 2 improves alignment with current data standards.
  - Recommend adding versioned metadata: data source (Landsat Collection 2), processing steps, interval (2-year), and code version.

- Data Quality, Format, and Reproducibility
  - Binary image export implies downstream analysis requirements; ensure compatibility of outputs with targets.
  - Document assumptions, processing steps, and any dependencies (e.g., Google Earth Engine).

- Sharing, Access, and Lifecycle
  - Ensure code is accessible in catalogues/portals with clear provenance and usage notes.
  - Include licensing/usage terms for Landsat data and for the code itself; maintain an audit trail of updates.

- Recommended Actions for Data Stewards
  - Implement proper versioning and change logs for both deprecated and migrated code.
  - Attach comprehensive metadata (title, creators, data sources, methodology, update frequency).
  - Validate migrated code yields consistent results and update related documentation as needed.