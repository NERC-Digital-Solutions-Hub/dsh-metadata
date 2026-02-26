# River Baseline Data Table (NRFA and related attributes)

- What this document is
  - A large, multi-site data table listing river basins and sub-sites (e.g., AVON, AYR, BEAU, CLWY, CONW, CREE, etc.) with a dense set of attributes per site.
  - Combines spatial references, land-cover/habitat extents, climate/hydrology indicators, and metadata flags.

- Key components and data types
  - Site identifiers and locations
    - River/basin codes and sub-site numbers (e.g., AVON 1–6, AYR 1–6, etc.)
    - Spatial references such as grid references and coarse coordinates (e.g., SH801580), sometimes accompanied by altitude (m).
  - Habitat and land-cover extents (hectares)
    - Fen, marsh & grassland (ha) with various sub-entries (Improved, etc.)
    - Broadleaf woodland (ha); Coniferous (ha); Neutral/acid grassland; Bog; Heather/heather grassland; Freshwater; Swamp; Suburban/Urban (ha) and related classifications.
    - Arable & horticulture (ha); Peat soil area (ha); Various land-cover combinations for each site.
  - Environmental and climatic indicators
    - Rainfall (mm) and other numeric climate/hydrology fields
    - Altitude (m); BFI (likely Base Flow Index) and other hydrological metrics
  - Data quality and metadata indicators
    - Boolean-like fields (TRUE/FALSE) and several missing/value placeholders (e.g., ., -), indicating incomplete data in many cells
    - Some rows repeat values across sub-sites, with occasional gaps or inconsistent formatting

- Structural observations
  - The table is highly granular, with many sites containing multiple sub-entries (up to 6 per site in the sample).
  - Data appears to be a raw extraction from a broader NRFA/environmental dataset, with a mix of numeric measurements, coordinates, and categorical indicators.
  - Presence of numerous missing values and non-uniform formatting across fields suggests variable data quality and completeness.

- Implications for Data Leaders
  - The dataset is potentially valuable for holistic, system-wide data governance and analytics, but requires standardization and quality controls to be production-ready.
  - Data discovery is challenging due to scattered site codes and inconsistent metadata; centralization would improve usability and collaboration with external partners.
  - Integration with downstream analytics (e.g., habitat assessment, hydrological modeling) depends on consistent units, complete metadata, and validated spatial references.

- Recommendations for next steps
  -Create a standardized data dictionary and unit conventions for all habitat, land-cover, and hydrological fields.
  -Implement data quality checks to address missing values, inconsistent formats (dots, dashes, TRUE/FALSE), and duplicated entries.
  -Develop a centralized metadata catalog with clear spatial references (CRS), coordinates, and grid references, plus provenance and update cadence.
  -Validate and harmonize spatial data (coordinates, grid refs) and align to a common coordinate reference system.
  -Assess data access and governance considerations, including any paywalls or restrictions, and establish clear data-sharing practices with partner networks.