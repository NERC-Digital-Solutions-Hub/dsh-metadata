# Supporting documentation

## Summary of dataset and purpose
- Provides modeled vegetation carbon output from the land surface model JULES, plus the input temperature and rainfall data, at a monthly 1.5 km resolution.
- Includes four JULES simulations driven by two climate projections under constant present-day atmospheric CO2 and under the SRES A1B CO2 pathway.

## Background and data provenance
- Climate data are downscaled from a 25 km grid to 1.5 km using the HadRM3-PPE-UK ensemble to drive the simulations.
- Uses standard configuration parameters (global climate sensitivity 3.5 K) and an ensemble member with higher sensitivity (7.1 K).
- Present-day CO2 set to 386.5 ppm; A1B CO2 pathway applied for the second scenario.
- Data and model details are anchored to JULES and its configuration within the Rose suite.

## Modeling and quality control
- JULES is a community-developed land surface model led by the UK Met Office and Centre for Ecology and Hydrology.
- Data produced with JULES version vn4.9; model configuration available in the Rose suite under branch transient_25km_drive.
- Access to JULES and data requires registration (JULES repository: code.metoffice.gov.uk/trac/jules; Rose suite: code.metoffice.gov.uk/trac/rosesu).

## Data structure and organization
- Data provided as NetCDF (.nc) files containing:
  - Lat/lon grid
  - Time series of monthly midpoints
  - The dataset values (vegetation carbon, temperature, rainfall)
- Directory structure:
  - 35K and 71K climatology folders
  - Within each, Const_CO2 and CO2 subdirectories
  - Each subdirectory contains 3 NetCDF files (e.g., Temp_35K_Const_CO2.nc) corresponding to the data objects described.

## Variables and formats
- Primary variables: vegetation carbon output, temperature, and rainfall
- Resolution: monthly data at 1.5 km
- File format: NetCDF

## Access and usage guidance for data support
- The dataset is designed to enable users to analyze climate impacts on vegetation carbon under different CO2 scenarios.
- Data can be located and accessed via the JULES repository (registration required) and through the Rose suite configuration:
  - JULES repository: https://code.metoffice.gov.uk/trac/jules
  - Rose suite: https://code.metoffice.gov.uk/trac/rosesu
- The four-simulation design supports comparative analyses of climate projections and CO2 pathways.

## References
- Nakicenovic, N.; Alcamo, J.; Davis, G. (2000) IPCC Special Report on Emission Scenarios. Cambridge.