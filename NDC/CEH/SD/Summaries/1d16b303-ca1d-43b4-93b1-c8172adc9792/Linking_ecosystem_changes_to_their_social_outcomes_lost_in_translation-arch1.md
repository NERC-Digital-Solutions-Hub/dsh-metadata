# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Introduction
- DigiBog (2D/3D) simulates peatland development over millennial timescales by building peat layers within hydrologically connected columns; the model is deterministic and yields the same output for the same inputs.
- Simulations start from a mineral soil base; individual peat layers are added to each model column annually, effectively growing the peatland upward from the base.
- Core processes:
  - Peat formation: annual addition of plant litter at the top of each column; layer thickness varies with annual average air temperature and annual average water-table depth.
  - Peat decomposition: sub-annual rate depending on layer position relative to the water table and annual air temperature.
  - Water movement: sub-annual horizontal transfer between columns driven by net rainfall and peat hydraulic properties.
- These interactions create feedbacks among peat accumulation, decomposition, changes in hydraulic properties, and water movement.

## Model set up
- Define the mineral ground topography and the number of peatland columns.
- Define model input parameters and set the model run time (in years).
- Create time series of net rainfall and temperature.
- Set the write-out time step for output files.

## Inputs
- Oxic decay: base parameter used to calculate oxic decay together with temperature and Q10 (units: proportion per year).
- Anoxic decay: base parameter used to calculate anoxic decay together with temperature and Q10 (units: proportion per year).
- Base temperature: used to calculate annual decay parameters.
- Bulk density: parameter related to peat properties.
- Drainable porosity: proportion.
- Saturated hydraulic conductivity: initial value that declines as peat decomposes (units: cm/yr).
- Net rainfall: time series (annual, monthly, or weekly) (units: cm/yr).
- Temperature: mean annual temperature (used in productivity and decomposition calculations) (units: °C).

## Outputs
- Time series of water-table depth (including mean annual and currently mean summer values).
- End-of-simulation depth profiles for each column (virtual peat cores).
- Residence time of ponding water.
- Column height (peat plus mineral soil thickness), in centimeters.