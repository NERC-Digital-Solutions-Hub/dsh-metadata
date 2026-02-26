# Historic Droughts

- A four-year, £1.5m project (2014–2018) funded by UK Research Councils to develop an interdisciplinary understanding of past UK droughts and to create tools for better drought management in the future.
- Involved eight UK institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and University of Oxford.
- Aimed to link hydrometeorological and social system factors by analyzing data across sectors (hydrometeorological, environmental, agricultural, regulatory, social, and cultural) to characterise and quantify UK drought history since the late 19th century.

- Key data asset: Historic Droughts Inventory
  - A knowledge base of past drought characteristics, drivers, impacts, and responses to support policy makers, water suppliers, agriculture, and industry with a common reference for planning.
  - Two integrated elements:
    - Hydro-meteorological timelines: rainfall, river flows, and groundwater with consistent drought indicators, extended back to the 19th century via modelling and data rescue.
    - Reference archive: past drought references from 19th century to present (newspapers, legislation, agricultural media, oral histories) with structured time/place data and links to full sources; aligned with, but extending beyond, the EDII framework.
  - References are standardized and linked to a separate HD_Inventory_of_UK_reservoirs_references.csv.

- Motivation and focus
  - Investigated water resource system drivers and responses, notably the spatial and temporal distribution of reservoir construction.
  - Created a coherent reservoir dataset to analyze changes over time and potential drivers of system change.

- Methods and data design
  - Inventory prioritised by storage volume, focusing on larger, strategically important reservoirs first.
  - Built to analyze reservoir systems with data on storage, inflows, and outflows; integrated upstream/downstream gauging information (NRFA) and historic streamflow reconstructions (Smith et al., 2018), plus reservoir storage data held by CEH.
  - Included planning and construction dates to understand timing and drivers of changes; notes field captures additional context.
  - Designed for easy filtering and extraction; data columns kept concise to enable straightforward classification.

- Data preparation and quality
  - Data sources include Environment Agency reservoirs data (Open Government Licence via FOI), the UK Lakes Portal (CEH), and various internet sources.
  - Data quality is variable; a flag system and notes are used to indicate quality and caveats.
  - Reservoirs included up to 1,600 Ml capacity (and smaller reservoirs included within groups if historical storage data and planning/construction dates are available); threshold chosen to balance data availability with coverage.

- Using the data
  - Inventory provided as CSV files with a supporting HD_Inventory_of_UK_reservoirs_references.csv for references.
  - Core columns cover: Reservoir name, location (Eastings/Northings), storage volume, upstream/downstream NRFA gauges, planning and completion dates, reservoir type, reconnection to flow data, timeseries group, initial purpose, notes, and reference IDs.
  - Aims to enable multi-sector analysis of reservoir systems, their evolution, and associated drivers and responses.

- Licensing and references
  - Data primarily under the Open Government Licence (EA data) with citations to Environment Agency sources and the Smith et al. (2018) river flow reconstruction dataset.
  - All references documented within HD_Inventory_of_UK_reservoirs_references.csv.

- Practical impact for data leaders
  - Demonstrates a structured approach to building a cross-sector data inventory that supports policy, regulation, and industry planning.
  - Emphasizes the importance of data provenance, quality flags, metadata notes, and cross-referencing to maintain a usable, trustworthy knowledge base.
  - Highlights the value of combining high-level indicators (hydrometeorological timelines) with granular historical references to enable comprehensive drought analysis and forecasting.