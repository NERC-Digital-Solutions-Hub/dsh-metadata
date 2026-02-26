# River Data Table with NRFA Site Metadata

- A large, multi-site dataset of river catchments and NRFA (National River Flow Archive) sites, with codes such as AVON, AYR, BEAU, CLWY, CONW, CREE, DART, EDEN, ESK, FORT, GREA, TYNE, TYWI, etc.
- Each site entry includes a wide range of attributes at the catchment/site level, intended to support data governance, discovery, and reuse by researchers, policymakers, and data users.

## Scope and purpose

- Documents site-level characteristics and metadata to support governance, usability, and discoverability of river-related data across many UK catchments.
- Aims to provide standardized information that data stewards can use to validate, catalog, and share datasets with proper context and limitations.

## Data structure and content (high level)

- Site identifiers: NRFA/site codes (e.g., AVON, AYR, BEAU, CLWY, CONW, CREE, DART, etc.), often paired with grid references or location descriptors.
- Spatial and geographic descriptors:
  - Catchment area figures (hectares, often noted as ha).
  - Grid references and location descriptors (e.g., SH, SJ coordinates, specific grid codes).
  - Altitude/elevation values (in meters) for sites.
- Land cover and habitat attributes:
  - Land cover categories (e.g., Coniferous, Broadleaf woodland, Fen, marsh & grassland, Freshwater, Hedgerow, Urban areas, Suburban, etc.).
  - Occasional notes on habitat types associated with sites (e.g., calcareous, peat soil areas, marshland types).
- Hydrological and environmental measurements:
  - Hydrological indices and indicators (e.g., BFI/BBI-like metrics, rainfall-related values in mm, other numeric environmental measures).
  - Seasonal/annual statistics and related numeric fields.
- Indicators and flags:
  - TRUE/FALSE fields indicating presence/validity or status of certain attributes.
  - Some fields appear to be missing (represented by dots or blanks) or contain mixed data formats.
- Data richness:
  - The dataset presents a dense, field-heavy table with numerous numeric columns per site, suggesting a comprehensive suite of environmental and hydrological attributes across many sites.

## Key governance and data quality considerations

- Metadata completeness:
  - Many fields exist, but some entries are incomplete or missing; ensure complete field definitions and documented gaps.
- Standardization:
  - Units (ha, mm, m) and field naming should be consistently defined across all sites to ensure comparability.
  - Habitat and land-cover categories should map to a controlled vocabulary.
- Provenance and versioning:
  - Track data sources, collection dates, and any transformations applied to raw inputs.
  - Maintain a data lineage to support reproducibility.
- Data freshness and updates:
  - Establish update cadence and embargo rules (if any) for sharing updated site information.
- Interoperability:
  - Data appear to span multiple systems and formats; implement a common schema or mapping to a unified data model for easy ingestion into data portals.
- Accessibility and discoverability:
  - Ensure catalog metadata (descriptions of each field, units, and permissible values) is available in portals so users can search and interpret site records correctly.
- Privacy and governance:
  - While primarily environmental data, confirm any sensitivities or embargoes related to specific locations or commercial data.

## Ingestion, sharing and stewardship actions

- Define and publish a data dictionary detailing each field, its unit, permissible values, and meaning.
- Normalize units and harmonize categorical codes (habitats, land cover) across all sites.
- Validate completeness per site, flag missing or ambiguous fields, and establish remediation workflows with data creators.
- Catalog the dataset in relevant portals with rich metadata to support discovery by data users.
- Implement data update procedures and version control to reflect changes and corrections over time.
- Document any data-sharing restrictions, embargo periods, or licensing terms.

## Use cases and applicability

- Cross-site hydrological and environmental analyses across UK rivers and catchments.
- Longitudinal studies tracking changes in land cover, habitat distribution, and hydrological indices across multiple NRFA sites.
- Data discovery and governance workflows for organisations managing large datasets of river-related information.
- Data stewardship exercises to improve metadata quality, interoperability, and reusability of site-level environmental data.

## Key challenges highlighted for Data Stewards

- Incomplete or evolving user needs for site-level metadata and discovery.
- Timely receipt of data from multiple data creators across diverse systems.
- Encouraging data creators to conform to metadata and standardization standards.
- Handling diverse formats and complex, large-scale datasets with numerous site attributes.
- Maintaining interoperability with legacy and updated databases while ensuring data can be easily shared and reused.