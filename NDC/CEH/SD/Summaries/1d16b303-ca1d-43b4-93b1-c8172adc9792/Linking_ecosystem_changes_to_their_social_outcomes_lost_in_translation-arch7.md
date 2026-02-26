# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

- Purpose and scope
  - Describes the DigiBog peatland development model (2D/3D) used to generate peat height and water-table depth outputs for analysis in conjunction with a 2021 Ecosystem Services paper.
  - Model is deterministic: same inputs yield identical outputs.
  - Simulates peatland development over millennial timescales by building peat layers within hydrologically connected columns, starting from a mineral soil base.

- Introduction and core processes
  - Peatland growth occurs by annual addition of plant litter to the top of each column; layer thickness depends on annual average air temperature and annual average water-table depth per column.
  - Sub-annual peat decomposition depends on a layer’s position relative to the water table and on annual air temperature.
  - Water movement between columns is modeled horizontally to simulate water-table behavior, driven by net rainfall and peat hydraulic properties.
  - Feedbacks exist among peat accumulation, decomposition, hydraulic properties, and water movement, causing spatial and vertical variation in peat layers.

- Model structure and outputs
  - The model comprises multiple columns representing the peatland, with topography of the mineral ground defined and the number of columns specified.
  - Outputs include:
    - Time series of water-table depth (mean annual and mean summer).
    - End-of-simulation depth profiles for each column (virtual cores of peat).
    - Additional metrics such as residence time of ponding water and column height (including mineral soil thickness).
  - Outputs emphasize both peat height and water-table depth, available in the repository for use in GIS/map-based analyses.

- Model setup (configuration)
  - Define peatland topography and the number of columns.
  - Specify model input parameters and run time (years).
  - Create time series of net rainfall and temperature.
  - Set the write-out time step for output files.

- Inputs and parameter descriptions
  - Oxic decay rate: base parameter used with temperature and Q10 to compute oxic decay (units: proportion per year).
  - Anoxic decay rate: base parameter used with temperature and Q10 to compute anoxic decay (units: proportion per year).
  - Base temperature: used to calculate annual decay parameters (units: degrees Celsius).
  - Bulk density: (units: g cm^-3; associated with soil/peat density).
  - Drainable porosity: (units: proportion).
  - Saturated hydraulic conductivity: initial value, changes as peat decomposes (units: cm yr^-1).
  - Net rainfall: time series input (units: cm yr^-1; can be annual, monthly, or weekly).
  - Temperature: mean annual temperature used in productivity and decomposition calculations (units: degrees Celsius).

- Outputs in detail
  - Water-table depth: time series (mean annual and current mean summer).
  - End-of-simulation peat depth profiles for each column (virtual cores).
  - Column height: total height including mineral soil thickness.
  - Potential to determine residence time of ponding water.