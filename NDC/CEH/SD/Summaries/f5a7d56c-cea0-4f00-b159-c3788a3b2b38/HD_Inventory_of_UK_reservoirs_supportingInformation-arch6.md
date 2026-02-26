# Historic Droughts

## Scope and Aim
- Four-year project (2014–2018) with £1.5m funding to develop cross-disciplinary understanding of UK droughts and create tools for better drought management.
- Eight UK institutions collaborated: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, and University of Oxford.
- Goal: combine hydrometeorological and social perspectives to understand droughts and water scarcity more comprehensively and support future decision-making.

## Context and Significance
- Droughts and water scarcity threaten livelihoods and wellbeing in the UK, with pressures from population growth and resource exploitation.
- DWS events are shaped by both natural factors and socio-economic/regulatory influences (e.g., consumption patterns, licensing).
- Emphasizes need for links between hydrometeorological data and social/regulatory systems to improve drought management.

## The Historic Droughts Inventory
- A knowledge base of past drought characteristics, drivers, impacts, and responses, designed as a common reference for policymakers, regulators, water suppliers, agriculture, and industry to enable consistent planning.
- Comprises two integrated elements:
  1) Hydro-meteorological timelines of rainfall, river flows, and groundwater with consistent drought indicators, extended back to the 19th century via modelling and data rescue.
  2) References to past droughts (19th century to present) from newspapers, legislation, agricultural media, and oral histories, formatted with time/place and links to full sources.
- Structure of references follows adapted fields from the European Drought Impact Inventory (EDII) for broad drought reference coverage, not limited to impacts.

## Motivation
- Aims to study water resource system drivers and responses, focusing on the spatial and temporal distribution of reservoir construction on a national scale.
- Seeks a coherent reservoir dataset to analyze changes over time and investigate drivers of system change.

## Methods
- Inventory’s primary purpose is to capture information about reservoir systems important to water supply; prioritises larger, more strategically important reservoirs by storage volume, starting with the largest.
- Designed to support analysis of storage, inflows, and outflows; integrates upstream/downstream gauging information from NRFA and historic flow reconstructions (Smith et al. 2018); signposts links to linked datasets (e.g., CEH reservoir storages).
- Notes section captures additional information not fit into primary data columns.
- Data quality is variable; a flag system and references are used to communicate quality and provenance.

## Preparation
- Data sources include Environment Agency (Open Government Licence via FOI) and the UK Lakes Portal (CEH), supplemented by internet searches.
- Data quality acknowledges variability; references are provided for all information; a data-flag system communicates confidence levels.
- Reservoirs included up to 1,600 Ml capacity, plus smaller reservoirs within groups where historic storage and planning/construction data exist. The 1,600 Ml threshold reflects data availability and coverage of Reservoirs Act 1975 context (approx. 90% of reservoirs by capacity).
- Source hierarchy used to assess data quality: Hansard, government department records, water company records, journals, peer-reviewed books, non-peer reviewed books, and online sources (with preference for referenced items).

## Using the Data
- The inventory is delivered as CSV files, accompanied by a References CSV (HD_Inventory_of_UK_reservoirs_references.csv) to be used together.
- Key columns in the reservoir inventory (examples):
  - Reservoir, Description; Easting, Northing (grid coordinates)
  - Storage_vol (maximum reservoir capacity in megalitres)
  - Storage_vol_ref (reference to the data source)
  - Upstream/downstream gauge IDs (US_gauge_1, US_gauge_2, DS_gauge) and their data flags
  - Planning_date, Completion_date and their data flags (Planning_DF, Completion_DF)
  - Res_type (impounding or non-impounding)
  - HD_recon_flow (NRFA gauge used for flow reconstruction)
  - Timeseries (reservoir group or usage context)
  - Inception_use (primary use at inception: hydro-electric, water resources, drainage, canal, flood storage, environmental)
  - Notes (qualitative context on drought-system links or other information)
  - Reference_ID (links to HD_Inventory_of_UK_reservoirs_references.csv)
- The references inventory provides source details for each data point, enabling traceability and quality assessment.
- The design emphasizes easy filtering and data extraction to support cross-sector analyses and decision-making.

## How This Supports Data Use
- Provides a shared, multi-sector reference framework for drought history, drivers, and responses.
- Enables self-serve exploration of reservoir system changes, storages, and related hydrometeorological data alongside regulatory and policy contexts.
- Facilitates integration with other datasets (e.g., NRFA flow data, Smith et al. 2018 reconstructions) to analyze drivers of system change and historical drought behavior.

## References
- Environment Agency (2017) Reservoir Safety. Available online.
- Smith, K.A., Tanguy, M., Hannaford, J., & Prudhomme, C. (2018). Historic reconstructions of daily river flow for 303 UK catchments (1891–2015). NERC Environmental Information Data Centre. DOI: 10.5285/f710bed1-e564-47bf-b82c-4c2a2fe2810e.
- All references used are included in HD_Inventory_of_UK_reservoirs_references.csv.