# Historic Droughts

## Project Overview
- A four-year, £1.5m UK Research Councils-funded project (2014–2018) to develop a cross-disciplinary understanding of past UK droughts and to develop improved tools for managing future droughts.
- Involved eight UK institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and the University of Oxford.
- Addresses the UK context where droughts and water scarcity threaten livelihoods and wellbeing, with growing pressures from population growth and resource exploitation.
- Aims to understand links between hydrometeorological and social systems to better manage droughts, by characterizing and quantifying UK drought history since the late 19th century using diverse sector information (hydrometeorological, environmental, agricultural, regulatory, social, and cultural).

## Inventory
- The Historic Droughts Inventory is a knowledge base of past drought characteristics, drivers, impacts, and responses designed as a common reference for policy makers, regulators, water suppliers, agriculture, and industry to enable more consistent, transparent planning.
- Comprises two integrated elements:
  1) Hydro-meteorological timelines of rainfall, river flows, and groundwater, presented as consistent drought indicators, extended back to the 19th century via modelling and data rescue.
  2) References to past droughts (from the 19th century to present) drawn from newspapers, legislation, agricultural media, and oral histories, with consistent time/place identifiers and links to full sources.
- Reference structure adapts fields from the European Drought Impact report Inventory (EDII) to cover a broad range of drought references, not just impacts.

## Motivation
- To examine water resource system-based drivers and responses to droughts, with a focus on the spatial and temporal distribution of reservoir construction nationally.
- A coherent reservoir dataset is needed to analyze changes over time and to investigate potential drivers of system change.

## Methods
- Primary purpose: establish information related to individual reservoir systems important for water supply; larger, strategically important reservoirs are prioritized due to better data availability.
- Inventory compiled by storage volume (largest first) to facilitate analysis of storage, inflows, and outflows.
- Incorporates upstream and downstream gauge data (NRFA) and links to the historic reconstructed streamflow dataset (Smith et al. 2018) and CEH reservoir storage data.
- Includes a notes section for information beyond standard fields and uses a data flag system to indicate data quality.
- Reservoirs up to 1,600 Ml capacity are included (with some smaller reservoirs in groups) to reflect data availability and to cover about 90% of reservoirs by capacity in the Reservoirs Act 1975 context.
- Reference sources include Hansard, government department records, water company records, journals, peer-reviewed and non-peer-reviewed works, and reputable websites.

## Preparation
- Data sources and quality assessment focus on planning and construction dates, plus notes on data limitations.
- Primary data sources: Environment Agency (Open Government Licence via FOI) and CEH UK Lakes Portal; supplemented by internet searches.
- Source hierarchy is documented; data quality is flagged, and references are provided for all inventory information.
- Reservoir group compositions are confirmed with water companies that submit storage data for Hydrological Summaries (CEH).
- The data set includes reservoirs up to 1,600 Ml capacity, with threshold justification tied to data availability and capacity coverage.

## Using the data
- Delivered as CSV files; accompanied by a references inventory (HD_Inventory_of_UK_reservoirs_references.csv) for cross-referencing.
- Key fields include:
  - Reservoir, Description; Easting, Northing; Storage_vol; Storage_vol_ref
  - Upstream/downstream NRFA gauge numbers (US_gauge_1, US_gauge_2, DS_gauge) and data flags
  - Planning_date, Planning_DF; Completion_date, Completion_DF
  - Res_type (impounding vs non-impounding)
  - HD_recon_flow (reconstructed flow linkage)
  - Timeseries (reservoir group) and Inception_use (primary initial use: hydro-electric, water resources, drainage, canal, flood storage, environmental)
  - Notes and Reference_ID for additional context
- Provides a structured, filterable dataset to support analysis of reservoir systems, storage changes, and system drivers in drought contexts.
- Emphasizes open data principles and clear data provenance to support governance and policy-informed decision making.

## References
- Environment Agency (2017) Reservoir Safety. Available online.
- Smith, K.A., Tanguy, M., Hannaford, J., & Prudhomme, C. (2018). Historic reconstructions of daily river flow for 303 UK catchments (1891–2015). NERC Environmental Information Data Centre. DOI provided.
- All references used are included in the HD_Inventory_of_UK_reservoirs_references.csv.