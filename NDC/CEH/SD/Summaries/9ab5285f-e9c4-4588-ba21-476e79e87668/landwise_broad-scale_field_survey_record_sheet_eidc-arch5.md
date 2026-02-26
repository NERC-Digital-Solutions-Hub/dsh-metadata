# LANDWISE Broad-scale Field Survey - Record Sheet

## Purpose and Scope
- A structured data collection form to capture field-scale land-use, soil/geology, and management information for broad-scale surveys.
- Supports data discovery and reuse by providing standardized fields and metadata for datasets managed by organisations with large numbers of records.
- Facilitates provenance, comparability, and governance across datasets by documenting site, field, and management details.

## Key Data Elements (Data Model)

- Identifiers and temporal/spatial context
  - Site name, Field name, Field/plot information
  - Date (DD/MM/YY), Field no.
  - Any unrepresentative field areas, Last ploughed

- General observations
  - Surface form and slope descriptors (flat, gentle, steep, undulating; furrowed/mounded, etc.)
  - Surface condition (unslaked to slaked, poached ground, tramline wheelings/ruts)
  - Erosion or deposition features
  - Sampling location information (additional details)

- LANDWISE Soil and Geology Class
  - Soil type descriptors (e.g., shallow over chalk/limestone, free draining loamy over chalk/limestone, impeded drainage loamy/clayey over chalk/limestone, etc.)
  - Deposits and overlying materials (e.g., gravel over mudstone)
  - Drainage status and groundwater characteristics
  - Landform context (floodplain, high groundwater, etc.)

- Land use and management (broad categories)
  - Land use types (Arable rotation with grass vs. without grass, Grassland, Woodland)
  - Specific management practices by land use (e.g., field drainage, buffer strips, organic/conventional status, organic amendments, cover crops, herbal leys)
  - livestock and grazing details (stocking density, mob/paddock grazing, stock out-wintered)
  - Crop types and rotations (including grass-only rotations, not just grass as break crops)
  - Management history and land-use history
  - Flooding history, water/ sediment runoff considerations
  - Tillage regime (conventional, minimum, none), Controlled traffic, tramline width/spacing
  - Age of field system, path management
  - Liming (noted as limed)

- Management practices by land category (detailed)
  - Arable: specific practices, crop rotations, drainage, cover crops, etc.
  - Woodland: drainage, management status, etc.
  - Grassland: grazing regimes, stocking density, cover crops, organic/conventional, etc.

## Data Quality and Governance Considerations
- Importance of standardized vocabularies for land-use types and soil/geology classes to ensure interoperability between datasets.
- Provenance: capture of date, field number, site/field identifiers, and unrepresentative areas to contextualize records.
- Completeness and consistency: key fields (dates, field numbers, soil class, management practices) should be complete and align with controlled terms.
- Update and versioning: mechanisms to reflect ongoing data updates and changes to management records or soil classifications.
- Handling of large datasets: plan for storage, transfer, and cataloguing to ensure timely sharing and discovery.
- Documentation of anomalies: note duplications or potential data entry issues (e.g., repeated “Limed?”) to maintain data quality.

## Practical Implications for Data Stewards
- Support for data discovery portals by providing structured, taggable fields (e.g., land-use types, soil classes, drainage status).
- Facilitate metadata completeness, including site, field, date, and sampling location information.
- Encourage adoption of consistent, machine-readable codes for categories (e.g., land use, soil class, management practices) to improve interoperability across systems.
- Ensure update workflows align with data users’ needs, including versioning of record sheets and field plots.
- Provide guidance on documenting non-standard or bespoke measurements and field observations to maintain usable records over time.