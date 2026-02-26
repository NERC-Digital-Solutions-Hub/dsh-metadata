# 10km occurrence data for terrestrial mammals in Great Britain and Northern Ireland, 1960-1992 & 2000-2016, as mapped in the 2020 Mammal Atlas

## Aim and scope
- Provides summarised 10km grid square occurrence data for terrestrial mammals across Great Britain and Northern Ireland, covering the atlas recording periods 1960-1992 and 2000-2016 (with some species using shorter periods).
- Excludes cetaceans from the dataset; cetacean data are provided separately via Sea Watch.
- Supports analysis of distribution changes since the 1993 atlas and informs related conservation outputs.

## Background and contributors
- Produced by the Mammal Society with assistance from Sea Watch Foundation, Biological Records Centre, UK Centre for Ecology and Hydrology, and the Staffordshire Mammal Group.
- Built on the MaWSE project and its Mammal Tracker app, expanding to UK-wide data collection.

## Data collection and validation
- Sources: National Biodiversity Network (NBN) gateway (NBN Atlas), local biological records centres, local and national monitoring schemes, Natural England, Mammal Society, Biological Records Centre, Sea Watch Foundation, iRecord, and Mammal Tracker app.
- Data types: Predominantly opportunistic citizen science records; includes structured surveys and professional surveys.
- Quality assurance:
  - External datasets often pre-validated before submission; Mammal Society verifiers validate iRecord and Mammal Tracker data.
  - Some datasets (not mammal-focused) may contain dubious records; to mitigate risk, only records for widespread species from these datasets were included.
  - Species experts review 10km square maps; any highlighted squares trigger record-level verification to determine retention or exclusion.
- Cetaceans: Cetacean data were not integrated into the atlas database; maps for these species are produced by Sea Watch separately.

## Dataset structure and formats
- CSV dataset:
  - Fields per row include SPECIES (scientific name), COMMON_NAME, GRIDREF, CATEGORY (time-period coverage: 1960-1992; 2000-2016; or both), TP_1960_1992, TP_2000_2016, LATITUDE, LONGITUDE, and country indicators (ENG, SCO, WAL, N_IRE, CI, ROI).
  - Grid references use OGB for GB, OSI for Northern Ireland, and truncated MGRS for Channel Islands; several grid references are mapped to the closest country.
  - Notes on time periods: three species used shortened periods (Water vole 2005-2016; Red squirrel 2010-2016; Grey squirrel 2010-2016).
- Geopackage (gpkg):
  - Contains the same data as separate layers per species, with 10km square boundaries as polygons.
  - Coordinate system: OSGB 36 (EPSG: 27700) for the British grid; Northern Ireland and Channel Islands squares re-projected to align with the British Grid.
  - Each polygon layer includes identical attribute fields as the CSV.

## Data provenance and governance
- Data provenance: Aggregated from diverse sources with varying collection methods and QA processes; effort to document and validate at both record and square levels.
- Metadata and use: Dataset details include country attribution for grid squares, grid reference systems used, and time-period categorisations to support reproducibility and data reuse.
- Availability and reuse: Provided in both CSV and GeoPackage formats to facilitate use in GIS and data analyses; suitable for national and regional conservation planning and research.

## Practical notes for data stewards
- Acknowledge the heterogeneity of data sources and varying QA standards; maintain clear documentation of validation steps and criteria for inclusion.
- Ensure ongoing updates are managed with consistent metadata, especially when incorporating new recording periods or new sources.
- Maintain transparency about limitations, such as potential recording biases from opportunistic data and the distinction between atlas-level validation and dataset-level verification.
- For cetacean data inquiries, refer to Sea Watch as the primary contact, since cetacean records are not included in this dataset.

## References
- Arnold, H. (1993). Atlas of mammals in Britain. HMSO.
- Hayhow, D.B. et al. (2019). The State of Nature 2019.
- Mathews, F. et al. (2018). A Review of the Population and Conservation Status of British Mammals.
- Mathews, F., & Harrower, C. (2020). IUCN-compliant Red List for Britain's Terrestrial Mammals.