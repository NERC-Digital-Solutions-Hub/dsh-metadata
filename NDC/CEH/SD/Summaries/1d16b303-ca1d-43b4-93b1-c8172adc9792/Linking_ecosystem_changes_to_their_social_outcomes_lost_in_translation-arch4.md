# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Overview
- DigiBog is a deterministic 2D/3D peatland development model that simulates peatland growth over millennial timescales.
- The model grows peat layers from a mineral soil base, producing outputs for peat height and water-table depth.
- It is designed to be used alongside the Ecosystem Services paper (2021) and aims to link ecosystem changes to social outcomes.

## How DigiBog works (concept)
- Peatlands are built up by adding layers of peat annually to each model column.
- Key processes:
  - Peat formation: annual addition of plant litter to the top of each column; layer thickness depends on annual mean air temperature and water-table depth.
  - Peat decomposition: occurs sub- annually, depending on layer position relative to the water table and annual temperature.
  - Water movement: sub- annually, horizontal water redistribution between columns driven by net rainfall and peat hydraulic properties.
- Interactions create feedbacks: peat accumulation, decomposition, hydraulic properties, and water movement influence each other.
- Peat layer decomposition affects saturated hydraulic conductivity, altering future water movement.
- The model starts with a mineral soil base and grows peat upward through time.

## Model setup
- Configure the peatland layout (topography, number of columns).
- Define a set of input parameters and simulation duration (years).
- Create time series for net rainfall and temperature.
- Set the output write-out interval for results.

## Inputs
- Oxic decay (base parameter) used with temperature and Q10 to calculate oxic decay rate (units: proportion per year).
- Anoxic decay (base parameter) used with temperature and Q10 to calculate anoxic decay rate (units: proportion per year).
- Base temperature (for annual decay calculations).
- Bulk density (units: g cm^-3; temp-related parameterization).
- Drainable porosity (units: proportion).
- Saturated hydraulic conductivity (initial value; changes as peat decomposes; units: cm yr^-1).
- Net rainfall (time series; units: cm yr^-1; can be yearly, monthly, or weekly).
- Temperature (mean annual; used in productivity and decomposition calculations; units: degrees Celsius).

## Outputs
- Time series of water-table depth (mean annual and mean summer).
- End-of-simulation depth profiles for each column (virtual cores of peat).
- Additional metrics available: residence time of ponding water.
- Column height output includes mineral soil thickness (units: cm).

## Data management and reuse considerations for data leaders
- Deterministic nature ensures reproducibility: identical inputs yield identical outputs.
- Outputs consist of time series and spatial depth profiles suitable for linking to social or policy analyses.
- Documentation needs: clear definitions of inputs, units, and topography settings to enable replication and cross-study comparisons.
- Opportunities for data sharing: model configuration, input time series, and resulting outputs can form reusable data products for ecosystem-service assessments and policy work.