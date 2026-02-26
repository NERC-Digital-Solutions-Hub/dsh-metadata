# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Overview of DigiBog
- A deterministic 2D/3D model that simulates peatland development over millennial timescales.
- Starts from a mineral soil base and builds peat layers annually, effectively growing the peatland upward.
- Outputs include peat height and water-table depth for analysis.

## How the model works (processes and feedbacks)
- Each year, a new peat layer is added to every model column; layer thickness depends on annual mean air temperature and annual mean water-table depth per column.
- Peat in each layer decomposes on a sub-annual basis; decomposition rate depends on position relative to the water table and the annual air temperature.
- Water moves horizontally between columns to mimic water-table behavior, driven by net rainfall and peat hydraulic properties.
- Peat layer decomposition changes saturated hydraulic conductivity, which feeds back into water movement and peat accumulation dynamics.
- Peat formation uses a plant litter productivity function; decomposition and hydrology interact to shape the evolving peat landscape.

## Model setup and configuration
- Define the mineral ground topography and the number of peatland columns.
- Define model input parameters and set the model run time (years).
- Create time series of net rainfall and temperature.
- Set the write-out time step for output files.

## Key inputs (with units)
- Oxic decay parameter and Anoxic decay parameter (yr^-1), calculated with temperature and Q10.
- Base temperature (used for annual decay calculations).
- Bulk density (units typically g cm^-3).
- Drainable porosity (unit: proportion).
- Saturated hydraulic conductivity (initial value; decreases as peat decomposes; units: cm yr^-1).
- Net rainfall (units: cm yr^-1; can be annual, monthly, or weekly time series).
- Temperature (mean annual; units: °C).

## Model outputs
- Time series of water-table depth.
- End-of-simulation depth profiles for each column (virtual peat cores).
- Water-table depth metrics: mean annual and mean summer values; residence time of ponding water.
- Column height: total depth including mineral soil thickness (units: cm).