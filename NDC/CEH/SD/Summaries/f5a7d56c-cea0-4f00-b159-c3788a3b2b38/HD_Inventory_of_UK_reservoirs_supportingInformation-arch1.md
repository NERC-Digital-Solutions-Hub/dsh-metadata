# Project Overview

- A four-year (2014–2018), £1.5m UK Research Councils-funded project to develop a cross-disciplinary understanding of historic UK droughts and to improve tools for drought management.
- Collaborative effort across eight UK institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and the University of Oxford.
- Aim: identify links between hydrometeorological and social systems during droughts to better understand, predict, and manage Drought and Water Scarcity (DWS) events.

## Inventory: Historic Droughts Inventory

- A knowledge base of past drought characteristics, drivers, impacts, and responses, drawing from multiple sectors (hydrometeorological, environmental, agricultural, regulatory, social, cultural).
- Purpose: provide a common reference for policymakers, regulators, water supply companies, agriculture, and industry to support consistent, transparent drought planning.
- Structure: two main, complementary components for multi-sectoral understanding:
  - Hydro-mmeteorological timelines: rainfall, river flows, groundwater; consistent drought indicators extended back to the 19th century through modelling and data rescue.
  - References to past droughts (19th century to present): newspapers, legislation, agricultural media, and oral histories, with standardized time/place data and links to full sources. Based on EDII (European Drought Impact report Inventory) groundwork but extended beyond impacts to include drivers and responses.

## Motivation

- To study water resource system-based drivers and responses to droughts and water scarcity, including the spatial and temporal distribution of reservoir construction on a national scale.
- A coherent reservoir dataset was needed to analyze changes over time and investigate drivers of system change.

## Methods

- Inventory purpose: compile information on reservoirs important to water supply; prioritise larger, strategically important reservoirs, and capture planning and construction dates to understand drivers and responses.
- Data sources and linkage:
  - Upstream and downstream gauge information (NRFA) to connect reservoirs with gauging data.
  - Historic streamflow reconstruction for UK gauges (Smith et al. 2018) and CEH reservoir storage data.
  - Cross-referencing with reservoir storage data held by CEH.
- Design for analysis: filterable inventory with a limited set of data columns for easy classification and extraction.

## Preparation and Data Quality

- Primary data sources:
  - Environment Agency (Open Government Licence) for reservoir storage information.
  - UK Lakes Portal (CEH) and additional internet sources.
- Data quality assessment:
  - A data flag system indicates varying data quality; notes capture additional context.
  - References are supplied for all information.
- Reservoir inclusion criteria:
  - Reservoirs up to 1,600 Ml capacity, plus smaller reservoirs within groups with historic storage data and planning/construction dates.
  - Rationale: covers ~90% of reservoirs by capacity within the Reservoirs Act 1975 context; large information gaps for smaller reservoirs exist.
- Reference sources used in selection:
  - Hansard, government department records, water company records, journals, peer-reviewed and non-peer-reviewed books, online sources with varying levels of verification.

## Using the Data

- The inventory is provided in CSV format with a companion references CSV (HD_Inventory_of_UK_reservoirs_references.csv) to be used together.
- Core columns (examples):
  - Reservoir, Description: name of reservoir (alphabetical order).
  - Easting, Northing: grid coordinates (Ordnance Survey National Grid).
  - Storage_vol: maximum reservoir storage in megalitres (Ml); refers to storage capacity, not live resources.
  - US_gauge_1, US_gauge_2, DS_gauge: NRFA gauge numbers for upstream/downstream gauges; associated Data Flags (DF).
  - Planning_date, Completion_date: years of planning and completion; Planning_DF and Completion_DF indicate data quality/definition variations.
  - Res_type: reservoir type (impounding or non-impounding).
  - HD_recon_flow: NRFA gauge used in Smith et al. (2018) reconstruction, if applicable.
  - Timeseries: identifies reservoir group usage (per CEH Monthly Hydrological Summary).
  - Inception_use: primary use at inception (Hydro-electric, Water resources, Drainage, Canal, Flood storage, Environmental).
  - Notes: extra information on drought-system linkages or data caveats.
  - Reference_ID: links to entries in HD_Inventory_of_UK_reservoirs_references.csv.
- The dataset emphasizes easy filtering and extraction via a compact, consistent schema.

## References

- Key data and methodology sources:
  - Environment Agency (2017) Reservoir Safety.
  - Smith, K.A., Tanguy, M., Hannaford, J. & Prudhomme, C. (2018). Historic reconstructions of daily river flow for 303 UK catchments (1891–2015). NERC EIDC.
- All references used are included in the HD_Inventory_of_UK_reservoirs_references.csv.