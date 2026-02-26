# This data is an ensemble of JULES (Best et al. (2011), Clark et al. (2011)) simulations, ran for a select set of 1kmx1km grid cells in Great Britain, each with a different set of parameter values, from 2001 to 2010.

## Purpose and scope
- Provides data for emulating high-resolution land surface models (JULES) using sparse Gaussian processes.
- Outputs Gross Primary Productivity (GPP) for five plant functional types plus a weighted total (gpp_gb) across 1km grid cells in Great Britain (2001–2010).
- Five plant functional types: Broadleaf trees (BT), Needleleaf trees (NT), C3 grasses (C3g), Shrubs (SH), Cropland (Cr).

## Experimental design and data splits
- Data is split into training and testing sets:
  - Training_Data_standardised.csv: used to fit the emulator.
  - Testing_Data_standardised.csv: used to validate the emulator.
- Data are scaled to facilitate modelling:
  - Inputs scaled to 0–1 range (unscale with Tr_max.csv and Tr_min.csv).
  - Outputs gpp_XX (except gpp_gb) scaled to have mean 0 and standard deviation 1 (unscale with mean_and_stddev.csv).

## Data structure and files
- Training_Data_standardised.csv
  - 91 columns including: index, lon/lat, X/Y (OSGB269 / EPSG:27700), grid-specific parameters for each pft (e.g., alpha_io, dqcrit_io_*, f0_io_*, g_grow_io_*, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*), time variables (time, dayofyear, year), and responses (gpp_gb, gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr).
- Testing_Data_standardised.csv
  - 91 columns described similarly to Training_Data_standardised.csv, but for the testing set.
- Tr_max.csv
  - 75 columns with maximum input values to rescale inputs back to their original scale.
- Tr_min.csv
  - 75 columns with minimum input values to rescale inputs back to their original scale.
- mean_and_stddev.csv
  - 10 columns with means and standard deviations for unstandardising gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (gpp_gb not included).

## Inputs and outputs
- Inputs (features) are a mix of spatial descriptors (lon, lat, X, Y, grid fractions for each pft, topographic and environmental parameters) and model parameters (e.g., alpha_io, dqcrit_io_*, f0_io_*, growth and leaf parameters, temperature and moisture related parameters).
- Outputs (responses) include:
  - gpp_gb (total GPP for the grid cell)
  - gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (GPP by plant functional type)

## Spatial and temporal coverage
- Spatial: select set of 1km x 1km grid cells in Great Britain.
- Temporal: 8-day averaged timesteps across 2001–2010 (fields include time, dayofyear, year).

## Data scaling and unscaling
- Input scaling: values scaled to [0, 1]; unscale using Tr_max.csv and Tr_min.csv.
- Output scaling: gpp_XX (excluding gpp_gb) scaled to mean 0 and std dev 1; unscale using mean_and_stddev.csv.

## Quality control
- Only runs that converged and passed quality checks are included; failed or non-convergent runs are discarded.

## How this GIS-focused data can be used
- Map-based data products: join with 1km GB grid to produce spatial maps of GPP by type or total GPP (gpp_gb).
- Reprojection and integration: coordinates include lon/lat and X/Y in British National Grid (EPSG:27700) for compatibility with GIS workflows; reproject as needed for mapping.
- Scenario and analysis workflows: emulator-trained dataset can support rapid generation of high-resolution GPP estimates across GB for policy, planning, or public visualization.
- Data preparation for GIS: use the Tr_max/Tr_min to re-derive original input scales; use mean_and_stddev to revert outputs to physical units.

## References
- Best, M. J., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 1: energy and water fluxes. Geoscientific Model Development, 2011.
- Clark, D. B., et al. The Joint UK Land Environment Simulator (JULES), model description-Part 2: carbon fluxes and vegetation dynamics. Geoscientific Model Development, 2011.