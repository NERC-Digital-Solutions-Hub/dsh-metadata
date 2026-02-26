# Supporting documentation

## Purpose and scope
- Provides modelled vegetation carbon output from the JULES land surface model, along with input temperature and rainfall outputs.
- Outputs are monthly and at a 1.5 km resolution.
- Includes four JULES simulations using two climate projections under two CO2 scenarios: present-day constant CO2 and the SRES A1B CO2 pathway.

## Data provenance and driving data
- Driving climatology downscaled from the HadRM3-PPE-UK ensemble (Hadley Centre, 2008) from 25 km to 1.5 km.
- Climate configurations include:
  - Standard configuration with global climate sensitivity 3.5 K.
  - An ensemble member with the highest global climate sensitivity (7.1 K).
- Present-day CO2 prescribed at 386.5 ppm; A1B CO2 pathway per Nakicenovic et al. (2000).

## Model and version details
- JULES: a community-developed land surface model led by the UK Met Office and Centre for Ecology and Hydrology.
- Data produced using model version vn4.9.
- Model configuration available in the Rose suite u-ao645, branch 'transient_25km_drive', on the JULES repository (registration required).

## Data format and structure
- Data stored as NetCDF files.
- Each NetCDF contains a lat-lon grid, time series of monthly midpoints, and the dataset values.
- Directory structure: 35K and 71K climatologies, each with Const_CO2 and CO2 subdirectories.
- Within each subdirectory are 3 NetCDF files; example: Temp_35K_Const_CO2.nc.

## Quality control, governance, and data stewardship
- JULES is a community-driven model with governance through the UK Met Office and CEH.
- Access to data and model code requires registration.
- Data versioning and provenance are maintained via the Rose suite and JULES repository.

## Access, openness, and reproducibility
- JULES model is publicly accessible upon registration.
- Data outputs are organized for reproducibility through defined directories and file naming conventions.
- References to the underlying emissions scenario (SRES) and climate projections support traceability.

## Metadata and interoperability
- NetCDF structure provides explicit grid, time, and data contents.
- Clear naming conventions for files (e.g., Temp_35K_Const_CO2.nc) to aid interoperability and reuse.
- Documentation links to source ensembles and CO2 pathways for context.

## Usage and applications for monitoring
- Useful for assessing climate-vegetation carbon interactions and impacts under different climate and CO2 scenarios.
- Supports environmental health monitoring and policy evaluation by providing spatially explicit vegetation carbon responses and climate drivers at high resolution.

## References
- Nakicenovic, N., Alcamo, J., Davis, G., (2000) IPCC Special Report on Emission Scenarios.