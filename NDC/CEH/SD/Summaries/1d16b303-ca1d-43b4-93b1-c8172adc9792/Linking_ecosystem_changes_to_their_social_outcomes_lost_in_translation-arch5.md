# Linking ecosystem changes to their social outcomes: lost in translation Description of the peatland model and the outputs

## Overview
- DigiBog is a deterministic 2D/3D peatland development model that simulates peatland growth over millennial timescales across hydrologically connected columns.
- Outputs include peat height and water-table depth, suitable for linking ecosystem changes to social outcomes.
- Because the model is deterministic, identical inputs (peatland configuration, peat properties, and climate) produce identical outputs.

## Model structure and processes
- Peat layers are added annually on top of a mineral soil base, with layer thickness depending on annual mean air temperature and annual mean water-table depth per column.
- Peat in each layer decomposes at sub-annual rates, influenced by the layer’s position relative to the water table and by annual temperature.
- Water moves horizontally between columns sub-annually to simulate water-table dynamics, driven by net rainfall and peat hydraulic properties.
- Decomposition alters saturated hydraulic conductivity, creating feedbacks among peat accumulation, decomposition, hydraulic properties, and water movement.
- Consequently, peat accumulation and decomposition vary both vertically (within a column) and horizontally (between columns), producing inter-column differences in peat thickness.

## Model set-up (data governance perspective)
- Configure the mineral-ground topography and the number of peatland columns.
- Define model input parameters and the total model run time.
- Create time series for net rainfall and temperature.
- Set the write-out time step for outputs.

## Inputs and parameters
- Oxic decay: base parameter used with temperature and Q10; units: proportion per year.
- Anoxic decay: base parameter used with temperature and Q10; units: proportion per year.
- Base temperature: used to calculate annual decay parameters.
- Bulk density: units: g cm^-3.
- Drainable porosity: units: proportion.
- Saturated hydraulic conductivity: initial value (changes as peat decomposes); units: cm yr^-1.
- Net rainfall: units: cm yr^-1; time series can be annual, monthly, or weekly.
- Temperature: mean annual; units: degrees Celsius.

## Outputs
- Water-table depth time series (mean annual and mean summer).
- End-of-simulation depth profiles for each column (virtual cores).
- Residence time of ponding water.
- Column height (mineral soil thickness plus peat) in cm.

## Reproducibility and provenance
- Outputs are fully determined by inputs due to the model’s deterministic nature.
- Outputs are generated to support the associated Ecosystem Services paper (2021) and to provide interpretable measures (peat height and water-table depth) for linking ecological changes to social outcomes.

## Data management considerations for Data Stewards
- Metadata should document: model version, authors, date, exact input configuration (peatland configuration, peat properties), climate time series (net rainfall and temperature), topography, number of columns, and run time.
- Capture and preserve the calculation logic for peat formation, decomposition, and water movement, including how peat layer thickness depends on temperature and water-table depth.
- Ensure unit consistency and record units for all inputs and outputs (e.g., time series, depths, and densities).
- Document output structure: time series and per-column depth profiles, plus any derived metrics (e.g., mean annual/summer water-table, ponding residence time).
- Link outputs to the exact input datasets and model configuration to support reproducibility; consider including a digital-twin snapshot (config, inputs, and outputs).
- Plan for data storage considerations given long simulation horizons and per-column depth-profile data.
- Include clear licensing and usage rights, with references to the publication for context.