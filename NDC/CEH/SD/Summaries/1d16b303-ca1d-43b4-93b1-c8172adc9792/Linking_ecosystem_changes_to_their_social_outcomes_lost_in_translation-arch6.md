# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Overview
- DigiBog is a deterministic 2D/3D peatland development model that simulates peatland growth over millennial timescales, building peat layers within hydrologically connected columns starting from a mineral soil base.
- It outputs peat height and water-table depth, designed to support analyses such as those in the associated Ecosystem Services paper (2021).

## How the model works
- Peat formation: each year, a new peat layer is added to the top of every model column; thickness depends on annual mean air temperature and annual mean water-table depth per column.
- Peat decomposition: sub-annual decomposition rates depend on layer position relative to the water table and the annual air temperature.
- Water movement: sub-annual horizontal water transfer between columns simulates water-table dynamics, driven by net rainfall and peat hydraulic properties.
- Feedbacks: interactions among peat accumulation, decomposition, hydraulic properties, and water movement create feedback loops that shape peat growth and hydrology.

## Model setup
- Configure the peatland: define topography of the mineral ground and the number of peatland columns.
- Define input parameters and set the model run time (years).
- Create time series for net rainfall and temperature.
- Set the output write-out time step.

## Inputs (parameters and units)
- Oxic decay: base parameter for calculating oxic decay with temperature and Q10; units = proportion (yr^-1).
- Anoxic decay: base parameter for calculating anoxic decay with temperature and Q10; units = proportion (yr^-1).
- Base temperature: used to calculate annual decay parameters.
- Bulk density: units = g cm^-3.
- Drainable porosity: units = proportion.
- Saturated hydraulic conductivity: initial value that declines as peat decomposes; units = cm yr^-1.
- Net rainfall: time series in cm yr^-1 (annual/monthly/weekly options).
- Temperature: mean annual temperature used in productivity and decomposition calculations; units = °C.

## Outputs
- Time series of water-table depth (mean annual and mean summer).
- End-of-simulation depth profiles for each column (virtual cores).
- Water-table-related metrics: residence time of ponding water.
- Column height: includes mineral soil thickness; units = cm.

## Reproducibility and use
- The model is deterministic: identical inputs produce identical outputs, enabling reproducible data products for analyzing ecosystem-to-social-outcome linkages.