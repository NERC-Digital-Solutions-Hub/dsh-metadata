# Buildings, infrastructure, and population in the potentially impacted areas by glacier lake outburst floods of Tsho Rolpa, Nepal, 2020: supporting document

## Overview
- Dataset identifies exposed objects at flooding risk from Tsho Rolpa Lake (downstream area around 27.5–27.85 N, 86.17–86.48 E; projection: WGS 1984 Transverse Mercator).
- Spatially corrected to align with high-resolution imagery from Google Earth; exact spatial accuracy not quantified due to lack of reference data.
- Exposure analysis covers multiple features (buildings, agriculture, roads, schools, hospitals, etc.) under various glacial lake outburst flood (GLOF) scenarios; includes a detailed exposure table.

## Data Content and Structure
- Data formats:
  - Agriculture land: a single TIFF file (resolution 30 m × 30 m).
  - Buildings, Infrastructure, Road: three shapefiles (points for buildings/infrastructure, lines for roads).
- Dataset comprises exposure estimations under different GLOF scenarios (final breach depths and water levels) for multiple object types (e.g., buildings, roads, schools, hospitals, parks, commercial outlets, and various business categories).
- Exposure values are presented per scenario and per object type (e.g., number of buildings affected, area for agriculture, length of road inundated, and estimated impacts on facilities).

## Collection Methods and Provenance
- Scenario creation: simple dam breach model to generate GLOF scenarios; flood dynamics simulated with a high-performance hydrodynamic model.
- Socioeconomic and exposure data sources: OpenStreetMap, Google Earth, and other global data products.
- Exposure identification: overlay predicted flood inundation maps with processed exposure datasets to locate affected objects.

## Quality Control and Data Quality
- Building data primarily from OpenStreetMap; positions cross-checked against sub-meter imagery in ArcGIS and Google Earth.
- Inundation area for the worst-case scenario revealed several missing buildings; these were manually mapped and corrected.
- Spatial accuracy is not quantified; corrections were made to align with high-resolution imagery.
- Data representations:
  - Agriculture land: raster (30 m resolution).
  - Buildings and infrastructure: point features.
  - Roads: line features.

## Analytical Methods
- Exposure assessment performed by overlaying predicted flood inundation maps with exposure datasets to identify affected objects.
- The dataset includes detailed scenario-based exposure estimates (e.g., final breach depths, water levels) across multiple land-use and infrastructure categories.

## Details of Data Structure
- 1 raster file: Agriculture land (TIFF, 30 m resolution).
- 3 vector files: Buildings (points), Infrastructure (points), Road (lines).

## Governance and Stewardship Considerations for Data Stewards
- Metadata and provenance:
  - Document data sources, modeling methods (dam breach and hydrodynamic modeling), temporal coverage (2020), projection, and explicit data lineage.
  - Record any manual corrections and the rationale behind them; note limitations in spatial accuracy.
- Data quality and interoperability:
  - Capture accuracy notes, especially where features were missing and subsequently added manually.
  - Maintain consistent coordinate reference system (WGS 1984 TM) and file formats (TIFF and shapefiles) to support interoperability.
- Access, licensing, and updates:
  - Specify usage rights, licensing, and any sharing restrictions.
  - Define update cadence and versioning to reflect new or corrected flood exposure data.
- Documentation and usability:
  - Include a clear description of the exposure table and scenario definitions to ensure datasets are usable by data users with diverse needs.
  - Provide guidance on how to reproduce the overlay analysis and how to interpret the scenario-based results.
- Data maintenance actions (operational items):
  - Maintain a data lineage log for all corrections and additions.
  - Ensure future updates (new imagery, revised models) are integrated with proper metadata and version control.