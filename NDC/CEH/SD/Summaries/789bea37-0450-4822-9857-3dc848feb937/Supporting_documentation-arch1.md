# This data is an ensemble of JULES (Best et al. (2011), Clark et al. 2011)) simulations, ran for a select set of 1kmx1km grid cells in Great Britain, each with a different set of parameter values, from 2001 to 2010.

## Overview and purpose
- An ensemble of Joint UK Land Environment Simulator (JULES) simulations across selected 1km grid cells in Great Britain for 2001–2010.
- Each run uses a unique combination of parameter values to produce Gross Primary Productivity (GPP) for five plant functional types (PFTs) and the total GPP (gpp_gb).
- Data are intended for building/validating an emulator of a high-resolution land surface model (as described in the referenced emulator study).

## What is included
- Outputs:
  - GPP for five PFTs: gpp_BT (Broadleaf trees), gpp_NT (Needleleaf trees), gpp_C3g (C3 grasses), gpp_SH (Shrubs), gpp_Cr (Cropland)
  - Total GPP: gpp_gb
- Inputs (per grid cell and parameter set):
  - Spatial identifiers: index, lon, lat, X, Y
  - Parameter sets for each PFT (e.g., alpha_io, dqcrit_io_*; f0_io_*; g_grow_io_*; ln/leaf turnover parameters; lai_max_io_*; nmass_io_*; rootd_ft_io_*; tleaf_of_io_*; tlow_io_*; tupp_io_*; vsl_io_*)
  - Environment and state variables: time (8-day timestep), dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas
  - Vegetation fractions: BT, NT, C3g, SH, Cr
  - Soil and topography parameters: slope, hcon1, hcon2, satcon1, satcon2, vcrit1, vcrit2, vast1, vsat2, vwilt1, vwilt2
  - Others related to canopy and photosynthesis: gpp-related internal parameters (e.g., vsl)
  - Temporal indices: dayofyear, year
- Outputs (per grid cell and parameter set):
  - gpp_gb and the component GPPs: gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr

## Experimental design
- Data split for emulator development:
  - Training_Data_standardised.csv: used to fit the emulator
  - Testing_Data_standardised.csv: used to validate the emulator
- All input and output columns in these files are scaled for model fitting (inputs scaled to [0,1]; outputs (gpp_XX, excluding gpp_gb) scaled to mean 0 and standard deviation 1).

## Scaling and unscaling
- Input scaling:
  - Scaling to [0,1] using Tr_max.csv and Tr_min.csv (same row names as the training/testing files)
- Output scaling:
  - gpp_XX (except gpp_gb) scaled to mean 0 and std 1
  - Unscaling guidance provided in mean_and_stddev.csv (means and stds for Tr_BT, Tr_NT, Tr_C3g, Tr_SH, Tr_Cr)
- Purpose: enables stable emulator training and easy back-transformation of predictions to original units.

## Data quality and preprocessing
- Quality control: failed runs or non-convergent runs were discarded and not included in the data.

## Data structure and files
- The data resource comprises five files:
  - Training_Data_standardised.csv (91 columns; includes unique identifier, location, inputs, and outputs)
  - Testing_Data_standardised.csv (same structure as training but for validation)
  - Tr_max.csv (maximum values for a subset of input columns; used for unscaling)
  - Tr_min.csv (minimum values for a subset of input columns; used for unscaling)
  - mean_and_stddev.csv (means and standard deviations for unstandardising gpp outputs)
- Key columns in training/testing data:
  - Identifiers: index, lon, lat, X, Y
  - PFT parameters and state variables grouped by io_ suffix (e.g., alpha_io, dqcrit_io_BT, f0_io_BT, g_grow_io_BT, lai_max_io_BT, nmass_io_BT, rootd_ft_io_BT, tleaf_of_io_BT, tlow_io_BT, tupp_io_BT, vsl_io_BT)
  - Time and environment: time, dayofyear, year, dtr, huss, precip, psurf, rlds, rsds, sfcWind, tas
  - Vegetation composition: BT, NT, C3g, SH, Cr
  - Soil/topographic attributes: slope, hcon1, hcon2, satcon1, satcon2, vcrit1, vcrit2, vast1, vsat2, vwilt1, vwilt2
  - Outputs: gpp_gb, gpp_BT, gpp_NT, gpp_C3g, gpp_SH, gpp_Cr

## Context and references
- Related emulator methodology: Emulation of high-resolution land surface models with sparse Gaussian processes with application to JULES
- Foundational model references: Best et al. (2011) and Clark et al. (2011) on JULES model descriptions (energy/water fluxes and carbon/vegetation dynamics)

## How analysts can use this data
- Build and validate a Gaussian-process emulator to predict GPP across GB grid cells given parameter sets.
- Assess how different PFT parameterizations influence GPP components and total GPP.
- Perform regional analyses at 1km resolution by coupling parameter variations with environmental covariates (tas, precip, radiation, etc.).
- Use training data to fit the emulator and testing data to evaluate predictive performance, then apply unscaling steps to interpret results in physical units.