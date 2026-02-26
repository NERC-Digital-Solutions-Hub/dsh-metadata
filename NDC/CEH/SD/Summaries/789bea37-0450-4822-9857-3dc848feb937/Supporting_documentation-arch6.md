# JULES ensemble GPP data for 1km grid cells in Great Britain (2001-2010)

## Overview
- Ensemble of JULES model simulations across select 1km x 1km grid cells in Great Britain (2001–2010).
- Includes Gross Primary Productivity (GPP) for five plant functional types (BT, NT, C3g, SH, Cr) and the total gpp_gb.
- Data designed for building and validating an emulator; split into training and testing datasets.

## What the data contains
- Training and testing data:
  - Training_Data_standardised.csv: 91 columns per row, plus a unique index per JULES run and grid cell coordinates.
  - Testing_Data_standardised.csv: same structure as training, for validation.
- Outputs and inputs:
  - gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr, and gpp_gb (total) values (outputs) for each run/grid cell.
  - A comprehensive set of input parameters (per plant functional type) and environmental/grid descriptors (e.g., lon, lat, X, Y, time, dtr, tas, psurf, precip, rlds, rsds, sfcWind, etc.).
  - The 5 plant functional type parameter groups include alpha_io, dqcrit_io_*, f0_io_*, g_grow_io_*, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*, and related descriptors.
- Scaling and unscaling resources:
  - Inputs scaled to [0, 1]. Unscale with Tr_max.csv and Tr_min.csv (same row names as training/testing data).
  - Outputs (gpp_XX, excluding gpp_gb) scaled to mean 0 and std 1. Unscale with mean_and_stddev.csv.
- Quality control:
  - Failed or non-converging runs were discarded from the dataset.

## Experimental design and data preparation
- Data split:
  - Training_Data_standardised.csv used to fit the emulator described in related JULES emulation work.
  - Testing_Data_standardised.csv used to validate the emulator.
- Scaling details:
  - Input features are scaled to [0, 1].
  - Output GPP components gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr are scaled to zero-mean, unit-variance.
  - Separate files provide the parameters to revert scaling (Tr_max.csv, Tr_min.csv for inputs; mean_and_stddev.csv for outputs).

## Data structure and files
- Training_Data_standardised.csv (91 columns)
  - Metadata: index (unique run), lon/lat, X, Y.
  - Input parameters (examples): alpha_io, dqcrit_io_* (BT, NT, C3g, SH, Cr), f0_io_*, g_grow_io_*, g_leaf_0_io, knl_io, lai_max_io_*, nmass_io_*, rootd_ft_io_*, tleaf_of_io_*, tlow_io_*, tupp_io_*, vsl_io_*, time, dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas, BT/NT/C3g/SH/Cr fractions, soil/veg-related parameters.
  - Outputs: gpp_gb and gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr.
  - Temporal descriptor: dayofyear, year.
- Testing_Data_standardised.csv (91 columns)
  - Same structure as Training, intended for emulator validation.
- Tr_max.csv (75 columns)
  - Maximum values for a subset of input variables to restore original scales.
- Tr_min.csv (75 columns)
  - Minimum values for the corresponding inputs to restore original scales.
- mean_and_stddev.csv (10 columns)
  - Tr_BT_mean, Tr_BT_std, Tr_NT_mean, Tr_NT_std, Tr_C3g_mean, Tr_C3g_std, Tr_SH_mean, Tr_SH_std, Tr_Cr_mean, Tr_Cr_std.
  - Used to unstandardise the gpp_XX outputs.

## How to use the data
- Re-create original scales:
  - Use Tr_max.csv and Tr_min.csv to unscale the input features from [0, 1].
  - Use mean_and_stddev.csv to unscale gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (not gpp_gb).
- Emulator development:
  - Train a surrogate model on Training_Data_standardised.csv to predict gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr (and gpp_gb if desired) from the standardized inputs.
  - Validate performance on Testing_Data_standardised.csv.
- Potential analyses:
  - Explore relationships between parameter settings and GPP across grid cells and plant functional types.
  - Compare emulator predictions against the underlying JULES outputs to assess feature importance and interactions.
- Reproducibility:
  - Random split used for training/testing; data have been quality-checked to exclude failed runs.

## Context and references
- Based on Joint UK Land Environment Simulator (JULES) model descriptions:
  - Best et al. 2011; Clark et al. 2011.
- Data supports emulation of high-resolution land-surface models with sparse Gaussian processes, with application to JULES.