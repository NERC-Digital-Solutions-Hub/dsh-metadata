# Historic Droughts

## Project overview
- A four-year (2014–2018), £1.5 million UK Research Councils–funded project.
- Aimed to develop a cross-disciplinary understanding of past UK droughts to improve future drought management tools.
- Involved eight UK institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and the University of Oxford.
- Focused on integrating hydrometeorological, environmental, agricultural, regulatory, social, and cultural perspectives to characterise UK droughts since the late 19th century.

## Inventory purpose and structure
- The Historic Droughts Inventory is a knowledge base of past drought characteristics, drivers, impacts, and responses.
- Designed to provide a common reference for policymakers, regulators, water suppliers, agriculture, and industry to enable more consistent,Transparent planning.
- Comprises two main, complementary elements:
  - Hydro-meteorological timelines: rainfall, river flows, and groundwater indicators, with drought signals extended back to the 19th century via modelling and data rescue.
  - Drought references: records from newspapers, legislation, agricultural media, and oral histories that document drivers, impacts, responses, and how these have changed over time.
- References structure is aligned with, but adapted from, European Drought Impact Inventory (EDII) fields to cover a broad range of drought references beyond just impacts.

## Motivation and focus
- Investigates water resource system drivers and responses to droughts and water scarcity.
- Emphasizes the spatial and temporal distribution of reservoir construction across the UK to understand changes in water supply systems.

## Methods and data preparation
- Inventory designed to capture information about reservoir systems important for water supply.
- Prioritized data collection by storage volume, starting with the largest reservoirs.
- Key data relationships:
  - Upstream and downstream gauging information from the National River Flow Archive (NRFA).
  - Historic streamflow reconstructions (Smith et al. 2018) for UK gauges.
  - Historic reservoir storages held by the Centre for Ecology & Hydrology (CEH).
- Data quality varies; a flag system and notes section are used to document quality and gaps.
- Reservoirs included up to 1,600 Ml capacity (plus smaller reservoirs grouped with enough information), chosen because this captures about 90% of capacity under the Reservoirs Act 1975 threshold.

## Data sources and reference flow
- Primary data sources:
  - Environment Agency (Open Government Licence) Reservoir Safety data (via FOI requests).
  - UK Lakes Portal (CEH) and internet searches.
  - Hansard, government department records, water company records, journals, peer-reviewed and non-peer-reviewed books, and reputable websites/blogs.
- Data inclusion order and quality notes are documented in Figure 1 (reference selection process).
- All references used are compiled in HD_Inventory_of_UK_reservoirs_references.csv.

## Using the data (format and content)
- Data format: comma-separated values (CSV) with a companion references inventory CSV.
- Core columns (examples):
  - Reservoir, Description: reservoir name and description; sorted alphabetically.
  - Easting, Northing: OS grid coordinates.
  - Storage_vol: maximum reservoir volume (Ml).
  - Storage_vol_ref: reference to the storage volume data.
  - US_gauge_1, US_gauge_1_DF; US_gauge_2: upstream NRFA gauges; DS_gauge, DS_gauge_DF: downstream gauge information.
  - Planning_date, Planning_DF: planning year(s) with data quality flags.
  - Completion_date, Completion_DF: completion year(s) with data quality flags.
  - Res_type: reservoir type (impounding or non-impounding).
  - HD_recon_flow: NRFA gauge used in the Smith et al. reconstruction.
  - Timeseries: reservoir group affiliation (per CEH Monthly Hydrological Summary).
  - Inception_use: primary use at inception (Hydro-electric, Water resources, Drainage, Canal, Flood storage, Environmental).
  - Notes: extra information on drought-system linkages or data context.
  - Reference_ID: index linking to the corresponding reference in HD_Inventory_of_UK_reservoirs_references.csv.
- The inventory is designed to be easily filterable for cross-cutting analysis and map-based visualization.

## Practical GIS implications
- Provides a multi-source, spatially explicit dataset suitable for map-based analyses of drought history, reservoir infrastructure, and hydrometeorological indicators.
- Enables exploration of drivers and responses to droughts across space and time, supporting policy, planning, and resource management.
- Data integration considerations:
  - Coordinate system via OS grid (Easting/Northing).
  - Cross-referencing multiple sources with explicit data quality flags.
  - Linking hydro records (NRFA, reconstructions) with socio-economic and regulatory references.

## Licensing and references
- Data sources include Environment Agency materials (Open Government Licence) and the Smith et al. 2018 historic river flow reconstructions.
- All references used are contained within the HD_Inventory_of_UK_reservoirs_references.csv.