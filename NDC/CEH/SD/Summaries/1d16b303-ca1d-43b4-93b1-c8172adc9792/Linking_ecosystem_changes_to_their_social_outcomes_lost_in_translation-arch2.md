# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Overview
- DigiBog (2D/3D) is a deterministic peatland development model that simulates peat formation and water-table dynamics over millennial timescales.
- It starts from a mineral soil base and grows peat layers annually, producing outputs of peat height and water-table depth.
- The model is designed to generate standardized outputs that can be used to examine environmental conditions and, in broader work, link ecological changes to social outcomes.

## How DigiBog works
- Annual peat formation: Each model column receives a new peat layer whose thickness is determined by a plant litter productivity function, influenced by annual mean air temperature and annual mean water-table depth.
- Decomposition: Sub-annual decomposition of peat in each layer depends on its depth relative to the water table and the mean annual temperature.
- Water movement: Sub-annual horizontal water transfer between columns simulates water-table behavior, driven by net rainfall and the peat’s hydraulic properties.
- Feedbacks: Decomposition alters saturated hydraulic conductivity, which in turn affects water movement, creating feedbacks between peat accumulation, decomposition, hydraulic properties, and hydrology.

## Model setup
- Define peatland configuration: topography of the mineral ground and the number of peatland columns.
- Define model inputs and run duration (in years).
- Create time series for net rainfall and temperature.
- Set the time step for output file writes.

## Inputs
- Oxic decay: base parameter used with temperature and Q10; units = proportion per year.
- Anoxic decay: base parameter used with temperature and Q10; units = proportion per year.
- Base temperature: used to calculate annual decay parameters.
- Bulk density: units = g cm^-3.
- Drainable porosity: units = proportion.
- Saturated hydraulic conductivity: initial value that changes as peat decomposes; units = cm yr^-1.
- Net rainfall: time series input (annual, monthly, or weekly); units = cm yr^-1.
- Temperature: mean annual temperature used in productivity and decomposition; units = °C.

## Outputs
- Time series of water-table depth.
- End-of-simulation depth profiles for each column (virtual cores).
- Water-table depth metrics: mean annual and mean summer values; residence time of ponding water.
- Column height: includes mineral soil thickness (units = cm).

## Relevance for environmental monitoring and policy
- Provides standardized, reproducible outputs (peat height and water-table depth) suitable for monitoring environmental change over time.
- Outputs can be integrated into broader data platforms and used to explore links between ecosystem changes and social outcomes, consistent with the accompanying Ecosystem Services paper.
- Deterministic nature supports reproducibility and comparability across scenarios and sites, aiding monitoring responsibilities and policy evaluation.